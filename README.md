# Development local stack

## Dependencies

* [Docker](https://docs.docker.com/install/)
* [Docker Compose](https://docs.docker.com/v17.09/compose/install/)

## Applications

* Postgres 12
* Redis 5.0.5
* Elasticsearch 7.3.1
* Kibana 7.3.1
* Localstack

## Usage

### Download images

```bash
docker-compose pull
```

### Run apps

```bash
docker-compose up -d # runs in background
```

### Stop apps

```bash
docker-compose stop
```

## Aliasing

By default, `docker-compose` will always lookup across the current directory to find a `docker-compose.yaml` and the most of the time you will be in your project directory.

To skip a lot of directories changes and speed up the development process you can use the [shell script aliases](https://www.gnu.org/software/bash/manual/html_node/Aliases.html) to make your life easer and create your own `dev-stack` CLI.

**Pro tip:** You can add this alias in your `.bashrc`, `.bash_profile`, `.zshrc`... to keep it up forever!

```bash
alias dev-stack='docker-compose -f /path/to/dev-stack/docker.compose.yaml'
```

### Download images

```bash
dev-stack pull
```

### Run apps

```bash
dev-stack up -d # runs in background
```

### Stop apps

```bash
dev-stack stop
```


## Authors

* **Júlio Corradi** - *Initial work* - [juliogc](https://github.com/juliogc)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details