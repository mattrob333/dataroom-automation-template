# Data Room Orchestrator Prompt

## Main Workflow Prompt

Copy and use this prompt to initiate the complete data room generation workflow:

---

**PROMPT:**

```
I need you to create a complete data room for {{COMPANY_NAME}} ({{COMPANY_URL}}).

Please follow this workflow:

## Phase 1: Research & Data Collection (30 minutes)

1. **Company Research Agent**
   - Search and analyze the company website
   - Extract: mission, products/services, team, history, news
   - Find: SEC filings, press releases, social media
   - Output: `research/company_profile.json`

2. **Market Research Agent**
   - Industry analysis and market size
   - Competitive landscape (identify 5-10 competitors)
   - Market trends and growth projections
   - Output: `research/market_analysis.json`

3. **Financial Research Agent**
   - Revenue data (if public)
   - Funding history
   - Financial news and analysis
   - Output: `research/financial_data.json`

4. **Technical Research Agent**
   - Technology stack
   - Product architecture
   - Technical capabilities
   - Output: `research/technical_profile.json`

## Phase 2: Document Generation (45 minutes)

Use the research outputs to generate these documents:

### Core Documents (Priority 1)
1. Executive Summary (2 pages)
2. Business Overview (5-7 pages)
3. Financial Model (Excel/spreadsheet format)
4. Market Analysis (8-10 pages)
5. Competitive Analysis (6-8 pages)

### Operational Documents (Priority 2)
6. Organization Chart
7. Management Bios
8. Product/Service Descriptions
9. Customer Analysis
10. Sales & Marketing Strategy

### Financial Documents (Priority 3)
11. Historical Financials
12. Financial Projections (3-5 years)
13. Cap Table
14. Use of Funds
15. Unit Economics

### Legal & Compliance (Priority 4)
16. Corporate Structure
17. IP Portfolio
18. Material Contracts
19. Regulatory Compliance
20. Risk Factors

### Technical Documents (Priority 5)
21. Technical Architecture
22. Product Roadmap
23. Technology Stack
24. Security & Infrastructure

## Phase 3: Quality Assurance (15 minutes)

1. Review all documents for consistency
2. Cross-reference data points
3. Ensure professional formatting
4. Validate calculations in financial models
5. Check for completeness

## Output Structure

```
dataroom/
├── 01_executive/
│   ├── executive_summary.pdf
│   └── company_overview.pdf
├── 02_business/
│   ├── business_model.pdf
│   ├── market_analysis.pdf
│   └── competitive_analysis.pdf
├── 03_financials/
│   ├── financial_model.xlsx
│   ├── historical_financials.pdf
│   └── projections.pdf
├── 04_legal/
│   ├── corporate_structure.pdf
│   ├── contracts.pdf
│   └── compliance.pdf
├── 05_technical/
│   ├── technical_architecture.pdf
│   └── product_roadmap.pdf
└── 06_supporting/
    ├── team_bios.pdf
    ├── customer_references.pdf
    └── press_coverage.pdf
```

## Execution Guidelines

1. **Use parallel processing**: Launch research agents simultaneously
2. **Validate data**: Cross-check facts across multiple sources
3. **Professional formatting**: Use clean, investor-grade templates
4. **Be thorough**: Better to have comprehensive documentation
5. **Flag gaps**: Note where information wasn't available

## Success Criteria

- [ ] All Priority 1 & 2 documents generated
- [ ] Financial model with formulas and projections
- [ ] At least 3 sources cited per major claim
- [ ] Professional PDF formatting
- [ ] Consistent branding and style
- [ ] No placeholder or dummy data

Begin the workflow and provide status updates at each phase.
```

---

## Variables to Replace

- `{{COMPANY_NAME}}`: The name of the target company
- `{{COMPANY_URL}}`: The company's website URL

## Usage Tips

1. **For public companies**: Add SEC Edgar API calls for official filings
2. **For private companies**: Rely more on news, Crunchbase, LinkedIn
3. **For technical companies**: Emphasize technical architecture and IP
4. **For consumer companies**: Focus on customer metrics and market size

## Estimated Time

- **Total**: 90-120 minutes
- **Research Phase**: 30 minutes
- **Generation Phase**: 45-60 minutes
- **QA Phase**: 15 minutes

## Next Steps After Generation

1. Review for accuracy
2. Add company-specific customizations
3. Update with real data where estimates were used
4. Have domain experts review their sections
5. Package for distribution
