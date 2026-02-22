<div align="center">

<br/>

```
██████╗  █████╗ ██╗   ██╗███╗   ███╗███████╗███╗   ██╗████████╗
██╔══██╗██╔══██╗╚██╗ ██╔╝████╗ ████║██╔════╝████╗  ██║╚══██╔══╝
██████╔╝███████║ ╚████╔╝ ██╔████╔██║█████╗  ██╔██╗ ██║   ██║   
██╔═══╝ ██╔══██║  ╚██╔╝  ██║╚██╔╝██║██╔══╝  ██║╚██╗██║   ██║   
██║     ██║  ██║   ██║   ██║ ╚═╝ ██║███████╗██║ ╚████║   ██║   
╚═╝     ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚═╝╚══════╝╚═╝  ╚═══╝   ╚═╝  
                    M A N A G E R   A P P
```

<br/>

**A full-stack payment management application built with ASP.NET Core Web API & Angular 16**

<br/>

![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Angular](https://img.shields.io/badge/Angular_16-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![Entity Framework](https://img.shields.io/badge/Entity_Framework-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)

<br/>

</div>

---

## 📖 Overview

**Payment Manager App** is a full-stack demo application that showcases the integration of **ASP.NET Core Web API** with **Angular 16**, implementing complete **CRUD operations** for managing payment records. This project serves as a practical reference for developers looking to understand how modern .NET backends and Angular frontends communicate in a real-world scenario.

The project covers everything from building a RESTful API with Entity Framework Core, setting up database migrations, configuring CORS policies, to building a reactive Angular frontend with form validation, toast notifications, and a clean UI.

---

## ✨ Features

| Feature | Description |
|---|---|
| 📋 **List Payments** | Retrieve and display all payment records in a clean tabular view |
| ➕ **Create Payment** | Add new payment entries via a validated Angular reactive form |
| ✏️ **Update Payment** | Edit existing payment details with pre-populated form fields |
| 🗑️ **Delete Payment** | Remove payment records with confirmation |
| 🔔 **Toast Notifications** | Real-time feedback for all CRUD operations |
| ✅ **Form Validation** | Client-side Angular validation with meaningful error messages |
| 🔄 **Form Reset** | One-click form reset functionality |
| 🌐 **CORS Configured** | Cross-origin requests properly enabled between API and Angular app |

---

## 🏗️ Architecture

```
Payment-Manager-App/
│
├── 📁 PaymentAPI/                  # ASP.NET Core Web API (Backend)
│   ├── Controllers/                # API Controllers with CRUD endpoints
│   ├── Models/                     # EF Core Entity Models
│   ├── Data/                       # DbContext & Database Configuration
│   ├── Migrations/                 # EF Core Database Migrations
│   └── Program.cs / Startup.cs    # App configuration, DI, CORS setup
│
└── 📁 PaymentApp/                  # Angular 16 Application (Frontend)
    ├── src/
    │   ├── app/
    │   │   ├── components/         # Angular components (list, form, etc.)
    │   │   ├── services/           # HTTP service layer
    │   │   └── models/             # TypeScript interfaces/models
    │   └── environments/           # Environment configuration
    └── angular.json
```

---

## 🛠️ Tech Stack

### Backend
- **ASP.NET Core** — RESTful Web API framework
- **Entity Framework Core** — ORM for database operations
- **SQL Server** — Relational database
- **Dependency Injection** — Built-in .NET DI container
- **CORS Policy** — Cross-origin resource sharing configuration

### Frontend
- **Angular 16** — Component-based SPA framework
- **TypeScript** — Strongly-typed JavaScript
- **Angular HttpClient** — HTTP communication with the API
- **Angular Reactive Forms** — Form management with validation
- **Toast Notifications** — User feedback for actions
- **HTML5 / CSS3** — Markup and styling

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed on your system:

| Tool | Version | Download |
|---|---|---|
| .NET SDK | 6.0 or later | [Download](https://dotnet.microsoft.com/download) |
| Node.js | 16.x or later | [Download](https://nodejs.org/) |
| Angular CLI | 16.x | `npm install -g @angular/cli` |
| SQL Server | Any edition | [Download](https://www.microsoft.com/sql-server) |
| Visual Studio / VS Code | Latest | [VS](https://visualstudio.microsoft.com/) / [VS Code](https://code.visualstudio.com/) |

---

### ⚙️ Backend Setup (ASP.NET Core API)

**1. Clone the repository**

```bash
git clone https://github.com/akash4550/Payment-Manager-App.git
cd Payment-Manager-App
```

**2. Navigate to the API project**

```bash
cd PaymentAPI
```

**3. Configure the database connection**

Open `appsettings.json` and update the connection string to point to your SQL Server instance:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=PaymentManagerDB;Trusted_Connection=True;"
  }
}
```

**4. Apply database migrations**

```bash
dotnet ef database update
```

> This will create the database and apply all pending migrations automatically.

**5. Run the API**

```bash
dotnet run
```

The API will start at `https://localhost:7001` (or the port shown in the console). You can explore the endpoints via the Swagger UI at:

```
https://localhost:{PORT}/swagger
```

---

### 🖥️ Frontend Setup (Angular App)

**1. Navigate to the Angular project**

```bash
cd ../PaymentApp
```

**2. Install dependencies**

```bash
npm install
```

**3. Configure the API URL** *(if needed)*

In `src/environments/environment.ts`, make sure the API URL points to your running backend:

```typescript
export const environment = {
  production: false,
  apiUrl: 'https://localhost:{PORT}/api'
};
```

**4. Start the Angular development server**

```bash
ng serve
```

The app will be available at:

```
http://localhost:4200
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/payments` | Retrieve all payment records |
| `GET` | `/api/payments/{id}` | Get a single payment by ID |
| `POST` | `/api/payments` | Create a new payment record |
| `PUT` | `/api/payments/{id}` | Update an existing payment |
| `DELETE` | `/api/payments/{id}` | Delete a payment record |

---

## 📚 Concepts Covered

This project walks through a comprehensive set of concepts for full-stack .NET + Angular development:

**Backend (ASP.NET Core)**
- Creating a Web API project from scratch
- Defining Entity Framework Core models and `DbContext`
- Running database migrations with EF Core CLI
- Building RESTful API controllers with CRUD operations
- Understanding how Dependency Injection (DI) works in ASP.NET Core
- Configuring and enabling CORS policies for cross-origin communication

**Frontend (Angular 16)**
- Scaffolding an Angular application
- Understanding Angular application structure
- JSON case conversion between .NET (PascalCase) and Angular (camelCase)
- Retrieving and displaying data using `HttpClient` and Observables
- Rendering arrays of objects with `*ngFor`
- Designing reactive forms with Angular
- Implementing form submit, reset, and validation
- Showing toast notifications for user feedback
- Performing full Update & Delete operations from the UI

---

## 🔍 How Dependency Injection Works in ASP.NET Core

One key concept illustrated in this project is how **DI** is configured in `Program.cs`:

```csharp
builder.Services.AddDbContext<PaymentDbContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));

builder.Services.AddCors(options =>
{
    options.AddPolicy("AllowAngularApp", policy =>
    {
        policy.WithOrigins("http://localhost:4200")
              .AllowAnyHeader()
              .AllowAnyMethod();
    });
});
```

The Angular app at `localhost:4200` is whitelisted to communicate with the API — a critical step for local full-stack development.

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

---



<div align="center">

Made with ❤️ by [akash4550](https://github.com/akash4550)

⭐ If you found this project helpful, please give it a star!

</div>
