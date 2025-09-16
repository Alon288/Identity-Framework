# Identity Framework Project

A web application demonstrating the implementation of ASP.NET Core Identity Framework.  
This project was built following the [YouTube tutorial](https://www.youtube.com/watch?v=wzaoQiS_9dI&t=901s) and extended/customized for learning and experimentation.

---

## Table of Contents

- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
  - [Configuration](#configuration)  
- [Project Structure](#project-structure)  
- [Usage](#usage)  
- [Authentication & Authorization](#authentication--authorization)  
- [Customizations Made](#customizations-made)  
- [Known Issues / Limitations](#known-issues--limitations)  

---

## Features

- User registration, login, logout  
- Role-based access control (e.g., Admin, User)  
- Secure password hashing  
- Email confirmation for new users  
- Profile management  
- Support for authorization policies/claims (if implemented)  
- (Any other features you added: e.g. Two-factor authentication, social login, etc.)

---

## Tech Stack

- **Framework:** ASP.NET Core  
- **Identity:** ASP.NET Core Identity Framework  
- **Database:** SQL Server / (or whichever DB you used)  
- **ORM:** Entity Framework Core  
- **Frontend:** Razor Pages / MVC / Blazor (whichever was used)  
- **Other tools:** (e.g., Visual Studio / VS Code, Git, etc.)

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

- [.NET SDK](https://dotnet.microsoft.com/download) (version X.Y.Z or higher)  
- Visual Studio 2022 / Visual Studio Code (optional but recommended)  
- SQL Server / LocalDB / SQLite (whatever you used)  
- Git

### Installation

1. Clone the repository:  
   ```bash
   git clone https://github.com/Alon288/identity-framework-project.git
   cd identity-framework
   ```
2. Restore NuGet packages:
    ```bash
    dotnet restore
    ```
3. Apply database migrations:
    ```bash
    dotnet ef database update
    ```
4. Run the project:
    ```bash
    dotnet run
    ```

### Configuration
- Edit appsettings.json to set your connection string for the database.
- If email confirmation is implemented, configure SMTP or email service settings.
- Optionally, configure roles you wish to seed (e.g., in Program.cs or a seed class).

###Project Structure
```bash
/IdentityFrameworkProject
├── Areas/
│   └── Identity/                     # Identity scaffolded files (Pages, Data, etc.)
├── Controllers/
├── Models/
├── Data/
│   └── ApplicationDbContext.cs       # The Identity DbContext
├── Services/                         # Any custom services (email, claims, etc.)
├── Views/ or Pages/                  # Frontend (Razor / MVC views)
├── Migrations/                       # EF Core migrations
├── appsettings.json
├── Program.cs
└── README.md
```
### Usage
1. Start the application.
2. Register a new user via the /Register page.
3. Confirm the account via the email link (if implemented).
4. Login.
5. Demonstrate role-based pages: e.g., /Admin only accessible by users in “Admin” role.
6. Test logout, password reset, profile update (if available).

### Authentication & Authorization
- Identity handles user authentication (login/logout).
- Passwords are stored securely (hashed + salted).
- Roles are used to control access to certain parts of the application.
- (If used) Policy-based authorization / claims-based authorization is configured.

### Customizations Made
- Renamed default DbContext to ApplicationDbContext to avoid naming conflicts.
- Seeded user roles at startup (Admin, User).
- Added custom UI pages / styling (if you changed scaffolded identity pages).
- Integrated email confirmation / password reset (if you implemented them).
- Additional claims or user data in user profile (if you added fields).

