IA04 | Architecture Decision Record and Failure Walkthrough
1. ADR-01: Responsive Web Application vs. Native Mobile Apps
Status: Accepted | Context: Serving customers, kitchen staff, and owner simultaneously without app store
deployment friction.
Decision: Build a unified Responsive Web Application using Next.js and Tailwind CSS instead of native
mobile apps.
Evaluation
Criteria Weight
Alternative A: Responsive Web App
(Chosen) Alternative B: Native Mobile Apps
Client & Data Fit High
Excellent across mobile, tablet, and
desktop
Requires separate web wrappers for
owner
Maintainability High Single repository, unified CI pipeline High maintenance overhead for student
team
Deployment &
Cost Medium Zero cost, instant Vercel deployment
App store fees and manual review
delays
[Original Identity-Bearing Personal Architecture Sketch Attached in Sakai]
Shows client tier (mobile/tablet/desktop), Vercel routing, Next.js API, and Supabase PostgreSQL. Drawn by
Benedicta Akyere Sika Quansah . 
2. Failure Walkthrough & Verification
Failure Scenario: Database connection timeout during peak lunch rush.
Detection & User Impact: API catches timeout; React error boundary displays a friendly retry message
without crashing.
Verification: Tested via mock timeout unit tests and GitHub Actions CI pipelines (`make test`).
