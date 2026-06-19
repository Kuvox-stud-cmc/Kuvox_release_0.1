# v0.1.0 - Initial Unified Release (Kuvox Platform)

## Summary

This is the first release of the Kuvox platform, integrating our powerful Backend API with the modern React Frontend. This release provides content creators and professionals with a unified experience to manage workspaces, configure their profiles, and access AI-driven features in a secure and scalable environment.

## New Features

- **Unified Monorepo Architecture**: Combined frontend and backend into a single repository for streamlined CI/CD and versioning.
- **Workspace Management**: Users can now create, switch, and manage multiple workspaces seamlessly.
- **Authentication Flow**: Secure login and registration integration.
- **Automated CI/CD**: Added GitHub Actions to automatically build and test both `.NET 8` API and `React/Vite` frontend on every push and PR.

## Bug Fixes

- Fixed minor responsive layout issues in the dashboard sidebars.
- Resolved environment variable parsing in the API configuration.

## Changed

- Refactored project structure to separate `/api` and `/frontend` cleanly.
- Updated `README.md` to include comprehensive setup instructions, product vision, and architecture details following *Engineering Software Products* principles.

## Installation / Upgrade

To run this release locally, download the source code zip or clone the tag:
```bash
git clone --branch v0.1.0 https://github.com/Kuvox-stud-cmc/Kuvox_release_0.1.git
```
Please refer to the `README.md` in the root directory for detailed steps on running via Docker Compose or native environments (Node & .NET SDK).

## Testing Evidence

- **Automated Tests**: CI/CD pipeline runs `.NET` tests and `npm` build checks. See the Actions tab for successful run evidence.
- **Manual QA**: All critical paths (Login, Workspace Switcher, Profile Management) have been manually tested against this tag.

## Known Issues

- Docker Compose setup currently does not auto-seed the database with mock data. You must manually run migrations.
- Mobile responsiveness on the Workspace Switcher dropdown needs slight adjustment on ultra-small screens (<320px).

## Contributors

- The Kuvox Engineering Team
