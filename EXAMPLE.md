# Example: Data Room Generation

This is a quick example of how to use the data room automation workflow.

## Simple Example

**User says:**
```
Generate a data room for Stripe
```

**Claude does:**
1. Creates project folder: `dataroom-stripe/`
2. Researches Stripe (web search, website scraping)
3. Analyzes the data (financial, market, risk)
4. Generates all documents
5. Presents complete data room

## What Gets Generated

```
dataroom-stripe/
├── research/
│   ├── company-overview.md
│   ├── market-data.md
│   ├── financial-data.md
│   └── team-data.md
├── analysis/
│   ├── financial-analysis.md
│   ├── market-analysis.md
│   └── risk-assessment.md
└── dataroom/
    ├── INDEX.md
    ├── 01-executive-summary.md
    ├── 02-company-overview.md
    ├── 03-market-analysis.md
    ├── 04-financial-overview.md
    ├── 05-risk-assessment.md
    ├── 06-due-diligence-checklist.md
    ├── 07-cap-table-analysis.md
    ├── 08-product-tech-overview.md
    ├── 09-team-org-structure.md
    └── 10-legal-compliance.md
```

## Custom Example

**User says:**
```
Generate a data room for Acme Corp (acmecorp.com). They're a Series A B2B SaaS 
startup that raised $10M last year. Focus on financial projections and competitive 
analysis.
```

**Claude does:**
Same process but with:
- Extra emphasis on financial projections
- Deep dive into competitive landscape
- Tailored analysis based on Series A stage
- B2B SaaS specific metrics

## Advanced Example

**User says:**
```
Create data rooms for three competitors: Stripe, Square, and Adyen. 
I need to compare their market positions.
```

**Claude does:**
1. Generates complete data room for each company
2. Creates comparison documents
3. Highlights key differentiators
4. Provides competitive matrix

## Iteration Example

**Initial request:**
```
Generate a data room for Notion
```

**Follow-up:**
```
The market analysis looks good, but can you add more detail on how Notion 
compares to Microsoft Loop and Coda?
```

**Claude:**
Updates the market analysis document with expanded competitive analysis.

## Tips

1. **Be specific**: More context = better results
2. **Iterate**: Ask for refinements
3. **Customize**: Request focus areas
4. **Verify**: Always check key facts
5. **Export**: Save the generated documents

## Next Steps

Ready to try it? Just say:
```
Generate a data room for [Your Company]
```
