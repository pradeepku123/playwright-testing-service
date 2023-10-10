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