## Case Study: Fraud Detection in Healthcare (DMEPOS Analysis)

-----------------------------------------------------------------------

# Team Members:
1) Sabrina Woo, Biohealth Analytics
2) Narsim Kamath, High Performance Computing
3) Cameron Kass, High Performance Computing
4) Love Ayinde, High Performance Computing
5) DSA Mentor: Dr. Timothy Haithcoat

------------------------------------------------------------------------

# Subject Matter Experts:

Director Arvids Petersons of the Missouri Medicaid Fraud Control Unit; Missouri Medicaid Audit and Compliance team, including Director Richard Ferrari, Darla Weekley, Colin Murdick and Jeffrey Rex; Lucas Gallardo from Alivia Analytics.

------------------------------------------------------------------------

# Abstract: 

Fraud is a pervasive and complex problem within the United States healthcare system necessitating evermore complex methods of detection to uncover increasingly convoluted schemes. Our approach uses an analytical framework that integrates Centers for Medicare & Medicaid Services (CMS) Durable Medical Equipment, Prosthetic Devices, Prosthetics, Orthotics, & Supplies (DMEPOS) claims, NPPES, Open Payments, the Office of Inspector General (OIG) Exclusion List, and U.S. Census indicators into a standardized provider–year dataset. We apply an explainable unsupervised ensemble to model baseline “normal” behavior within each specialty, then flag providers who are statistically atypical without relying on large numbers of confirmed fraud labels. Key signals include year-over-year changes, z-scored billing and payment spikes, and utilization mix patterns derived from HCPCS codes and product categories. Each provider receives a risk score by scaling and aggregating anomaly outputs across models (K-Means, LOF, Isolation Forest), producing a ranked list for triage. For transparency, the score is paired with top contributing anomaly factors and an evidence summary that documents the specific behaviors driving the flag, enabling faster, more consistent investigative prioritization. We determine that the top HCPCS service codes billed by fraudulent referring providers demonstrate a significant association with fraud compared to their prevalence in the general population of referring providers for the Medicare DMEPOS program over the period studied. We separately conclude that supervised machine learning methodology is not amenable to the extreme class imbalanced scenario of Medicare fraud.

------------------------------------------------------------------------

# Intended Audience:

Our project is designed for a broad network of fraud prevention stakeholders, including CMS Medicare fraud teams, the Office of Inspector General (OIG), State Medicaid Fraud Control Units (MFCUs), and state program integrity units. The CMS Medicare Fraud Strike Force, jointly led by the Department of Justice (DOJ) and the Department of Health and Human Services (HHS) OIG, targets large-scale Medicare fraud schemes. Supporting these enforcement efforts, state program integrity units within Medicaid agencies focus on preventing improper payments, conducting audits, and referring suspicious cases for further review. State Attorneys General (AGs), and MFCUs investigate and prosecute fraud, waste, and abuse in federally funded healthcare programs through both criminal and civil actions. Collectively, these entities form a unified system dedicated to protecting public healthcare funds and preserving the integrity of Medicare and Medicaid programs.
The impact of our project has both direct and indirect consequences. Preventing FWA in socially funded programs such as Medicare and Medicaid provides an indirect financial benefit to all U.S. taxpayers by preserving public funds and ensuring better financial sustainability of these programs. In addition, this project offers a direct business benefit for fraud investigation teams by generating leads on potential fraud schemes and possibly uncovering national trends. Collectively, these outcomes reduce the systemic risk of undetected FWA and strengthen institutional accountability.

------------------------------------------------------------------------

# Data:
1) CMS Open Payments- General Payments
2) CMS Open Payments- Ownership Payments
3) CMS Part B DMEPOS by Referring Provider
4) CMS Part B DMEPOS by Referring Provider/ Service
5) CMS Part B DMEPOS by Supplier
6) CMS Part B DMEPOS by Supplier/Service
7) OIG Exclusion List 
8) Medicare Enrollment Data 
9) Census Tract Data

