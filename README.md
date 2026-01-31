# 🏢 Data Room Automation Template

**Transform a company URL into a complete data room in minutes using AI**

This repository contains a complete workflow template for automatically generating comprehensive data room documents using Claude Code and AI agents.

## 🎯 What This Does

Given just a **company URL or name**, this workflow will:
- Research the company comprehensively
- Generate 20+ professional data room documents
- Create financial models and projections
- Perform competitive analysis
- Build risk assessments
- Generate legal and compliance documentation

## 📋 Quick Start

### Prerequisites
- Claude Code or Claude API access
- Web search capability (for company research)
- Optional: Access to company databases, financial APIs

### Usage

1. **Clone this repository**
   ```bash
   git clone https://github.com/mattrob333/dataroom-automation-template.git
   cd dataroom-automation-template
   ```

2. **Run the workflow**
   
   In Claude Code, use the main orchestrator prompt:
   ```
   I need you to create a complete data room for [COMPANY_NAME] at [COMPANY_URL]. 
   Follow the workflow in ORCHESTRATOR_PROMPT.md
   ```

3. **Review and customize**
   - Documents are generated in `output/` directory
   - Review and edit as needed
   - Templates are in `templates/` directory

## 📂 Repository Structure

```
dataroom-automation-template/
├── README.md                          # This file
├── ORCHESTRATOR_PROMPT.md            # Main workflow orchestration prompt
├── WORKFLOW_GUIDE.md                 # Detailed workflow explanation
├── agents/                           # Sub-agent configurations
│   ├── research_agent.md
│   ├── financial_agent.md
│   ├── legal_agent.md
│   └── technical_agent.md
├── templates/                        # Document templates
│   ├── executive_summary.md
│   ├── business_overview.md
│   ├── financial_model.md
│   ├── market_analysis.md
│   ├── technical_assessment.md
│   ├── legal_documents.md
│   └── ... (20+ templates)
├── prompts/                          # Specialized prompts
│   ├── research_prompts.md
│   ├── analysis_prompts.md
│   └── generation_prompts.md
├── tools/                            # Tool configurations
│   ├── web_search_config.md
│   ├── data_extraction_config.md
│   └── document_generation_config.md
└── examples/                         # Example outputs
    └── sample_dataroom/
```

## 🔧 Customization

### Modify Templates
Edit files in `templates/` to customize document formats and sections.

### Adjust Workflow
Modify `ORCHESTRATOR_PROMPT.md` to change the workflow steps or add/remove documents.

### Configure Agents
Update agent prompts in `agents/` to change research depth or analysis style.

## 📚 Documentation

- **[ORCHESTRATOR_PROMPT.md](ORCHESTRATOR_PROMPT.md)** - Main workflow prompt
- **[WORKFLOW_GUIDE.md](WORKFLOW_GUIDE.md)** - Detailed step-by-step guide
- **[agents/](agents/)** - Sub-agent documentation
- **[templates/](templates/)** - Document templates

## 🚀 Features

- ✅ Fully automated company research
- ✅ 20+ professional document templates
- ✅ Financial modeling and projections
- ✅ Competitive analysis
- ✅ Risk assessment
- ✅ Legal and compliance documentation
- ✅ Customizable templates
- ✅ Parallel processing with sub-agents
- ✅ Quality validation

## 🤝 Contributing

Feel free to submit issues or pull requests to improve this template!

## 📄 License

MIT License - feel free to use and modify for your needs.

## 🙏 Credits

Created with Claude Code and Anthropic's AI capabilities.