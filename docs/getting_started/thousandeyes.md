# ThousandEyes

## Log In to ThousandEyes

Use the workshop account to access ThousandEyes:

- Go to the [ThousandEyes Log In page](https://app.thousandeyes.com/login).
- Enter the following credentials:
    - **Email**: `xxx`
    - **Password**: `xxx`

## Create a ThousandEyes Page Load Test

For ThousandEyes to be able to stream data to Splunk, first it needs to be collected by ThousandEyes. To achieve this, we need to create a ThousandEyes test.

For this exercise, we are going to create a `Page Load` test that checks the availability and performance of `www.cisco.com` page.
To learn more about Page Load tests, check the [Page Load Test documentation](https://docs.thousandeyes.com/product-documentation/tests/web-layer-tests#page-load-test)

### Create a Test

- Click on `Network & App Synthetics` in the left navigation bar
- Select `Test Settings`
- Click the `Add New Test`
- Select `Page Load` from the test type options

![create Page Load Test](../img/thousandeyes/te_create_page_load_test.png)

### Configure Test

For this workshop, we will need only the Basic section:

- **URL**: Enter `https://www.cisco.com/`
- **Frequency**: Leave it at 1 minute
- **Test location**: Click `Select Agents` and select 1 or 2 _Cloud Agents_ (e.g., Denver and Edinburgh)
- **Alerts**: All enabled
- **Test Name**: Enter a unique descriptive name that includes your participant number or your initials
- Click `Deploy`

![config Page Load Test](../img/thousandeyes/te_config_page_load_test.png)
