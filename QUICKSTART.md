# 🚀 Quick Start Guide

## Get Your Data Room in 3 Steps

This guide will help you generate a complete data room in under 2 hours.

---

## Step 1: Prepare Your Input

You only need **two pieces of information**:

1. **Company Name**: e.g., "Acme Corp"
2. **Company URL**: e.g., "https://acme.com"

---

## Step 2: Copy the Prompt

Open Claude Code and paste this prompt (replace the placeholders):

```
I need you to create a complete data room for [COMPANY_NAME] at [COMPANY_URL].

Please follow this workflow:

## Phase 1: Research & Data Collection (30 minutes)

Launch 4 parallel research agents:

1. **Company Research Agent**
   - Analyze company website, extract mission/products/team
   - Find SEC filings, press releases, social media
   - Save to: research/company_profile.json

2. **Market Research Agent**
   - Industry analysis, market size (TAM/SAM/SOM)
   - Identify 5-10 competitors
   - Market trends and growth projections
   - Save to: research/market_analysis.json

3. **Financial Research Agent**
   - Revenue data, funding history
   - Financial news and analysis
   - Unit economics estimates
   - Save to: research/financial_data.json

4. **Technical Research Agent**
   - Technology stack identification
   - Product architecture analysis
   - Technical capabilities assessment
   - Save to: research/technical_profile.json

## Phase 2: Document Generation (45 minutes)

Using the research outputs, generate these documents:

### Priority 1: Core Documents
1. Executive Summary (2 pages)
2. Business Overview (5-7 pages)
3. Financial Model (Excel format with formulas)
4. Market Analysis (8-10 pages)
5. Competitive Analysis (6-8 pages)

### Priority 2: Operational Documents
6. Organization Chart
7. Management Bios
8. Product/Service Descriptions
9. Customer Analysis
10. Sales & Marketing Strategy

### Priority 3: Financial Documents
11. Historical Financials
12. Financial Projections (3-5 years)
13. Cap Table
14. Use of Funds
15. Unit Economics

### Priority 4: Legal & Compliance
16. Corporate Structure
17. IP Portfolio
18. Material Contracts
19. Regulatory Compliance
20. Risk Factors

### Priority 5: Technical Documents
21. Technical Architecture
22. Product Roadmap
23. Technology Stack
24. Security & Infrastructure

## Phase 3: Quality Assurance (15 minutes)

1. Review all documents for consistency
2. Cross-reference data points
3. Ensure professional formatting
4. Validate financial calculations
5. Check completeness

## Output Structure

Organize files as:

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

## Guidelines

- Use parallel processing for research agents
- Validate data with multiple sources (minimum 3)
- Use professional, investor-grade formatting
- Flag any information gaps
- Cite all sources

## Success Criteria

- [ ] All Priority 1 & 2 documents generated
- [ ] Financial model with working formulas
- [ ] Minimum 3 sources per major claim
- [ ] Professional PDF formatting
- [ ] Consistent branding
- [ ] No placeholder data

Provide status updates at the end of each phase.
```

---

## Step 3: Let Claude Work

Claude will:
1. ✅ Launch research agents in parallel
2. ✅ Gather comprehensive company data
3. ✅ Generate all documents
4. ✅ Perform quality checks
5. ✅ Package everything in organized folders

**Estimated Time: 90-120 minutes**

---

## Example Usage

### For a Tech Startup

```
I need you to create a complete data room for Stripe at https://stripe.com.
[Follow the workflow above...]
```

### For a Public Company

```
I need you to create a complete data room for Shopify at https://shopify.com.
[Follow the workflow above...]

Note: For public companies, prioritize SEC filings and official financial reports.
```

### For a Private Company

```
I need you to create a complete data room for Notion at https://notion.so.
[Follow the workflow above...]

Note: For private companies, focus on news articles, Crunchbase, and LinkedIn data.
```

---

## Tips for Best Results

### 🎯 Research Phase
- Be patient during research - comprehensive data collection is key
- Claude will search multiple sources automatically
- Review the research JSONs before document generation

### 📝 Generation Phase
- Documents use templates from this repo
- Financial models will have working Excel formulas
- All charts and tables will be properly formatted

### ✅ Quality Assurance
- Review generated documents for accuracy
- Update any estimates with actual data if available
- Customize branding and formatting as needed

---

## Customization Options

### Add More Documents
Edit the prompt to include additional documents:
```
Also generate:
- Customer Case Studies
- Product Demo Script
- Investor FAQ
```

### Change Priorities
Reorder the priority levels based on your needs:
```
Generate in this order:
1. Financial Documents (Priority 1)
2. Executive Summary (Priority 2)
...
```

### Adjust Detail Level
Specify the depth you need:
```
For the Financial Model:
- Include detailed cohort analysis
- Add sensitivity tables for key variables
- Create scenario comparisons (best/base/worst)
```

---

## Troubleshooting

### Issue: Research taking too long
**Solution**: Claude is being thorough. You can ask for a progress update:
```
What's the status of the research phase?
```

### Issue: Missing information for private company
**Solution**: This is normal. Claude will:
- Note gaps in the documents
- Provide estimates with confidence levels
- Suggest where to find missing data

### Issue: Need to regenerate a document
**Solution**: Ask Claude to recreate specific documents:
```
Please regenerate the Market Analysis with more competitor detail.
```

---

## What You'll Get

### 📊 Research Data
- 4 comprehensive JSON files with all company intelligence
- Source URLs for every claim
- Confidence ratings on estimates

### 📄 Documents
- 20+ professional PDF documents
- 1 Excel financial model with formulas
- Organized folder structure
- Investor-ready formatting

### ⚡ Time Saved
- Manual research: 20+ hours
- Document creation: 10+ hours
- Formatting & QA: 5+ hours
- **Total saved: 35+ hours** ⏰

---

## Next Steps

1. ✅ Generate your data room using the prompt above
2. 📝 Review and customize the output
3. 🎨 Add your branding (logo, colors)
4. 🔒 Set up secure sharing (data room platform)
5. 📤 Distribute to investors/stakeholders

---

## Support

For issues or questions:
- Check [WORKFLOW_GUIDE.md](WORKFLOW_GUIDE.md) for detailed documentation
- Review [agents/](agents/) for agent-specific guidance
- Modify [templates/](templates/) to customize output

---

## Pro Tips 💡

1. **Run during off-hours**: Let Claude research overnight
2. **Start with Priority 1**: Get core docs first, then expand
3. **Use for multiple companies**: Template works for any company
4. **Keep research data**: Reuse for future updates
5. **Automate updates**: Re-run quarterly for fresh data

---

**Ready to build your data room? Copy the prompt above and get started!** 🚀