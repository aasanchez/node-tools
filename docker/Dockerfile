ARG NODE_VERSION=latest
FROM node:${NODE_VERSION}
RUN apk add --no-cache git
RUN npm install -g pnpm
WORKDIR /app
CMD ["node"]