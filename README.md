# Aptabase Self-Hosting Guide

This guide will help you get started with self hosting Aptabase. 
You can alternatively use our [Cloud Hosting](https://aptabase.com) for a zero maintenance and fully managed solution.

## Prerequisites

All you need is to have a recent version of [Docker](https://docs.docker.com/get-docker/) as this guide uses Docker Compose.

## How-to

1. Clone this repository

```sh
git clone https://github.com/aptabase/self-hosting
```

2. Modify the `docker-compose.yml` file to your liking, but especially the sections with comments as the default values are just dummy examples.

3. Run the following command to start the services:

```sh
docker-compose up -d
```

4. That's it! You can now access Aptabase at `http://localhost:8000` 🎉

**Note:** By default, Aptabase is not configured to send email via SMTP . You can either see the emails in the logs or add the relevant SMTP variables in the `docker-compose.yml` file. A list of all Environment Variables is available [here](https://github.com/aptabase/aptabase/blob/main/src/Features/EnvSettings.cs).

> If that's not working, please check the logs with `docker-compose logs -f` and make sure there are no errors.

## First Login / Account

There is no default login. Once you are able to access your self-hosted instance, you need to create/register a new account. After registering, the activation link that is required to activate it will be in the container logs. Once you follow that link, your new account will be active, and you will be able to access Aptabase in its entirity.
