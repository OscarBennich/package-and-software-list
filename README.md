# List of Packages and Software for .NET development
This is a list of packages and software that I want to keep track of, so I'm collecting information about them here.

## Nuget Packages / Libraries
### SignalR
https://github.com/SignalR/SignalR \
Web-socket implementation for .NET core. Enables real-time information to be pushed from the server to the client.


### FluentValidation
https://github.com/JeremySkinner/FluentValidation \ 
A small validation library that uses a fluent interface and lambda expressions for building validation rule.
```csharp
RuleFor(x => x.Forename).NotEmpty().WithMessage("Please specify a first name");
```
This is great for validating input for APIs and more.

### FluentAssertions
https://github.com/fluentassertions/fluentassertions \
Description: Allows you to write things like this in unit tests:
```csharp
accountNumber.Should().Be("0987654321")
```

### Serilog
https://github.com/serilog/serilog \
Serilog is a diagnostic logging library for .NET applications.
```csharp
_logger.Error("Something went wrong", caught);
```

### AutoMapper
https://github.com/AutoMapper/AutoMapper \ 
AutoMapper is a simple little library built to solve a deceptively complex problem - getting rid of code that mapped one object to another.
```csharp
var configuration = new MapperConfiguration(cfg => 
{
    cfg.CreateMap<Foo, FooDto>();
});

var fooDto = mapper.Map<FooDto>(foo);
```

### MediatR
Description: Mediator pattern implementation for .NET\
Link: https://github.com/jbogard/MediatR

### RawRabbit
Description: RabbitMQ implementation for .NET\
Link: https://github.com/pardahlman/RawRabbit

### Hangfire
Description: An easy way to perform background jobs and schedule future jobs in .NET\ 
Link: https://github.com/HangfireIO/Hangfire

### Swagger
Description: Automatic and easy way for API self-documentation\
Link: https://swagger.io/

### IdentityServer4
Description: OpenID Connect and OAuth 2.0 Framework for ASP.NET Core\
Link: https://github.com/IdentityServer/IdentityServer4

### IdentityModel
Description: \
Link:

### Flurl
Description: \
Link:

## Software
### ReSharper
Description: Visual Studio extension\
Link: https://www.jetbrains.com/resharper/

### SQL Server Management Studio
Description: - \
Link: https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017

### TortoiseGit
Description: TortoiseGit is a Windows Shell Interface to Git and based on TortoiseSVN\
Link: https://tortoisegit.org/download/

### BeyondCompare
Description: Makes comparing files easy, good for commits and especially merge conflicts\
Link: https://www.scootersoftware.com/

### Postman
Description:\
Link:
