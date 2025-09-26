ARG NODE_VERSION=latest
FROM node:${NODE_VERSION}
SHELL ["/bin/sh", "-eo", "pipefail", "-c"]

RUN apk update \
    && apk upgrade --no-cache \
    && GIT_VERSION="$(apk policy git | sed -n '1s/^git-//;1s/:$//p')" \
    && apk add --no-cache "git=${GIT_VERSION}" \
    && npm install -g "npm@$(npm view npm version)" \
    && npm install -g "pnpm@$(npm view pnpm version)"

WORKDIR /app
CMD ["node"]