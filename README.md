## nodebff95

Backend for Frontend (BFF) project with ExpressJS on NodeJS

[![](https://img.shields.io/badge/bluemix-powered-blue.svg)](https://bluemix.net)
[![Platform](https://img.shields.io/badge/platform-NODE-lightgrey.svg?style=flat)](https://developer.apple.com/swift/)
[![Create Toolchain](https://console.ng.bluemix.net/devops/graphics/create_toolchain_button.png)](https://console.ng.bluemix.net/devops/setup/deploy/)

### Table of Contents
* [Summary](#summary)
* [Requirements](#requirements)
* [Configuration](#configuration)
* [Run](#run)

### Summary

A Backend for Frontend (BFF) is a pattern that allows your frontend to talk to your backend....

### Requirements
#### Local Development Tools Setup (optional)


- Install the latest [NodeJS](https://nodejs.org/en/download/) 6+ LTS version.

#### Bluemix development tools setup (optional)

1. Install [Docker](http://docker.io) on your machine.
2. Install the [Bluemix CLI](https://console.ng.bluemix.net/docs/cli/index.html)
3. Download the [Bluemix developer tools plugin](https://plugins.stage1.ng.bluemix.net/ui/repository.html#bluemix-plugins)
4. Go to the directory you downloaded the image to, and install the plugin with:

  `bx plugin install <name-of-the-dev-plugin>`


### Configuration

Your application configuration information is stored in `config.json`:

```json
{
  "vcap": {
    "services": {}
  }
}
```

If you selected services added to your project, you will see Cloudant, Object Storage, and other services with their connection information such as username, password, and hostname listed here. This is useful for connecting to remote services while running your application locally.

When you push your application to Bluemix, however, these values are no longer used, and instead Bluemix automatically connects to those bound services through the use of environment variables.

### Run
#### Using Bluemix development CLI
The Bluemix development plugin makes it easy to compile and run your application if you do not have all of the tools installed on your computer yet. Your application will be compiled with Docker containers. To compile and run your app, run:

```bash
bx dev run
```

Your application will be running at `http://localhost:8080/`.

#### Using a local development environment


Visit `http://localhost:8080/` in your browser.