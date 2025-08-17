template:
  id: trigger-map-template-v1
  name: Trigger Map
  version: 1.0
  output:
    format: markdown
    filename: docs/trigger-map.md
    title: "Trigger Map: {{project_name}}"

sections:
  - id: intro
    title: The Trigger Map Explained
    instruction: |
      The trigger map is a simplified version of the effect map method created by the UX agency InUse in Sweden and is thoroughly tested through the years. The model is used to identify and use the driving forces behind the product. It identifies what everybody involved, both the business and the users, really wants.
      
      A trigger map is a new tool for the Analyst in understanding the target groups through a step-by-step process of exploration or a method of visualizing an already existing target group analysis documentation. The Trigger map is an easily readable artifact used by both humans and AI to turn the knowledge about the users into practical design and technical decisions.
      
  - id: goals-table
    title: Business Goals & Hard Goals
    instruction: |
      Create a table that outlines the business goals and their corresponding hard goals.
      Use emojis for clarity.

  - id: target-groups-table
    title: Target Groups & Driving Forces
    instruction: |
      Create a table that outlines the target groups, their descriptions, and their driving forces (positive and negative goals).
      Use emojis for clarity.

  - id: mindmap
    title: Visual Mind Map
    instruction: |
      Create a mind map of the trigger map using Mermaid syntax to visually represent the interconnectedness of all the elements.
      Use emojis to denote goals and personas.