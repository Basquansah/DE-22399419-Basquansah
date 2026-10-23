IA06 | Data Model, Query and State Walkthrough
1. Entities & Relationships
Core PostgreSQL tables: `users`, `orders`, `order_items`, `menu_items`, and `ingredients`. Enforces strict
foreign keys, atomic transactions, and enum validation (`user_role`, `order_status`, `fulfillment_type`).
[Original Identity-Bearing ERD Sketch Attached in Sakai]
Drawn by Benedicta Akyere Sika Quansah. 
2. Query Walkthrough & Privacy
State Change: Transitioning order status from PENDING to PREPARING triggers atomic inventory decrements
across respective raw ingredients.
Privacy: Customer PII restricted to authorized staff/owner; synthetic sample records used exclusively in
testing.
