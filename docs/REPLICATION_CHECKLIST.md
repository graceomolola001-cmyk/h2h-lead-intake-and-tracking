# Reproducing the Heart2Heart lead and payment workflow

1. Import `workflows/17-h2h-srm-path-a-lead-intake.json` into a test n8n instance.
2. Configure a fictional lead form and Google Sheet with fields matching the workflow node mappings.
3. Create a synthetic master lead tracker and a separate independent payment-verification source.
4. Replace placeholder spreadsheet IDs and reconnect Google Sheets and Gmail OAuth.
5. Run test cases for an enquiry with no payment, claimed payment awaiting verification, and independently verified payment.
6. Inspect the master tracker, next-step states and Gmail test notifications.
7. Confirm that missing payment evidence does not mark a lead as paid.

## Separate measurement work

The landing page, Google Ads, GA4 / GTM tracking, and Meta conversion configurations are part of the larger Heart2Heart implementation. Their full source/configuration is not bundled here. Reproduce those separately with your own website and authorized advertising assets.

## Caution

Do not run tests using real payment accounts or customer data. These steps are a **checklist**, not a claim of completed external integration testing.
