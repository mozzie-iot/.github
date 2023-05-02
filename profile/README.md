# [v0.1.0-beta](https://github.com/huebot-iot/hub-runner/releases/latest)

## Getting Started
1. Install the CLI:<br>
`bash <(wget -qO- http://huebot-cli.s3-website-us-east-1.amazonaws.com/install.sh)`
2. Install the Huebot environment:<br>
`sudo huebot install` (sudo is required to install apt-get packages and create directories)
3. Create an admin user:<br>
`huebot create-admin` (required to access API endpoints)

## Test API Endpoint
1. Login as admin
```
curl -X POST http://[computer name OR IP address]/user/login \
   -H "Content-Type: application/json" \
   -d '{"username": "my_username", "password": "my_password"}'
```
If successful, this will return session cookie<br>

2. Get current user
```
curl --cookie "sid=[cookie];" http://[computer name OR IP address]/user/me
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
