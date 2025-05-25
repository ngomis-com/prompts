# User Prompt for Projects Overview Generation

Generate the Projects Overview section in Markdown format using the following list of projects. Follow the instructions provided in the corresponding system prompt.

**Projects List (`projects`):**
`{projects}`

*   *Example (List of ProjectContext objects):*
    ```json
    [
      {
        "project_id": "Sanchay-Punjab-PRIF",
        "name": "Sanchay",
        "goal": "Improve ground water level by creating surface water storage...",
        "start_date": "2022-06-17",
        "end_date": "2023-03-31",
        "status": "Completed",
        "summary": "Focuses on rainwater harvesting and chemical-free agriculture in Derabassi block, Punjab.",
        "key_activities": ["Pond Desilting", "Rooftop Harvesting", "Sprinkler Setup", "SHG Formation", "FPO Setup"],
        "key_outcomes": ["16.5M liters water storage created", "Reduced input costs", "Market linkages via FPO"]
      },
      {
        "project_id": "EnhancingIncomes-UP-APPI",
        "name": "Enhancing Marginalized Household Incomes",
        "goal": "To achieve a sustainable increase of Rs. 25,000 in annual incomes for 4,500 families...",
        "start_date": "2022-07-01", // Assuming Phase 2 start for this example
        "end_date": "2027-06-30", // Assuming Phase 2 end
        "status": "Ongoing",
        "summary": "Aims to improve incomes for marginalized households in Rudauli, Uttar Pradesh through SRI, goatery, and CBO strengthening.",
        "key_activities": ["SRI/SWI Scaling", "Goat Rearing Support", "Kisan Pathshala", "Pashu Pathshala", "FPO Strengthening"],
        "key_outcomes": ["Increased crop yields", "Avg Rs 11,000 income increase from goatery", "Strengthened SHGs & FPO"]
      },
      {
        "project_id": "Skills-Dasra",
        "name": "Skilling and Livelihoods",
        "goal": "To provide skilling opportunities...", // Example goal
        "start_date": "2021-11-01",
        "end_date": "2022-12-31",
        "status": "Completed",
        "summary": "Provided skilling opportunities in partnership with Dasra.",
        "key_activities": ["Training sessions", "Placement support"], // Example activities
        "key_outcomes": ["Number of youth trained", "Number placed in jobs"] // Example outcomes
      }
      // ... more project objects
    ]
    ```

<!-- Corresponds to models.py: ProjectsContext (containing a list of ProjectContext objects) -->

---
*Please generate only the Markdown content for the Projects Overview section based on these inputs.*
