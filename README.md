# Sigvotatug Vedotin + Pembrolizumab: Be6A Lung-02 Outcome Prediction

## Description:
This repository predicts the Phase III results of sigvotatug vedotin + pembrolizumab vs.pembrolizumab alone in first-line, locally advanced/metastatic NSCLC with PD-L1 TPS ≥50%(Be6A Lung-02, NCT06758401), using a three-agent LLM pipeline for structured retrieval,scoring, and prediction.

## Key Findings:
- **Primary endpoints predicted:** PFS and OS, per Be6A Lung-02's trial design (published in *Future Oncology*).
- **Prediction:** PFS [XX%–XX%] / OS [XX%–XX%]
- **Limitation:** No backtest validation was performed. This framework should be read as a structured reasoning aid, not a validated predictive model.

## How it work:
This framework comprised of 3 agents. 
- **Master Agent** - orchestrates the pipeline and performs quality control across the other two agents' outputs.
- **Parser Agent** - retrieves available data and structures it into scored factors. 
- **Factor Agent** - scores the structured factors and make predictions.

## Repository Structure:
- `schemas/` — Parser Agent output schema (JSON)
- `outputs/` — final structured outputs from each agent, final compiled report

## How to Product:
1. run Parser Agent
2. run Factor Generator Agent
3. run Master Agent
