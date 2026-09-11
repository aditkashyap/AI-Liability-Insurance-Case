# Quantify 2026 Case Competition: Brand New Market — AI Liability Insurance

**Team:** 2ronto  
**Delegates:** Adit Kashyap & Advaith Gopaljee  
**Target Entity:** TileShield Insurance (TSI) Board of Directors  
**Partner Organizations:** Canadian Institute of Actuaries (CIA) & ASNA  

---

## Executive Summary

TileShield Insurance (TSI), a mid-sized Canadian P&C insurer headquartered in Toronto (~1% national market share, $834.2M 2025 earned premium), is evaluating market entry into artificial intelligence liability. TSI's SME client base is experiencing rapid disruption from commercial AI tools while deploying generative AI across professional workflows, introducing operational and legal exposures not contemplated by legacy commercial forms.

This repository contains the end-to-end actuarial models, insurability segmentation, product architecture, and 10-slide board presentation evaluating TSI's market entry.

**Strategic Recommendation:** Execute **Option B (AI-Specific Policy Endorsements)** attached to existing Errors & Omissions (E&O), Cyber Liability, and Commercial General Liability (CGL) policies. This strategy captures early-mover advantage while avoiding the un-sublimited catastrophic tail risks of a standalone product (Option A) and preventing the client churn associated with delaying entry (Option C).

---

## Key Actuarial & Data Insights

### 1. Portfolio Readiness & Volatility Analysis (Exhibit A)
* **Capital Buffers in Core Lines:** TSI's balance sheet is supported by established, highly profitable anchor books:
  * **Commercial General Liability (CGL):** Generated $1.04B in 5-year earned premium at a steady 77.13% combined ratio, exhibiting negligible year-over-year volatility (standard deviation of 0.38%).
  * **Errors & Omissions (E&O):** Produced $437.66M in 5-year earned premium at an 85.90% combined ratio (standard deviation of 3.02%), consistently yielding ~14% underwriting profit margins.
* **Specialty Anchor Fit:** E&O demonstrates tight parameter stability across both claim frequency (mean = 0.1191, standard deviation = 0.0030) and claim severity (mean = $96.8k, standard deviation = $5.4k). This predictability establishes E&O as the ideal actuarial vehicle to host initial endorsements.
* **Cyber Line Warning:** Cyber Liability experienced significant underwriting deterioration, reaching a 97.64% combined ratio in 2025 due to an 82.2% surge in average claim severity ($164.4k in 2021 to $299.6k in 2025). This volatility confirms that TSI cannot prudently absorb an un-sublimited, standalone AI line.

### 2. AI Incident Anatomy & Insurability Diagnostics (Exhibit B)
Evaluating the 135 external incidents ($446.1M total insured losses) indicates that AI liability is **partially insurable** through targeted peril segmentation:
* **Insurable Segment (High Frequency / Bounded Severity):** 
  * *Hallucinated Output:* 36 claims (26.7% share), mean severity of $151.8k, maximum observed loss of $289.0k.
  * *Misinformation:* 19 claims (14.1% share), mean severity of $585.3k, maximum observed loss of $1.19M.
  * *Algorithmic Bias:* 26 claims (19.3% share), mean severity of $2.79M.
* **Uninsurable Tail Risk:**
  * *Autonomous System Failures:* Accounted for only 9 claims (6.7% of count) but drove $179.1M (40.1% of all losses) with an average cost of $19.90M per event (maximum $31.17M). A single physical autonomous failure would impair multi-year underwriting earnings, requiring an absolute policy exclusion.
* **Human-in-the-Loop (HITL) Impact:**
  * Incidents with verified human oversight averaged $2.40M versus $4.23M for unmonitored systems—representing an immediate 43.3% severity reduction ($1.83M savings per claim).

---

## Option B: Product Design & Risk Controls

* **E&O Endorsement Rider:** Covers legal defense costs and financial liabilities arising from generative AI hallucinations, professional service advisory errors, and algorithmic bias.
  * *Sub-limit:* Capped at $250,000 to $500,000 per policy year, with defense costs eroding within the limit.
* **Cyber Endorsement Rider:** Protects against direct losses from deepfake executive impersonation, prompt injection exploits, and unauthorized funds-transfer fraud.
  * *Sub-limit:* Capped at $500,000 aggregate per policy year.
* **Contractual Verifiability & Loss Sharing:**
  * Replaces subjective oversight definitions with verifiable audit requirements (immutable system logs, signed code reviews, or CMS publication timestamps).
  * Incorporates a tiered coinsurance schedule: verified human-in-the-loop workflows qualify for standard $5,000 deductibles and 90/10 coverage, while automated batch pipelines require a $25,000 deductible and 50% coinsurance.
* **Policy Exclusions:** Absolute exclusions for physical autonomous machinery/vehicles, intentional civil rights violations, and upstream hyperscaler cloud outages.
* **Capital Protection:** 50% quota-share reinsurance treaty structure paired with standardized affirmative exclusions attached to base policies that decline the endorsement.
