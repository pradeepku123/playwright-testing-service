# To Configure playwright.service.config.ts file.

# Learn More about Playwright Testing Service
- https://learn.microsoft.com/en-gb/azure/playwright-testing/


# Configure PLAYWRIGHT_SERVICE_URL & 

# BASH
 - export PLAYWRIGHT_SERVICE_ACCESS_TOKEN={}


# BASH
 - export PLAYWRIGHT_SERVICE_URL=wss://eastasia.api.playwright.microsoft.com/api/authorize/connectSession
# Powershell
- $env:PLAYWRIGHT_SERVICE_URL="wss://eastasia.api.playwright.microsoft.com/api/authorize/connectSession"


Execute PW
- npx playwright test --config=playwright.service.config.ts --workers=20


# Sharding & Report Generation


- configure playwright.config.ts file
  -  /* Reporter to use. See https://playwright.dev/docs/test-reporters */
  -  reporter: "blob",
  - Will Generate /blob-report

npx playwright test --shard=1/3
npx playwright test --shard=2/3
npx playwright test --shard=3/3


npx playwright merge-reports /blob-report --reporter html ./all-blob-reports
