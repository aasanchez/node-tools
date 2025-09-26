ARG NODE_VERSION=latest
FROM node:${NODE_VERSION}

# Install Git (usually included, but ensure)
RUN apt-get update && apt-get install -y --no-install-recommends git && rm -rf /var/lib/apt/lists/*

# Install PNPM globally
RUN npm install -g pnpm

# Set working directory
WORKDIR /app

# Default command
CMD ["node"]