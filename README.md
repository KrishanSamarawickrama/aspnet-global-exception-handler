# ASP.NET Global Exception Handler

This repository contains an ASP.NET Core project named [`aspnet-global-exception-handler.API`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FBatcave%2FProjects%2Faspnet-global-exception-handler%2Faspnet-global-exception-handler.API%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Batcave\Projects\aspnet-global-exception-handler\aspnet-global-exception-handler.API"), designed to demonstrate a global exception handling mechanism in ASP.NET Core applications. The primary focus is on the `GlobalExceptionHandlerMiddleware` class, which intercepts exceptions thrown by the application, logs them, and returns a standardized error response to the client.

## Project Structure

- **GlobalExceptionHandlerMiddleware.cs**: The core of the project, this file contains the `GlobalExceptionHandlerMiddleware` class that catches unhandled exceptions, logs them using Serilog, and returns a generic error response to the client.
- **Program.cs**: The entry point of the application, where the middleware is configured and added to the HTTP request pipeline. It also contains the Serilog configuration.
- **appsettings.json** & **appsettings.Development.json**: Configuration files for the application, including logging settings.
- **aspnet-global-exception-handler.API.csproj**: The project file containing project dependencies and configurations.
- **.idea/config/applicationhost.config**: Configuration for the application host, useful for development environments.

## Features

- **Global Exception Handling**: Utilizes middleware to catch unhandled exceptions across the entire application, ensuring that no exception goes unnoticed.
- **Logging with Serilog**: Integrates Serilog for robust logging capabilities, including logging to the console and to files with a daily rolling interval.
- **Standardized Error Response**: Converts exceptions into a standard JSON response format, improving the client's error handling experience.

## Setup and Configuration

1. **Clone the Repository**: Start by cloning this repository to your local machine.
2. **Restore Dependencies**: Run `dotnet restore` to install the necessary packages.
3. **Configure Serilog**: Adjust the Serilog configuration in [`Program.cs`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FBatcave%2FProjects%2Faspnet-global-exception-handler%2Faspnet-global-exception-handler.API%2FProgram.cs%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Batcave\Projects\aspnet-global-exception-handler\aspnet-global-exception-handler.API\Program.cs") as needed. By default, logs are written to the console and to files in the `logs` directory.
4. **Run the Application**: Execute `dotnet run` to start the application. By default, it will listen on http://localhost:5000.

## Usage

Once the application is running, it will intercept any unhandled exceptions thrown by the application, log them, and return a generic error response to the client. This mechanism is crucial for production environments where detailed error information should not be exposed directly to the client but should be logged for analysis by developers.

## Contributing

Contributions to improve the global exception handler or to extend the project's functionality are welcome. Please feel free to submit pull requests or open issues to discuss potential improvements.

## License

This project is licensed under the MIT License - see the [`LICENSE`](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FBatcave%2FProjects%2Faspnet-global-exception-handler%2FLICENSE%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Batcave\Projects\aspnet-global-exception-handler\LICENSE") file for details.