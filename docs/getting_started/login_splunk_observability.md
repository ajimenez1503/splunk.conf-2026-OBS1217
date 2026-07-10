# Log In to Splunk Observability Cloud

This guide will help you log into Splunk Observability Cloud and obtain an access token for the ThousandEyes stream.

Use the workshop account to access Splunk Observability Cloud:

- Go to [Splunk Observability Cloud](https://app.us1.observability.splunkcloud.com/#/home).
- Enter the following credentials:
    - **Email**: `antonjim+conf@cisco.com`
    - **Password**: `Antonjim+conf@cisco.com1`
- Click `Sign In`

## Generate Access Token

Once you're logged into Splunk Observability Cloud, generate your access token:

- Navigate to the `Settings` -> `Access Tokens`
- Click `Create Token`
- Configure the token settings:
    - `Name`: Enter a descriptive name that includes your seat number (e.g., "ThousandEyes Integration Token - Seat 12") to avoid collisions with other participants
    - `Scope`: Select `INGEST` and `API` 
        - Check `Please accept to continue with your selection.`
- Click `Next` to proceed the `Permissions` section
- Keep the default permissions settings
- Click `Next` to proceed the `Expiration` section
- Keep the default `Expiration` settings
- Click `Create Token`
- Copy the token

![access token](../img/splunk_observability/access_token.png)
