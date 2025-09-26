ARG NODE_VERSION=latest
FROM node:${NODE_VERSION}
RUN apk update \
    && apk upgrade --no-cache \
    && apk add --no-cache git \
    && npm install -g npm@latest \
    && npm install -g pnpm
WORKDIR /app
CMD ["node"]