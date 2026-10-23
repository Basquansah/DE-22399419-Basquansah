IA07 | Test Evidence, PR Review and CI Walkthrough
1. Test Cases (Summary)
Test ID Category Scenario Expected Result Result
TST-01 Normal Case Pickup order calculation Delivery Fee = 0.00 PASSED
TST-02 Normal Case Home delivery (4km) Fee = 24.00, Total = 74.00 PASSED
TST-03 Invalid Input Negative subtotal Validation error thrown PASSED
TST-04 Security Unauthenticated /admin access Blocked by RBAC middleware PASSED
TST-05 Failure Simulated DB outage HTTP 500 with user error PASSED
TST-06 Regression Full suite run via `make test` All unit tests pass PASSED
PR Review & CI: PR #04 reviewed for requirement fit, validation, tests, and security. GitHub Actions CI runs
make setup, make lint, make test, and make build successfully
