# NGO/MIS Base Prompts

NGO/MIS Prompts contains a collection of base "meta prompts" designed to be used with a Large Language Model (LLM) to generate various documents and reports for Non-Governmental Organizations (NGOs).

## Purpose

The goal of this project is to provide a standardized, modular, and reusable set of prompts that can be programmatically combined and populated with an organization's specific data. This allows for the automated generation of consistent, high-quality documents such as:

*   Annual Reports
*   Funding Proposals
*   Grant Announcements
*   Project Reports
*   And more...

By using a structured prompt system, NGOs can significantly reduce the time and effort required for documentation and reporting.

## Structure

All prompts are located in the `markdown/` directory. Each file represents a "meta prompt" for generating a specific section or a complete document. The prompts are designed to be modular and, in some cases, can call each other to build complex documents from smaller, reusable components.

## How to Use

These prompts are not intended to be used directly by a human user. They are designed to be used by a processing engine that:

1.  Selects a top-level prompt (e.g., `annual_report.md`).
2.  Gathers the required context data from a database or other sources.
3.  Injects the context data into the placeholders (e.g., `{organization_name}`).
4.  Handles nested prompt calls (e.g., `{about_us_section: from_prompt('markdown/about-us.md')}`).
5.  Sends the final, fully-formed prompt to an LLM for generation.

## Prompts Included

This repository includes a wide range of prompts covering most common NGO documentation needs:

*   **Core Documents:**
    *   `annual_report.md`: A comprehensive annual report.
    *   `knowledge_base.md`: A complete internal summary of the organization.
    *   `funding_proposal.md`: For drafting grant proposals.
    *   `grant_announcement.md`: For announcing new grant opportunities.
    *   `project_report.md`: For detailed reporting on a specific project.
*   **Component Sections:**
    *   `about-us.md`: Organization's mission, vision, and history.
    *   `projects.md`: A summary table of all projects.
    *   `social_impact_areas.md`: Describes focus areas and their projects.
    *   `project_detail.md`: Formats a single project's details.
    *   `locations.md`: Geographical focus areas.
    *   `teams.md`: Team and governance structure.
    *   `stakeholders.md`: Key stakeholders and partners.
    *   `compliances.md`: Legal and compliance details.
    *   `organization_factsheet.md`: Key metrics and data points.
    *   `testimonials.md`: Beneficiary and partner testimonials.
    *   `theory_of_change.md`: The organization's impact model.
    *   And more...

## Contributing

We welcome contributions to improve existing prompts or add new ones! Please feel free to fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
