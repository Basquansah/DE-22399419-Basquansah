IA01 | Personal System Request-Flow Diagram & Explanation
1. Feature & Path Overview
Feature explored: Remote Customer Order Placement with Dynamic Delivery Fee Calculation (US-01). The
complete request flow travels from the customer's mobile browser, across Vercel edge routing via HTTPS, into
Next.js App Router API backend logic executing delivery calculation algorithms, and persisting data atomically
into Supabase PostgreSQL.
[Original Identity-Bearing Handwritten Sketch Attached in Sakai Submission]
Contains: User device, mobile browser, domain routing, DNS, HTTPS POST request, Next.js API server,
calculateOrderPricing logic, Supabase PostgreSQL database, JSON response, failure point (database timeout), and
security concern (PII encryption). Drawn by Benedicta Akyere Sika Quansah (ID: 22399419). 
2. Typed Explanation (12-Question Summary)
(1) User Device: Customer mobile smartphone or tablet running Android/iOS.
(2) Browser: Chrome/Safari mobile browser executing React 18 client scripts.
(3) URL / Route: https://sarahstastyfoods.vercel.app/checkout dispatching to /api/orders.
(4) Protocol: HTTPS over TLS 1.3 encryption.
(5) Data Sent: JSON payload containing customer name, phone number, fulfillment type ("DELIVERY"),
distance in kilometers (4.0 km), item array, and payment mode ("MOMO").
(6) Request Validation: Next.js API validates input types, non-empty phone numbers, and positive numeric
values.
(7) Database: Supabase PostgreSQL relational database tables (`orders`, `order_items`, `users`).
(8) Returned Response: HTTP 201 Created JSON response with generated order ID, order number, delivery
fee, and total amount.
(9) Validation Failure: Missing mandatory fields trigger an HTTP 400 Bad Request error response.
(10) Database Outage: Caught database exceptions return HTTP 500 while frontend displays a friendly retry
message.
(11) 500 Concurrent Users: Handled via Vercel edge function scaling and Supabase connection pooling.
(12) Security / Privacy: Customer PII (phone number/address) is protected via HTTPS transmission
encryption and strict data minimization.
Oral Explanation Video (2-3 Minutes):
Unlisted YouTube Video Link: https://youtu.be/placeholder-ia01-benedicta
Explains name, student ID (22399419), project, request flow, failure point, security concern, and personal learning
reflection. No slides used.
AI Disclosure: I used AI assistance to format and structure this explanation based on team deliverables. All
technical details were verified by me.
