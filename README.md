# AI-Liability-Insurance-Case
# Quantify 2026 Case Competition: Brand New Market — AI Liability Insurance

**Team:** 2ronto  
**Delegates:** Adit Kashyap & Advaith Gopaljee  
**Target Entity:** TileShield Insurance (TSI) Board of Directors  
**Partner Organizations:** Canadian Institute of Actuaries (CIA) & ASNA  

---

## Executive Summary

TileShield Insurance (TSI), a mid-sized Canadian P&C insurer headquartered in Toronto (~1% national market share, $834.2M 2025 earned premium), is evaluating entry into the nascent artificial intelligence liability market. TSI's tech-heavy SME client base is experiencing rapid operational disruption from AI tools while simultaneously adopting generative AI in client workflows—introducing novel operational, legal, and financial liabilities not contemplated by standard legacy commercial forms.

This repository contains the end-to-end actuarial diagnostics, insurability segmentation, product architecture, and 10-slide board presentation evaluating whether and how TSI should enter this market. 

**Strategic Recommendation:** Execute **Option B (AI-Specific Policy Endorsements)** attached to TSI's existing Errors & Omissions (E&O), Cyber Liability, and Commercial General Liability (CGL) policies, while rejecting an un-sublimited Standalone product (Option A) and avoiding the client churn of delaying entry (Option C).

---

## Key Actuarial & Data Insights

### 1. Portfolio Readiness & Volatility Analysis (Exhibit A)
* **Capital Buffer in Core Lines:** TSI's balance sheet is supported by highly stable, profitable anchor lines:
  * **Commercial General Liability (CGL):** $1.04B 5-year earned premium at a **77.13% 5-year combined ratio** ($\sigma_{\text{CR}} = 0.38\%$).
  * **Errors & Omissions (E&O):** $437.66M 5-year earned premium at an **85.90% 5-year combined ratio** ($\sigma_{\text{CR}} = 3.02\%$), maintaining steady ~14% underwriting profit margins.
* **Specialty Anchor Fit:** E&O exhibits ultra-low parameter variance in both claim frequency ($\bar{f} = 0.1191$, $\sigma_f = 0.0030$) and average severity ($\bar{s} = \$96.8\text{k}$, $\sigma_s = \$5.4\text{k}$), establishing it as the ideal actuarial vehicle to host new add-on endorsements.
* **Cyber Line Warning (The Standalone Deterrent):** Cyber Liability experienced severe underwriting margin deterioration, reaching a **97.64% combined ratio in 2025** driven by an 82.2% surge in average claim severity ($\$164.4\text{k} \rightarrow \$299.6\text{k}$). This margin sensitivity cautions against launching an open-ended, un-sublimited standalone line (Option A).

### 2. AI Incident Anatomy & Insurability Diagnostics (Exhibit B)
Analysis of the 135 external AI incident dataset ($446.1M total insured losses) indicates that AI liability is **partially insurable** through strict peril partitioning:
* **Insurable Segment (High-Frequency / Bounded Severity):** 
  * *Hallucinated Output* (36 claims, 26.7% share, mean severity $\$151.8\text{k}$, maximum $\$289.0\text{k}$).
  * *Misinformation* (19 claims, 14.1% share, mean severity $\$585.3\text{k}$, maximum $\$1.19\text{M}$).
  * *Algorithmic Bias* (26 claims, 19.3% share, mean severity $\$2.79\text{M}$).
* **Uninsurable Tail Risk (Must Exclude):**
  * *Autonomous System Failures* accounted for only 9 claims (6.7% count) but generated **$179.1M (40.1% of all losses)**, with a mean severity of **$19.90M per event** (maximum $\$31.17\text{M}$). A single physical autonomous failure would impair multi-year line earnings for a carrier of TSI's scale.
* **Human-in-the-Loop (HITL) Severity Compression:**
  * Incidents with documented human oversight averaged **$\$2.40\text{M}$** vs. **$\$4.23\text{M}$** for unmonitored systems—a statistically significant **43.3% severity reduction** ($\Delta = \$1.83\text{M}$ per claim).

---

## Option B: Product Design & Governance Architecture

* **E&O Endorsement Rider:** Covers legal defense costs and financial liabilities arising from generative AI hallucinations, professional service advisory errors, and algorithmic bias in software delivery.
  * **Sub-limit:** Capped at **$\$250,000\text{--}\$500,000$** per policy year (defense costs eroding inside the limit).
* **Cyber Endorsement Rider:** Covers direct financial losses from AI-synthesized deepfake executive impersonation, prompt injection exploits, and unauthorized funds transfer fraud.
  * **Sub-limit:** **$\$500,000$** aggregate annual cap.
* **Contractual Verifiability & Loss Sharing:**
  * Replaces subjective oversight definitions with immutable system/API logs (e.g., GitHub PR approvals, CMS publish sign-offs).
  * Enforces a tiered coinsurance/retention schedule: verified HITL workflows qualify for a standard $\$5,000$ deductible (90/10 coverage), while automated/batch pipelines carry a $\$25,000$ deductible and 50% coinsurance.
* **Explicit Policy Carve-Outs:** Absolute exclusions for physical autonomous machinery/vehicles, intentional civil rights violations, and upstream foundation model hyperscaler cloud outages.
* **Capital Ring-Fencing:** 50% quota-share reinsurance treaty structure paired with standardized affirmative exclusions attached to base policies declining the rider (eliminating "Silent AI" ambiguity).

---

## Repository Structure

```plaintext
├── data/
│   ├── Exhibits 2026 Quantify Case Study.xlsx  # Raw financial, incident, and market data
│   └── 2026 Quantify Case Study.pdf           # Full case mandate and instructions
├── presentations/
│   ├── 2ronto Quantify Case Comp.pptx         # Finalized 10-slide competition deck
│   └── Team2ronto_Submission.pdf              # Round 1 PDF deliverable
├── scripts/
│   ├── financial_diagnostics.py               # 5-year Loss, Expense, and Combined Ratio models
│   ├── actuarial_stability.py                 # Variance, standard deviation, and parameter stability models
│   └── incident_segmentation.py               # Exhibit B frequency-severity & HITL cross-tabulations
└── README.md
