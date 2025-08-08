# Library App

## Description

Library App is a sample library management system built with .NET. It demonstrates clean architecture principles, separation of concerns, and testable code. The application allows searching for patrons, managing book loans, and handling memberships, using JSON files for data storage and a console interface for user interaction.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Json/
    - Program.cs
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
- tests/
  - UnitTests/
    - LoanFactory.cs
    - ...

## Key Classes and Interfaces

- **Library.ApplicationCore**
  - `Entities/Patron`, `Entities/Book`, `Entities/Loan`: Core domain models.
  - `Interfaces/IPatronRepository`, `Interfaces/ILoanRepository`: Repository interfaces for data access.
  - `Services/PatronService`, `Services/LoanService`: Business logic and domain services.
- **Library.Infrastructure**
  - `Data/JsonData`: Loads, saves, and populates data from JSON files.
  - `Data/JsonPatronRepository`: Implements patron data access using JSON.
  - `Data/JsonLoanRepository`: Implements loan data access using JSON.
- **Library.Console**
  - `ConsoleApp`: Main console UI workflow and state management.
  - `Program.cs`: Application entry point and dependency injection setup.
- **tests/UnitTests**
  - Unit tests for core services and business logic.

## Usage

1. **Build the solution:**
   ```sh
   dotnet build
2. **Run the console application:**
   dotnet run --project src/Library.Console/Library.Console.csproj
3. **Run unit tests:**
   dotnet test