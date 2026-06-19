# Kuvox - AI-Powered Web Application

Kuvox is a modern, responsive web application that leverages AI to provide powerful tools for its users. This repository is a monorepo containing both the Frontend and the Backend API services.

## 1. Product Vision & Personas (Engineering Software Products)

### Product Vision
Our vision is to empower creators and professionals with an intelligent, easy-to-use platform that accelerates content creation and management workflows using advanced AI. We bridge the gap between complex AI capabilities and intuitive user experiences.

### Target Personas
1. **The Creator (Alice)**: A content creator who needs quick, high-quality generated assets to match her branding.
2. **The Professional (Bob)**: A business professional seeking automated workflows to reduce repetitive tasks and improve efficiency.

### User Stories / Scenarios
- *As Alice, I want to create a new studio workspace so I can organize all my AI-generated assets in one place.*
- *As Bob, I want to quickly toggle between workspaces so I can handle multiple client projects without logging out.*

## 2. Architecture & Design

This project adopts a clean client-server architecture:
- **Frontend**: A modern web client built with React, Vite, and React Router.
- **Backend API**: A robust RESTful service built with .NET 8 (C#) using a modular structure.
- **Database**: Entity Framework Core with migrations.
- **Infrastructure**: Containerized with Docker and Docker Compose for easy deployment.

## 3. Agile & Process

We follow an iterative development process:
- Features are developed in isolated branches and merged via Pull Requests.
- The `main` branch is kept stable and deployable.
- GitHub Actions is used for Continuous Integration (CI).

## 4. Setup and Deployment

### Prerequisites
- Node.js 20+
- .NET 8 SDK
- Docker & Docker Compose

### Running Locally

1. **Clone the repository** (or download the source code from the latest release).
2. **Configure Environments**:
   - Navigate to `api/` and copy `.env.example` to `.env`. Update variables as needed.
   - Navigate to `frontend/` and copy `.env.example` to `.env`. Update variables.

3. **Start the API**:
   ```bash
   cd api
   dotnet restore
   dotnet run
   ```

4. **Start the Frontend**:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

5. **Using Docker** (Production/Staging):
   We provide a `docker-compose.yml` for orchestrating the services.
   ```bash
   cd api
   docker-compose up --build -d
   ```

## 5. Security & Privacy

- **No Secrets in Repo**: All sensitive keys are managed via `.env` files (ignored in `.gitignore`).
- **Validation**: Input validation is handled at both the frontend boundary and the API controllers.

## 6. Testing

- **API Tests**: Execute `dotnet test` in the `api` folder.
- CI/CD automatically runs test suites on every pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
