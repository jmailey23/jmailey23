### Jeffrey Mailey

Forward deployed engineer in Dallas. I embed in a company's operations, find the work done by hand every week, and ship the AI system that replaces it. Founder of [Jump Automations](https://jumpautomations.com).

Most of what I build runs inside client businesses, so the repositories are private. Here is what's in them.

**Byrom Rose Ops** · operations platform for a Dallas general contractor

An LLM agent reads every inbound email and JobTread update for the business (686 since July), pulls out the action items, and files 97 percent of job related ones to the right job with no human sorting. Owner level decisions are flagged rather than guessed. JobTread job costing, calendar invites to meetings, weekly crew timesheets, a client portal, voice notes and photos into the same pipeline. Supabase Postgres, 16 Deno edge functions, 72 row level security policies across eight roles. Empty project to production in under three weeks.

**Snailmail** · AI inbox agent, web and iOS

Paid SaaS. Claude classifies each message into structured JSON that drives the agent. Passed Google OAuth verification for restricted Gmail scopes and a CASA Tier 2 security assessment. FastAPI, Supabase, Stripe, SwiftUI.

**Jump billing** · invoicing and client payments

Stripe Checkout with signed webhooks, installment plans allocated in SQL so balances cannot drift, tokenized client pages, PDF invoices, reminders and weekly client recaps. Guarded by a pre deploy check that fails the build on leaked secrets and broken invariants.

**Client platforms and sites** · Next.js and Sanity

A HubSpot backed client dashboard for an apartment locating brokerage, and marketing sites on a reusable Next.js and Sanity starter.

**Stack**

TypeScript, Python, PostgreSQL, Supabase, Next.js, React, Swift, Deno, Stripe, Anthropic Claude API (tool calling, structured output), Gmail, HubSpot and JobTread APIs.

[Case studies](https://jumpautomations.com/work) · [LinkedIn](https://linkedin.com/in/jeffreymailey) · jeffrey@jumpautomations.com
