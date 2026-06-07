# InvestWise PRD Generation Guide

## Overview

This guide explains the InvestWise PRD generation prompt and how to use it effectively.

---

## What's Included

### 1. **INVESTWISE_PRD_PROMPT.md**
A comprehensive prompt ready to be used with an AI model to generate a complete InvestWise Product Requirements Document (PRD).

---

## Key Features of This Prompt

### **Structural Alignment**
- Mirrors the BuyWise PRD structure for consistency across TrueOwn products
- Ensures stakeholders see a familiar format and organization

### **CashFlow Module Integration**
- Positions CashFlow as a **core module within InvestWise** (not separate)
- Includes 6 distinct CashFlow capabilities:
  1. Property-level cash flow analysis
  2. Portfolio-level aggregation
  3. Advanced forecasting
  4. Scenario and stress testing
  5. Performance optimization
  6. Tax integration and planning

### **Comprehensive Investor Coverage**
- 5 distinct investor personas (First-time → Institutional)
- Addresses different investment strategies (buy-and-hold, flipping, multi-asset)
- Market gap analysis specific to investor pain points

### **Business & Technical Depth**
- 5-phase delivery roadmap (12 months)
- 15-20 functional requirement categories
- Competitive differentiation vs. existing platforms
- Go-to-market strategy considerations

---

## How to Use This Prompt

### **Option 1: Direct Use with AI Models**
Copy the entire content of `INVESTWISE_PRD_PROMPT.md` into your preferred AI model (ChatGPT, Claude, etc.) and request the PRD generation.

### **Option 2: Iterative Refinement**
1. Use the prompt as-is for a first draft
2. Request specific expansions (e.g., "Expand the CashFlow module section")
3. Ask for competitive analysis details
4. Request specific use cases or workflows

### **Option 3: Custom Integration**
Integrate sections of this prompt into your internal documentation or combine with internal context:
- Your TrueOwn company vision
- Specific market research findings
- Investor interviews or persona data
- Competitive intelligence
- Technical architecture decisions

---

## Prompt Components Breakdown

### **Section 1: Context**
Establishes the product ecosystem and TrueOwn's portfolio of 7 products.

### **Section 2: Reference Structure**
Points to BuyWise as a template to ensure consistency and professionalism.

### **Section 3: Key Requirements**
Includes:
- **Product Definition** - Clear positioning for InvestWise
- **CashFlow Module Specification** - Detailed feature list
- **User Personas** - 5 investor types
- **Functional Requirements** - Core areas to cover
- **Success Metrics** - Investor-specific KPIs
- **Timeline** - Phase breakdown
- **Differentiation** - Why InvestWise is distinct from BuyWise
- **Ecosystem Integration** - Cross-product synergies

### **Section 4: Deliverables**
Checklist of 17 required PRD sections to ensure completeness.

### **Section 5: Tone & Style**
Guidance on professional voice, using real numbers, and investor terminology.

### **Section 6: Success Criteria**
10 checkpoints to validate PRD quality.

### **Section 7: Output Format**
Specification for markdown format suitable for GitHub and stakeholder review.

---

## CashFlow Module Highlights

The prompt emphasizes CashFlow as a **primary value driver** for InvestWise:

### **Why CashFlow is Central**
- Real estate investing is fundamentally about cash flow optimization
- Existing platforms lack sophisticated cash flow modeling
- Investors spend disproportionate time on Excel-based models
- Market opportunity: Automate cash flow analysis with AI-powered insights

### **Key CashFlow Capabilities**
1. **Operating Expense Breakdown**
   - Property taxes, insurance, maintenance, HOA, utilities
   - Market-based estimates vs. owner input

2. **Rental Income Forecasting**
   - Market rates vs. user projections
   - Vacancy modeling

3. **Portfolio Aggregation**
   - Cross-property cash flow visibility
   - Income vs. expense trends

4. **Advanced Modeling**
   - 5-30 year projections
   - Rent growth and expense inflation
   - Interest rate sensitivity

5. **Scenario Testing**
   - "What-if" analyses
   - Economic downturn resilience
   - Rate hike impact

6. **Tax Optimization**
   - Depreciation tracking
   - 1031 exchange planning
   - Passive loss management

---

## Differentiation from BuyWise

| Aspect | BuyWise | InvestWise |
|--------|---------|-----------|
| **Primary User** | Home buyers | Real estate investors |
| **Core Decision** | Buy vs. Rent | Where to invest & optimize returns |
| **Key Metric** | Affordability score | Cash flow & ROI |
| **Timeline Focus** | 30-year homeownership | Multi-year investment cycles |
| **Portfolio Scope** | Single property (primary residence) | Multiple properties (investments) |
| **Tax Focus** | Mortgage interest deduction | Depreciation, passive loss, cost segregation |
| **Exit Strategy** | N/A (staying long-term) | Refinance, 1031 exchange, sale planning |

---

## Deliverables Checklist

When using this prompt, ensure the generated PRD includes:

- [ ] Executive summary (1-2 pages)
- [ ] Market opportunity and problem statement
- [ ] 5-6 detailed investor personas
- [ ] 15-20 functional requirements with descriptions
- [ ] Non-functional requirements (performance, security, scalability)
- [ ] 8-10 user stories with workflows
- [ ] Dedicated CashFlow module specification
- [ ] Success metrics with targets
- [ ] 5-phase timeline with deliverables
- [ ] Competitive differentiation analysis
- [ ] 20+ identified gaps with recommendations
- [ ] Technical architecture overview
- [ ] Go-to-market strategy outline
- [ ] Assumptions, constraints, and out-of-scope items

---

## Next Steps

### **1. Generate the PRD**
Use the prompt with your chosen AI model to generate the initial PRD document.

### **2. Refine & Iterate**
- Review with product team
- Incorporate company-specific vision
- Adjust timelines based on resource availability
- Add competitive research findings

### **3. Engineering Review**
- Technical feasibility assessment
- Architecture implications
- Data integration requirements
- API specifications

### **4. Stakeholder Alignment**
- Investor pitch preparation
- Sales enablement materials
- Marketing positioning
- Roadmap communication

---

## Prompt Customization Tips

### **To Emphasize CashFlow More:**
Add to the prompt: "CashFlow analysis is the core competitive advantage. Spend significant effort detailing cash flow forecasting accuracy, modeling sophistication, and investor workflows."

### **To Focus on Specific Investor Segments:**
Modify: "Prioritize features for [segment]. Ensure this persona is well-represented in user stories and phase planning."

### **To Add Market Research:**
Include: "Here is our market research on investor pain points: [data]. Ensure these are prominently featured in the problem statement and solution design."

### **To Adjust Timeline:**
Specify: "Timeline should span [6/9/18 months]. Prioritize phases accordingly."

### **To Include Technical Constraints:**
Add: "Technical constraints: [list]. Ensure all architectural recommendations respect these constraints."

---

## Output Validation

After generating the PRD, verify:

1. ✅ **Comprehensiveness** - All 17 sections present and detailed
2. ✅ **Investor Focus** - Investor pain points are articulated and addressed
3. ✅ **CashFlow Prominence** - CashFlow module is featured prominently throughout
4. ✅ **Realism** - Features and timeline are achievable
5. ✅ **Differentiation** - Clear separation from BuyWise and competitors
6. ✅ **Metrics Clarity** - Success criteria are measurable and specific
7. ✅ **Regulatory Compliance** - Legal disclaimers and compliance considerations included
8. ✅ **Ecosystem Integration** - Cross-product opportunities identified
9. ✅ **Professionalism** - Format suitable for investors and engineers

---

## Document Location

The prompt is saved at:
```
c:\Hari\Venkat\repos\invest_wise\INVESTWISE_PRD_PROMPT.md
```

---

## Questions to Guide PRD Usage

When generating the PRD, you may want to ask follow-up questions:

1. **"Expand the CashFlow module with specific example workflows"**
   - Request detailed user journeys through the cash flow analysis feature

2. **"What are the top 3 investor pain points this solves?"**
   - Get prioritized problem statements

3. **"Compare InvestWise to [competitor platform]"**
   - Get detailed competitive differentiation

4. **"What's the minimum viable CashFlow feature set?"**
   - For Phase 1 delivery prioritization

5. **"Generate sample investor personas with specific metrics they care about"**
   - Get more actionable persona data

6. **"What tax planning scenarios should CashFlow support?"**
   - For investor trust and differentiation

7. **"Create a detailed Phase 1 specification"**
   - To guide initial engineering efforts

---

## Related Documentation

- **BuyWise PRD:** [vkondepati/buywise on GitHub](https://github.com/vkondepati/buywise)
- **BuyWise Architecture:** See DESIGN_AND_ARCHITECTURE.md in BuyWise repo
- **TrueOwn Product Portfolio:** 7 products mentioned in prompt context

---

## Contact & Support

If you have questions about:
- **The prompt structure:** Review the "Prompt Components Breakdown" section
- **CashFlow module:** See "CashFlow Module Highlights" section
- **Customization:** See "Prompt Customization Tips" section
- **Validation:** See "Output Validation" section

---

Generated: 2026-06-07
Status: Ready to use
Format: Markdown (.md)
Target Output: PRD Document (3000-4000+ words)
