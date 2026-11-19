### Jeffrey Mailey

Forward deployed engineer in Dallas, and founder of [Jump Automations](https://jumpautomations.com). Most of a small business still runs on ordinary email. I build the systems that read it, file it to the right place and act on it, so only the decisions reach a person. Built with Claude, run on Claude.

Most of what I build runs inside client businesses or my own products, so those repositories are private. Three are rebuilt in public with fictional companies so the design can be read and run:

- [**inbox-agent**](https://github.com/jmailey23/inbox-agent): the engine behind Snailmail below. Rules decide first, Claude only sees borderline mail, anything unsure is flagged for a person, and nothing is ever deleted outright. 39 tests.
- [**ops-intake**](https://github.com/jmailey23/ops-intake): the Byrom Rose email pipeline below. Rules where a mistake is expensive, Claude where it is cheap to catch, row level security in Postgres, 25 tests.
- [**client-portal**](https://github.com/jmailey23/client-portal): the CPK Collective portal below. A live CRM behind a server function that never hands the browser its token, allowlisted fields, idempotent welcome emails, 32 tests.

**Snailmail** · iPhone email app with a sidekick, [on the App Store](https://apps.apple.com/app/id6825403744)

A native email client for Gmail, live on the App Store since November 15, 2026. The inbox is free; Gary, the sidekick, finds the junk and lines it up for you to swipe away for $2.99 a month. 720,000+ emails scanned since February. Rules settle most decisions, Claude only weighs in on borderline mail, and Gary flags rather than deletes: only senders you blocked are cleared on their own. Google verified its restricted Gmail access, and it passed an independent CASA Tier 2 security assessment. SwiftUI, FastAPI on Railway, Supabase, StoreKit.

**Byrom Rose Ops** · operations platform for a Dallas general contractor

Every inbound email for the business arrives from its Google Workspace inbox and runs through one pipeline: 1,435 messages since July. Notes from the team become tasks, and 97 percent of job related tasks file themselves to the right job by deterministic matching. Anything ambiguous waits for a person instead of guessing, and money, scope and client issues are flagged for the owner. Every new CompanyCam project becomes a job within seconds, pinned on the map (195 so far). Claude works where judgment is needed and a mistake is cheap to catch: reading meetings out of notes, turning site walkthrough recordings into recaps (Deepgram transcribes), and reading photos of checks and receipts into structured facts a person then approves. Job costing, weekly crew timesheets, a client portal and estimate PDFs. Supabase Postgres, Deno edge functions, row level security across eight roles. Empty project to production in under three weeks.

**CPK Collective** · client platform for a Dallas apartment locating brokerage

106 clients log in to a dashboard built around how the brokerage actually works: search status, tour schedule and properties report, pulled live from their HubSpot CRM through an authenticated edge function so the CRM token never reaches the browser. Freeform notes from the brokers are parsed into structured tour cards, and the dashboard changes shape from search to move in as the client's stage changes. Signup checks the email against the CRM first, a scheduled function emails each client the moment their search is ready (91 sent since June, replacing the HubSpot automation tier the brokerage paid about $800 a month for), and the brokers edit site content from a Google Sheet without a developer. Supabase with row level security, Deno edge functions, vanilla JavaScript.

**Jump billing** · invoicing and client payments

Stripe Checkout with signed webhooks, installment plans allocated in SQL so balances cannot drift, tokenized client pages, PDF invoices, reminders and weekly client recaps. Guarded by a pre deploy check that fails the build on leaked secrets and broken invariants.

**Stack**

TypeScript, Python, PostgreSQL, Supabase, Next.js, React, Swift, Deno, Stripe, Anthropic Claude API (tool calling, structured output), Claude Code, Gmail, Google Workspace, CompanyCam, HubSpot and Deepgram APIs.

[Case studies](https://jumpautomations.com/work) · [LinkedIn](https://linkedin.com/in/jeffreymailey) · jeffrey@jumpautomations.com
