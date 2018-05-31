# ASP.NET Core 2 Controller Cancellation Token Example

This is a simple ASP.NET Core 2 project that demonstrates using a CancellationToken with Controller Actions and an ExceptionFilter to help intercept the resulting TokenCancellationExpcetions and TaskCancellationExceptions. 

This project was derived by following along with the blog post [Using CancellationTokens in ASP.NET Core MVC controllers](https://andrewlock.net/using-cancellationtokens-in-asp-net-core-mvc-controllers/). I highly recommend you read that article to follow along with this code.

## How to run

### Inside VS Code

If you've opened up this project in Visual Studio Code, simply run the Debug launch profile (```Debug -> Start Debugging (F5)```).

### From the CLI

If you're in a terminal / command prompt at the root directory of the project, simply run ```dotnet run```

## Endpoints to test with

http://localhost:5000/slowtest - Test without a CancellationToken involved

http://localhost:5000/slowtestwithtoken - Test with a CancellationToken introduced

http://localhost:5000/slowtestwithsynchronousoperation - Test with a wrapped Synchronous operation and CancellationToken
