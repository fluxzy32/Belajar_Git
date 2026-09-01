# Roadmap Belajar

## Git
1. Git rmote
2. Git pull request

---

# Roadmap Belajar C# & .NET (Dari JavaScript)

## 📋 Prasyarat
- [ ] Sudah menguasai JavaScript (ES6+, async/await, Promise, module)
- [ ] Paham konsep OOP dasar (class, inheritance, polymorphism)
- [ ] Paham konsep async programming (event loop, callback, promise)

---

## 🚀 Phase 1: Fundamentals C# (Minggu 1-2)

### 1. Setup Environment
- [ ] Install .NET SDK (LTS version: .NET 8)
- [ ] Install VS Code + C# Dev Kit extension **atau** Visual Studio Community
- [ ] Setup terminal: `dotnet --version`, `dotnet new console -n HelloWorld`

### 2. Sintaks Dasar & Perbandingan JS
| Konsep | JavaScript | C# |
|--------|------------|-----|
| Variable | `let/const` | `var` (type inference), explicit type `int`, `string`, `bool` |
| Function | `function` / arrow | `void Method()` / `T Method()` |
| Class | `class` | `class` (sama, tapi strict) |
| Null | `null`/`undefined` | `null` + `?` nullable types |
| Async | `async/await` | `async/await` + `Task<T>` |

### 3. Tipe Data & Variabel
- [ ] Value types vs Reference types (struct vs class)
- [ ] Primitive types: `int`, `double`, `decimal`, `bool`, `char`, `string`
- [ ] Nullable types: `int?`, `string?`
- [ ] `var` vs explicit typing
- [ ] Constants: `const` vs `readonly`

### 4. Control Flow
- [ ] `if/else`, `switch` (pattern matching modern)
- [ ] Loops: `for`, `foreach`, `while`, `do-while`
- [ ] Pattern matching: `is`, `switch` expression

### 5. Methods & Parameters
- [ ] Method signature, return types
- [ ] `ref`, `out`, `in`, `params`
- [ ] Optional parameters, named arguments
- [ ] Expression-bodied members `=>`

### 6. OOP di C#
- [ ] Class, Interface, Abstract class
- [ ] Properties (auto-implemented, full) vs Fields
- [ ] Access modifiers: `public`, `private`, `protected`, `internal`, `protected internal`, `private protected`
- [ ] Inheritance, `virtual`/`override`/`sealed`
- [ ] Interface default implementation (C# 8+)
- [ ] Records (C# 9+) - immutable data types
- [ ] Pattern matching dengan records

---

## 🔧 Phase 2: .NET Ecosystem & Tooling (Minggu 3)

### 1. Project Structure
- [ ] `dotnet new sln`, `dotnet new classlib`, `dotnet new webapi`, `dotnet new xunit`
- [ ] `.csproj` format (SDK-style) - mirip `package.json`
- [ ] `dotnet add reference`, `dotnet add package` (NuGet = npm)

### 2. Dependency Injection (Built-in)
- [ ] `IServiceCollection`, `ServiceLifetime` (Singleton, Scoped, Transient)
- [ ] Constructor injection
- [ ] `IOptions<T>` pattern untuk configuration

### 3. Configuration & Settings
- [ ] `appsettings.json` (mirip `.env` + `config`)
- [ ] Environment variables, User Secrets
- [ ] `IConfiguration`, `IOptionsMonitor<T>`

### 4. Logging
- [ ] `ILogger<T>`, Log Levels
- [ ] Structured logging, Serilog integration

---

## ⚡ Phase 3: Async Programming & Modern C# (Minggu 4)

### 1. Task & Async/Await
- [ ] `Task`, `Task<T>`, `ValueTask<T>`
- [ ] `async`/`await` mechanics (state machine)
- [ ] `ConfigureAwait(false)` - library vs app code
- [ ] Parallel: `Task.WhenAll`, `Task.WhenAny`, `Parallel.ForEachAsync`

### 2. Modern C# Features (C# 8-12)
- [ ] Nullable reference types (`#nullable enable`)
- [ ] Pattern matching enhancements
- [ ] Records & `with` expressions
- [ ] Init-only setters, required properties (C# 11)
- [ ] Primary constructors (C# 12)
- [ ] Collection expressions `[1, 2, 3]` (C# 12)
- [ ] File-scoped types

### 3. LINQ (Language Integrated Query)
- [ ] Query syntax vs Method syntax
- [ ] Deferred execution vs Immediate
- [ ] `IEnumerable<T>` vs `IQueryable<T>`
- [ ] Common operators: `Where`, `Select`, `GroupBy`, `Join`, `Aggregate`

---

## 🌐 Phase 4: ASP.NET Core Web API (Minggu 5-7)

### 1. Minimal APIs vs Controllers
- [ ] Minimal APIs (modern, ringan - mirip Express/Fastify)
- [ ] Controllers (tradisional, fitur lengkap)
- [ ] Route groups, Route handlers

### 2. Request/Response Handling
- [ ] Model binding, Validation (`[ApiController]`, `FluentValidation`)
- [ ] `IResult`, `Results.Ok()`, `Results.NotFound()`, `TypedResults`
- [ ] ProblemDetails (RFC 7807)

### 3. Data Access - Entity Framework Core
- [ ] Code-First vs Database-First
- [ ] `DbContext`, `DbSet<T>`, Migrations (`dotnet ef migrations add`)
- [ ] LINQ to Entities, Tracking vs NoTracking
- [ ] Relationships: One-to-One, One-to-Many, Many-to-Many
- [ ] Performance: `AsNoTracking`, `AsSplitQuery`, compiled queries

### 4. Authentication & Authorization
- [ ] JWT Bearer tokens
- [ ] ASP.NET Core Identity
- [ ] Policy-based authorization, Claims, Roles
- [ ] OpenID Connect / OAuth2 integration

### 5. API Documentation & Testing
- [ ] Swagger/OpenAPI (Scalar, Swashbuckle)
- [ ] Integration testing dengan `WebApplicationFactory<T>`
- [ ] Unit testing: xUnit, NUnit, Moq/NSubstitute

---

## 🗄️ Phase 5: Data & Persistence Lanjutan (Minggu 8)

### 1. EF Core Lanjutan
- [ ] Raw SQL, Stored Procedures
- [ ] Change tracking, Concurrency tokens
- [ ] Global query filters (soft delete)
- [ ] Performance tuning, Query splitting

### 2. Caching
- [ ] `IMemoryCache`, `IDistributedCache` (Redis)
- [ ] Response caching, Output caching
- [ ] Cache aside pattern

### 3. Message Queues & Background Jobs
- [ ] `IHostedService`, `BackgroundService`
- [ ] Hangfire, MassTransit, MediatR
- [ ] RabbitMQ / Azure Service Bus / Kafka basics

---

## 🧪 Phase 6: Testing & Quality (Minggu 9)

### 1. Unit Testing
- [ ] xUnit fundamentals, AAA pattern
- [ ] Mocking: Moq / NSubstitute / FakeItEasy
- [ ] Testcontainers untuk integration test DB

### 2. Architecture Testing
- [ ] NetArchTest / ArchUnitNET
- [ ] Clean Architecture enforcement

### 3. Code Quality
- [ ] `dotnet format`, EditorConfig
- [ ] Roslyn Analyzers, SonarAnalyzer
- [ ] StyleCop, ReSharper/ Rider inspections

---

## 🚢 Phase 7: Deployment & DevOps (Minggu 10)

### 1. Containerization
- [ ] Dockerfile multi-stage build untuk .NET
- [ ] `dotnet publish -c Release -o out`
- [ ] Distroless / Alpine images

### 2. CI/CD
- [ ] GitHub Actions / GitLab CI / Azure DevOps
- [ ] Build, Test, Publish, Deploy pipeline

### 3. Observability
- [ ] OpenTelemetry, Prometheus, Grafana
- [ ] Health checks (`/health`, `/health/ready`)
- [ ] Structured logging di production

---

## 📚 Phase 8: Specialization (Pilih 1+ berdasarkan minat)

### Backend Enterprise
- [ ] Clean Architecture / Vertical Slice Architecture
- [ ] Domain-Driven Design (DDD), CQRS, Event Sourcing
- [ ] MediatR, FluentValidation, Mapster/AutoMapper

### Cloud Native
- [ ] Azure / AWS / GCP services
- [ ] Kubernetes basics untuk .NET
- [ ] .NET Aspire untuk local dev

### Real-time & Modern Web
- [ ] SignalR (WebSockets)
- [ ] gRPC, Protobuf
- [ ] Blazor (WASM / Server) - fullstack C#

### Data Engineering
- [ ] Apache Spark .NET, ML.NET
- [ ] Time-series databases, OLAP

---

## 🎯 Project Milestones (Portfolio)

| Level | Project | Teknologi Utama |
|-------|---------|-----------------|
| Beginner | Console App: Task Manager CLI | C# basics, File I/O, DI |
| Beginner | Web API: Todo CRUD | Minimal API, EF Core, SQLite |
| Intermediate | E-commerce API | Auth, Payments, Background jobs, Redis |
| Advanced | Multi-tenant SaaS Starter | Clean Arch, DDD, Multi-tenancy, SignalR |

---

## 📖 Referensi Belajar Recommended

### Official (Gratis)
- [Microsoft Learn C#](https://learn.microsoft.com/dotnet/csharp/)
- [ASP.NET Core Docs](https://learn.microsoft.com/aspnet/core/)
- [EF Core Docs](https://learn.microsoft.com/ef/core/)

### Books
- *C# in Depth* - Jon Skeet
- *Concurrency in C#* - Stephen Cleary
- *Architecting ASP.NET Core Applications* - Carl-Hugo Marcander

### YouTube Channels
- Nick Chapsas (Modern .NET)
- Tim Corey (Deep dives)
- Milan Jovanović (Architecture)
- Code Maze (Tutorials)

### Practice
- [Exercism C# Track](https://exercism.org/tracks/csharp)
- [LeetCode C#](https://leetcode.com/tag/csharp/)
- [Codewars](https://www.codewars.com/)

---

## ⏱️ Estimasi Waktu Total: ~10-12 Minggu (part-time 10-15 jam/minggu)

### Tips dari JS Developer:
1. **Jangan skip nullable reference types** - bikin code lebih safe kayak TypeScript strict mode
2. **EF Core ≠ Prisma/TypeORM** - EF Core tracking behavior beda, pelajari `ChangeTracker`
3. **DI adalah first-class citizen** - beda dengan JS manual wiring
4. **Struct vs Class** - value types (struct) di-stack, reference types (class) di-heap
5. **Async di C# benar-benar async** - tidak single-threaded seperti JS event loop

---

## ✅ Checklist Progres

- [ ] Phase 1: Fundamentals C#
- [ ] Phase 2: .NET Ecosystem
- [ ] Phase 3: Async & Modern C#
- [ ] Phase 4: ASP.NET Core Web API
- [ ] Phase 5: Data & Persistence
- [ ] Phase 6: Testing & Quality
- [ ] Phase 7: Deployment & DevOps
- [ ] Phase 8: Specialization
- [ ] Portfolio Project 1 (Beginner)
- [ ] Portfolio Project 2 (Intermediate)
- [ ] Portfolio Project 3 (Advanced)