# Financial Reporting Microservices

A portfolio project demonstrating enterprise-style financial reporting with ASP.NET Core, Clean Architecture principles, SQL Server, Docker, JWT-ready API design, and CI automation.

> This is a personal demonstration project inspired by common financial-services engineering patterns. It contains no employer code or confidential data.

## Features

- RESTful reporting API
- Revenue and transaction summaries
- EF Core data access
- SQL Server support
- Docker Compose for local SQL Server
- Swagger/OpenAPI
- Global exception handling
- xUnit test project
- GitHub Actions CI workflow

## Run locally

```bash
dotnet restore
dotnet run --project src/Reporting.Api
```

Open the Swagger page shown in the console.

## Docker database

```bash
docker compose up -d sqlserver
```

Update the connection string in `src/Reporting.Api/appsettings.json` if needed.

## Example endpoint

```http
GET /api/reports/revenue?from=2026-01-01&to=2026-12-31
```

## Architecture

```text
Reporting.Api -> Reporting.Infrastructure -> SQL Server
       |
       -> Reporting.Domain
```

## Technologies

C#, .NET 8, ASP.NET Core Web API, Entity Framework Core, SQL Server, Docker, Swagger, xUnit, GitHub Actions.
