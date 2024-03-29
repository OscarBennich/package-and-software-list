# List of Packages and Software for .NET development
This is a list of packages and software that I want to keep track of, so I'm collecting information about them here.

## Nuget Packages / Libraries
### SignalR
https://github.com/SignalR/SignalR \
Web-socket implementation for .NET core. Enables real-time information to be pushed from the server to the client.

<br/>

### FluentValidation
https://github.com/JeremySkinner/FluentValidation \
A small validation library that uses a fluent interface and lambda expressions for building validation rule.
```csharp
RuleFor(x => x.Forename).NotEmpty().WithMessage("Please specify a first name");
```
This is great for validating input for APIs and more.

<br/>

### FluentAssertions
https://github.com/fluentassertions/fluentassertions \
Allows you to write things like this in unit tests:
```csharp
accountNumber.Should().Be("0987654321")
```

<br/>

### NSubstitute
https://github.com/nsubstitute/NSubstitute \
A great mocking library for .NET.
```csharp
//Create:
var calculator = Substitute.For<ICalculator>();

//Set a return value:
calculator.Add(1, 2).Returns(3);
Assert.AreEqual(3, calculator.Add(1, 2));

//Check received calls:
calculator.Received().Add(1, Arg.Any<int>());
calculator.DidNotReceive().Add(2, 2);

//Raise events
calculator.PoweringUp += Raise.Event();
```

<br/>

### Serilog
https://github.com/serilog/serilog \
Serilog is a diagnostic logging library for .NET applications.
```csharp
_logger.Error("Something went wrong", caught);
```

<br/>

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

<br/>

### MediatR
https://github.com/jbogard/MediatR \
Mediator pattern implementation for .NET.

<br/>

### RawRabbit
https://github.com/pardahlman/RawRabbit \
RabbitMQ implementation for .NET.
```csharp
var client = RawRabbitFactory.CreateSingleton();
await client.SubscribeAsync<BasicMessage>(async msg =>
{
  Console.WriteLine($"Received: {msg.Prop}.");
});

await client.PublishAsync(new BasicMessage { Prop = "Hello, world!"});
```

<br/>

### Hangfire
https://github.com/HangfireIO/Hangfire \
An easy way to perform background jobs and schedule future jobs in .NET.
```csharp
BackgroundJob.Schedule(() => Console.WriteLine("Reliable!"), TimeSpan.FromDays(7));
```

<br/>

### Swagger
https://swagger.io/ \
Automatic and easy way for API self-documentation (and more).

<br/>

### Swashbuckle
https://github.com/domaindrivendev/Swashbuckle \
Seamlessly adds a Swagger to WebApi projects in .NET.

```csharp
httpConfiguration
     .EnableSwagger(c => c.SingleApiVersion("v1", "A title for your API"))
     .EnableSwaggerUi();
```

<br/>

### IdentityServer4
https://github.com/IdentityServer/IdentityServer4 \
OpenID Connect and OAuth 2.0 Framework for ASP.NET Core.

<br/>

### IdentityModel
https://github.com/IdentityModel/IdentityModel \
IdentityModel contains client libraries for many interactions with endpoints defined in OpenID Connect and OAuth 2.0
```csharp
var request = new ClientCredentialsTokenRequest
{
    Address = "https://demo.identityserver.io/connect/token",
    ClientId = "client",
    ClientSecret = "secret"
});
```

<br/>

### Flurl
https://github.com/tmenier/Flurl \
Flurl is a modern, fluent, asynchronous, testable, portable, buzzword-laden URL builder and HTTP client library for .NET.
```csharp
// fake & record all http calls in the test subject
using (var httpTest = new HttpTest()) {
    // arrange
    httpTest.RespondWith(200, "OK");
    // act
    await sut.CreatePersonAsync();
    // assert
    httpTest.ShouldHaveCalled("https://api.com/*")
        .WithVerb(HttpMethod.Post)
        .WithContentType("application/json");
}
```

<br/>

### Newtonsoft
https://github.com/JamesNK/Newtonsoft.Json \
Json.NET is a popular high-performance JSON framework for .NET.

<br/>

###  Middleware
https://github.com/khellang/Middleware \
Various ASP.NET Core middleware. Mostly for use in APIs.

<br/>

###  Autofac
https://github.com/autofac/Autofac \
Autofac is an IoC container for Microsoft .NET. It manages the dependencies between classes so that applications stay easy to change as they grow in size and complexity. This is achieved by treating regular .NET classes as components.

<br/>

###  AutoFixture
https://github.com/AutoFixture/AutoFixture \
AutoFixture is an open source library for .NET designed to minimize the 'Arrange' phase of your unit tests in order to maximize maintainability.
```csharp
[Fact]
public void IntroductoryTest()
{
    // Arrange
    Fixture fixture = new Fixture();

    int expectedNumber = fixture.Create<int>();
    MyClass sut = fixture.Create<MyClass>();
    // Act
    int result = sut.Echo(expectedNumber);
    // Assert
    Assert.Equal(expectedNumber, result);
}
```

<br/>

## Software
### ReSharper
https://www.jetbrains.com/resharper \
Visual Studio extension. Makes life easier.

<br/>

### SQL Server Management Studio
https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-2017 \
Client used for viewing and manipulating SQL databases.

<br/>

### TortoiseGit
https://tortoisegit.org/download \
TortoiseGit is a Windows Shell Interface to Git and based on TortoiseSVN.

<br/>

### BeyondCompare
https://www.scootersoftware.com/ \
Makes comparing files easy, good for commits and especially merge conflicts.

<br/>

### Postman
https://www.getpostman.com/ \
Easy way to set up, make, test, and distribute API calls.

<br/>


### Docker Desktop
https://www.docker.com/products/docker-desktop \
Docker desktop client.
