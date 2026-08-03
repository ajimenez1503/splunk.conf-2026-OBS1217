# Configure the Alerting Integrations for ITSI and ThousandEyes

In this step you'll set up the two-way alert loop: ThousandEyes alerts flow into ITSI as episodes, and ITSI episodes appear on the ThousandEyes timeline with a link back to Splunk. This enables Network and X-Ops teams to see the same incident from their preferred perspective.

## Install the ITSI Monitoring and Alerting Content Pack

This content pack provides the event-management framework the alerting integration builds on, so we'll install it first.

To install it, follow these steps:

- In Splunk ITSI, go to `Configuration` -> `Data Integrations` -> `Content Library`
- Select the `ITSI Monitoring and Alerting` content pack
- Review what's included, then click `Proceed`
- Make sure you install all objects
    - Take note of the aggregation policies imported by this content pack
- Click `Import as enabled`
- Optionally, add a prefix to help with the filtering, for example: `<your-unique-id>-obs1217-`
- Optionally backfill your environment with the previous seven days of KPI data
- Click `Install selected`, then `Install` in the confirmation dialog

## Send ThousandEyes Alerts to ITSI

To forward ThousandEyes alerts into ITSI, follow these steps:

- In ThousandEyes, create a custom webhook for sending alerts to Splunk ITSI
- In Splunk ITSI, go to `Configuration` -> `Data Integrations`
- Under `Alerts`, click `Cisco ThousandEyes`
- In the connections table, click the `⋮` (more actions) menu for `thousandeyes_default`, then click `Activate`
- The connection status should update to `Active`

## Send ITSI Episodes to ThousandEyes

The ITSI Monitoring and Alerting content pack ships several aggregation policies named `Episodes by ...` (for example, `Episodes by ITSI Service`).

To surface ITSI episodes back in ThousandEyes, follow these steps:

- Go to `Configuration` -> `Event Management` -> `Notable Event Aggregation Policies`
- For each aggregation policy from the content pack:
    - Open the `Action Rules` tab and click `+ Add Rule`
    - Under `If`, select `The number of events in this episode is` -> `Greater than or equal to` -> `1`
    - Under `Then`, select `Send to ThousandEyes` and `Repeat every event while episode is active`
    - Click `Configure` and enter the URL of your Splunk instance
    - Find the closing-episode rule: `If the episode is broken, then change status to Closed for the episode ...`, and edit it to add an extra action:
        - Select the rule and click `+Add`
        - Under `And`, select `Send to ThousandEyes`
        - Click `Configure` and enter the same URL
- Click `Done`, then `Save`

## Visualize ITSI Episodes in ThousandEyes

To confirm episodes are flowing back into ThousandEyes, follow these steps:

- Open a ThousandEyes test impacted by an ITSI episode
- In the test timeline, ITSI episodes appear as swimlane annotations below the primary metric
- Hover over an annotation to see the number of episodes and total notable events at that point in time
- Click the `Splunk ITSI` tab to view episode details
- Click the `ITSI URL` to jump back to the episode in Splunk
