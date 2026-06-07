# InvestWise PRD Generation Prompt

Use this prompt to generate a comprehensive Product Requirements Document (PRD) for InvestWise, a product of TrueOwn Company.

---

## PROMPT FOR PRD GENERATION

You are an expert product manager creating a comprehensive Product Requirements Document (PRD) for **InvestWise**, a product within the **TrueOwn** company ecosystem. 

InvestWise is an AI-powered real estate investment platform designed to help investors identify profitable properties, manage multi-property portfolios, optimize cash flows, and make data-driven investment decisions. **CashFlow** is a core integrated module within InvestWise that provides comprehensive cash flow analysis, forecasting, and portfolio-level insights.

### **CONTEXT**

**TrueOwn Company** is an LLC offering AI-native real estate solutions:
1. **BuyWise** - AI advisor for home buyers to understand affordability and make confident purchase decisions
2. **InvestWise** - AI investment platform for real estate investors (primary focus)
3. **SellWise** - Tools for sellers to optimize pricing and timing
4. **CashFlow** - (Integrated within InvestWise) Cash flow analysis and portfolio management module
5. **LoanAdvise** - Mortgage and financing guidance
6. **HomeWarranty** - Protection and insurance products
7. **Services** - Professional real estate services marketplace

### **REFERENCE STRUCTURE**

Use the BuyWise PRD as your structural template (available at: https://github.com/vkondepati/buywise), but adapt all content for InvestWise. Follow this section order:

1. **Product Overview**
2. **Problem Statement** (Investor pain points)
3. **Goals & Objectives**
4. **User Personas** (Investor segments)
5. **Requirements** (Functional & Non-Functional)
6. **User Stories & Use Cases**
7. **Success Metrics**
8. **Timeline & Milestones** (5 Phases)
9. **Missing Features & Gaps Analysis**
10. **Assumptions & Constraints**
11. **Out of Scope**

---

## **KEY REQUIREMENTS FOR INVESTWISE PRD**

### **1. PRODUCT DEFINITION**

**InvestWise** is an AI-powered investment analytics platform enabling real estate investors to:
- Identify, evaluate, and compare investment properties intelligently
- Analyze cash flow, ROI, cap rate, and appreciation potential
- Manage multi-property portfolios with real-time performance dashboards
- Forecast financial outcomes with scenario modeling
- Optimize tax strategies and wealth building
- Access market intelligence and competitive analysis
- Receive AI-powered investment recommendations

**Core Differentiator:** InvestWise focuses on **return optimization and portfolio management** for investors (both individual and institutional), whereas BuyWise focuses on buy-vs-rent decision-making for homeowners.

---

### **2. CASHFLOW MODULE SPECIFICATION**

**CashFlow** must be thoroughly integrated as a core module within InvestWise (not a separate product). It should include:

#### **Core Features:**
1. **Property-Level Cash Flow Analysis**
   - Monthly/annual operating expense breakdown (taxes, insurance, maintenance, management, HOA, utilities)
   - Rental income projections (market-based and user-input)
   - Vacancy assumptions (by market and property type)
   - Net cash flow calculation
   - Cash-on-cash return and cap rate calculations

2. **Portfolio-Level Cash Flow Dashboard**
   - Aggregated cash flow across all properties
   - Income vs. expenses visualization
   - Multi-year cash flow forecasts (5/10/15/20/30 years)
   - Seasonal cash flow patterns (e.g., higher vacancies in winter)
   - Tax bracket impact on after-tax cash flow

3. **Advanced Forecasting**
   - Rent growth projections (historical, market, custom)
   - Expense inflation modeling
   - Mortgage paydown tracking
   - Refinance scenario analysis
   - Interest rate sensitivity analysis

4. **Scenario & Stress Testing**
   - "What-if" analyses: vacancy increases, rent decreases, unexpected expenses
   - Economic downturn scenarios
   - Rate hike impact on new purchases vs. portfolio
   - Property-level and portfolio-level scenario comparison

5. **Performance Optimization**
   - Identify underperforming properties
   - Rental rate optimization recommendations ("Can I increase rent to market?")
   - Expense reduction opportunities
   - Capital improvement ROI calculator
   - Portfolio rebalancing recommendations

6. **Tax Integration & Planning**
   - Depreciation tracking (building vs. land)
   - Cost segregation opportunity identification
   - 1031 exchange tracking and recommendations
   - Passive loss tracking and carryforward
   - Estimated tax payment guidance
   - Tax-deferred reinvestment strategies

---

### **3. USER PERSONAS**

Define at least 5 investor personas:

1. **First-Time Investor** - Buying their first rental property, needs education and confidence
2. **Active Investor** - Owns 5-20 properties, actively trading, needs portfolio optimization
3. **Institutional/Portfolio Investor** - Manages 50+ properties, needs reporting and institutional features
4. **House Flipper** - Short-term hold strategy, needs renovation cost analysis and exit planning
5. **Multi-Asset Investor** - Owns rentals + flips + commercial, needs consolidation

---

### **4. CORE FUNCTIONAL REQUIREMENTS**

Include sections for:
- Property search & discovery (REI-focused filters)
- Investment scoring and opportunity ranking
- Cash flow analysis (CashFlow module)
- Portfolio tracking & management
- AI conversational investment advisor
- Market intelligence & neighborhood analysis
- Financing & mortgage intelligence
- Tax optimization guidance
- Due diligence support
- Alerts & notifications
- Reporting & analytics
- API & third-party integrations

---

### **5. SUCCESS METRICS** 

Include investor-specific KPIs:
- Properties analyzed per user
- Portfolio size (# of properties tracked)
- Average cash flow per portfolio
- Investment decision conversion rate
- Time-to-close reduction
- User satisfaction with ROI accuracy
- Retention rate by investor stage

---

### **6. TIMELINE** 

Create 5 phases:
- **Phase 1 (Months 0-2):** Foundation - Property discovery, basic cash flow analysis
- **Phase 2 (Months 2-4):** AI Layer - Conversational advisor, advanced cash flow modeling
- **Phase 3 (Months 4-6):** Portfolio Intelligence - Multi-property dashboards, market analysis
- **Phase 4 (Months 6-9):** Advanced Optimization - Tax planning, refinancing, scenario modeling
- **Phase 5 (Months 9-12):** Community & Ecosystem - Agent network, fund integrations, institutional features

---

### **7. DIFFERENTIATION FROM BUYWISE**

Ensure the PRD clearly differentiates InvestWise from BuyWise:
- BuyWise: Helps individuals buy their primary residence
- InvestWise: Helps investors build and optimize investment portfolios
- Different KPIs, features, and user journeys
- InvestWise emphasizes ROI, portfolio management, and wealth building
- BuyWise emphasizes affordability, homeownership costs, and buy-vs-rent

---

### **8. ECOSYSTEM INTEGRATION**

Mention integration points with other TrueOwn products:
- **BuyWise Integration:** Investors can use BuyWise for personal residence decisions
- **SellWise Integration:** Exit planning for rental properties or flips
- **LoanAdvise Integration:** Refinancing and portfolio financing
- **HomeWarranty Integration:** Protection recommendations
- **Services Integration:** Contractor and property management marketplace

---

## **DELIVERABLES**

Generate a complete PRD document (minimum 3000-4000 words) with:

1. ✅ Executive Summary
2. ✅ Company & Product Context
3. ✅ Problem Statement (with market gap analysis)
4. ✅ Goals & Objectives (business + product + user)
5. ✅ Comprehensive User Personas (5-6 personas with detailed profiles)
6. ✅ Requirements Section:
   - Functional Requirements (15-20 categories)
   - Non-Functional Requirements (Performance, Scalability, Security, Compliance)
7. ✅ User Stories & Use Cases (8-10 detailed scenarios)
8. ✅ CashFlow Module Deep Dive (Feature specifications)
9. ✅ Success Metrics (Quantifiable KPIs)
10. ✅ Timeline & Milestones (5 phases with deliverables)
11. ✅ Why InvestWise Wins (Competitive differentiation)
12. ✅ Key Differentiators by User Segment
13. ✅ Assumptions & Constraints
14. ✅ Out of Scope Features
15. ✅ Missing Features & Gaps Analysis (20+ identified gaps with recommendations)
16. ✅ Technical Architecture Callouts (High-level)
17. ✅ Go-to-Market Strategy Summary

---

## **TONE & STYLE**

- Professional, data-driven, investor-focused
- Use real numbers and benchmarks where applicable
- Include investor terminology naturally
- Provide specific use cases and workflows
- Balance ambition with pragmatism
- Include risk mitigation strategies

---

## **CRITICAL REQUIREMENTS FOR CASHFLOW MODULE**

The CashFlow module must be positioned as:
- **Core to InvestWise value proposition** (not optional)
- **Automated yet customizable** (template + custom inputs)
- **Accurate and trusted** (cite real data sources)
- **Forward-looking** (5-30 year projections)
- **Actionable** (recommendations for optimization)
- **Integrated with portfolio** (not property-level only)
- **Tax-intelligent** (real tax implications, not theoretical)

---

## **SUCCESS CRITERIA FOR PRD**

Your PRD will be considered complete and high-quality if it:

✓ Stands as a comprehensive standalone document (not dependent on BuyWise PRD to understand)
✓ Clearly articulates investor problems and how InvestWise solves them
✓ Positions CashFlow as central to the product experience
✓ Includes 3-5 detailed cash flow modeling examples
✓ Specifies data sources and refresh rates
✓ Addresses tax and regulatory considerations
✓ Maps out a realistic 12-month delivery roadmap
✓ Identifies 20+ specific features and their phase placement
✓ Includes competitive analysis vs. existing platforms (e.g., Roofstock, MLS360, PropertyShark)
✓ Provides credible success metrics tied to investor behavior and business outcomes

---

## **OUTPUT FORMAT**

Generate as a markdown (.md) document suitable for:
- GitHub repository
- Internal stakeholder review
- Investor pitch deck source
- Engineering sprint planning
- Design system requirements

Include:
- Clear headings and subheadings
- Tables for comparisons and matrices
- Bulleted lists for clarity
- Code blocks for data structures (if applicable)
- Example workflows in narrative form
- Appendices with detailed feature specifications

---

END PROMPT
