# InvestWise UI/UX Flows & Persona Journeys

**Date:** June 7, 2026  
**Version:** 1.0  
**Status:** Ready for Design & Development

---

## Overview

This document maps user personas to specific UI flows and interactions in the TrueOwn prototype, ensuring design and development align with real investor workflows.

---

## Persona Summary

| Persona | Goal | Primary Flow | Key Features |
|---------|------|--------------|--------------|
| **Maya Patel** | First-time buyer | Property search → affordability check → purchase confidence | BuyWise affordability |
| **David Chen** | Active investor | Portfolio consolidation → optimization → tax planning | InvestWise portfolio, CashFlow |
| **Lisa Martinez** | House flipper | Quick deal evaluation → ARV estimation → profit modeling | InvestWise flip analyzer |
| **Arjun Sharma** | Institutional investor | Property aggregation → LP reporting → performance tracking | Enterprise features, API |

---

## Flow 1: Maya Patel — First-Time Home Buyer

### User Profile
- Age: 32
- Income: $150K household
- Tech-savvy, nervous about investment
- First time buying primary residence
- Goal: Understand affordability and neighborhood fit

### Primary User Journey

```
START: Maya is browsing Zillow, finds a house she likes
   ↓
ENTER ADDRESS: Pastes URL or searches address in InvestWise
   ↓
SEARCH: System returns property details
   ↓
AFFORDABILITY ANALYSIS: Enters income, down payment, debts
   ↓
SYSTEM CALCULATES: Monthly payment, true cost of ownership, risk
   ↓
VIEW RESULTS: 
   - Affordability score (84/100)
   - Monthly payment breakdown
   - True cost vs. mortgage-only
   - 30-year wealth projection
   ↓
NEIGHBORHOOD CHECK: Clicks "Neighborhood Intelligence"
   ↓
VIEW NEIGHBORHOOD:
   - Schools, crime, parks nearby
   - Demographics, income distribution
   - Future development signals
   ↓
DECISION: "This property works for me"
   ↓
SAVE PROPERTY: Adds to favorites for follow-up
   ↓
MAKE OFFER: Proceeds to purchase
```

### Key UI Screens

#### Screen 1: Property Search
```
[Top Bar: TrueOwn logo | Search bar (focused) | User profile]

Search Input:
┌─────────────────────────────────────┐
│ Search address, city, or zip code... │ 🔎
└─────────────────────────────────────┘

Suggested Properties:
┌─────────────────────────────────────┐
│ 1248 Maple Creek Dr, Frisco, TX    │
│ 4 bed • 3 bath • 2,800 sqft        │
│ $585,000                            │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ 8821 Willow Bend Ln, Plano, TX     │
│ 3 bed • 2.5 bath • 2,200 sqft      │
│ $435,000                            │
└─────────────────────────────────────┘
```

#### Screen 2: Affordability Calculator
```
[Back] Affordability Analysis

Home Price: $585,000
Down Payment: $117,000 (20%)
Loan Amount: $468,000

Monthly Income: $12,500 (household)
Existing Debts: $1,200/month

┌─────────────────────────────────┐
│ Results                          │
├─────────────────────────────────┤
│ Monthly Mortgage:     $2,760     │
│ Property Tax:          $610      │
│ Insurance:             $185      │
│ Maintenance (reserve): $240      │
├─────────────────────────────────┤
│ TOTAL MONTHLY:        $3,795     │
│ % of Income:          30.4%      │
├─────────────────────────────────┤
│ Affordability Score: 84/100     │
│ Assessment: Good fit             │
└─────────────────────────────────┘

[📊 View 30-Year Analysis] [❤️ Save Property] [→ View Neighborhood]
```

#### Screen 3: Neighborhood Intelligence
```
[Back] Neighborhood: Frisco, TX 75034

Overview Map
[Mapbox showing schools, parks, crime heat layer]

School Districts:
┌─────────────────────────┐
│ Vaughn Elementary       │
│ Rating: 8/10 ⭐⭐⭐⭐  │
│ Distance: 0.8 miles    │
├─────────────────────────┤
│ Top High School (nearby)│
│ Rating: 9/10 ⭐⭐⭐⭐⭐ │
│ Distance: 2.3 miles    │
└─────────────────────────┘

Safety & Crime:
┌─────────────────────────┐
│ Safety Score: 8.2/10   │
│ Violent Crime: Low     │
│ Property Crime: Low    │
│ 5-Year Trend: ↑ Better│
└─────────────────────────┘

Nearby Amenities:
┌─────────────────────────┐
│ Parks: 4 within 1 mile │
│ Retail: 12 nearby      │
│ Restaurants: 24 nearby │
└─────────────────────────┘

[Compare with other neighborhoods] [Save comparison]
```

### Conversion Path
```
Property Search
     ↓ (2 min)
Property Details + Score
     ↓ (5 min)
Affordability Calculator
     ↓ (8 min)
Neighborhood Intelligence
     ↓ (5 min)
DECISION: Buy / Not Buy / Save for Later
```

### Success Metrics
- Time to decision: <30 min
- Confidence score: 8+/10
- Actual vs. forecast accuracy: ±10%

---

## Flow 2: David Chen — Active Real Estate Investor

### User Profile
- Age: 42
- Portfolio: 12 rental properties
- Income: $250K employment + $40K rental income
- Uses 3-5 disconnected tools currently
- Goal: Consolidate portfolio, identify optimizations, plan tax efficiently

### Primary User Journey

```
START: David wants consolidated view of all 12 properties
   ↓
LOGIN: Existing user (already has InvestWise account)
   ↓
IMPORT PORTFOLIO: 
   - Manually enters existing properties OR
   - Connects accounting system (QuickBooks)
   ↓
SYSTEM IMPORTS: Retrieves property details, rent, expenses
   ↓
PORTFOLIO DASHBOARD: Aggregated view of all 12 properties
   ↓
REVIEW METRICS:
   - Total cash flow: $4,200/month
   - Total equity: $441K
   - Weighted avg cap rate: 5.4%
   - Performance ranking (best to worst)
   ↓
IDENTIFY OPPORTUNITIES:
   - Property #7: Rent 12% below market (+$250/month potential)
   - Property #4: Refinance opportunity (save $120/month)
   - Tax depreciation: $8,500/year benefit
   ↓
TAKE ACTION:
   - Increase rent on Property #7
   - Model refinance scenario on Property #4
   - Plan 1031 exchange on underperformer
   ↓
GENERATE TAX REPORT: 
   - Depreciation schedule
   - Passive loss carryforward
   - Estimated taxes
   ↓
EXPORT FOR CPA: PDF/Excel report for tax professional
```

### Key UI Screens

#### Screen 1: Portfolio Dashboard (Main View)
```
[Sidebar: Portfolio selected] [Top bar: search, user menu]

Portfolio Summary
┌─────────────┬─────────┬────────┬──────────┐
│ Properties  │ Equity  │Monthly │ Avg Cap  │
│     12      │ $441K   │ $4.2K  │  5.4%    │
└─────────────┴─────────┴────────┴──────────┘

Performance Alerts
┌──────────────────────────────────────────┐
│ 🔴 Property #7: Rent optimization       │
│    Current: $1,900 | Market: $2,150     │
│    Annual upside: +$3,000                │
├──────────────────────────────────────────┤
│ 🟡 Property #4: Refinance watch         │
│    Could save $120/month (break-even 24m)│
├──────────────────────────────────────────┤
│ 🟢 Tax efficiency: +$8.5K depreciation   │
└──────────────────────────────────────────┘

Portfolio Properties Table
┌─────────────────────────────────────────────┐
│ Property         │ Value  │ Equity │ CF/mo │
├──────────────────┼────────┼────────┼────────┤
│ Dallas Duplex    │$420K   │$98K    │$612   │
│ Plano Townhome   │$385K   │$112K   │$430   │
│ Houston SFH      │$318K   │$76K    │$275   │
│ Austin Condo     │$510K   │$155K   │-$40   │
└─────────────────────────────────────────────┘

[View Property Detail] [Compare Properties] [Export to PDF]
```

#### Screen 2: Property Detail (Opportunity)
```
[Back to Portfolio] Dallas Duplex 84/100 Score

Address: 4109 Bryan St, Dallas, TX

Key Metrics
┌─────────────────┬─────────────────┐
│ Price: $420,000 │ Equity: $98,000 │
│ Rent: $3,900    │ Cap Rate: 6.4%  │
│ Cash Flow: $612 │ CoC Return: 6.2%│
└─────────────────┴─────────────────┘

Optimization Opportunities
┌──────────────────────────────────────┐
│ Rental Rate Gap: $200/month          │
│                                      │
│ Current Rent:     $3,900/month      │
│ Market Rent:      $4,100/month      │
│ Annual Upside:    +$2,400           │
│                                      │
│ [Increase Rent Scenario]            │
└──────────────────────────────────────┘

Cash Flow Analysis
[Chart: Monthly cash flow breakdown - mortgage, taxes, insurance, net]

Risk Assessment
┌────────────────────────────────────┐
│ Vacancy Risk:      Low (6% assumed) │
│ Interest Rate Risk: Medium          │
│ Neighborhood:      Stable           │
│ Recommendation:    Hold + Optimize  │
└────────────────────────────────────┘

[Model Refinance] [Plan 1031 Exit] [Ask AI] [Export Report]
```

#### Screen 3: Tax Planning
```
[Sidebar] Tax Planning

Annual Tax Summary
┌──────────────────────────────────┐
│ Gross Rental Income:   $46,800   │
│ Operating Expenses:   -$26,200    │
│ Net Income:            $20,600    │
├──────────────────────────────────┤
│ Depreciation Deduction: -$8,500   │
│ Taxable Income:        $12,100    │
│ Estimated Tax:          $3,630    │
└──────────────────────────────────┘

Depreciation Schedule
┌─────────────────────────────────────┐
│ Property               │ Annual Dep │
├───────────────────────┼────────────┤
│ Dallas Duplex         │ $2,100     │
│ Plano Townhome        │ $1,950     │
│ Houston SFH           │ $1,800     │
│ Austin Condo          │ $2,650     │
└─────────────────────────────────────┘

Cost Segregation Opportunities
┌──────────────────────────────────────┐
│ Dallas Duplex: +$8,000/year benefit  │
│ Plano Townhome: +$6,500/year benefit │
│                                      │
│ [Schedule Professional Review]      │
└──────────────────────────────────────┘

[Generate Tax Report for CPA] [Export to QuickBooks]
```

### Conversion Path
```
Portfolio Import/Setup
     ↓ (15 min)
Portfolio Dashboard
     ↓ (10 min)
Identify Opportunities
     ↓ (5 min per property)
Take Action (Model scenarios, export reports)
     ↓ (varies)
OUTCOME: Consolidated, optimized, tax-ready portfolio
```

### Success Metrics
- Setup time: <1 hour
- Optimizations identified: 3-5 per portfolio
- Annual value surfaced: $15K-40K (tax, rent, refi)
- Time savings: 10-15 hours/month → 5 hours/month
- Retention: >80% after 6 months

---

## Flow 3: Lisa Martinez — House Flipper

### User Profile
- Age: 38
- Active flips: 3-4 concurrent projects
- Time constraint: Rapid decision-making critical
- Goal: Quick deal evaluation, ARV estimation, profit forecast

### Primary User Journey

```
START: Lisa receives off-market deal opportunity
        Address: 2708 Hemphill St, Fort Worth, TX
        Asking: $265,000
        Condition: Needs work (roof, kitchen, flooring)
   ↓
QUICK ENTRY: Enters address + estimated renovation cost ($35K)
   ↓
SYSTEM ANALYZES:
   - Pulls comparable sales (15 recent sales in area)
   - Estimates after-repair value (ARV)
   - Calculates equity and profit potential
   ↓
FLIP ANALYSIS:
   - Purchase Price: $265,000
   - Est. Renovations: $35,000
   - Estimated ARV: $375,000
   - Est. Gross Profit: $75,000
   - Less soft costs (~4%): -$15,000
   - Less financing (6 months): -$12,500
   - Net Profit: $47,500 (17.9% ROI)
   ↓
SCENARIO TEST:
   "What if renovations cost $45K?"
   → Net Profit: $37,500 (14.2% ROI, still acceptable)
   ↓
DECISION: Risk/reward acceptable, make offer
   ↓
TRACK PROJECT: Adds to active flip pipeline
```

### Key UI Screens

#### Screen 1: Quick Flip Analyzer
```
[Top bar] Flip Analyzer | New Deal

Property Entry
┌─────────────────────────────────────┐
│ Address: 2708 Hemphill St, Fort Worth, TX
│ Zip: 76110                          │
└─────────────────────────────────────┘

Deal Terms
┌──────────────────────────────┐
│ Purchase Price: $265,000     │
│ Down Payment: 25% ($66,250)  │
│ Estimated Renovations: $35K  │
│ Hold Period: 6 months        │
└──────────────────────────────┘

[Analyze Deal]
```

#### Screen 2: Flip Analysis Results
```
[Flip Analysis: 2708 Hemphill St, Fort Worth, TX]

Deal Score: 78/100 ✓ Proceed with caution

Quick Summary
┌──────────────────────────────────┐
│ Purchase Price:      $265,000    │
│ Estimated ARV:       $375,000    │
│ Potential Equity:    $110,000    │
│                                  │
│ Est. Profit:         $47,500     │
│ ROI:                 17.9%       │
│ Break-even point:    14 months   │
├──────────────────────────────────┤
│ Risk Level: MEDIUM               │
│ Market: Seller's Market (slower) │
└──────────────────────────────────┘

ARV Justification
┌──────────────────────────────────┐
│ Based on 15 comp sales in area:  │
│ • Median sale price: $375K       │
│ • Your estimate: $375K (aligned) │
│ • Confidence: 85%                │
└──────────────────────────────────┘

Renovation Cost Breakdown
┌──────────────────────────────────┐
│ Roof:        $8,000              │
│ Kitchen:     $15,000             │
│ Flooring:    $8,000              │
│ Painting:    $2,000              │
│ Other:       $2,000              │
│ TOTAL:       $35,000             │
└──────────────────────────────────┘

[Test Scenarios] [Add to Pipeline] [Ask AI] [Share Deal]
```

#### Screen 3: Scenario Modeling
```
[Flip Analyzer: Scenario Tests]

Base Case: $47,500 profit (17.9% ROI)

Scenario: Renovations $45K (vs. $35K estimate)
┌──────────────────────────────────┐
│ Net Profit: $37,500 (14.2% ROI)  │
│ Change: -$10,000 (-21%)          │
│ Still acceptable? YES             │
└──────────────────────────────────┘

Scenario: ARV drops to $350K (vs. $375K)
┌──────────────────────────────────┐
│ Net Profit: $32,500 (12.3% ROI)  │
│ Change: -$15,000 (-32%)          │
│ Risk Assessment: MEDIUM           │
└──────────────────────────────────┘

Scenario: Hold extended to 9 months
┌──────────────────────────────────┐
│ Additional financing cost: $3,750 │
│ Net Profit: $43,750 (16.5% ROI)  │
│ Still profitable                  │
└──────────────────────────────────┘

Best Case: Renovations $30K, ARV $380K
┌──────────────────────────────────┐
│ Net Profit: $54,500 (20.6% ROI)  │
│ Upside potential exists          │
└──────────────────────────────────┘

[Decision: PROCEED] [Hold for more data]
```

### Conversion Path
```
Quick Entry
     ↓ (2 min)
Analysis Results
     ↓ (3 min)
Scenario Testing
     ↓ (5 min)
DECISION: Go/No-Go (10 min total)
```

### Success Metrics
- Analysis time: <15 min per deal
- ARV accuracy: ±10% vs. actual
- Deal volume: 5-15 deals analyzed/month
- Completion rate: 3-5 flips/year with >25% ROI
- Repeat usage: 80%+

---

## Flow 4: Arjun Sharma — Institutional Investor

### User Profile
- Age: 52
- Managing: REI fund, 120 properties across 5 states
- Responsibilities: LP reporting, portfolio optimization, investor communications
- Pain: 20+ hours/month manual reporting
- Goal: Automated dashboards, reporting, compliance

### Primary User Journey

```
START: Month-end, Arjun needs to generate LP report
   ↓
LOGIN: Access institutional dashboard
   ↓
AGGREGATE DATA:
   - System auto-pulls property data from multiple sources
   - Consolidates rental income, expenses, cash distributions
   - Calculates performance metrics across portfolio
   ↓
GENERATE REPORT:
   - Monthly summary (cash collected, distributed, available)
   - Performance vs. targets
   - Property-by-property breakdown
   - Benchmarking vs. comparable funds
   ↓
LP DASHBOARD:
   - Portfolio overview (market value, equity, cash flow)
   - Performance tracking (YTD, 3-year, since inception)
   - Distribution history
   - Risk metrics
   ↓
EXPORT: PDF/Excel for LP distribution
   ↓
SHARE: Email to LPs with password protection
   ↓
COMPLIANCE: Archive report for audit trail
```

### Key UI Screens

#### Screen 1: Institutional Dashboard
```
[Sidebar: Admin mode] [Top bar: fund selection, settings]

Fund Summary
┌──────────────────────────────────────┐
│ Total Properties: 120                │
│ Portfolio Value: $48M                │
│ Total Equity: $12.4M                 │
│ Monthly Cash Flow: $180K             │
│ Avg Cap Rate: 5.8%                   │
└──────────────────────────────────────┘

Performance vs. Targets
┌──────────────────────────────────────┐
│ Year-to-Date Performance:            │
│ • Cash Flow Generated: $450K (on track) │
│ • Appreciation: +$1.8M (target: $1.6M) │
│ • Distributions Paid: $420K          │
├──────────────────────────────────────┤
│ LTV: 62% (target: 65%) ✓             │
│ Debt Service Coverage: 1.8x (good)   │
└──────────────────────────────────────┘

Property Distribution
┌──────────────────────────────────────┐
│ Texas: 45 properties (38% of portfolio) │
│ Florida: 35 properties (29%)         │
│ California: 25 properties (21%)      │
│ Other: 15 properties (12%)           │
└──────────────────────────────────────┘

[Portfolio Details] [LP Dashboard] [Generate Report]
```

#### Screen 2: LP Dashboard (Investor View)
```
[Limited Partner Access - Read-Only]

Your Investment Summary
┌──────────────────────────────────────┐
│ Original Capital Invested: $500,000  │
│ Current Equity Value: $675,000       │
│ Gain: $175,000 (35%)                 │
│                                      │
│ YTD Cash Distributions: $45,000      │
│ Distribution Yield: 9%               │
└──────────────────────────────────────┘

Performance Tracking
┌──────────────────────────────────────┐
│ Fund Performance:                    │
│ 1-Year Return: 12.4%                 │
│ 3-Year Return: 10.8% annualized      │
│ Since Inception: 9.2% annualized     │
│                                      │
│ vs. Benchmarks:                      │
│ • NCREIF: 8.6% (✓ ahead)             │
│ • REITs: 5.2% (✓ ahead)              │
└──────────────────────────────────────┘

Distribution History
┌──────────────────────────────────────┐
│ Distribution Schedule:               │
│ • Q1: $12,500 (paid Mar 31)          │
│ • Q2: $11,250 (paid Jun 30)          │
│ • Q3: $12,750 (paid Sep 30)          │
│ • Q4: $8,500 (estimated Dec 31)      │
└──────────────────────────────────────┘

[Detailed Holdings] [Contact Manager] [Download Statement]
```

#### Screen 3: Monthly Report Generation
```
[Admin: Generate Monthly Report]

Report Configuration
┌─────────────────────────────────┐
│ Select Month: June 2026          │
│ Report Type: LP Summary          │
│ Include Benchmarks? Yes          │
│ Confidentiality: Password-Protected
│ Recipients: [predefined list]    │
└─────────────────────────────────┘

Report Preview
┌──────────────────────────────────────┐
│ FUND MONTHLY REPORT                  │
│ Period: June 1-30, 2026              │
│                                      │
│ PORTFOLIO SUMMARY                    │
│ Properties: 120                      │
│ Total Value: $48M                    │
│ Total Equity: $12.4M                 │
│                                      │
│ MONTHLY ACTIVITY                     │
│ Rent Collected: $145K                │
│ Operating Expenses: -$52K            │
│ Debt Service: -$45K                  │
│ Net Cash Flow: $48K                  │
│ Distribution to LPs: $42K (87%)      │
│ Reserve: $6K (13%)                   │
│                                      │
│ [View detailed breakdown]            │
│ [Review property-by-property]        │
│ [Generate PDF]                       │
└──────────────────────────────────────┘

[Generate & Send] [Schedule Recurring] [Archive]
```

### Conversion Path
```
Data Aggregation (automatic)
     ↓ (0 min user action)
Dashboard Review
     ↓ (5 min)
Report Generation (automated)
     ↓ (2 min)
Distribution to LPs
     ↓ (1 min)
OUTCOME: 20 hours/month → 10 minutes (95% time savings)
```

### Success Metrics
- Report generation time: <15 min (vs. 20 hours manual)
- Data accuracy: >99%
- System uptime: 99.95%
- LP satisfaction: NPS >60
- Compliance audit pass rate: 100%

---

## Cross-Persona Design Consistency

### Navigation Structure
All personas see the same **sidebar navigation** but with context-aware defaults:

```
Maya (First-Time):        David (Investor):        Arjun (Institutional):
├─ Home                   ├─ Portfolio              ├─ Dashboard
├─ Search Properties      ├─ Analytics              ├─ Property Manager
├─ My Favorites           ├─ Market Analysis        ├─ LP Reporting
├─ Affordability          ├─ Tax Planning           ├─ User Management
└─ Neighborhood           ├─ AI Advisor             ├─ Compliance
                          └─ Settings               └─ Settings
```

### Common Components
1. **Search Bar** (Top bar) - Works across all personas
2. **Property Card** - Same template, different data highlighted
3. **Chart Visualizations** - Consistent styling, different metrics
4. **Button Actions** - Consistent primary/secondary styles
5. **Modal Dialogs** - Consistent spacing, typography

### Responsive Behavior
```
Desktop (>1024px): Full sidebar + main content
Tablet (640-1024px): Collapsible sidebar + responsive grid
Mobile (<640px): Hamburger menu + single-column layout
```

---

## Interaction Principles

### 1. Progressive Disclosure
Data reveals itself based on user action:
- **Initial view:** Essential metrics only
- **Expand action:** Detailed breakdown
- **Detail view:** Full analysis with charts

### 2. Immediate Feedback
- Buttons show loading state
- Calculations show progress spinner
- Errors show clear, specific messages
- Success shows confirmation badge

### 3. Reversible Actions
- Delete = Move to trash (30-day recovery)
- Scenario = Save without committing
- Preference changes = "Save" or "Discard"

### 4. Consistency
- Same icon = Same action everywhere
- Same color = Same meaning everywhere
- Same terminology = No "Properties" vs. "Assets" confusion

---

## Accessibility Features

### WCAG 2.1 AA Compliance

✅ **Color Contrast**
- Text vs. background: 4.5:1 minimum
- Interactive elements: Clear visual states

✅ **Keyboard Navigation**
- Tab through all interactive elements
- Enter/Space to activate buttons
- Escape to close modals

✅ **Screen Reader Support**
- Form labels properly associated
- Table headers marked
- Icons have aria-labels
- Charts include alt text

✅ **Focus Management**
- Visible focus outline on all elements
- Logical tab order (left-to-right, top-to-bottom)
- Focus doesn't get trapped

---

## Mobile-Specific Interactions

### Responsive Adjustments

**Search**
- Desktop: Full search bar in top bar
- Mobile: Search icon opens full-screen overlay

**Tables**
- Desktop: Full table with horizontal scroll
- Mobile: Vertical card layout (1 property per card)

**Charts**
- Desktop: Full interactive charts
- Mobile: Simplified charts, pinch-to-zoom

**Actions**
- Desktop: Hover tooltips
- Mobile: Long-press for context menu

---

## Performance Considerations

### Critical Pages (Target <3s load)
1. Home/Dashboard (cached, critical data only)
2. Property Detail (pre-fetch on hover)
3. Search Results (paginated, lazy loading)

### Optimization Techniques
- Debounce calculator inputs (500ms)
- Cache property details (1 hour)
- Lazy load images (below fold)
- Code splitting (route-based)
- Service worker (offline mode)

---

## Analytics Events to Track

### User Engagement
```
- property_viewed
- affordability_calculated
- scenario_created
- property_saved
- portfolio_property_added
- tax_report_generated
- advisor_question_asked
- property_exported
```

### Funnel Analysis
```
Property Search → Property Detail → Affordability Calc → Save Property → Portfolio Add
     (100%)      → (60%)        → (45%)             → (40%)        → (30%)
```

### Success Metrics
```
- Time on property detail: 3-5 minutes
- Affordability calc completion rate: 70%
- Report export rate: 25%
- Portfolio consolidation: 80% (after onboarding)
```

---

## Testing Checklist

### Functional Testing
- [ ] Search returns accurate results
- [ ] Calculations match manual verification
- [ ] Portfolio aggregation accurate (50+ properties)
- [ ] Reports generate without errors
- [ ] Filters work correctly
- [ ] Sorting works correctly

### Responsive Testing
- [ ] Desktop (1920x1080, 1366x768)
- [ ] Tablet (768x1024, 600x900)
- [ ] Mobile (375x667, 414x896)
- [ ] Orientation changes (portrait/landscape)

### Accessibility Testing
- [ ] Keyboard-only navigation works
- [ ] Screen reader compatible
- [ ] Color contrast ≥4.5:1
- [ ] Focus states visible
- [ ] No keyboard traps

### Performance Testing
- [ ] Page load <3s (lighthouse green)
- [ ] First contentful paint <1.5s
- [ ] Time to interactive <3.5s
- [ ] Lighthouse score ≥80

### Cross-Browser Testing
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)

---

**Document Status:** Complete - Ready for Design & QA  
**Last Updated:** June 7, 2026  
**Next Steps:** Design handoff to frontend team, create interactive prototypes
