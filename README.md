# 🔥 Brotal.FireflyIII

[![Workflow](https://img.shields.io/github/actions/workflow/status/skb50bd/firefly-iii-ai-ingest/publish.yml)](https://github.com/skb50bd/Brotal.FireflyIII/actions)
[![NuGet](https://img.shields.io/nuget/v/Brotal.FireflyIII.svg)](https://www.nuget.org/packages/Brotal.FireflyIII/)
[![License](https://img.shields.io/github/license/skb50bd/Brotal.FireflyIII)](./LICENSE)
[![.NET](https://img.shields.io/badge/.NET-9.0-blue.svg)](https://dotnet.microsoft.com/)

A comprehensive .NET client library for the [Firefly III](https://firefly-iii.org/) personal finance manager API, automatically generated from the official OpenAPI specification.


## 📋 Table of Contents

- [About](#🎯-about)
- [Installation](#📦-installation)
- [Quick Start](#🚀-quick-start)
- [Usage Examples](#💡-usage-examples)
- [API Information](#📚-api-information)
- [Generation](#🔧-generation)
- [Development](#🛠️-development)
- [Troubleshooting](#🚨-troubleshooting)
- [API Reference](#api-reference)

## 🎯 About

This C# SDK provides a complete .NET client for the Firefly III API, enabling you to interact with your personal finance data programmatically. The library is built with modern .NET practices and includes comprehensive error handling, retry policies, and dependency injection support.

### ✨ Features

- 🔐 **Authentication Support**: Bearer token, API key, and OAuth authentication
- 🔄 **Retry Policies**: Built-in retry, timeout, and circuit breaker policies
- 🏗️ **Dependency Injection**: Native .NET DI container support
- 📊 **Type Safety**: Strongly typed models and responses
- 🚀 **Async/Await**: Full async support for all operations
- 🛡️ **Error Handling**: Comprehensive error handling and validation

### 📦 Package Details

- **SDK Version**: [![NuGet](https://img.shields.io/nuget/v/Brotal.FireflyIII.svg)](https://www.nuget.org/packages/Brotal.FireflyIII/)
- **Target Framework**: [![.NET](https://img.shields.io/badge/.NET-9.0-blue.svg)](https://dotnet.microsoft.com/)
- **API Version**: Firefly III API v6.3.0
- **Generator**: OpenAPI Generator 7.16.0-SNAPSHOT

## 📦 Installation

### NuGet Package

```bash
dotnet add package Brotal.FireflyIII
```

### Package Manager

```powershell
Install-Package Brotal.FireflyIII
```

## 🚀 Quick Start

### Basic Setup

```csharp
var fireflyPat = 
    builder
        .Configuration
        .GetValue<string>("Firefly:PersonalAccessToken");

var fireflyUrl = 
    builder
        .Configuration
        .GetValue<string>("Firefly:Url");

builder.Services.AddApi(options =>
{
    BearerToken bearerToken = new(fireflyPat);
    OAuthToken oauthToken = new(fireflyPat);
    options.AddTokens(bearerToken);
    options.AddTokens(oauthToken);
    options.UseProvider<RateLimitProvider<BearerToken>, BearerToken>();
    options.UseProvider<RateLimitProvider<OAuthToken>, OAuthToken>();

    options.AddApiHttpClients(client =>
    {
        client.BaseAddress = new Uri(fireflyUrl);
    }, builder =>
    {
        builder
            .AddRetryPolicy(2)
            .AddTimeoutPolicy(TimeSpan.FromSeconds(10))
            .AddCircuitBreakerPolicy(10, TimeSpan.FromSeconds(10));
    });
});
```

## 💡 Usage Examples

### Making API Calls

```csharp
// Get account information
var accountsApi = host.Services.GetRequiredService<IAccountsApi>();
var accounts = await accountsApi.GetAccountAsync(accountId);

// Create a transaction
var transactionsApi = host.Services.GetRequiredService<ITransactionsApi>();
var transaction = new TransactionStore
{
    Transactions = new List<Transaction>
    {
        new Transaction
        {
            Type = TransactionTypeEnum.Withdrawal,
            Amount = "100.00",
            Description = "Grocery shopping",
            Date = DateTime.Now
        }
    }
};
var result = await transactionsApi.StoreTransactionAsync(transaction);
```

### Error Handling

```csharp
var response = await api.GetAboutAsync("todo");

if (response.IsSuccessStatusCode())
{
    var data = response.Ok();
    // Process successful response
}
else
{
    var error = response.Error();
    // Handle error response
}
```


## 📚 API Information

- **Application Name**: Firefly III API v6.3.0
- **Version**: v6.3.0
- **Description**: Comprehensive API for Firefly III personal finance manager
- **Documentation**: [Firefly III API Documentation](https://docs.firefly-iii.org/references/firefly-iii/api/)

## API Reference

Below is a comprehensive list of available API documentation for this SDK. Each API is documented in detail in the [`docs/apis/`](docs/apis/) directory:

| API | Documentation |
|-----|--------------|
| AboutApi | [AboutApi.md](docs/apis/AboutApi.md) |
| AccountsApi | [AccountsApi.md](docs/apis/AccountsApi.md) |
| AttachmentsApi | [AttachmentsApi.md](docs/apis/AttachmentsApi.md) |
| AutocompleteApi | [AutocompleteApi.md](docs/apis/AutocompleteApi.md) |
| AvailableBudgetsApi | [AvailableBudgetsApi.md](docs/apis/AvailableBudgetsApi.md) |
| BillsApi | [BillsApi.md](docs/apis/BillsApi.md) |
| BudgetsApi | [BudgetsApi.md](docs/apis/BudgetsApi.md) |
| CategoriesApi | [CategoriesApi.md](docs/apis/CategoriesApi.md) |
| ChartsApi | [ChartsApi.md](docs/apis/ChartsApi.md) |
| ConfigurationApi | [ConfigurationApi.md](docs/apis/ConfigurationApi.md) |
| CurrenciesApi | [CurrenciesApi.md](docs/apis/CurrenciesApi.md) |
| CurrencyExchangeRatesApi | [CurrencyExchangeRatesApi.md](docs/apis/CurrencyExchangeRatesApi.md) |
| DataApi | [DataApi.md](docs/apis/DataApi.md) |
| InsightApi | [InsightApi.md](docs/apis/InsightApi.md) |
| LinksApi | [LinksApi.md](docs/apis/LinksApi.md) |
| ObjectGroupsApi | [ObjectGroupsApi.md](docs/apis/ObjectGroupsApi.md) |
| PiggyBanksApi | [PiggyBanksApi.md](docs/apis/PiggyBanksApi.md) |
| PreferencesApi | [PreferencesApi.md](docs/apis/PreferencesApi.md) |
| RecurrencesApi | [RecurrencesApi.md](docs/apis/RecurrencesApi.md) |
| RuleGroupsApi | [RuleGroupsApi.md](docs/apis/RuleGroupsApi.md) |
| RulesApi | [RulesApi.md](docs/apis/RulesApi.md) |
| SearchApi | [SearchApi.md](docs/apis/SearchApi.md) |
| SummaryApi | [SummaryApi.md](docs/apis/SummaryApi.md) |
| TagsApi | [TagsApi.md](docs/apis/TagsApi.md) |
| TransactionsApi | [TransactionsApi.md](docs/apis/TransactionsApi.md) |
| UserGroupsApi | [UserGroupsApi.md](docs/apis/UserGroupsApi.md) |
| UsersApi | [UsersApi.md](docs/apis/UsersApi.md) |
| WebhooksApi | [WebhooksApi.md](docs/apis/WebhooksApi.md) |

## 🔧 Generation

This library was generated using the OpenAPI Generator from the official Firefly III API specification.

### Generation Command

```bash
docker run --rm -v ./:/local openapitools/openapi-generator-cli generate \
  -i https://api-docs.firefly-iii.org/firefly-iii-6.3.0-v1.yaml \
  -g csharp \
  -o /local \
  --additional-properties=packageName=Brotal.FireflyIII
```

### Manual Generation

If you need to regenerate the library manually:

1. **Create a config.yaml file**:
```yaml
generatorName: csharp
inputSpec: https://api-docs.firefly-iii.org/firefly-iii-6.3.0-v1.yaml
outputDir: out

additionalProperties:
  packageGuid: '{0C876866-5C9F-4F05-BAA0-94B9382A2695}'
```

2. **Run the generator**:
```bash
java -jar openapi-generator-cli.jar generate -c config.yaml
```

## 🛠️ Development

### Building Locally

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

### Testing

```bash
# Run all tests
dotnet test Brotal.FireflyIII.sln

# Run specific test project
dotnet test src/Brotal.FireflyIII.Test/Brotal.FireflyIII.Test.csproj
```

## ❓ Frequently Asked Questions

### 🔄 **What about HttpRequest failures and retries?**
Configure Polly in the IHttpClientBuilder using the provided extension methods.

### 🔑 **How are tokens used?**
Tokens are provided by a TokenProvider class. The default is RateLimitProvider which performs client-side rate limiting. Other providers can be used with the UseProvider method.

### ⚠️ **Does an HttpRequest throw an error when the server response is not Ok?**
It depends on the return type:
- `ApiResponse<T>`: No error thrown, check StatusCode and ReasonPhrase
- `T`: Will throw on error
- `TOrDefault`: Returns null on error

### ✅ **How do I validate requests and process responses?**
Use the provided On and After partial methods in the api classes for custom validation and processing.

## 🚨 Troubleshooting

### Common Issues

1. **🔐 Authentication Failed**
   - Verify your token/API key is correct
   - Ensure the token has the required permissions
   - Check if the token is expired

2. **🌐 Network Issues**
   - Verify your Firefly III instance is accessible
   - Check firewall settings
   - Ensure proper SSL/TLS configuration

3. **📦 Build Failures**
   - Ensure .NET 9.0 SDK is installed
   - Check all dependencies are properly restored
   - Verify the solution file structure

4. **🔍 API Errors**
   - Check the API response status codes
   - Verify request payload format
   - Review Firefly III API documentation

### Useful Commands

```bash
# Check package contents
dotnet nuget list source

# Verify package
dotnet nuget verify nupkgs/*.nupkg

# Test package locally
dotnet nuget add source ./nupkgs -n local
dotnet add package Brotal.FireflyIII --source local

# Check if package version exists on NuGet
curl -s "https://api.nuget.org/v3/registration3/Brotal.FireflyIII/index.json" | grep -o '"version":"[^"]*"'
```

## 🔗 Related Links

- 📦 [NuGet Package](https://www.nuget.org/packages/Brotal.FireflyIII/)
- 📚 [Firefly III API Documentation](https://docs.firefly-iii.org/references/firefly-iii/api/)
- 🏠 [Firefly III Homepage](https://firefly-iii.org/)
- 🔧 [OpenAPI Generator](https://openapi-generator.tech)
- 📂 [GitHub Repository](https://github.com/skb50bd/firefly-iii-ai-ingest)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

---

<div align="center">
  <p>Made with ❤️ for the Firefly III community</p>
  <p>Generated with <a href="https://openapi-generator.tech">OpenAPI Generator</a></p>
</div>
