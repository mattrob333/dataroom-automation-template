# Data Room Generation Workflow Guide

## Overview

This guide provides a detailed walkthrough of the data room generation process, including agent orchestration, tool usage, and quality assurance.

## Workflow Architecture

### Phase 1: Research & Data Collection

#### 1.1 Company Research Agent

**Purpose**: Gather comprehensive company information

**Tools Required**:
- Web search
- Web scraping/fetching
- Data extraction

**Prompt Template**:
```
You are a Company Research Agent. Your task is to gather comprehensive information about {{COMPANY_NAME}}.

Research Areas:
1. Company Overview
   - Mission and vision
   - Founded date and history
   - Headquarters location
   - Number of employees

2. Products & Services
   - Core offerings
   - Product lines
   - Service descriptions
   - Pricing models (if available)

3. Leadership Team
   - CEO and founders
   - Executive team
   - Board members
   - Key advisors

4. Company News
   - Recent announcements
   - Press releases
   - Media coverage
   - Significant milestones

5. Online Presence
   - Website analysis
   - Social media presence
   - Customer reviews
   - Industry reputation

Output Format: Structured JSON with all findings, including source URLs for verification.
```

**Expected Output**: `research/company_profile.json`

#### 1.2 Market Research Agent

**Purpose**: Analyze market opportunity and competitive landscape

**Prompt Template**:
```
You are a Market Research Agent analyzing the market for {{COMPANY_NAME}} in the {{INDUSTRY}} industry.

Research Areas:
1. Industry Analysis
   - Total Addressable Market (TAM)
   - Serviceable Addressable Market (SAM)
   - Serviceable Obtainable Market (SOM)
   - Market growth rate (CAGR)

2. Market Trends
   - Industry trends
   - Technology trends
   - Consumer behavior shifts
   - Regulatory changes

3. Competitive Landscape
   - Direct competitors (5-10)
   - Indirect competitors
   - Competitive positioning
   - Market share estimates

4. Market Dynamics
   - Key success factors
   - Barriers to entry
   - Buyer power
   - Supplier power

Output Format: Structured analysis with data sources and confidence levels.
```

**Expected Output**: `research/market_analysis.json`

#### 1.3 Financial Research Agent

**Purpose**: Gather financial data and funding history

**Prompt Template**:
```
You are a Financial Research Agent collecting financial information for {{COMPANY_NAME}}.

Research Areas:
1. Financial Data (if available)
   - Revenue (historical and current)
   - Growth rates
   - Profitability metrics
   - Unit economics

2. Funding History
   - Funding rounds
   - Investors
   - Valuations
   - Total capital raised

3. Financial News
   - Recent financial announcements
   - Analyst reports
   - Financial performance trends

4. Financial Benchmarks
   - Industry multiples
   - Comparable company metrics
   - Valuation benchmarks

Output Format: Financial data with sources and date stamps.
```

**Expected Output**: `research/financial_data.json`

#### 1.4 Technical Research Agent

**Purpose**: Analyze technical capabilities and infrastructure

**Prompt Template**:
```
You are a Technical Research Agent assessing {{COMPANY_NAME}}'s technology.

Research Areas:
1. Technology Stack
   - Programming languages
   - Frameworks and libraries
   - Infrastructure (cloud, on-prem)
   - Databases and data stores

2. Product Architecture
   - System design
   - Scalability approach
   - Integration capabilities
   - API architecture

3. Technical Capabilities
   - Engineering team size
   - Development practices
   - Technical innovations
   - Patents and IP

4. Security & Compliance
   - Security certifications
   - Compliance standards
   - Data privacy measures
   - Infrastructure security

Output Format: Technical profile with confidence ratings.
```

**Expected Output**: `research/technical_profile.json`

---

### Phase 2: Document Generation

#### 2.1 Executive Summary Generation

**Input**: All research outputs
**Template**: `templates/executive_summary.md`
**Output**: `dataroom/01_executive/executive_summary.pdf`

**Generation Prompt**:
```
Using the research data, create a 2-page Executive Summary that includes:

1. Company Snapshot (1 paragraph)
2. Business Model (1 paragraph)
3. Market Opportunity (1 paragraph)
4. Competitive Advantages (bullet points)
5. Financial Highlights (table or bullets)
6. Investment Highlights (3-5 key points)
7. Use of Funds (if applicable)

Style: Professional, investor-focused, fact-based
Tone: Confident but not promotional
Length: 2 pages maximum
```

#### 2.2 Business Overview Generation

**Input**: Company research, market research
**Template**: `templates/business_overview.md`
**Output**: `dataroom/02_business/business_overview.pdf`

**Generation Prompt**:
```
Create a comprehensive 5-7 page Business Overview including:

1. Company History
2. Mission & Vision
3. Products & Services
4. Business Model
5. Go-to-Market Strategy
6. Customer Segments
7. Revenue Streams
8. Key Partnerships
9. Operational Model

Include charts, diagrams, and visual elements where appropriate.
```

#### 2.3 Financial Model Generation

**Input**: Financial research, market projections
**Template**: `templates/financial_model.xlsx`
**Output**: `dataroom/03_financials/financial_model.xlsx`

**Generation Prompt**:
```
Build a comprehensive 5-year financial model with:

Sheets:
1. Summary Dashboard
2. Revenue Model
3. Cost Structure
4. P&L Statement
5. Cash Flow
6. Balance Sheet
7. Key Metrics
8. Assumptions

Include:
- Monthly breakdown (Year 1-2)
- Quarterly (Year 3-5)
- Sensitivity analysis
- Scenario planning (base, best, worst)
- Key ratio calculations
- Charts and visualizations

All formulas must be functional and linked.
```

#### 2.4 Market Analysis Generation

**Input**: Market research
**Template**: `templates/market_analysis.md`
**Output**: `dataroom/02_business/market_analysis.pdf`

**Generation Prompt**:
```
Create an 8-10 page Market Analysis covering:

1. Industry Overview
2. Market Size & Growth
3. Market Segmentation
4. Target Customer Profile
5. Market Trends
6. Competitive Analysis
7. Competitive Positioning
8. Market Entry Strategy
9. Market Risks & Opportunities

Include visual elements: charts, graphs, competitive matrices.
```

---

### Phase 3: Quality Assurance

#### QA Checklist

**Data Validation**:
- [ ] All claims have sources cited
- [ ] Financial calculations are accurate
- [ ] Dates are consistent across documents
- [ ] Company facts are verified
- [ ] Competitor information is current

**Formatting**:
- [ ] Professional PDF formatting
- [ ] Consistent fonts and styles
- [ ] Page numbers on all documents
- [ ] Headers/footers with document titles
- [ ] Table of contents where appropriate

**Completeness**:
- [ ] All Priority 1 documents generated
- [ ] All Priority 2 documents generated
- [ ] No "TODO" or placeholder text
- [ ] No missing sections
- [ ] All tables and charts complete

**Consistency**:
- [ ] Consistent company description
- [ ] Consistent financial figures
- [ ] Consistent terminology
- [ ] Consistent branding/colors
- [ ] Cross-references are accurate

#### Quality Assurance Prompt

```
Review all generated data room documents for:

1. Accuracy: Verify all facts and figures
2. Consistency: Ensure data matches across documents
3. Completeness: Check for missing sections
4. Professional Quality: Assess formatting and presentation
5. Investor-Readiness: Evaluate from investor perspective

Provide:
- List of issues found
- Severity rating (Critical, High, Medium, Low)
- Recommended fixes
- Overall readiness score (1-10)
```

---

## Agent Coordination

### Parallel Processing Strategy

```
Phase 1 (Parallel):
├── Company Research Agent → 30 min
├── Market Research Agent → 30 min
├── Financial Research Agent → 30 min
└── Technical Research Agent → 30 min

Phase 2 (Sequential by Priority):
Priority 1: Core Documents (Parallel)
├── Executive Summary
├── Business Overview
├── Financial Model
├── Market Analysis
└── Competitive Analysis

Priority 2: Operational Documents (Parallel)
├── Organization Chart
├── Management Bios
├── Product Descriptions
└── Customer Analysis

Priority 3: Financial Documents (Parallel)
├── Historical Financials
├── Financial Projections
├── Cap Table
└── Unit Economics

Phase 3 (Sequential):
├── Document Review
├── Cross-Reference Check
├── Format Standardization
└── Final QA
```

---

## Tool Configurations

### Web Search Configuration

**Recommended Settings**:
- Search depth: Comprehensive
- Source diversity: High
- Date range: Last 2 years (prioritize recent)
- Source types: News, official websites, financial databases

### Web Fetch Configuration

**Settings**:
- User agent: Standard browser
- JavaScript rendering: Enabled
- Timeout: 30 seconds
- Retry: 3 attempts

### Data Extraction Configuration

**Settings**:
- Output format: Structured JSON
- Validation: Enabled
- Source tracking: Required
- Confidence scoring: Enabled

---

## Customization Guide

### Adding New Documents

1. Create template in `templates/`
2. Add generation prompt in `prompts/`
3. Update orchestrator prompt
4. Add to QA checklist

### Modifying Existing Templates

1. Edit template file
2. Update generation prompts
3. Test generation
4. Update documentation

### Changing Workflow Order

1. Update `ORCHESTRATOR_PROMPT.md`
2. Adjust agent dependencies
3. Update time estimates
4. Test full workflow

---

## Troubleshooting

### Common Issues

**Issue**: Research agents return incomplete data
**Solution**: Increase search depth, add more sources, use alternative search queries

**Issue**: Financial model formulas broken
**Solution**: Regenerate from template, validate cell references

**Issue**: Inconsistent data across documents
**Solution**: Run consistency check, update master data source, regenerate affected docs

**Issue**: Poor document formatting
**Solution**: Re-apply templates, check PDF generation settings

---

## Best Practices

1. **Always validate sources**: Don't rely on single source for critical claims
2. **Use confidence ratings**: Mark data as verified, estimated, or assumed
3. **Keep templates updated**: Regular review and improvement
4. **Document assumptions**: Clearly state where estimates are used
5. **Version control**: Track changes to generated documents
6. **Backup research data**: Save all research outputs for future reference

---

## Success Metrics

- **Completeness**: 95%+ of required documents generated
- **Accuracy**: <5% error rate in factual claims
- **Timeliness**: 90-120 minutes total generation time
- **Quality**: Professional, investor-ready output
- **Consistency**: 100% data consistency across documents
