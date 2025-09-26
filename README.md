# Node Tools

A Docker image providing a Node.js environment with additional development tools.

## Features

- Node.js runtime (Alpine Linux base)
- pnpm package manager
- git for version control
- Minimal image size

### Running a Container

```bash
docker run -it aasanchez/node-tools:22.20.0-alpine
```

This will start an interactive shell in the container.

## Building Locally

To build the image locally:

```bash
cd docker
docker build --build-arg NODE_VERSION=22.20.0 -t node-tools .
```

## CI/CD

This project uses GitHub Actions for automated builds and security scanning:

- **Build Workflow**: Builds and pushes Docker images on push to master branch and weekly schedule
- **SAST Workflow**: Runs Dockerfile linting and vulnerability scanning with Trivy

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
