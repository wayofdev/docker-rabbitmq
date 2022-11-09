<br>

<div align="center">
<img width="456" src="https://raw.githubusercontent.com/wayofdev/docker-rabbitmq/master/assets/logo.gh-light-mode-only.png#gh-light-mode-only">
<img width="456" src="https://raw.githubusercontent.com/wayofdev/docker-rabbitmq/master/assets/logo.gh-dark-mode-only.png#gh-dark-mode-only">
</div>

<br>

<br>

<div align="center">
<a href="https://actions-badge.atrox.dev/wayofdev/docker-rabbitmq/goto"><img alt="Build Status" src="https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Fwayofdev%2Fdocker-rabbitmq%2Fbadge&style=flat-square"/></a>
<a href="https://github.com/wayofdev/docker-rabbitmq/tags"><img src="https://img.shields.io/github/v/tag/wayofdev/docker-rabbitmq?sort=semver&style=flat-square" alt="Latest Version"></a>
<a href="https://hub.docker.com/repository/docker/wayofdev/postgres"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/wayofdev/postgres?style=flat-square"></a>
<a href="LICENSE.md"><img src="https://img.shields.io/github/license/wayofdev/docker-rabbitmq.svg?style=flat-square&color=blue" alt="Software License"/></a>
<a href="#"><img alt="Commits since latest release" src="https://img.shields.io/github/commits-since/wayofdev/docker-rabbitmq/latest?style=flat-square"></a>
</div>

<br>

# Docker Image: RabbitMQ

Repository has Dockerfile with pre-configured Alpine RabbitMQ with following plugins:

* rabbitmq-delayed-message-exchange
* rabbitmq-message-timestamp
* rabbitmq_amqp1_0
* rabbitmq_shovel

Optional (Enabled on management version of images):

* rabbitmq-shovel-management

<br>

If you **like/use** this repository, please consider **starring** it. Thanks!

<br>

## ⚙️ Development

To install dependencies and start development you can check contents of our `Makefile`

### →  Requirements

For testing purposes we use **goss** and **dgoss**, follow installation instructions on [their official README](https://github.com/aelsabbahy/goss/blob/master/extras/dgoss/README.md)

<br>

### → Building locally

Generating distributable Dockerfiles from yaml source code:

```bash
$ make generate
```

<br>

Building default image:

```bash
$ git clone git@github.com:wayofdev/docker-rabbitmq.git
$ make build
```

To **build** image, **test** it and then **clean** temporary files run:

```bash
$ make
```

Building all images:

```bash
$ make build TEMPLATE="alpine"
$ make build TEMPLATE="management-alpine"
```

<br>

## 🧪 Testing

Testing default image:

```bash
$ make test
```

To test all images:

```bash
$ make test TEMPLATE="alpine"
$ make test TEMPLATE="management-alpine"
```

<br>

### → Code quality tools

Run **yamllint** to validate all yaml files in project:

```bash
$ make lint
```

Run hadolint to validate created Dockerfiles:

```bash
$ make hadolint
```

<br>

## 🤝 License

[![Licence](https://img.shields.io/github/license/wayofdev/docker-postgres?style=for-the-badge&color=blue)](./LICENSE)

<br>

## 🙆🏼‍♂️ Author Information

This repository was created in **2022** by [lotyp / wayofdev](https://github.com/wayofdev).

<br>

## 🫡 Contributors

<img align="left" src="https://img.shields.io/github/contributors-anon/wayofdev/docker-postgres?style=for-the-badge"/>

<a href="https://github.com/wayofdev/docker-rabbitmq/graphs/contributors">
  <img src="https://opencollective.com/wod/contributors.svg?width=890&button=false">
</a>

<br>

