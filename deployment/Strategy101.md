## Rolling
Replace the running instance with the new one.
- technical difficulty : low

## Blue/Green
Create whole new environment and tests it. After test successfully, then change routing.
- technical difficulty : medium

## Canary
Provision both version in production but only route a few user to new feature to test if it's good. This required kind of smart routing to be part of deployment strategy.
- technical difficulty : high
