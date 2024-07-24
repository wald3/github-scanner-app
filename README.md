# GitHub Scanner App

Welcome to the GitHub Scanner App repository. This application is designed to scan GitHub repositories and provide insights based on the analysis. The repository includes two submodules and uses Docker Compose to streamline the deployment process.

## Repository Structure

- **Main Application**: Contains the core functionality of the GitHub Scanner App.
- **Server**: A submodule that provides GraphQL api for the application.
- **Client**: Another submodule with fontend for the application.

## Prerequisites

Before you can deploy the application, ensure you have the following installed:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Setting Up the Repository

**Clone the repository**:

```bash
git clone --recurse-submodules https://github.com/wald3/github-scanner-app.git
cd github-scanner-app
```

## Creating a GitHub Access Token

To access private repositories and webhooks, you need to create a GitHub access token. You can choose between a fine-grained token or a classic token.

### Fine-Grained Token

1. Go to [GitHub - Fine-Grained Tokens](https://github.com/settings/tokens?type=beta).
2. Click **Generate New Token**.
3. Select **Fine-Grained Token**.
4. Specify the permissions needed for accessing repositories and webhooks.
5. Click **Generate Token** and save the token securely.

### Classic Token

1. Go to [GitHub - Classic Tokens](https://github.com/settings/tokens).
2. Click **Generate New Token**.
3. Provide a note for the token.
4. Select the required scopes such as `repo` for full control of private repositories and `admin:repo_hook` for managing webhooks.
5. Click **Generate Token** and save the token securely.

## Deployment

To deploy the GitHub Scanner App using Docker Compose, run:

```bash
docker-compose -p github-scanner-app up --build
```
