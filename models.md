## Data Models and Enums from models.py

This document outlines the Pydantic models and Enums used for structuring data.

### Enums

**OutputFormatType:**
*   `markdown_standard`: Default: paragraphs, headings, lists
*   `markdown_table`
*   `mermaid_diagram`
*   `map_geojson`: GeoJSON map data

**DocumentType:**
*   `knowledge-base`
*   `annual-report`
*   `project-report`
*   `organizational-financial-report`
*   `project-financial-report`
*   `project-proposal`
*   `grant-announcement`
*   `about-us`
*   `brand`
*   `compliances`
*   `locations`
*   `organization_factsheet`
*   `projects`
*   `social_impact_areas`
*   `stakeholders`
*   `teams`
*   `testimonials`
*   `theory_of_change`
*   `prompts`

**LocationType:**
*   `operational_area`
*   `head_office`
*   `field_office`
*   `project_office`
*   `registered_office`
*   `other`

**StakeholderType:**
*   `Donor`
*   `Government`
*   `Knowledge Partner`
*   `Implementation Partner`
*   `Technology Partner`
*   `Community`
*   `Private Sector`
*   `Other`

**TeamType:**
*   `Governing Body`
*   `Senior Management`
*   `Project Team`
*   `Field Team`
*   `Advisory`
*   `Other`

### Core Document & API Models

**DocumentMetadata:**
*   `doc_id`: string (Unique identifier)
*   `doc_type`: DocumentType (Enum)
*   `organization_id`: string
*   `project_id`: Optional[string]
*   `title`: Optional[string]
*   `created_at`: datetime
*   `last_modified_at`: datetime
*   `version`: int (default: 1)
*   `source_prompt`: Optional[string]
*   `filters`: Optional[Dict[str, Any]]

**Document:**
*   `metadata`: DocumentMetadata
*   `content`: LexicalContent (Dict[str, Any])

**GenerateDocumentRequest:**
*   `organization_alias`: string
*   `doc_type`: DocumentType
*   `project_id`: Optional[string]
*   `filters`: Optional[Dict[str, Any]]
*   `output_format`: Optional[OutputFormatType]

**EditDocumentRequest:**
*   `user_prompt`: string
*   `context_markdown`: string (Section selected by user as Markdown)

**SectionUrl:**
*   `section`: string
*   `url`: string

**DocumentResponse:**
*   `metadata`: DocumentMetadata
*   `saved_lexical_signed_url`: Optional[string]
*   `section_markdown_signed_urls`: Optional[List[SectionUrl]]

**EditResponse:**
*   `updated_context`: LexicalContent (Dict[str, Any])

**RenameDocumentRequest:**
*   `title`: string

**CreateDocumentResponse:**
*   `message`: string (default: "Document created successfully.")
*   `new_document_metadata`: DocumentMetadata

**EditorListItem:**
*   `id`: string
*   `title`: string
*   `item_type`: string
*   `document_type`: Optional[string]
*   `last_modified_at`: datetime

### Context Models

**AboutUsContext:**
*   `organization_name`: string
*   `mission`: Optional[string]
*   `vision`: Optional[string]
*   `history`: Optional[str]
*   `values`: Optional[List[str]]
*   `legal_name`: Optional[string]
*   `short_name`: Optional[string]
*   `brand_name`: Optional[string]
*   `abbreviated_name`: Optional[string]
*   `website`: Optional[string]

**BrandContext:**
*   `logo_description`: Optional[string]
*   `color_palette`: Optional[Dict[str, str]]
*   `fonts`: Optional[List[str]]
*   `messaging_guidelines`: Optional[str]
*   `social_media_links`: Optional[Dict[str, str]]

**ComplianceContext:** (Registration Details Only)
*   `registration_authority`: Optional[string]
*   `legal_status`: Optional[string]
*   `registration_number_orgid`: Optional[string]
*   `registration_number_specific`: Optional[string]
*   `registration_act`: Optional[string]
*   `registration_country`: Optional[string]
*   `registration_state`: Optional[string]
*   `registration_district`: Optional[string]
*   `registration_city`: Optional[string]
*   `registration_address`: Optional[string]
*   `incorporation_date`: Optional[datetime.date]
*   `registration_certificate_available`: Optional[bool]
*   `tax_id`: Optional[string]
*   `key_filings`: Optional[Dict[str, str]]

**LocationIndiaRural:**
*   `location_type`: LocationType
*   `organization_id`: string
*   `project_id`: Optional[string]
*   `type`: "rural"
*   `country`: "India"
*   `state`: string
*   `district`: string
*   `block`: Optional[string]
*   `gram_panchayat`: Optional[string]
*   `village`: string
*   `address_line`: Optional[string]
*   `pincode`: Optional[string]

**LocationIndiaUrban:**
*   `location_type`: LocationType
*   `organization_id`: string
*   `project_id`: Optional[string]
*   `type`: "urban"
*   `country`: "India"
*   `state`: string
*   `district`: Optional[string]
*   `city_town`: string
*   `ward`: Optional[string]
*   `address_line`: string
*   `pincode`: Optional[string]

**LocationIndia:** (Union of Rural/Urban)
*   Fields depend on `type` ("rural" or "urban")

**LocationContext:**
*   `summary`: Optional[string]
*   `relevant_locations`: List[LocationIndia]
*   `filters_applied`: Optional[Dict[str, Any]]

**OrganizationFactsheetContext:**
*   `year_founded`: Optional[int]
*   `employee_count`: Optional[int]
*   `volunteer_count`: Optional[int]
*   `beneficiaries_reached_total`: Optional[int]
*   `beneficiaries_reached_last_year`: Optional[int]
*   `annual_budget`: Optional[float]
*   `currency`: string (default: "INR")
*   `issues_addressed`: Optional[List[str]]
*   `operation_states`: Optional[List[str]]
*   `operation_districts`: Optional[List[str]]
*   `achievements_summary`: Optional[str]
*   `pan_status`: Optional[string]
*   `pan_number`: Optional[string]
*   `pan_issuance_authority`: Optional[str]
*   `pan_issuance_date`: Optional[datetime.date]
*   `pan_copy_available`: Optional[bool]
*   `fcra_status`: Optional[str]
*   `fcra_number`: Optional[str]
*   `fcra_issuing_authority`: Optional[str]
*   `fcra_validity_date`: Optional[datetime.date]
*   `executive_name`: Optional[string]
*   `executive_designation`: Optional[string]
*   `executive_email`: Optional[str]
*   `executive_mobile`: Optional[str]
*   `executive_telephone`: Optional[str]
*   `executive_photo_link`: Optional[str]

**FinancialStatementItem:**
*   `category`: string
*   `amount`: float
*   `notes`: Optional[string]

**FinancialStatement:**
*   `year`: int
*   `type`: string (e.g., Income, Expenditure)
*   `items`: List[FinancialStatementItem]
*   `currency`: string (default: "INR")

**FinancialReportContext:**
*   `statements`: List[FinancialStatement]

**ProjectFinancialReportContext:** (Inherits FinancialReportContext)
*   `project_id`: string

**ProjectContext:**
*   `project_id`: string
*   `name`: string
*   `goal`: Optional[string]
*   `start_date`: Optional[datetime.date]
*   `end_date`: Optional[datetime.date]
*   `status`: Optional[string]
*   `summary`: Optional[str]
*   `key_activities`: Optional[List[str]]
*   `key_outcomes`: Optional[List[str]]

**ProjectsContext:**
*   `projects`: List[ProjectContext]

**SocialImpactArea:**
*   `name`: string
*   `description`: Optional[string]

**SocialImpactAreaContext:**
*   `areas`: List[SocialImpactArea]

**StakeholderGroup:**
*   `type`: StakeholderType (Enum)
*   `description`: Optional[str]
*   `key_stakeholders`: Optional[List[str]]

**StakeholderContext:**
*   `groups`: List[StakeholderGroup]

**TeamMember:**
*   `name`: string
*   `designation`: string
*   `gender`: Optional[string]
*   `bio_short`: Optional[string]
*   `bio_long`: Optional[string]
*   `keywords`: Optional[List[str]]
*   `cv_link`: Optional[string]
*   `photo_link`: Optional[string]
*   `avatar_link`: Optional[string]
*   `email`: Optional[str]
*   `phone_number`: Optional[str]
*   `linkedin_url`: Optional[str]

**TeamGroup:**
*   `type`: TeamType (Enum)
*   `members`: List[TeamMember]

**TeamStrengthEntry:**
*   `office_name`: string
*   `team_count`: int

**TeamContext:**
*   `governance_summary`: Optional[str]
*   `team_groups`: List[TeamGroup]
*   `team_strength_by_location`: Optional[List[TeamStrengthEntry]]

**Testimonial:**
*   `quote`: string
*   `name`: Optional[string]
*   `context`: Optional[string]

**TestimonialContext:**
*   `testimonials`: List[Testimonial]

**TheoryOfChangeContext:**
*   `problem_statement`: Optional[str]
*   `inputs`: Optional[List[str]]
*   `activities`: Optional[List[str]]
*   `outputs`: Optional[List[str]]
*   `outcomes`: Optional[List[str]]
*   `impact`: Optional[str]
*   `assumptions`: Optional[List[str]]

**FundingProposalContext:**
*   `donor_name`: string
*   `project_context`: ProjectContext
*   `organization_context`: AboutUsContext
*   `requested_amount`: float
*   `currency`: string (default: "INR")
*   `proposal_focus`: Optional[str]
*   `budget_summary`: Optional[FinancialReportContext]

### GeoJSON Models

**GeoJsonProperties:**
*   `village_code`: Optional[string]
*   `village_name`: Optional[string]
*   `gram_panchayat_code`: Optional[str]
*   `gram_panchayat_name`: Optional[str]

**GeoJsonGeometry:**
*   `type`: string (e.g., Polygon, Point)
*   `coordinates`: Any

**GeoJsonFeature:**
*   `type`: "Feature"
*   `geometry`: Optional[GeoJsonGeometry]
*   `properties`: GeoJsonProperties

**GeoJsonFeatureCollection:**
*   `type`: "FeatureCollection"
*   `features`: List[GeoJsonFeature]
