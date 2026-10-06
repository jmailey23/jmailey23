### Jeffrey Mailey

Forward deployed engineer in Dallas. I embed in a company's operations, find the work done by hand every week, and ship the AI system that replaces it. Founder of [Jump Automations](https://jumpautomations.com).

Most of what I build runs inside client businesses, so the repositories are private. Here is what's in them.

**Byrom Rose Ops** · operations platform for a Dallas general contractor

Every inbound email and JobTread update for the business runs through one pipeline, 686 since July. Notes from the team become tasks, and 97 percent of job related tasks file themselves to the right job by deterministic matching. Anything ambiguous waits for a person instead of guessing, and money, scope and client issues are flagged for the owner. Claude works where judgment is needed and a mistake is cheap to catch: reading meetings out of notes, turning site visit recordings into recaps, and reading photos of checks and receipts into structured facts a person then approves. JobTread job costing, weekly crew timesheets, a client portal and estimate PDFs. Supabase Postgres, 16 Deno edge functions, 72 row level security policies across eight roles. Empty project to production in under three weeks.

**CPK Collective** · client platform for a Dallas apartment locating brokerage

106 clients log in to a dashboard built around how the brokerage actually works: search status, tour schedule and properties report, pulled live from their HubSpot CRM through an authenticated edge function so the CRM token never reaches the browser. Freeform notes from the brokers are parsed into structured tour cards, and the dashboard changes shape from search to move in as the client's stage changes. Signup is limited to verified clients, every new account gets a welcome email, and the brokers edit site content from a Google Sheet without a developer. Supabase with row level security, Deno edge functions, vanilla JavaScript.

**Snailmail** · AI inbox agent, web and iOS

Paid SaaS. Claude classifies each message into structured JSON that drives the agent. Passed Google OAuth verification for restricted Gmail scopes and a CASA Tier 2 security assessment. FastAPI, Supabase, Stripe, SwiftUI.

**Jump billing** · invoicing and client payments

Stripe Checkout with signed webhooks, installment plans allocated in SQL so balances cannot drift, tokenized client pages, PDF invoices, reminders and weekly client recaps. Guarded by a pre deploy check that fails the build on leaked secrets and broken invariants.

**Stack**

TypeScript, Python, PostgreSQL, Supabase, Next.js, React, Swift, Deno, Stripe, Anthropic Claude API (tool calling, structured output), Gmail, HubSpot and JobTread APIs.

[Case studies](https://jumpautomations.com/work) · [LinkedIn](https://linkedin.com/in/jeffreymailey) · jeffrey@jumpautomations.com
