![version](https://img.shields.io/github/package-json/v/huebot-iot/hub-runner)
![core-deploy](https://github.com/huebot-iot/hub-core/actions/workflows/deploy.yml/badge.svg)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Description
Huebot is an IoT framework that allows clients to be controlled or sensed via HTTP endpoint. 
<br><br>
While Huebot makes use of a number of libraries, core functionality is made possible by [Mosquitto](https://github.com/eclipse/mosquitto), [NGINX](https://github.com/nginx), [NestJS](https://github.com/nestjs/nest) and [MicroPython](https://github.com/micropython/micropython)

## Getting Started
1. Install the CLI:<br>
`bash <(wget -qO- http://huebot-cli.s3-website-us-east-1.amazonaws.com/install.sh)`
2. Install the Huebot environment:<br>
`sudo huebot install` (sudo is required to install apt-get packages and create directories)
3. Create an admin user:<br>
`huebot create-admin` (required to access API endpoints)

## Test API Endpoint
1. Login
```
curl -X POST http://[computer name OR IP address]/user/login \
   -H "Content-Type: application/json" \
   -d '{"username": "my_username", "password": "my_password"}'
```
If successful, this will return an access token and refresh token<br>

2. Get current user
```
curl http://[computer name OR IP address]/user/me \
   -H "Content-Type: application/json" \
   -H "Authorization: Bearer [access token]" 
```
## CLI commands
- `install`<br>
Install and run environment
- `uninstall`<br>
Uninstall environment
- `hub-version`<br>
Get currently installed environment version
- `create-admin`<br>
Create admin user (required to get started with http endpoints)
