# Shared Tools

The shared development tools and environments available to all software developers working in the organization.

## Source and Version Control

We use [git][git] for version control.

We use [GitHub][github] as a repository store for all services, to track issues, and to coordinate development.

## Service Generator

All services adhere to a specified file structure template.

We use custom Yeoman generators to build new services according to our specified templates.

## Default Disk Image

We maintain a Docker image with a standard environment setup. Using the [Docker Toolbox][docker-toolbox] learners and partners can run this containerized environment on their local machine.

We also use this image as the default for our remote pairing service.

## Remote Pairing

An early proof-of-concept for our remote pairing tool exists. It is based on [Floobits][floobits] and is called [Cloud Collab][cloud-collab].

<!-- references -->

[docker-toolbox]:https://www.docker.com/docker-toolbox
[git]:https://git-scm.com/
[github]:https://github.com/
[cloud-collab]:[https://github.com/LearnersGuild/cloud-collab-docker]
