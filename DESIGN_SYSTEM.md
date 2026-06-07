# TrueOwn Design System & UI Specifications

**Date:** June 7, 2026  
**Version:** 1.0  
**Status:** Design Phase Complete

---

## Design Overview

TrueOwn's UI/UX is built on a **modular, investment-first design system** that supports two primary applications (BuyWise for home buyers, InvestWise for investors) while maintaining a unified, professional aesthetic suitable for both consumer and institutional users.

### Design Principles

1. **Clarity Over Cleverness** - Investment decisions require transparent data and reasoning
2. **Modular Components** - Reusable components across BuyWise and InvestWise
3. **Mobile-First** - Responsive design for property viewing on-site
4. **Data Visualization** - Charts, graphs, and visual comparisons drive insight
5. **Conversational AI** - Natural language integration throughout
6. **Institutional Grade** - Professional enough for fund managers and CPAs

---

## Color Palette

### Primary Colors
- **Primary Blue:** `#0066CC` (Action, primary buttons, links)
- **Dark Gray:** `#1F2937` (Text, headings)
- **Light Gray:** `#F3F4F6` (Backgrounds, cards)
- **Success Green:** `#10B981` (Positive indicators, recommendations)
- **Warning Orange:** `#F59E0B` (Caution, risks, alerts)
- **Error Red:** `#EF4444` (Errors, negative cash flow)

### Secondary Colors
- **Accent Blue:** `#3B82F6` (Highlights, secondary actions)
- **Neutral Gray:** `#6B7280` (Secondary text, muted)
- **Light Blue:** `#DBEAFE` (Background tints, disabled states)

### Application-Specific
- **BuyWise:** Primary Blue accent (for home buyer context)
- **InvestWise:** Accent Blue accent (for investor context)

---

## Typography

### Font Family
- **Primary:** Inter (weights: 400, 600, 700, 800, 900)
- **Monospace:** Courier New (for financial data, code)

### Type Scale

| Role | Size | Weight | Line Height | Usage |
|------|------|--------|-------------|-------|
| **H1 - Page Title** | 32px | 800 | 1.3 | Section headings |
| **H2 - Section Header** | 24px | 700 | 1.3 | Subsection titles |
| **H3 - Card Title** | 18px | 600 | 1.4 | Component titles |
| **Body Large** | 16px | 400 | 1.6 | Main content |
| **Body Regular** | 14px | 400 | 1.5 | Standard text |
| **Body Small** | 12px | 400 | 1.4 | Secondary text, muted |
| **Label** | 12px | 600 | 1.4 | Form labels, badges |
| **Monospace** | 13px | 400 | 1.5 | Financial figures, code |

---

## Component Library

### 1. Buttons

**Primary Button**
```
Background: #0066CC
Text: White
Padding: 12px 24px
Border Radius: 6px
Font Weight: 600
Hover: #0052A3 (darker)
```

**Secondary Button**
```
Background: Transparent
Border: 1px #0066CC
Text: #0066CC
Padding: 12px 24px
Hover: Light Blue background
```

**Tertiary Button**
```
Background: Transparent
Text: #0066CC
Padding: 8px 16px
Font Size: 14px
Hover: #DBEAFE background
```

**Disabled State**
```
Opacity: 0.5
Cursor: Not-allowed
```

---

### 2. Cards

**Standard Card**
```
Background: White
Border: 1px #E5E7EB
Border Radius: 8px
Padding: 20px
Box Shadow: 0 1px 3px rgba(0,0,0,0.1)
```

**Card with Badge**
```
Badge positioning: Top-right
Badge styles: 
  - Primary: Blue background, white text
  - Secondary: Gray background, dark text
  - Warning: Orange background, dark text
  - Success: Green background, white text
```

**Property Card (Specialized)**
```
Components:
  - Image placeholder (3:2 ratio)
  - Address and property type
  - Key metrics (beds, baths, sqft)
  - Investment score (if InvestWise)
  - CTA buttons (View Details, Add to Favorites, etc.)
```

---

### 3. Input Fields & Forms

**Text Input**
```
Border: 1px #D1D5DB
Border Radius: 6px
Padding: 10px 12px
Font Size: 14px
Focus: Border color #0066CC, box-shadow
Placeholder: #9CA3AF (gray)
```

**Select/Dropdown**
```
Same styling as text input
Arrow icon: Right-aligned
Option list: Dropdown below
```

**Number Input (Currency)**
```
Font: Monospace
Text Align: Right
Prefix/Suffix support
Currency symbol: Inline or separate
```

**Checkbox**
```
Size: 16x16px
Border: 1px #D1D5DB
Checked: Background #0066CC, checkmark icon
```

**Radio Button**
```
Size: 16x16px
Border: 2px #D1D5DB
Selected: Inner circle #0066CC
```

---

### 4. Tables

**Table Header**
```
Background: #F9FAFB
Font Weight: 600
Font Size: 12px
Color: #374151
Border Bottom: 1px #E5E7EB
Padding: 12px
```

**Table Row**
```
Padding: 12px
Border Bottom: 1px #E5E7EB
Hover: Background #F3F4F6
Alternate row: White (no alternating color)
```

**Table Data Cell**
```
Font Size: 14px
Color: #1F2937
Alignment: Left (text), Right (numbers)
Monospace: For financial figures
```

---

### 5. Badges & Tags

**Badge Styles**

| Style | Background | Text | Use Case |
|-------|-----------|------|----------|
| **Primary** | #DBEAFE | #0066CC | App/feature indicators |
| **Blue** | #DBEAFE | #0066CC | InvestWise specific |
| **Success** | #D1FAE5 | #047857 | Positive indicators |
| **Warning** | #FEF3C7 | #D97706 | Caution/alerts |
| **Gray** | #E5E7EB | #6B7280 | Neutral info |

**Badge Size:**
```
Padding: 4px 10px
Font Size: 12px
Border Radius: 4px
Font Weight: 600
```

---

### 6. Charts & Visualizations

**Chart Container**
```
Background: White
Border: 1px #E5E7EB
Border Radius: 8px
Padding: 16px
Aspect Ratio: Varies (bar: 4:3, line: 16:9)
```

**Chart Colors**
```
Primary Series: #0066CC
Secondary Series: #3B82F6
Accent: #F59E0B (highlights)
Neutral: #D1D5DB (reference lines)
```

**Common Charts:**
- **Bar Chart:** Monthly cash flow by property, expense breakdown
- **Line Chart:** Appreciation trend, rent growth over time
- **Pie Chart:** Portfolio allocation, asset class breakdown
- **Gauge Chart:** Investment Score (1-100), affordability (%)
- **Scatter:** Risk vs. return matrix

---

### 7. Modals & Dialogs

**Modal Container**
```
Background: White
Border Radius: 8px
Box Shadow: 0 20px 25px rgba(0,0,0,0.15)
Padding: 24px
Max Width: 600px (standard), 900px (large)
```

**Modal Header**
```
Title: H2 (24px, 700)
Close Button: Top-right (X icon)
Divider: 1px #E5E7EB below
```

**Modal Content**
```
Body text: 14px, line-height 1.5
Form fields: Standard input styles
Actions: Button group at bottom
```

---

### 8. Navigation

**Sidebar Navigation**
```
Background: White
Width: 260px (desktop), collapsible mobile
Border Right: 1px #E5E7EB
```

**Navigation Link**
```
Padding: 12px 16px
Font Size: 14px
Color: #6B7280 (inactive), #0066CC (active)
Background: #F3F4F6 (active)
Border Left: 3px #0066CC (active)
Icon: 16x16px, left-aligned
Hover: Background #F9FAFB
```

**Section Header**
```
Font Size: 12px
Font Weight: 600
Color: #9CA3AF
Padding: 12px 16px
Text Transform: Uppercase
Letter Spacing: 0.05em
```

---

### 9. Top Bar/Header

**Top Bar Container**
```
Background: White
Border Bottom: 1px #E5E7EB
Height: 64px
Padding: 0 24px
Display: Flex
Justify Content: Space-between
```

**Search Bar**
```
Background: #F3F4F6
Border Radius: 6px
Padding: 10px 12px
Width: 400px (flexible)
Icon: Search (left)
Placeholder: "Search address, market, portfolio, or ask AI..."
Focus: Border #0066CC
```

**User Profile Pill**
```
Display: Flex, gap 12px
Avatar: 32x32px, circular, initials
Text: Name (14px bold), role (12px gray)
Hover: Background #F3F4F6
```

---

### 10. Key Metric Display (KPI Card)

**Structure**
```
┌─────────────────────┐
│ Badge (optional)    │
├─────────────────────┤
│ KPI Value (large)   │
│ 84 or $612/mo       │
├─────────────────────┤
│ Description text    │
│ (14px, #6B7280)     │
└─────────────────────┘
```

**KPI Value Styling**
```
Font Size: 32px (primary metric), 24px (secondary)
Font Weight: 800
Color: #1F2937
Monospace: For financial figures
```

---

## Layout Patterns

### 1. Page Layout

**Standard Page**
```
┌────────────────────────────────────────┐
│ Sidebar    │ Top Bar                    │
├────────────┼────────────────────────────┤
│            │ Section Title              │
│ Nav Links  ├────────────────────────────┤
│            │ Content Area               │
│            │ (Grid of cards/tables)     │
│            │                            │
│            │                            │
└────────────┴────────────────────────────┘
```

**Content Grid**
```
Desktop: 1-4 columns (responsive)
  cols-1: Single column (full width)
  cols-2: Two equal columns
  cols-3: Three equal columns
  cols-4: Four equal columns

Tablet: Max 2 columns
Mobile: Single column (stacked)

Gap: 16px between columns
```

---

### 2. Property Detail Layout

```
┌─────────────────────────────────────────┐
│ Title + Badge                           │
├──────────────┬──────────────────────────┤
│ Image (3:2)  │ Score Card               │
│              │ Investment Score 84      │
├──────────────┼──────────────────────────┤
│ Address      │ Key Metrics Table        │
│ Beds, Baths  │ Price, Rent, CF, Cap    │
└──────────────┴──────────────────────────┘
├─────────────────────────────────────────┤
│ Risk & Opportunity Breakdown (4 cols)   │
├─────────────────────────────────────────┤
│ Cash Flow Analysis Chart                │
├─────────────────────────────────────────┤
│ Market Analysis & Comparables           │
└─────────────────────────────────────────┘
```

---

### 3. Dashboard Layout (Portfolio)

```
┌─────────────────────────────────────────┐
│ KPI Cards (4 cards: Properties, CF, Equity, Opp) │
├─────────────────────────────────────────┤
│ Properties Table (sortable, filterable) │
├─────────────────────────────────────────┤
│ Optimization Alerts (3 cards)           │
├─────────────────────────────────────────┤
│ Charts: Cash Flow Trend, Allocation     │
└─────────────────────────────────────────┘
```

---

## Responsive Design Breakpoints

```
Mobile: < 640px
Tablet: 640px - 1024px
Desktop: > 1024px

- Sidebar: Hidden on mobile (hamburger menu)
- Cards: Stack to 1 column on mobile
- Top bar: Simplified on mobile (no search)
- Tables: Horizontal scroll on mobile
- Modals: Full screen on mobile
```

---

## Interaction Patterns

### 1. Data Entry (Calculator)

**Input → Calculation → Display Flow**
```
User enters: Income, down payment, property price
↓
System calculates: Monthly payment, cash flow, metrics
↓
Display results in cards + chart
↓
User modifies inputs → Recalculate instantly (debounced)
```

### 2. Property Search & Filter

**Search Flow**
```
User enters address/location
↓
Real-time autocomplete with property suggestions
↓
User selects property
↓
System loads property details + analysis
↓
Display enriched property card with recommendation
```

### 3. Portfolio Navigation

**Portfolio Flow**
```
Dashboard KPI view (overview)
↓
Click property → Property detail view
↓
View optimization opportunities
↓
Implement change (rent increase, refinance scenario)
↓
Return to dashboard (updated)
```

### 4. AI Advisor Conversation

**Conversational Flow**
```
User asks question (text input)
↓
AI processes context (portfolio, persona, market)
↓
AI generates response with explanations
↓
Display answer with:
  - Main recommendation
  - Supporting data/charts
  - Assumptions disclosed
  - Links to detailed analysis
↓
User asks follow-up or requests more details
```

---

## Data Visualization Standards

### Investment Score Gauge

**Design:**
- Circular gauge (0-100)
- Color zones:
  - 80-100: Green (Excellent)
  - 60-79: Blue (Good)
  - 40-59: Yellow (Caution)
  - 20-39: Orange (Risk)
  - 0-19: Red (Avoid)
- Center text: Large score number

### Cash Flow Chart

**Design:**
- Bar or line chart
- X-axis: Months or years
- Y-axis: Dollar amount
- Positive cash flow: Green bars
- Negative cash flow: Red bars
- Tooltip on hover: Exact values

### Portfolio Allocation Pie

**Design:**
- Donut chart (preferred over pie)
- Segments: Asset classes or markets
- Colors: Blue shades or strategic colors
- Labels: Inside or legend
- Hover: Shows percentage and value

---

## Error & Success States

### Error Message
```
Background: #FEE2E2 (light red)
Border: 1px #FCA5A5
Icon: ⚠️ (warning)
Text: #DC2626 (dark red)
Padding: 12px
Border Radius: 6px
```

### Success Message
```
Background: #DCFCE7 (light green)
Border: 1px #86EFAC
Icon: ✓ (checkmark)
Text: #16A34A (dark green)
Padding: 12px
Border Radius: 6px
```

### Warning Alert
```
Background: #FFFBEB (light yellow)
Border: 1px #FCD34D
Icon: ⚠️ (warning)
Text: #B45309 (dark orange)
Padding: 12px
Border Radius: 6px
```

---

## Accessibility Standards

### WCAG 2.1 AA Compliance

1. **Color Contrast:**
   - Text vs. background: 4.5:1 minimum
   - Large text (18px+ or 14px+ bold): 3:1 minimum

2. **Focus States:**
   - All interactive elements: Visible focus outline
   - Focus color: #0066CC with 2px outline

3. **Keyboard Navigation:**
   - Tab order: Logical left-to-right, top-to-bottom
   - Skip links: For sidebar navigation on desktop
   - Enter/Space: Activates buttons

4. **Screen Reader Support:**
   - ARIA labels on icons
   - Form labels properly associated
   - Tables with proper headers
   - Alt text on images

5. **Font Sizing:**
   - Minimum 12px for body text
   - Responsive scaling (1.125x on larger screens)

---

## Component Interaction Examples

### Property Analysis Card

**States:**
1. **Empty State** - Before property is selected
2. **Loading State** - Fetching property data
3. **Loaded State** - Display full analysis
4. **Error State** - Property not found or API error

**Actions:**
- Click to expand detail view
- Save/favorite button (heart icon)
- Share button (generates shareable link)
- Export button (downloads PDF report)

### Cash Flow Calculator

**States:**
1. **Default** - Empty inputs with placeholders
2. **Focused** - User is entering data
3. **Calculating** - Briefly shows loading
4. **Calculated** - Results displayed
5. **Comparing** - Multiple scenarios shown

**Interactions:**
- Type in field → Debounced recalculation (500ms)
- Toggle expense categories (expand/collapse)
- Compare scenarios (side-by-side view)
- Save scenario for reference

---

## Mobile Design Considerations

### Responsive Adjustments

**Navigation**
```
Desktop: Sidebar (260px)
Tablet: Sidebar (collapsible)
Mobile: Hamburger menu + drawer
```

**Grid Layouts**
```
Desktop: 2-4 columns
Tablet: 2 columns
Mobile: 1 column (stacked)
```

**Modals**
```
Desktop: Centered, 600px wide
Tablet: Centered, 90vw wide
Mobile: Full screen, no backdrop
```

**Forms**
```
Desktop: Horizontal layout
Mobile: Vertical layout (100% width inputs)
```

**Tables**
```
Desktop: Horizontal scroll if needed
Tablet: Horizontal scroll
Mobile: Vertical cards (one property per card)
```

---

## Design System Files

### Figma/Design Assets
- Color palette components
- Typography styles
- Component library (buttons, cards, inputs, etc.)
- Page templates (home, property detail, portfolio, etc.)
- Mobile breakpoint layouts

### Implementation
- CSS variables for colors, typography, spacing
- SCSS mixins for responsive breakpoints
- Component React/Vue/Web Components
- Storybook for component documentation

---

## Future Design Enhancements

1. **Dark Mode** - High contrast mode for accessibility
2. **Animated Transitions** - Smooth page transitions, loading states
3. **Micro-interactions** - Button feedback, input validation
4. **Advanced Charts** - D3.js visualizations for complex data
5. **AR Features** - Phone camera integration for property viewing
6. **Voice Input** - Voice commands for queries ("Show me 3BR under $400K")

---

**Document Status:** Complete - Ready for Implementation  
**Next Step:** Development task breakdown and sprint planning
