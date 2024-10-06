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

```sh

npm adduser --registry http://localhost:4873

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
