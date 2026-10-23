IA10 | Final Individual System Defence and Contribution Evidence
1. Personal Contribution Summary
Student Name: Benedicta Akyere Sika Quansah (ID: 22399419)
Contribution: Design and implementation of the Customer Remote Ordering Portal, Shopping Cart State
Management, and Dynamic Delivery Fee Calculation Engine (US-01 / US-03).
GitHub Evidence: PR #04 (Delivery Calculation & Cart Engine), branch `ia1-Basquansah-remote-ordering`,
source files `components/cart/CartDrawer.tsx` and `utils/deliveryCalculator.ts`.
2. System Impact & Honest Limitation
Impact: Automates delivery pricing, eliminating manual errors during rush hours and providing transparent
billing.
Limitation: Relies on manual customer distance input rather than live GPS coordinate mapping.
Future Improvement: Integrate postcode-based zone mapping for automated distance detection.
D10 Individual Cross-Reference: Role: Frontend & Cart State Developer. Defendable artifacts: `utils/
deliveryCalculator.ts`, `__tests__/deliveryCalculator.test.ts`, requirement US-01, and ADR-01.
