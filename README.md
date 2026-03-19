# SupportDesk.Api

SupportDesk.Api is an ASP.NET Core 8 Web API portfolio project for ticket management. It demonstrates modern backend development concepts including JWT authentication, EF Core with PostgreSQL, user registration, role and ownership-based authorization, pagination, filtering, sorting, structured logging, and integration testing.

## Tech Stack

- ASP.NET Core 8 Web API
- EF Core 8
- PostgreSQL
- JWT Authentication
- Serilog
- xUnit integration tests

## Features

- User registration with hashed passwords
- Login with JWT bearer tokens
- Current user endpoint
- Ticket CRUD
- Ownership-based authorization
- Admin override for ticket updates/deletes
- Pagination
- Filtering and sorting on ticket list
- Structured logging
- Integration tests

## Authorization Rules

- Authenticated users can create tickets
- Ticket owners can update and delete their own tickets
- Admin users can update and delete any ticket

## Ticket Query Options

`GET /api/tickets` supports:

- `page`
- `pageSize`
- `status`
- `search`
- `createdBy`
- `sortBy`
- `sortDirection`

Supported `sortBy` values:

- `createdAtUtc`
- `id`
- `title`
- `status`
- `createdBy`

Supported `sortDirection` values:

- `asc`
- `desc`

## Run Locally

1. Start PostgreSQL
2. Update `appsettings.Development.json` if needed
3. Apply migrations

```bash
dotnet ef database update
