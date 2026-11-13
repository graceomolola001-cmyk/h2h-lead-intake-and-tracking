# Node-by-node workflow map

This map covers the **14-node** sanitized `H2H SRM | Path A | Lead Intake` n8n export.

| Node | Role |
| --- | --- |
| Form Submission | Watches the Google Sheets intake source |
| Collect data | Maps form fields to the intake contract |
| Clean data | Normalizes incoming values in JavaScript |
| Collect only fields we need to proceed | Selects required fields |
| Add lead data to Master tracker | Stores a normalized lead row |
| payment claimed to be made | Checks the prospect's payment claim |
| Check to verify payment | Looks up payment evidence from Sheets |
| Has not paid, warm lead | Routes unpaid prospects to tracking |
| Requests followup | Checks whether follow-up is needed |
| Update Tracker to Followup Active | Updates the follow-up state |
| Send a message / Send a message1 / Send a message2 | Gmail notifications |
| Update tracker to Future Sales Opportunities | Preserves the lead for future contact |

Names and branch behavior come from the original export; verify field mappings and branches before testing with synthetic records.

The broader Heart2Heart project includes the landing page, Google Ads, GA4/GTM, and Meta CAPI, which are documented in the [README](../README.md) but not fully exported here.
