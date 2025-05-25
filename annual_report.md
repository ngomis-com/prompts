Please generate the Annual Report for **{organization_name}** for the year **{year}**.

Use the following context sections, incorporating them into a full report structure with relevant introductory/concluding remarks, highlights, and future plans based on the overall context provided.

---

**About Us:**
{about_us_section}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   **Organization Name:** [Nonprofit Organization Name] ([Short Name/Acronym])
*   **Mission:** To mobilize, empower, and enable poor and disadvantaged communities...
*   **Vision:** An egalitarian society where poverty, malnutrition, illiteracy... are eliminated.
*   **Geographic Focus:** Rural North India - Rajasthan (Alwar), Uttar Pradesh (Ayodhya, Kanpur Dehat), Haryana (Nuh, Sonipat), Himachal Pradesh (Solan), Punjab (Derabassi).
*   **Key Message:** Since 2008, creating sustainable livelihoods, positively impacted over 27,500 families.
<!-- Corresponds to models.py: AboutUsContext, LocationContext -->

---

**Projects Summary:**
{projects_summary}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   **Social Impact Areas:** Livelihood Promotion, Women Empowerment, Natural Resource Management.
*   **Showcase Projects:**
    *   **Sankalp (Haryana):** Climate-smart agriculture, water conservation, NRM, CBO strengthening (SHGs, Sankalp Samitis). Partner: M3M Foundation. Impact: 700+ households. Activities: Vermicomposting, rainwater harvesting, orchard development.
    *   **Enhancing Marginalized Household Incomes (Uttar Pradesh):** Integrated livelihoods (SRI farming, goatery), CBO strengthening (SHGs, FPOs - Rudauli Kisan Utpadak Sangathan, Rudauli Bakri Palak Sangh). Partner: Azim Premji Foundation. Impact: Aiming for Rs. 25,000 income increase for 4,500 families; Avg Rs. 11,000 increase from goatery. Activities: Kisan Pathshala, Pashu Pathshala, SRI demos.
    *   **Jal Sankalp (Uttar Pradesh):** Water conservation, regenerative agriculture. Partner: Pernod Ricard India Foundation (PRIF). Activities: Water body revival, CBO formation (Water Resource Management Groups).
    *   **Neer Sanrakshan (Haryana):** Water conservation for irrigation & livestock. Partner: PRIF. Activities: Pond rejuvenation, solar pumps. Impact: 21 Million Liters water potential created.
    *   **Sanchay (Punjab):** Water conservation infrastructure, livelihood improvement. Partner: PRIF. Activities: Rooftop rainwater harvesting, sprinkler setup, SHG formation, FPO (WAL Derabassi FPCL).
    *   **Bhujal (Himachal Pradesh):** Water conservation for drinking & agriculture. Partner: Greenlam Industries, Sattva. Activities: Pond construction/rejuvenation, sprinkler demos, VDC formation.
    *   **Water Steward (Haryana):** Integrated WASH & water conservation. Partner: Water Aid. Activities: Model WASH villages, rainwater harvesting, shallow aquifer recharge, WASH facilities in schools/homes. Impact: 58,470 cubic meters groundwater recharge.
*   **Cross-cutting themes:** FPO promotion, CBO strengthening (SHGs, VDCs, Samitis), capacity building (CRPs like Pashu Sakhi, Kisan Sakhi), sustainable/natural farming techniques, water conservation infrastructure.
<!-- Corresponds to models.py: ProjectsContext (list of ProjectContext), SocialImpactAreaContext -->

---

**Financial Summary:**
{financial_summary}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   Brief overview mentioning the inclusion of the Balance Sheet and Income & Expenditure Account for the fiscal year {year}. (Note: Actual figures would be included here if available, referencing specific categories like program expenses, administrative costs, income sources).
<!-- Corresponds to models.py: FinancialReportContext (list of FinancialStatement) -->

---

**Team & Governance:**
{team_section}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   **Governance:** Board of Trustees (e.g., Achintya Ghosh, Thomas Mathew, Asif Zaidi - Executive Director).
*   **Team Structure:** Head office (Alwar), field locations, technical team (agriculture, marketing, engineering, etc.), project implementation teams.
*   **Team Strength:** Total 49 members across locations like Bhiwadi (8), DeraBassi (12), Rudauli (10), etc.
<!-- Corresponds to models.py: TeamContext (team_groups with type GOVERNING_BODY, team_strength_by_location) -->

---

**Stakeholders & Partnerships:**
{stakeholders_section}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   **Key Stakeholder Groups:** Community-Based Organizations (SHGs, Federations), Community Resource Persons (Samuha Sakhi, Kisan Sakhi, Pashu Sakhi), Local Self-Governments (Panchayats), State Governments (Dept. of Agriculture, SRLMs), Funding Partners (CSR, Private Foundations), Knowledge Partners.
*   **Named Partners:** M3M Foundation, Azim Premji Foundation, Pernod Ricard India Foundation (PRIF), Greenlam Industries Limited, Sattva, Water Aid.
<!-- Corresponds to models.py: StakeholderContext (list of StakeholderGroup) -->

---

**Compliance Information:**
{compliance_section}

*Example Content (based on [Nonprofit Organization Name] Annual Report FY[Year]):*
*   Statement confirming compliance with relevant regulations.
*   Mention of key registrations (e.g., Registered under [Registration Act] with Registration No. [Number], PAN: [Number], FCRA: [Number/Status], 12A, 80G status if applicable).
<!-- Corresponds to models.py: ComplianceContext, OrganizationFactsheetContext (for PAN/FCRA) -->

---

Generate the full report structure in Markdown, incorporating these sections and adding relevant introductory/concluding remarks, highlights, and future plans based on the overall context provided.
