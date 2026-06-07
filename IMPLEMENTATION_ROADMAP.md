# InvestWise Implementation Roadmap & Task Breakdown

**Project:** InvestWise (Real Estate Investment Platform)  
**Duration:** 12 months (5 phases)  
**Team Size:** 8-10 engineers (scalable)  
**Current Date:** June 7, 2026  
**Status:** Ready for Sprint Planning

---

## Executive Summary

This document maps the InvestWise PRD (4,200+ words, 17 sections) into phased, actionable engineering tasks with effort estimates, technical requirements, and success criteria.

### Key Metrics
- **Total Story Points:** ~650 SP (8 engineers × 12 weeks = ~600 SP capacity)
- **Phase 1 (Months 0-2):** Foundation MVP - 120 SP
- **Phase 2 (Months 2-4):** AI Intelligence - 140 SP
- **Phase 3 (Months 4-6):** Portfolio Management - 150 SP
- **Phase 4 (Months 6-9):** Advanced Optimization - 180 SP
- **Phase 5 (Months 9-12):** Community & Scale - 180 SP

---

## Phase 1: Foundation (Months 0-2) — **120 Story Points**

**Goal:** Build MVP with property search, basic analysis, and portfolio tracking  
**Team:** 3-4 engineers (full-time)  
**Deliverables:** Property discovery, basic cash flow calculator, user authentication, portfolio dashboard  

### 1.1 Infrastructure & Backend Setup

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.1.1** Setup AWS/cloud infrastructure (ECS, RDS, S3) | 13 SP | P0 | DevOps | None |
| **1.1.2** PostgreSQL schema design (properties, users, portfolios, analyses) | 8 SP | P0 | Backend Lead | 1.1.1 |
| **1.1.3** Redis setup (cache, sessions, rate limiting) | 5 SP | P1 | DevOps | 1.1.1 |
| **1.1.4** Authentication service (OAuth2, JWT, user profiles) | 13 SP | P0 | Backend | 1.1.2 |
| **1.1.5** API gateway & request routing | 8 SP | P0 | Backend | 1.1.4 |
| **1.1.6** Logging & monitoring (CloudWatch, Datadog) | 5 SP | P1 | DevOps | 1.1.1 |

**Subtotal: 52 SP**

---

### 1.2 Data Integration & Sources

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.2.1** MLS data integration (API connection, schema mapping) | 21 SP | P0 | Backend | 1.1.2 |
| **1.2.2** Property data pipeline (daily ingestion, dedupe, validation) | 13 SP | P0 | Data Eng | 1.2.1 |
| **1.2.3** Comparable sales data (county assessor integration) | 13 SP | P1 | Data Eng | 1.1.2 |
| **1.2.4** Mortgage rates feed (daily updates, historical tracking) | 5 SP | P1 | Backend | 1.1.5 |
| **1.2.5** Data quality & freshness monitoring | 5 SP | P1 | Data Eng | 1.2.2 |

**Subtotal: 57 SP**

---

### 1.3 Property Search & Discovery

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.3.1** Property search API (location, price, type, bedrooms) | 13 SP | P0 | Backend | 1.1.5, 1.2.2 |
| **1.3.2** Search index optimization (Elasticsearch or PostgreSQL FTS) | 8 SP | P1 | Backend | 1.3.1 |
| **1.3.3** Property autocomplete (as-user-types suggestions) | 5 SP | P1 | Backend | 1.3.1 |
| **1.3.4** Property detail page API (full enrichment) | 8 SP | P0 | Backend | 1.3.1 |
| **1.3.5** Search frontend (React component, responsive) | 13 SP | P0 | Frontend | 1.3.1 |
| **1.3.6** Property detail frontend (rich UI, image carousel) | 13 SP | P0 | Frontend | 1.3.4 |
| **1.3.7** Saved/favorites feature (backend + frontend) | 5 SP | P2 | Full-stack | 1.1.4, 1.3.5 |

**Subtotal: 65 SP**

---

### 1.4 Basic Cash Flow Calculator

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.4.1** Cash flow calculation engine (Python) | 21 SP | P0 | Backend | 1.1.2 |
| **1.4.2** Expense estimation models (tax, insurance, maintenance) | 13 SP | P0 | Backend/Analytics | 1.4.1 |
| **1.4.3** Cap rate & cash-on-cash calculations | 5 SP | P0 | Backend | 1.4.1 |
| **1.4.4** Cash flow API endpoint (takes property + inputs) | 8 SP | P0 | Backend | 1.4.1 |
| **1.4.5** Cash flow frontend (React calculator, interactive inputs) | 13 SP | P0 | Frontend | 1.4.4 |
| **1.4.6** Results visualization (metrics cards, summary table) | 8 SP | P0 | Frontend | 1.4.5 |
| **1.4.7** Cash flow export to PDF | 5 SP | P2 | Backend | 1.4.4 |

**Subtotal: 73 SP**

---

### 1.5 User Authentication & Profiles

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.5.1** User registration (email, password, basic profile) | 8 SP | P0 | Backend | 1.1.4 |
| **1.5.2** Email verification workflow | 5 SP | P0 | Backend | 1.5.1 |
| **1.5.3** Login/logout (session management) | 5 SP | P0 | Backend | 1.1.4 |
| **1.5.4** Password reset flow | 5 SP | P1 | Backend | 1.5.1 |
| **1.5.5** User profile page (edit name, email, preferences) | 8 SP | P1 | Frontend | 1.5.1 |
| **1.5.6** Persona detection (first-time buyer, investor, flipper) | 5 SP | P2 | Backend | 1.5.1 |

**Subtotal: 36 SP**

---

### 1.6 Portfolio Tracking (Basic)

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.6.1** Portfolio database schema (properties, ownership) | 8 SP | P0 | Backend | 1.1.2 |
| **1.6.2** Add property to portfolio API | 5 SP | P0 | Backend | 1.6.1, 1.3.4 |
| **1.6.3** Portfolio dashboard API (list properties, basic metrics) | 13 SP | P0 | Backend | 1.6.2 |
| **1.6.4** Portfolio dashboard frontend (property list, KPI cards) | 13 SP | P0 | Frontend | 1.6.3 |
| **1.6.5** Portfolio summary metrics (total equity, cash flow) | 5 SP | P0 | Backend | 1.6.3 |
| **1.6.6** Remove property from portfolio | 3 SP | P1 | Backend | 1.6.2 |

**Subtotal: 47 SP**

---

### 1.7 Frontend App Shell & Navigation

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **1.7.1** React app setup (Create React App, routing, state mgmt) | 13 SP | P0 | Frontend Lead | None |
| **1.7.2** Sidebar navigation (responsive, collapsible) | 8 SP | P0 | Frontend | 1.7.1 |
| **1.7.3** Top bar (search, user profile, settings) | 8 SP | P0 | Frontend | 1.7.1 |
| **1.7.4** Page routing (home, search, property detail, portfolio) | 8 SP | P0 | Frontend | 1.7.1 |
| **1.7.5** Design system CSS (colors, typography, spacing) | 13 SP | P0 | Frontend | None |
| **1.7.6** Component library (buttons, cards, inputs, tables) | 21 SP | P0 | Frontend | 1.7.5 |
| **1.7.7** Responsive design (mobile, tablet, desktop) | 13 SP | P1 | Frontend | 1.7.6 |

**Subtotal: 84 SP**

---

### Phase 1 Summary

**Total: 414 SP** (Exceeds estimate — will prioritize)

**Critical Path (P0 only):** ~280 SP (1.5-2 months for 3-4 engineers)

**Phase 1 MVP Scope (Reduced for 12 weeks):**
- Infrastructure & auth (1.1, 1.5)
- MLS data integration (1.2.1, 1.2.2)
- Property search & discovery (1.3)
- Basic cash flow calculator (1.4)
- Portfolio tracking (1.6)
- Frontend app shell (1.7)

**Deprioritized to Phase 2:**
- Advanced data sources (1.2.3, 1.2.4)
- Search optimization (1.3.2)
- PDF export (1.4.7)
- Email verification (1.5.2)
- Persona detection (1.5.6)

**By End of Phase 1:**
- 500+ beta users
- 1K properties analyzed
- >80% test accuracy
- MVP core features operational

---

## Phase 2: AI Intelligence (Months 2-4) — **140 Story Points**

**Goal:** Add AI advisor, investment scoring, forecasting, alerts  
**Team:** 4-5 engineers  
**Deliverables:** AI advisor, investment score v2, scenario simulation, market intelligence, alerts

### 2.1 AI/LLM Integration

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.1.1** LLM API integration (OpenAI/Anthropic) | 13 SP | P0 | Backend | 1.1.5 |
| **2.1.2** Prompt engineering for investment advisor | 13 SP | P0 | AI/ML | 2.1.1 |
| **2.1.3** Context injection (portfolio data, market data to LLM) | 8 SP | P0 | Backend | 2.1.1, 1.6.3 |
| **2.1.4** Conversation history & memory (multi-turn) | 8 SP | P1 | Backend | 2.1.3 |
| **2.1.5** Response streaming (show answer as it generates) | 5 SP | P2 | Frontend | 2.1.1 |
| **2.1.6** Cost tracking & rate limiting (LLM usage) | 5 SP | P1 | Backend | 2.1.1 |

**Subtotal: 52 SP**

---

### 2.2 Investment Scoring Engine v2

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.2.1** ML model training (investment score algorithm) | 21 SP | P0 | ML Engineer | 1.2.2, 1.4.1 |
| **2.2.2** Score calculation service (takes property + user profile) | 13 SP | P0 | Backend | 2.2.1 |
| **2.2.3** Component scoring (affordability, appreciation, timing, risk, etc.) | 13 SP | P0 | Backend | 2.2.2 |
| **2.2.4** Score explanation (why did it get 78?) | 8 SP | P0 | Backend | 2.2.3 |
| **2.2.5** Confidence scoring (how confident in this score?) | 5 SP | P1 | Backend | 2.2.3 |
| **2.2.6** Score visualization (gauge chart, component breakdown) | 13 SP | P0 | Frontend | 2.2.3 |

**Subtotal: 73 SP**

---

### 2.3 AI Conversational Advisor

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.3.1** AI advisor chat UI (message input, response display) | 13 SP | P0 | Frontend | 2.1.1 |
| **2.3.2** Chat message history (store, retrieve, display) | 8 SP | P0 | Backend | 2.1.4 |
| **2.3.3** Question interpretation (investor intent detection) | 8 SP | P1 | AI/ML | 2.1.2 |
| **2.3.4** Response formatting (markdown, charts in chat) | 5 SP | P1 | Frontend | 2.3.1 |
| **2.3.5** Link to detailed analysis (chat answer → property analysis) | 5 SP | P2 | Frontend | 2.3.1 |
| **2.3.6** Advisor guardrails (financial advice disclaimers) | 5 SP | P0 | Backend | 2.1.2 |

**Subtotal: 44 SP**

---

### 2.4 Market Intelligence & Summaries

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.4.1** Market data aggregation (buyer vs. seller market signals) | 13 SP | P0 | Backend/Data | 1.2.2, 1.2.3 |
| **2.4.2** Market summary generation (AI-written market explanation) | 13 SP | P0 | Backend | 2.4.1, 2.1.2 |
| **2.4.3** Neighborhood intelligence API (schools, crime, amenities) | 13 SP | P1 | Backend | 1.2.3 |
| **2.4.4** Market trends visualization (appreciation trend, price trend) | 8 SP | P1 | Frontend | 2.4.1 |
| **2.4.5** Comparable sales analysis (automatic comps pull) | 8 SP | P1 | Backend | 2.4.1 |

**Subtotal: 55 SP**

---

### 2.5 Scenario Simulation (Basic)

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.5.1** Scenario engine (what-if model for cash flow) | 13 SP | P0 | Backend | 1.4.1 |
| **2.5.2** Vacancy rate scenarios (±2%, ±5%, ±10%) | 5 SP | P0 | Backend | 2.5.1 |
| **2.5.3** Rent change scenarios (±5%, ±10%, ±20%) | 5 SP | P0 | Backend | 2.5.1 |
| **2.5.4** Scenario comparison UI (side-by-side results) | 13 SP | P0 | Frontend | 2.5.1 |
| **2.5.5** Scenario export/save | 5 SP | P2 | Backend | 2.5.1 |

**Subtotal: 41 SP**

---

### 2.6 Alerts & Notifications

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **2.6.1** Alert rules engine (price drop >10%, market shift, etc.) | 13 SP | P1 | Backend | 1.6.2 |
| **2.6.2** In-app notifications (bell icon, notification center) | 8 SP | P1 | Frontend | 2.6.1 |
| **2.6.3** Email digest (daily/weekly/monthly summaries) | 8 SP | P2 | Backend | 2.6.1 |
| **2.6.4** Push notifications (mobile app, browser) | 5 SP | P2 | Frontend | 2.6.1 |
| **2.6.5** Notification preferences (user control) | 5 SP | P2 | Frontend | 2.6.2 |

**Subtotal: 39 SP**

---

### Phase 2 Summary

**Total: 304 SP** (Exceeds estimate)

**Critical Path (P0 only):** ~200 SP (2 months for 4 engineers)

**Phase 2 MVP Scope:**
- LLM integration (2.1)
- Investment scoring v2 (2.2)
- AI advisor (2.3)
- Market intelligence (2.4)
- Basic scenario simulation (2.5)

**Deprioritized to Phase 3:**
- Advanced alerts (2.6.3, 2.6.4)
- Response streaming (2.1.5)
- Question interpretation (2.3.3)

**By End of Phase 2:**
- 5K users
- 50%+ using AI advisor
- NPS >40
- 10K+ properties analyzed

---

## Phase 3: Portfolio Intelligence (Months 4-6) — **150 Story Points**

**Goal:** Multi-property portfolio management, market analysis, financing intelligence  
**Team:** 5 engineers  
**Deliverables:** Portfolio optimization, market intelligence, financing analysis, due diligence support

### 3.1 Advanced Portfolio Analytics

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **3.1.1** Portfolio aggregation API (50+ properties) | 13 SP | P0 | Backend | 1.6.1 |
| **3.1.2** Portfolio cash flow summation (monthly/annual) | 8 SP | P0 | Backend | 3.1.1, 1.4.1 |
| **3.1.3** Property performance ranking (best to worst) | 5 SP | P0 | Backend | 3.1.2 |
| **3.1.4** Portfolio metrics dashboard (total equity, avg cap rate) | 13 SP | P0 | Frontend | 3.1.1 |
| **3.1.5** Property comparison (2-5 properties side-by-side) | 13 SP | P0 | Frontend | 3.1.3 |
| **3.1.6** Portfolio allocation visualization (charts) | 8 SP | P1 | Frontend | 3.1.1 |
| **3.1.7** Geographic heatmap (property distribution) | 8 SP | P2 | Frontend | 3.1.1 |

**Subtotal: 68 SP**

---

### 3.2 Market Intelligence Hub

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **3.2.1** Neighborhood comparison tool (2-3 neighborhoods) | 13 SP | P0 | Backend/Frontend | 2.4.3 |
| **3.2.2** School ratings integration (GreatSchools API) | 8 SP | P1 | Backend | 3.2.1 |
| **3.2.3** Crime data integration (FBI UCR, local police) | 8 SP | P1 | Backend | 3.2.1 |
| **3.2.4** Amenities data (parks, retail, restaurants, transit) | 8 SP | P1 | Backend | 3.2.1 |
| **3.2.5** Interactive map (Mapbox integration) | 13 SP | P1 | Frontend | 3.2.1 |
| **3.2.6** Demographic breakdown (income, education, age) | 8 SP | P2 | Backend | 3.2.1 |
| **3.2.7** Market comparison table (side-by-side metrics) | 5 SP | P1 | Frontend | 3.2.1 |

**Subtotal: 63 SP**

---

### 3.3 Financing & Mortgage Intelligence

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **3.3.1** Mortgageability score (loan approval prediction) | 13 SP | P0 | ML Engineer | 2.2.1 |
| **3.3.2** Mortgage rate feed (daily updates, historical) | 5 SP | P0 | Backend | 1.2.4 |
| **3.3.3** Mortgage scenarios (different down payments, terms) | 13 SP | P0 | Backend | 3.3.1 |
| **3.3.4** Lock vs. float decision tool (rate lock analysis) | 8 SP | P1 | Backend | 3.3.3 |
| **3.3.5** Mortgage visualization (monthly payment breakdown) | 13 SP | P0 | Frontend | 3.3.1 |
| **3.3.6** Lending product comparison (conventional, portfolio, DSCR) | 8 SP | P2 | Backend | 3.3.1 |

**Subtotal: 60 SP**

---

### 3.4 Due Diligence & Reporting

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **3.4.1** Investment report generation (PDF export) | 13 SP | P0 | Backend | 1.4.7 |
| **3.4.2** Report template (executive summary + detail sections) | 8 SP | P0 | Frontend | 3.4.1 |
| **3.4.3** Analysis checklist (legal, inspection, appraisal tracking) | 8 SP | P1 | Frontend | 3.4.1 |
| **3.4.4** Comparables analysis (auto-pull similar properties) | 8 SP | P1 | Backend | 2.4.5 |
| **3.4.5** Risk assessment summary (in report) | 5 SP | P1 | Backend | 3.4.1 |

**Subtotal: 42 SP**

---

### 3.5 API v1 & Third-Party Integrations

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **3.5.1** Public API infrastructure (versioning, documentation) | 13 SP | P1 | Backend | 1.1.5 |
| **3.5.2** Property analysis endpoint (public API) | 8 SP | P1 | Backend | 3.5.1, 2.2.2 |
| **3.5.3** Portfolio endpoint (public API) | 8 SP | P2 | Backend | 3.5.1, 3.1.1 |
| **3.5.4** Market data endpoint (public API) | 5 SP | P2 | Backend | 3.5.1, 2.4.1 |
| **3.5.5** API documentation (Swagger/OpenAPI) | 8 SP | P1 | Backend | 3.5.1 |
| **3.5.6** Rate limiting & usage tracking | 5 SP | P1 | Backend | 3.5.1 |

**Subtotal: 47 SP**

---

### Phase 3 Summary

**Total: 280 SP** (Exceeds estimate)

**Critical Path (P0 only):** ~150 SP (2 months for 5 engineers)

**Phase 3 MVP Scope:**
- Advanced portfolio analytics (3.1)
- Market intelligence basics (3.2.1, 3.2.5)
- Financing intelligence (3.3)
- Due diligence support (3.4)
- API v1 (3.5.1, 3.5.2)

**Deprioritized to Phase 4:**
- Advanced map features (3.2.7)
- Demographic data (3.2.6)
- DSCR loans (3.3.6)

**By End of Phase 3:**
- 25K users
- Average portfolio: 5-8 properties
- 30% implementing recommendations
- $10K+ avg tax savings identified

---

## Phase 4: Advanced Optimization (Months 6-9) — **180 Story Points**

**Goal:** Tax optimization, wealth planning, refinancing, institutional features  
**Team:** 6-7 engineers  
**Deliverables:** Tax planning, 30-year wealth projections, portfolio rebalancing, mobile app, institutional reporting

### 4.1 Tax Optimization Engine

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **4.1.1** Depreciation tracking & scheduling | 13 SP | P0 | Backend/Tax | 1.4.1 |
| **4.1.2** Cost segregation analyzer | 21 SP | P0 | ML Engineer/Tax | 4.1.1 |
| **4.1.3** 1031 exchange tracking | 13 SP | P1 | Backend | 4.1.1 |
| **4.1.4** Passive loss carryforward management | 8 SP | P1 | Backend | 4.1.1 |
| **4.1.5** Estimated tax payment calculator | 8 SP | P1 | Backend | 4.1.1 |
| **4.1.6** Tax optimization recommendations | 8 SP | P0 | Backend | 4.1.1 |
| **4.1.7** Tax report generation (Schedule E prep) | 13 SP | P0 | Backend | 4.1.1 |
| **4.1.8** Tax planning UI (dashboard, scenarios, export) | 13 SP | P0 | Frontend | 4.1.1 |

**Subtotal: 97 SP**

---

### 4.2 Wealth Building & Goal Planning

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **4.2.1** 30-year wealth projection model | 21 SP | P0 | Backend/Analytics | 1.4.1, 3.1.2 |
| **4.2.2** Equity accumulation forecasting | 13 SP | P0 | Backend | 4.2.1 |
| **4.2.3** Appreciation & rent growth assumptions | 8 SP | P0 | Backend | 4.2.1 |
| **4.2.4** Goal-based planning (user defines $5M goal) | 8 SP | P1 | Backend | 4.2.1 |
| **4.2.5** Wealth projection visualization (chart) | 13 SP | P0 | Frontend | 4.2.1 |
| **4.2.6** Compare rent vs. own outcomes | 8 SP | P1 | Backend | 4.2.1 |
| **4.2.7** Tax-deferred growth scenarios | 8 SP | P2 | Backend | 4.2.1 |

**Subtotal: 79 SP**

---

### 4.3 Refinancing & Portfolio Rebalancing

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **4.3.1** Refinance analyzer (break-even calculation) | 13 SP | P0 | Backend | 3.3.4 |
| **4.3.2** Multi-property refinance impact model | 13 SP | P0 | Backend | 4.3.1, 3.1.2 |
| **4.3.3** Portfolio rebalancing recommendations | 13 SP | P1 | Backend | 3.1.3 |
| **4.3.4** Hold vs. sell vs. refinance decision engine | 13 SP | P1 | Backend | 4.3.1, 4.3.3 |
| **4.3.5** Rebalancing scenario UI | 13 SP | P0 | Frontend | 4.3.1 |
| **4.3.6** Capital deployment recommendations | 8 SP | P2 | Backend | 4.3.3 |

**Subtotal: 73 SP**

---

### 4.4 Mobile App (React Native)

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **4.4.1** React Native app setup (Expo/bare workflow) | 13 SP | P0 | Mobile Lead | None |
| **4.4.2** Mobile navigation (bottom tabs, stack nav) | 8 SP | P0 | Mobile | 4.4.1 |
| **4.4.3** Mobile property search (optimized UX) | 13 SP | P0 | Mobile | 1.3.5, 4.4.1 |
| **4.4.4** Mobile property detail | 13 SP | P0 | Mobile | 1.3.6, 4.4.1 |
| **4.4.5** Mobile portfolio dashboard | 13 SP | P0 | Mobile | 1.6.4, 4.4.1 |
| **4.4.6** Mobile cash flow calculator | 13 SP | P0 | Mobile | 1.4.5, 4.4.1 |
| **4.4.7** Camera integration (property photos) | 8 SP | P2 | Mobile | 4.4.1 |
| **4.4.8** Offline mode (view saved properties) | 8 SP | P2 | Mobile | 4.4.1 |
| **4.4.9** Push notifications | 5 SP | P1 | Mobile | 2.6.1, 4.4.1 |
| **4.4.10** App store deployment (iOS + Android) | 8 SP | P1 | DevOps | 4.4.9 |

**Subtotal: 102 SP**

---

### 4.5 Institutional Features v1

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **4.5.1** Multi-user access control (RBAC) | 13 SP | P1 | Backend | 1.1.4 |
| **4.5.2** Institutional reporting (monthly/quarterly templates) | 13 SP | P1 | Backend | 3.4.1 |
| **4.5.3** LP dashboard (summary for limited partners) | 13 SP | P2 | Frontend | 4.5.2 |
| **4.5.4** Data export capabilities (CSV, Excel, PDF) | 8 SP | P1 | Backend | 4.5.2 |
| **4.5.5** Compliance & audit log | 13 SP | P1 | Backend | 1.1.6 |
| **4.5.6** Custom reporting builder | 8 SP | P2 | Frontend | 4.5.2 |

**Subtotal: 68 SP**

---

### Phase 4 Summary

**Total: 419 SP** (Exceeds estimate significantly)

**Critical Path (P0 only):** ~200 SP (3 months for 6-7 engineers)

**Phase 4 MVP Scope:**
- Tax optimization (4.1)
- Wealth projection (4.2)
- Refinancing analyzer (4.3.1)
- Mobile app (4.4) [can be parallel track]
- Institutional basics (4.5)

**Deprioritized to Phase 5:**
- Advanced rebalancing (4.3.3, 4.3.4)
- 1031 exchange (4.1.3)
- Passive loss (4.1.4)
- Camera integration (4.4.7, 4.4.8)
- LP dashboard (4.5.3)

**By End of Phase 4:**
- 50K users
- $15-25K average tax savings/user
- Mobile app: 50K+ downloads
- Institutional customers acquired

---

## Phase 5: Community & Ecosystem (Months 9-12) — **180 Story Points**

**Goal:** Community features, ecosystem integrations, public launch, scaling  
**Team:** 8-10 engineers  
**Deliverables:** Professional network, educational content, integrations, institutional reporting v2, public beta launch

### 5.1 Professional Advisor Network

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.1.1** Advisor profile system (agents, CPAs, brokers) | 13 SP | P1 | Backend | 1.1.4 |
| **5.1.2** Advisor verification & credentials | 8 SP | P1 | Backend | 5.1.1 |
| **5.1.3** Advisor rating system (user reviews) | 8 SP | P2 | Frontend | 5.1.1 |
| **5.1.4** Advisor marketplace (searchable directory) | 13 SP | P1 | Frontend | 5.1.1 |
| **5.1.5** Referral integration (link InvestWise to LoanAdvise) | 13 SP | P0 | Backend | 1.1.5 |
| **5.1.6** Commission tracking (affiliate management) | 8 SP | P2 | Backend | 5.1.5 |

**Subtotal: 63 SP**

---

### 5.2 Educational Content & Onboarding

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.2.1** Blog system (CMS integration) | 13 SP | P2 | Backend | None |
| **5.2.2** Market report generation (automated weekly) | 13 SP | P1 | Backend | 2.4.2 |
| **5.2.3** Educational guides (investing basics, tax tips) | 21 SP | P2 | Content | None |
| **5.2.4** Video tutorials (hosted, embedded in app) | 13 SP | P2 | Content | None |
| **5.2.5** Interactive onboarding flow (5-10 min) | 13 SP | P1 | Frontend | 1.7.1 |
| **5.2.6** Email course "30-Day to Invest Ready" | 8 SP | P2 | Marketing | None |

**Subtotal: 81 SP**

---

### 5.3 API v2 & Advanced Integrations

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.3.1** Webhooks (portfolio changes, market alerts) | 13 SP | P1 | Backend | 3.5.1 |
| **5.3.2** QuickBooks integration | 13 SP | P2 | Backend | 3.5.1 |
| **5.3.3** Yardi integration (property management) | 13 SP | P2 | Backend | 3.5.1 |
| **5.3.4** Tax software integration (TurboTax, ProConnect) | 13 SP | P2 | Backend | 4.1.7 |
| **5.3.5** Mortgage broker integrations (rate quotes) | 13 SP | P1 | Backend | 3.3.1 |
| **5.3.6** Google Sheets two-way sync | 8 SP | P2 | Backend | 3.5.1 |
| **5.3.7** SDK packages (Python, JavaScript, Go) | 13 SP | P2 | Backend | 3.5.1 |

**Subtotal: 86 SP**

---

### 5.4 Institutional Reporting v2

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.4.1** Advanced LP dashboard (performance tracking) | 13 SP | P1 | Frontend | 4.5.3 |
| **5.4.2** Automated monthly report generation | 13 SP | P1 | Backend | 4.5.2 |
| **5.4.3** Benchmarking comparison (vs. targets, vs. peers) | 13 SP | P2 | Backend | 4.5.2 |
| **5.4.4** White-label reporting (custom branding) | 13 SP | P2 | Frontend | 4.5.2 |
| **5.4.5** Distribution reporting (cash flow, capital returns) | 8 SP | P2 | Backend | 4.5.2 |
| **5.4.6** Compliance export (for audits, SEC filings) | 8 SP | P2 | Backend | 4.5.5 |

**Subtotal: 68 SP**

---

### 5.5 Community Features (Read-Only)

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.5.1** Community moderation admin panel | 13 SP | P2 | Backend | None |
| **5.5.2** Content moderation AI (auto-flag inappropriate) | 13 SP | P2 | AI/ML | None |
| **5.5.3** Neighborhood reviews (read-only aggregation) | 13 SP | P2 | Frontend | None |
| **5.5.4** Investor success stories (anonymized) | 8 SP | P2 | Frontend | None |
| **5.5.5** Expert Q&A system (curated answers) | 13 SP | P2 | Backend | None |

**Subtotal: 60 SP**

---

### 5.6 Platform Scaling & Operations

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.6.1** Performance optimization (query optimization, caching) | 13 SP | P0 | DevOps/Backend | 1.1.3 |
| **5.6.2** Load testing (1M concurrent users simulation) | 13 SP | P1 | DevOps | 5.6.1 |
| **5.6.3** Multi-region deployment (reduce latency) | 13 SP | P1 | DevOps | 1.1.1 |
| **5.6.4** Disaster recovery (backup, failover testing) | 8 SP | P1 | DevOps | 1.1.1 |
| **5.6.5** Security audit (penetration testing, compliance) | 13 SP | P0 | Security | 1.1.1 |
| **5.6.6** Monitoring & alerting (ops dashboards) | 8 SP | P1 | DevOps | 1.1.6 |
| **5.6.7** Cost optimization (cloud spend) | 5 SP | P2 | DevOps | 5.6.1 |

**Subtotal: 73 SP**

---

### 5.7 Public Launch & Marketing

| Task | Story Points | Priority | Owner | Dependencies |
|------|-------------|----------|-------|--------------|
| **5.7.1** Marketing website (landing page, product pages) | 21 SP | P1 | Frontend/Marketing | None |
| **5.7.2** Public beta announcement (Product Hunt, media) | 0 SP | P1 | Marketing | None |
| **5.7.3** Content marketing (blog, guides, tutorials) | 21 SP | P2 | Content | 5.2.1 |
| **5.7.4** SEM campaign (Google Ads, paid search) | 0 SP | P2 | Marketing | None |
| **5.7.5** Partnership announcements (BuyWise, LoanAdvise) | 0 SP | P1 | Business Dev | None |

**Subtotal: 42 SP**

---

### Phase 5 Summary

**Total: 473 SP** (Exceeds estimate significantly)

**Critical Path (P0 only):** ~80 SP + Platform scaling (5.6) ~60 SP = 140 SP

**Phase 5 MVP Scope (Focus on Launch):**
- Professional network (5.1.5)
- API v2 webhooks (5.3.1)
- Institutional reporting basics (5.4.1, 5.4.2)
- Platform scaling & security (5.6)
- Public launch (5.7)

**Deprioritized to Year 2:**
- Community features (5.5)
- Advanced integrations (5.3.3, 5.3.4, 5.3.6)
- White-label features (5.4.4)
- Advanced educational content (5.2.3, 5.2.4)

**By End of Phase 5:**
- 100K+ users
- Public launch with Series A funding
- $500K+ institutional ARR
- 500+ professional advisors in network

---

## Cross-Phase Dependencies & Risk Management

### Critical Path
```
Phase 1: Infrastructure (1.1) → Data (1.2) → Search (1.3) → Cash Flow (1.4) → Portfolio (1.6)
    ↓
Phase 2: LLM (2.1) → Scoring (2.2) → Advisor (2.3) → Market (2.4)
    ↓
Phase 3: Analytics (3.1) → Market Intel (3.2) → Financing (3.3)
    ↓
Phase 4: Tax (4.1) → Wealth (4.2) → Rebalancing (4.3)
    ↓
Phase 5: Integrations (5.3) → Reporting (5.4) → Launch (5.7)
```

### Parallel Tracks
- **Mobile App (4.4)** can start in Phase 3 (parallel to 3.x)
- **Content & Marketing (5.2, 5.7)** can start in Phase 2 (no dependencies)
- **Integrations (5.3)** can start in Phase 3 (after API v1)

### High-Risk Items
1. **MLS Data Licensing** - Regional complexity, licensing delays
   - Mitigation: Start early (Phase 1), use alternative data sources as backup
2. **LLM Accuracy** - Hallucination risk, forecasting variance
   - Mitigation: Rigorous testing, confidence scoring, human review gates
3. **Data Quality** - Garbage in → garbage out
   - Mitigation: Strong data validation, automated quality checks
4. **Regulatory** - Investment advice compliance, fair housing
   - Mitigation: Legal review, clear disclaimers, guardrails in code

---

## Team Composition & Hiring Plan

### Phase 1 (Months 0-2)
- 1 Engineering Manager
- 2-3 Backend Engineers
- 1-2 Frontend Engineers
- 1 DevOps/Infrastructure Engineer
- 1 Data Engineer (part-time)
- **Total: 5-7 FTE**

### Phase 2 (Months 2-4)
- Add 1 ML Engineer (LLM, scoring models)
- Add 1 Analytics Engineer
- **Total: 7-9 FTE**

### Phase 3+ (Months 4+)
- Add 1 Mobile Engineer
- Add 1 Senior Backend (scaling, optimization)
- **Total: 8-10 FTE at peak**

---

## Success Metrics & KPIs

### By Phase

| Phase | User Target | Features Live | Key Metric |
|-------|-------------|---------------|-----------|
| **1** | 500 beta | Core MVP | >80% accuracy |
| **2** | 5K | AI features | 50%+ NPS |
| **3** | 25K | Portfolio mgmt | $10K tax ID |
| **4** | 50K | Tax optimization | 30% implement |
| **5** | 100K | Enterprise ready | Series A funded |

### Overall Success Criteria

✅ **Product Quality**
- Forecasting accuracy: 95% within 5% variance
- System uptime: 99.9% SLA
- API response: <3sec p95

✅ **User Adoption**
- 100K+ MAU by Month 12
- 10-15% paid conversion
- NPS >50

✅ **Business**
- $1M+ ARR
- <5% monthly churn
- 30+:1 LTV:CAC ratio

✅ **Data**
- 1B+ properties analyzed
- 10M+ investment decisions informed
- Proprietary ML models trained

---

## Implementation Notes

1. **Agile Workflow:** 2-week sprints, weekly standups, bi-weekly demos
2. **Code Review:** All PRs reviewed by 2+ engineers before merge
3. **Testing:** 80%+ code coverage, automated tests on every commit
4. **Documentation:** Code comments, API docs (Swagger), architecture ADRs
5. **DevOps:** CI/CD pipeline (GitHub Actions), automated deployments
6. **Monitoring:** Datadog dashboards, alerts on errors/latency
7. **Security:** TLS everywhere, encryption at rest, regular audits

---

**Document Status:** Complete - Ready for Sprint Planning  
**Last Updated:** June 7, 2026  
**Next Steps:** Begin Phase 1 implementation, hire team, launch sprint 0
