# GitHub Workflow for NuGet Publishing

This directory contains the GitHub workflow for building, testing, and publishing the Brotal.FireflyIII NuGet package to nuget.org.

## Workflow Overview

The workflow (`build-and-publish.yml`) performs the following actions:

1. **Build Job**: Runs on every PR and tag push
   - Restores dependencies
   - Builds the solution
   - Runs tests
   - Creates NuGet package
   - Uploads artifacts

2. **Publish Job**: Runs only on version tags (e.g., `v1.0.0`)
   - Downloads the NuGet package
   - Validates the package
   - Publishes to nuget.org
   - Creates a GitHub release

## Setup Instructions

### 1. NuGet API Key Setup

To publish packages to nuget.org, you need to set up an API key:

#### Option A: Using NuGet.org Website
1. Go to [nuget.org](https://www.nuget.org)
2. Sign in to your account
3. Go to your profile → API Keys
4. Create a new API key
5. Copy the API key (you won't be able to see it again)

#### Option B: Using NuGet CLI
```bash
# Install NuGet CLI if you haven't already
dotnet tool install -g dotnet-nuget

# Login to NuGet
dotnet nuget add source https://api.nuget.org/v3/index.json -n nuget.org
dotnet nuget add source https://api.nuget.org/v3/index.json -n nuget.org -u YOUR_USERNAME -p YOUR_API_KEY --store-password-in-clear-text
```

### 2. GitHub Secrets Configuration

Add the following secrets to your GitHub repository:

1. Go to your repository → Settings → Secrets and variables → Actions
2. Click "New repository secret"
3. Add the following secret:
   - **Name**: `NUGET_API_KEY`
   - **Value**: Your NuGet API key from step 1

### 3. Repository Settings

Ensure your repository has the following settings:
- **Branch protection**: Enable for `main` or `master` branch
- **Required status checks**: Enable the workflow as a required check for PRs

## Usage

### Publishing a New Version

1. **Update Version**: Modify the version in `src/Brotal.FireflyIII/Brotal.FireflyIII.csproj`
2. **Create Tag**: Create and push a version tag:
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```
3. **Monitor**: Check the Actions tab in GitHub to monitor the build and publish process

### Manual Trigger

You can manually trigger the workflow:
1. Go to Actions tab in your repository
2. Select "Build and Publish NuGet Package"
3. Click "Run workflow"
4. Choose the branch and click "Run workflow"

### Testing Locally

Before pushing, test the build locally:
```bash
# Restore dependencies
dotnet restore Brotal.FireflyIII.sln

# Build
dotnet build Brotal.FireflyIII.sln --configuration Release

# Test
dotnet test Brotal.FireflyIII.sln --configuration Release

# Pack
dotnet pack src/Brotal.FireflyIII/Brotal.FireflyIII.csproj --configuration Release --output nupkgs
```

## Version Management

The workflow automatically handles versioning:
- **Tag-based**: When you push a tag like `v1.0.0`, it uses that version
- **Pre-release**: For non-tag pushes, it creates a pre-release version like `0.0.0-prerelease-123`

## Troubleshooting

### Common Issues

1. **Authentication Failed**
   - Verify your `NUGET_API_KEY` secret is correctly set
   - Ensure the API key has publish permissions
   - Check if the API key is expired

2. **Package Already Exists**
   - NuGet doesn't allow overwriting existing packages
   - Increment the version number before publishing

3. **Build Failures**
   - Check the build logs in the Actions tab
   - Ensure all dependencies are properly restored
   - Verify the .NET version compatibility

### Useful Commands

```bash
# Check package contents
dotnet nuget list source

# Verify package
dotnet nuget verify nupkgs/*.nupkg

# Test package locally
dotnet nuget add source ./nupkgs -n local
dotnet add package Brotal.FireflyIII --source local
```

## Security Notes

- Never commit API keys to your repository
- Use GitHub secrets for sensitive information
- Regularly rotate your NuGet API keys
- Consider using scoped API keys for better security

## Support

If you encounter issues:
1. Check the workflow logs in the Actions tab
2. Verify your NuGet API key is valid
3. Ensure your package version is unique
4. Check NuGet.org status page for service issues
