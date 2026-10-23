IA02 | Client Interview Evidence and Requirement Transformation
Memo
1. Personal Question Set (Excerpt)
Prepared 12 questions covering workflow, pain points, data, success criteria, security, and exception handling.
Example: "How are remote customer delivery fees currently calculated during busy service hours?"
2. Authentic Interview Evidence
Date & Time: March 14, 2026. Participant: Restaurant Owner (Sarah's Tasty Foods). Medium: In-person
observation and interview.
Raw Client Statement: "During peak afternoon rushes, customers calling in get frustrated because we
calculate delivery fees manually in our heads based on rough estimates, leading to miscalculated totals or
disputes when riders arrive. Also, kitchen staff lose paper order tickets."
3. Requirement Transformation
Functional Requirement: The system shall automatically compute remote delivery fees using a dynamic
distance-based formula and present itemized costs.
Non-Functional Requirement: Delivery calculation APIs must respond within < 1.5 seconds.
User Story (US-01): As a remote customer, I want my delivery fee calculated automatically based on my
distance, so that I receive an accurate order total before confirming payment.
Acceptance Criteria: Given items worth GHS 50.00, when delivery and 4km distance are selected, display
GHS 24.00 delivery fee and GHS 74.00 total.
API & Data Implication: Requires POST /api/delivery/calculate and decimal fields in `orders` table.
Test Idea: Unit test verifying pickup returns 0.00 and delivery calculates correctly.
4. Reflection (Summary)
The interview revealed that manual delivery fee calculations caused direct customer friction. Transforming
qualitative feedback into precise functional requirements and Given-When-Then scenarios taught me the
importance of automating business logic to eliminate operational errors.
AI Disclosure: AI was used as a structural assistant; all transformation reasoning and reflection are my own.
