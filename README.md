# Containers

Welcome! This repository contains a collection of Dockerfiles for different use cases, designed to simplify the deployment and management of various applications and environments using Docker.

## Table of Contents

- [Overview](#overview)
- [Dockerfiles](#dockerfiles)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview
The **Containers** project provides Dockerfiles for various live cases, helping set up containerized environments. This repository includes ready-to-use Dockerfiles tailored for different scenarios.

## Dockerfiles
Here is a list of Dockerfiles available in this repository. Each Dockerfile is located in its respective directory with a descriptive name for easy identification:
- [**CPPPO (C3PO)**](https://github.com/kormiltsev/containers/tree/main/c3po): A mock Rockwell Automation device. Responses on 44818 port with CIP.
- [**Goa gen**](https://github.com/kormiltsev/containers/tree/main/goagen): Autogenerate API handlers using Goagen without installing goagen and avoid version dependencies.
- [**Go Builder**](https://github.com/kormiltsev/containers/tree/main/gobuilder): Build go applications from sourse code without go installed.
- [**Go Runner**](https://github.com/kormiltsev/containers/tree/main/gorunner): Build go applications and run with alpine.

## Getting Started
To get started with this project, clone the repository:
```bash
git clone https://github.com/kormiltsev/containers.git
cd containers
```

## Usage

1. Build the Docker image:
```bash
docker build -t <image-name> <directory-name>/Dockerfile
```
2. Run the Docker container:
```bash
docker run -d --name <container-name> <image-name>
```
Each directory contains additional details on environment variables, volume mounts, and ports required for each specific use case. Refer to the README.md in each folder for further customization and usage instructions.

## Example
1. To generate API using goagen build an Image:
```bash
docker build -t goav3 goagen/Dockerfile
```
2. Generate code in the project:
```bash
cd /path/to/project/backend/api/design # location of design.go, see go gen documentation
docker run -v $PWD:/goa --rm goav3 goa gen github.com/kormiltsev/backend/api/design -o ./api
```

## Contributing
We welcome contributions! If you have Dockerfiles for other use cases or improvements to existing ones, feel free to submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](https://github.com/kormiltsev/containers/blob/main/LICENSE) file for more details.
