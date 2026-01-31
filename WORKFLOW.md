# 🔄 Data Room Automation Workflow

This document outlines the complete methodology for automating data room document generation.

## Overview

The workflow uses a **multi-agent orchestration pattern** where specialized AI agents work together to research, analyze, and generate comprehensive data room documents.

## Architecture

### Agent Hierarchy

```
Main Orchestrator (Claude Code)
    ├── Research Agent (Web search, scraping, data extraction)
    ├── Analysis Agent (Financial, market, risk analysis)
    └── Document Generation Agent (Template population, formatting)
```

## Workflow Phases

### Phase 1: Initialization & Planning

**Input**: Company name or URL

**Steps**:
1. Parse input and extract company identifier
2. Create project directory structure
3. Initialize tracking system
4. Load templates and configurations

**Outputs**:
- Project folder structure
- Initialized task list
- Configuration loaded

---

### Phase 2: Research & Data Collection

**Research Agent Tasks**:

#### 2.1 Company Information Gathering
- **Web Search**: Company overview, history, funding
- **Website Scraping**: About page, team, products
- **Document Extraction**: Pitch decks, financials (if available)

#### 2.2 Market Research
- **Industry Analysis**: Market size, growth, trends
- **Competitive Landscape**: Key competitors, positioning
- **Market Dynamics**: Opportunities, threats

#### 2.3 Financial Research
- **Funding History**: Rounds, investors, amounts
- **Revenue Data**: Public information, estimates
- **Financial Metrics**: Burn rate, runway (if available)

#### 2.4 Team & Organization
- **Leadership Team**: Founders, executives
- **Advisory Board**: Advisors, board members
- **Team Size**: Employee count, growth

**Tools Used**:
- WebSearch - Market research and company info
- WebFetch - Website scraping
- Task tool with Explore agent - Deep codebase/document analysis

**Outputs**:
- research/company-overview.json
- research/market-data.json
- research/financial-data.json
- research/team-data.json

---

### Phase 3: Analysis & Insights

**Analysis Agent Tasks**:

#### 3.1 Financial Analysis
- Revenue projections
- Cost structure analysis
- Funding requirements
- Valuation estimates

#### 3.2 Market Analysis
- TAM/SAM/SOM calculation
- Competitive positioning
- Market entry strategy assessment
- Growth potential evaluation

#### 3.3 Risk Assessment
- Market risks
- Execution risks
- Financial risks
- Regulatory risks
- Technology risks

#### 3.4 SWOT Analysis
- Strengths identification
- Weaknesses assessment
- Opportunities mapping
- Threats evaluation

**Outputs**:
- analysis/financial-analysis.json
- analysis/market-analysis.json
- analysis/risk-assessment.json
- analysis/swot-analysis.json

---

### Phase 4: Document Generation

**Document Generation Agent Tasks**:

#### 4.1 Core Documents Generated

1. **Executive Summary** - High-level overview
2. **Company Overview** - Detailed company information
3. **Market Analysis** - Market size, trends, competition
4. **Financial Overview** - Revenue, funding, projections
5. **Risk Assessment** - Identified risks and mitigations
6. **Due Diligence Checklist** - Verification items
7. **Cap Table Analysis** - Ownership structure
8. **Product/Technology Overview** - Product details
9. **Team & Organization** - Leadership and structure
10. **Legal & Compliance** - Legal status and compliance

#### 4.2 Quality Assurance
- Consistency check across documents
- Fact verification
- Format standardization
- Citation validation

**Outputs**:
- dataroom/01-executive-summary.md
- dataroom/02-company-overview.md
- dataroom/03-market-analysis.md
- ... (all documents)
- dataroom/INDEX.md

---

### Phase 5: Packaging & Delivery

#### 5.1 Organization
- Create logical folder structure
- Generate master index
- Create table of contents for each document
- Add cross-references

#### 5.2 Final Review
- Spell check
- Grammar review
- Link validation
- Source verification

---

## Implementation Pattern

### Using Claude Code

```
Step 1: User provides company name/URL
Step 2: Claude creates project structure
Step 3: Research agent gathers information
Step 4: Analysis agent processes data
Step 5: Generation agent creates documents
Step 6: Claude reviews and delivers
```

### Task Tool Usage

Claude Code uses the Task tool to launch specialized agents:

- **Explore agent**: For deep research and information gathering
- **General-purpose agent**: For complex multi-step tasks
- **Main Claude**: Orchestrates everything and does final generation

### Data Flow

```
Input (Company Name/URL)
    ↓
[Research Phase] → Raw data → research/
    ↓
[Analysis Phase] → Insights → analysis/
    ↓
[Generation Phase] → Documents → dataroom/
    ↓
Output (Complete Data Room)
```

---

## Customization Points

### 1. Document Selection
Choose which documents to generate based on your needs

### 2. Research Depth
Adjust how deep the research goes

### 3. Analysis Focus
Emphasize specific aspects (financial, market, risk)

### 4. Template Customization
Edit templates to match your standards

### 5. Output Format
Choose Markdown, PDF, or other formats

---

## Best Practices

1. **Always validate sources** - Ensure data accuracy
2. **Cite everything** - Track data sources
3. **Maintain consistency** - Use same terminology across docs
4. **Be transparent** - Note assumptions and limitations
5. **Focus on insights** - Don't just compile data, analyze it
6. **Professional formatting** - Clean, readable output

---

**This workflow is designed to be flexible and adaptable. Modify it to fit your specific needs!**
