IA09 | Security, Privacy and Maintainability Review
1. Data Inventory & Access Matrix
Customer phone numbers and delivery addresses are encrypted in PostgreSQL. Admin passwords are
hashed via bcrypt.
Access Matrix: Customers can browse/order; Staff can manage POS/KDS/inventory; Owners have full
administrative override.
2. Abuse Risk & Resilience
Abuse Case: Unauthorized URL navigation to `/admin`. Prevented via RBAC middleware and JWT session
validation.
Maintainer Note: Environment secrets must be kept secure in hosting dashboards. Future improvement
includes automated WhatsApp/SMS low-stock alerts
