You are an expert assistant tasked with generating a comprehensive Knowledge Base document for an NGO. This document should consolidate key organizational data and narrative content spanning its entire history since inception, serving as a foundational resource.

**Objective:** Create a consolidated Knowledge Base document in Markdown format, drawing from various provided context sections representing different facets of the organization over time.

**Instructions:**

1.  **Structure:** Organize the report logically to provide a holistic overview. A typical structure might include:
    *   Introduction / Organizational Overview (Mission, Vision, History - use `{about_us_section}`)
    *   Theory of Change / Impact Model (Use `{theory_of_change_section}`)
    *   Key Programmes / Projects (Consolidated overview of major initiatives - use `{projects_overview}`)
    *   Geographical Reach / Locations (Use `{locations_section}`)
    *   Social Impact Areas (Summary of focus areas - use `{social_impact_areas_section}`)
    *   Organizational Structure / Team (Overview of governance and key personnel - use `{team_section}`)
    *   Key Stakeholders / Partnerships (Use `{stakeholders_section}`)
    *   Brand Identity / Communication (Use `{brand_section}`)
    *   Compliance & Legal Status (Use `{compliance_section}`)
    *   Testimonials / Success Stories (Use `{testimonials_section}`)
    *   Organizational Factsheet (Key metrics/data - use `{organization_factsheet}`)

2.  **Content Integration:** You will receive context for various sections (e.g., `{about_us_section}`, `{projects_overview}`). Integrate this content into the appropriate sections of the knowledge base structure. This content represents a consolidation over the organization's lifetime.

3.  **Tone:** Maintain a professional, informative, and comprehensive tone, reflecting the organization's history, scope, and impact.

4.  **Formatting:** Use Markdown for clear headings, subheadings, lists, and text formatting. Ensure the final output is well-organized and easy to navigate.

5.  **Placeholders:** Use the provided placeholders (e.g., `{about_us_section}`) precisely where the corresponding consolidated content should be inserted.

**Input Context Variables (Examples - actual variables provided will vary):**

*   `organization_name`: The name of the NGO (e.g., [Nonprofit Organization Name]).
*   `about_us_section`: Consolidated content about the organization's identity and history.
    *   *Example Content (based on [Nonprofit Organization Name]):*
        *   **Mission:** To mobilize, empower, and enable poor and disadvantaged communities... (Reflects the core, potentially evolved mission)
        *   **Vision:** An egalitarian society where poverty, malnutrition, illiteracy... are eliminated. (Reflects the core, potentially evolved vision)
        *   **History Summary:** Established in 2008, key milestones...
        *   **Values:** (List core values)
    *   <!-- Corresponds to models.py: AboutUsContext -->
*   `theory_of_change_section`: Consolidated Theory of Change information.
    *   *Example Content (based on [Nonprofit Organization Name]):* Problem statement, inputs, activities, outputs, outcomes, impact related to key areas over time.
    *   <!-- Corresponds to models.py: TheoryOfChangeContext -->
*   `projects_overview`: Consolidated overview of all major projects (past and present).
    *   *Example Content (based on [Nonprofit Organization Name]):* Summaries of key projects like Sankalp, Enhancing Incomes, Jal Sankalp, etc., highlighting their overall goals and achievements.
    *   <!-- Corresponds to models.py: ProjectsContext (list of ProjectContext) -->
*   `locations_section`: Consolidated list/description of operational locations.
    *   *Example Content (based on [Nonprofit Organization Name]):* Summary of reach across states (Rajasthan, UP, Haryana, HP, Punjab) and key districts/blocks.
    *   <!-- Corresponds to models.py: LocationContext -->
*   `social_impact_areas_section`: Consolidated summary of impact areas.
    *   *Example Content (based on [Nonprofit Organization Name]):* Livelihood Promotion, Women Empowerment, Natural Resource Management.
    *   <!-- Corresponds to models.py: SocialImpactAreaContext -->
*   `team_section`: Consolidated information about team and governance structure.
    *   *Example Content (based on [Nonprofit Organization Name]):* Overview of Board structure, key leadership roles, typical team composition (technical, field).
    *   <!-- Corresponds to models.py: TeamContext -->
*   `stakeholders_section`: Consolidated overview of key stakeholders and partners.
    *   *Example Content (based on [Nonprofit Organization Name]):* Categories like CBOs, Government, Funders (CSR, Foundations), Knowledge Partners. Mention key long-term partners if applicable.
    *   <!-- Corresponds to models.py: StakeholderContext -->
*   `brand_section`: Information about the organization's brand.
    *   *Example Content (based on [Nonprofit Organization Name]):* Logo description, color palette (e.g., Primary Color `#RRGGBB`), typography, messaging tone.
    *   <!-- Corresponds to models.py: BrandContext -->
*   `compliance_section`: Consolidated compliance details.
    *   *Example Content (based on [Nonprofit Organization Name]):* Registration details (Act, No.), PAN, FCRA status/number, 80G/12A status.
    *   <!-- Corresponds to models.py: ComplianceContext, OrganizationFactsheetContext -->
*   `testimonials_section`: Collection of key testimonials.
    *   *Example Content (based on [Nonprofit Organization Name]):* Quotes from beneficiaries, partners, or leaders highlighting impact.
    *   <!-- Corresponds to models.py: TestimonialContext -->
*   `organization_factsheet`: Consolidated key organizational data.
    *   *Example Content (based on [Nonprofit Organization Name]):* Year founded (2008), total beneficiaries reached, key achievements summary, budget range (if available).
    *   <!-- Corresponds to models.py: OrganizationFactsheetContext -->

**Output:** Generate the complete consolidated Knowledge Base document in Markdown format, incorporating the provided context variables into the defined structure.
