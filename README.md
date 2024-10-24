# Private NPM registry setup

### Docker setup

- Start

```sh

docker compose up -d

```

- Stop

```sh

docker compose down --remove-orphans

```

- Stop and delete all data

```sh

docker compose down --remove-orphans --volumes

```

### Using the registry

- Login to the registry

Verdaccio (the registry) is configured to allow anonymous publishing but npm (the package manager) still requires an auth token in order to publish a package. https://github.com/npm/cli/blob/latest/lib/commands/publish.js#L149

```sh

echo "//localhost:4873/:_authToken=fake-token" >> ~/.npmrc

```

- Publish a package

```sh

npm publish --registry http://localhost:4873

```

- Unpublish a package

```sh

npm unpublish --force --registry http://localhost:4873

```

- Install a package

```sh

npm install <packagename> --registry http://localhost:4873

```
