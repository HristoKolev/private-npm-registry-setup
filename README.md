# Private NPM registry setup

### Docker setup

- How to start

```sh

docker compose up -d

```

- How to stop

```sh

docker compose down --remove-orphans

```

- How to reset everything completely

```sh

docker compose down --remove-orphans --volumes

```

### Using the registry

- Login into the registry

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
