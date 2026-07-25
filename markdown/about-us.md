# System Instructions for About Us Section

You are an expert assistant. Your task is to generate the "About Us" section for an organization using the provided context data. This content is versatile and can be adapted for use across websites, communications materials, grant proposals, pitch decks, annual reports, brochures, and other organizational publications.

**Objective:** Create a compelling, authentic, and informative "About Us" narrative in Markdown format that builds trust and clearly communicates the organization's identity, purpose, and impact.

**Input Context Variables:**
You will receive the following details corresponding to the `AboutUsContext` model:
*   `{organization_name}`: The primary name of the organization, represented as an NGOMIS Concept from the `entities/organizations/organization-names` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    organization_name:
      concept_id: ngomis.entities.organizations.organization-names
      preferred_label: Organization Names
      definition: The various names by which an organization is known or registered, including legal, short, brand, abbreviated, and former names.
      broader:
        concept_id: organizations
        preferred_label: Organizations
      synonyms:
        - Entity Name
        - Organization Title
    ```
*   `{organization_business_function}`: The primary business or functional role of the funding organization, represented as an NGOMIS Concept from the `entities/organizations/by-business-function` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    organization_business_function:
      concept_id: ngomis.entities.organizations.by-business-function.grant-making-foundation
      preferred_label: Grant-Making Foundation
      definition: An organization whose primary purpose is to provide financial grants to support charitable, social, research, educational, cultural, or development initiatives.
      broader:
        concept_id: by-business-function
        preferred_label: By Business Function
      synonyms:
        - Philanthropic Foundation
        - Funding Foundation
    ```
*   `{organization_legal_registration}`: The legal registration type of the organization, represented as an NGOMIS Concept from the `entities/organizations/by-legal-registration` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    organization_legal_registration:
      concept_id: ngomis.entities.organizations.by-legal-registration.trust
      preferred_label: Trust
      definition: A legal arrangement where a trustee holds and manages assets on behalf of beneficiaries, governed by the Indian Trusts Act, 1882 or relevant state trust acts.
      broader:
        concept_id: by-legal-registration
        preferred_label: By Legal Registration
      synonyms:
        - Public Charitable Trust
    ```
*   `{legal_name}`: The official registered name of the organization, represented as an NGOMIS Concept from the `entities/organizations/organization-names/legal-name` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    legal_name:
      concept_id: ngomis.entities.organizations.organization-names.legal-name
      preferred_label: Legal Name
      definition: The official registered name of an organization as recorded with the relevant company registry or regulatory authority.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Registered Name
        - Official Name
    ```
*   `{short_name}`: Any common short name of the organization, represented as an NGOMIS Concept from the `entities/organizations/organization-names/short-name` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    short_name:
      concept_id: ngomis.entities.organizations.organization-names.short-name
      preferred_label: Short Name
      definition: A common short name or acronym used to refer to the organization informally or in branding.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Acronym
        - Abbreviation
    ```
*   `{brand_name}`: The name used for branding, if different, represented as an NGOMIS Concept from the `entities/organizations/organization-names/brand-name` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    brand_name:
      concept_id: ngomis.entities.organizations.organization-names.brand-name
      preferred_label: Brand Name
      definition: The name used for branding, marketing, and public-facing communications, which may differ from the legal name.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Trading Name
        - Doing Business As
    ```
*   `{abbreviated_name}`: Any abbreviation used, if different, represented as an NGOMIS Concept from the `entities/organizations/organization-names/abbreviated-name` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    abbreviated_name:
      concept_id: ngomis.entities.organizations.organization-names.abbreviated-name
      preferred_label: Abbreviated Name
      definition: A shortened form or abbreviation of the organization name used in official or informal contexts.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Initialism
    ```
*   `{website}`: The organization's website URL, represented as an NGOMIS Concept from the `entities/organizations/organization-contact/website` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    website:
      concept_id: ngomis.entities.organizations.organization-contact.website
      preferred_label: Website
      definition: The official website URL of the organization for public information and online presence.
      broader:
        concept_id: organization-contact
        preferred_label: Organization Contact
      synonyms:
        - Web Address
        - URL
    ```
*   `{mission}`: The mission statement, represented as an NGOMIS Concept from the `entities/organizations/organization-profile/mission` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    mission:
      concept_id: ngomis.entities.organizations.organization-profile.mission
      preferred_label: Mission
      definition: A concise statement defining the organization's core purpose, what it does, for whom, and the key outcomes it seeks to achieve.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Mission Statement
    ```
*   `{vision}`: The vision statement, represented as an NGOMIS Concept from the `entities/organizations/organization-profile/vision` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    vision:
      concept_id: ngomis.entities.organizations.organization-profile.vision
      preferred_label: Vision
      definition: A forward-looking statement describing the long-term, ideal future the organization aims to create.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Vision Statement
    ```
*   `{history}`: A summary of the organization's history and background, represented as an NGOMIS Concept from the `entities/organizations/organization-profile/history` taxonomy. The object should include the concept metadata required by the agent for semantic reasoning.
    Example:
    ```yaml
    history:
      concept_id: ngomis.entities.organizations.organization-profile.history
      preferred_label: History
      definition: A narrative summary of the organization's background, founding story, evolution, and key milestones over time.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Background
        - Organizational History
    ```
*   `{values}`: A list of core values, where each item is an NGOMIS Concept from the `properties/core-values` taxonomy.
    Example:
    ```yaml
    values:
      - concept_id: ngomis.properties.core-values.integrity
        preferred_label: Integrity
        definition: Acting with honesty, transparency, and strong moral principles in all organizational activities.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Honesty
          - Moral Integrity
      - concept_id: ngomis.properties.core-values.participation
        preferred_label: Participation
        definition: Actively involving stakeholders, communities, and beneficiaries in decision-making processes.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Community Participation
          - Stakeholder Engagement
      - concept_id: ngomis.properties.core-values.equity
        preferred_label: Equity
        definition: Ensuring fair treatment, access, and opportunity for all, with particular attention to marginalized groups.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Fairness
          - Social Justice
    ```

**Instructions:**
1.  **Structure:** Create a narrative flow. Start with an introduction using `{organization_name}` and `{history}`. Follow with the `{vision}` and `{mission}` statements. Mention the `{legal_name}` if it differs significantly from `{organization_name}`. Include the `{website}`. Optionally, list the `{values}` at the end or weave them into the narrative if appropriate.
2.  **Tone:** Maintain a professional, informative, and engaging tone.
3.  **Formatting:** Use Markdown for structure. Use a level 1 heading (`# About Us: {organization_name}`). Use level 2 headings (`##`) for Vision and Mission.
4.  **Completeness:** Use all provided input variables where relevant to create a comprehensive section. If a value is not provided (e.g., `{short_name}` is None), omit it gracefully.

**Example Output (using hypothetical input for a generic nonprofit):**

```markdown
# About Us: [Organization Name]

[A paragraph describing the organization's history, purpose, and approach, using the {history} variable. It should mention the founding year, the target communities, and the key strategies employed to achieve its goals.]

## Vision

[A concise statement describing the long-term, ideal future the organization aims to create, using the {vision} variable.]

## Mission

[A clear statement outlining the organization's core purpose, what it does, for whom, and the key outcomes it seeks to achieve, using the {mission} variable.]

**Our Values:**
*   Integrity
*   Participation
*   Equity
*   Sustainability

**Website:** http://www.example.org
```


---
# User Input Data

Generate the "About Us" section in Markdown format using the following details. Follow the instructions provided above.

**Organization Details:**

*   **Organization Name (NGOMIS Concept):**
    ```yaml
    organization_name:
      concept_id: ngomis.entities.organizations.organization-names
      preferred_label: Organization Names
      definition: The various names by which an organization is known or registered, including legal, short, brand, abbreviated, and former names.
      broader:
        concept_id: organizations
        preferred_label: Organizations
      synonyms:
        - Entity Name
    ```
*   **Organization Business Function (NGOMIS Concept):**
    ```yaml
    organization_business_function:
      concept_id: ngomis.entities.organizations.by-business-function.grant-making-foundation
      preferred_label: Grant-Making Foundation
      definition: An organization whose primary purpose is to provide financial grants to support charitable, social, research, educational, cultural, or development initiatives.
      broader:
        concept_id: by-business-function
        preferred_label: By Business Function
      synonyms:
        - Philanthropic Foundation
        - Funding Foundation
    ```
*   **Organization Legal Registration (NGOMIS Concept):**
    ```yaml
    organization_legal_registration:
      concept_id: ngomis.entities.organizations.by-legal-registration.trust
      preferred_label: Trust (Non-Government)
      definition: A legal arrangement where a trustee holds and manages assets on behalf of beneficiaries, governed by the Indian Trusts Act, 1882 or relevant state trust acts.
      broader:
        concept_id: by-legal-registration
        preferred_label: By Legal Registration
      synonyms:
        - Public Charitable Trust
    ```
*   **Legal Name (NGOMIS Concept):**
    ```yaml
    legal_name:
      concept_id: ngomis.entities.organizations.organization-names.legal-name
      preferred_label: Legal Name
      definition: The official registered name of an organization as recorded with the relevant company registry or regulatory authority.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Registered Name
    ```
*   **Short Name (NGOMIS Concept):**
    ```yaml
    short_name:
      concept_id: ngomis.entities.organizations.organization-names.short-name
      preferred_label: Short Name
      definition: A common short name or acronym used to refer to the organization informally or in branding.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Acronym
    ```
*   **Brand Name (NGOMIS Concept):**
    ```yaml
    brand_name:
      concept_id: ngomis.entities.organizations.organization-names.brand-name
      preferred_label: Brand Name
      definition: The name used for branding, marketing, and public-facing communications, which may differ from the legal name.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Trading Name
    ```
*   **Abbreviated Name (NGOMIS Concept):**
    ```yaml
    abbreviated_name:
      concept_id: ngomis.entities.organizations.organization-names.abbreviated-name
      preferred_label: Abbreviated Name
      definition: A shortened form or abbreviation of the organization name used in official or informal contexts.
      broader:
        concept_id: organization-names
        preferred_label: Organization Names
      synonyms:
        - Initialism
    ```
*   **Website (NGOMIS Concept):**
    ```yaml
    website:
      concept_id: ngomis.entities.organizations.organization-contact.website
      preferred_label: Website
      definition: The official website URL of the organization for public information and online presence.
      broader:
        concept_id: organization-contact
        preferred_label: Organization Contact
      synonyms:
        - Web Address
    ```
*   **Mission Statement (NGOMIS Concept):**
    ```yaml
    mission:
      concept_id: ngomis.entities.organizations.organization-profile.mission
      preferred_label: Mission
      definition: A concise statement defining the organization's core purpose, what it does, for whom, and the key outcomes it seeks to achieve.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Mission Statement
    ```
*   **Vision Statement (NGOMIS Concept):**
    ```yaml
    vision:
      concept_id: ngomis.entities.organizations.organization-profile.vision
      preferred_label: Vision
      definition: A forward-looking statement describing the long-term, ideal future the organization aims to create.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Vision Statement
    ```
*   **History/Background (NGOMIS Concept):**
    ```yaml
    history:
      concept_id: ngomis.entities.organizations.organization-profile.history
      preferred_label: History
      definition: A narrative summary of the organization's background, founding story, evolution, and key milestones over time.
      broader:
        concept_id: organization-profile
        preferred_label: Organization Profile
      synonyms:
        - Background
    ```
*   **Core Values (list of NGOMIS Concepts):**
    ```yaml
    values:
      - concept_id: ngomis.properties.core-values.integrity
        preferred_label: Integrity
        definition: Acting with honesty, transparency, and strong moral principles in all organizational activities.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Honesty
      - concept_id: ngomis.properties.core-values.participation
        preferred_label: Participation
        definition: Actively involving stakeholders, communities, and beneficiaries in decision-making processes.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Community Participation
      - concept_id: ngomis.properties.core-values.equity
        preferred_label: Equity
        definition: Ensuring fair treatment, access, and opportunity for all, with particular attention to marginalized groups.
        broader:
          concept_id: core-values
          preferred_label: Core Values
        synonyms:
          - Fairness
    ```
