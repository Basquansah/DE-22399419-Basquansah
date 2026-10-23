IA05 | API Contract and Failure-Response Walkthrough
1. Contract Specification (`POST /api/orders`)
Purpose: Enables remote customers to submit food orders with dynamic delivery calculations.
Caller: Frontend Client | Provider: Next.js API Route (`/api/orders`).
{
 "customer_id": "a0eebc99-9c0b-4ef8-bb6d-6bb9bd380a11",
 "fulfillment": "DELIVERY",
 "distance_km": 4.50,
 "food_subtotal": 50.00,
 "payment_method": "MOMO",
 "items": [{"menu_item_id": "b1ffbc88-8b0a-3ef7-aa5c-5aa8ac270f00", "quantity": 1, 
"unit_price": 50.00}]
}
2. Validation, Errors & Tests
Validation Rules: Fulfillment must be PICKUP/DELIVERY; distance required if delivery; items must be in
stock.
Error Model: Invalid input returns HTTP 400 (`ERR_INVALID_PAYLOAD`); Stock out returns HTTP 409
(`ERR_STOCK_OUT_OF_STOCK`); DB timeout returns HTTP 500.
Test Plan: 6 test cases covering valid requests, missing fields, unauthorized callers, duplicates, dependency
failures, and response shape verification.
