# Local Codespaces

This repository contains all Docker configurations to set-up GitHub Codespaces-like environment on my local machine.

- **Author:** Apache X692 Attack Helicopter
- **Created on:** 04/07/2024

## Special Thanks

Special thanks to [LinuxServer](https://github.com/linuxserver) for providing the base image pre-built making my life easier.

## Set-up

To set-up the workspace, first copy the example secrets file to a `.env` file with the following command:

```bash
cd "./<path>"
cp ./env.example ./.env
```

Fill-out the secrets in the `.env` file and build the image as follows. Note that this step is optional if you've already built the image.

```bash
docker build --tag codeserver-<stack> --file ./codeserver-<stack>/Dockerfile ./
```

The `<stack>` placeholder must be replaced with the `DOCKER_STACK` environment variable value and must match the stack mentioned in the specified folder. Now, run the `docker-compose-yaml` file as follows:

```bash
docker compose up -d
```

Once you open the web interface, to install extensions, you can either use the "Extensions" sidebar or use the `install-extensions` command that comes with this image.
