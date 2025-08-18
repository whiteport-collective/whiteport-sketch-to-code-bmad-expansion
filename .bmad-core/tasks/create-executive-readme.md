# create-executive-readme

## Purpose

To create a comprehensive README.md file that serves as both an executive summary and navigation hub for the entire project. This document should tell the strategic story while providing easy access to all project artifacts.

## Process

**CRITICAL: This README should focus on strategic takeaways and business insights rather than document format descriptions.**

### Step 1: Strategic Introduction
Create a compelling introduction that includes:
- **Project vision and mission** - What problem does this solve?
- **Target market and timeline** - Who benefits and when?
- **Technology foundation** - Brief technical positioning
- **Key differentiators** - What makes this unique?

### Step 2: Embedded Trigger Map Visualization
**MANDATORY**: Include the trigger map Mermaid diagram directly in the README using GitHub-compatible syntax:
- Use `flowchart LR` for left-to-right flow
- Apply light gray color scheme for professional appearance
- Include central platform/product node for clarity
- Show business goals → platform → target groups → driving forces flow

### Step 3: Strategic Insights Section
Extract and present key strategic insights from the user research:
- **Primary revenue drivers** - Which user types are most critical?
- **Network effects** - How do user types strengthen each other?
- **Competitive advantages** - What creates sustainable differentiation?
- **Market positioning** - Where does this fit in the ecosystem?

### Step 4: Market Opportunity & Business Case
Summarize the business opportunity with:
- **Market gap analysis** - What problem exists?
- **Strategic advantages** - How does the solution address it?
- **Revenue model resilience** - Why is this sustainable?
- **Timing rationale** - Why now?

### Step 5: Streamlined Documentation Navigation
Provide clean, strategic links to detailed documentation:
- **Strategic Foundation** - Link to product brief with brief description of insights
- **User Research** - Link to trigger map with key findings summary
- **Target Group Profiles** - Persona links with one-line descriptions
- Avoid listing document structure; focus on strategic value

## Mermaid Best Practices for GitHub Compatibility

### Color Scheme Guidelines
Use light gray palette for professional appearance:
```yaml
classDef businessGoal fill:#f3f4f6,color:#000000,stroke:#d1d5db,stroke-width:3px
classDef platform fill:#e5e7eb,color:#000000,stroke:#d1d5db,stroke-width:4px
classDef targetGroup fill:#f9fafb,color:#000000,stroke:#d1d5db,stroke-width:2px
classDef drivingForces fill:#f3f4f6,color:#000000,stroke:#d1d5db,stroke-width:2px
```

### Layout Guidelines
- **Use `flowchart LR`** for left-to-right trigger map flow
- **Include central platform node** between business goals and target groups
- **Limit diagram complexity** - GitHub has rendering limits for very complex diagrams
- **Use descriptive but concise labels** - Avoid overwhelming detail in diagram nodes

### GitHub Rendering Optimization
- **Test in README.md files** - These render most reliably
- **Avoid excessive styling** - Keep it simple for maximum compatibility
- **Use standard Mermaid syntax** - Avoid experimental features
- **Consider diagram size** - Very large diagrams may not render properly

## Output Requirements

### File Location
- **Always place in repository root** as `README.md`
- This ensures GitHub displays it automatically on repository homepage

### Content Structure
1. **Project title and tagline**
2. **Strategic introduction**
3. **Embedded trigger map visualization**
4. **Strategic insights from research**
5. **Market opportunity and business case**
6. **Streamlined documentation links**
7. **Project status and stakeholder information**

### Tone and Audience
- **Executive-ready** - Suitable for investor and stakeholder presentations
- **Strategic focus** - Emphasize business insights over document structure
- **Visual impact** - Embedded diagram provides immediate strategic understanding
- **Professional language** - Clear, confident, and compelling

## Success Criteria

The README should serve as:
- **Standalone executive summary** that tells the complete strategic story
- **Visual trigger map showcase** that immediately communicates user-business relationships
- **Navigation hub** that provides easy access to detailed documentation
- **Professional presentation** suitable for sharing with investors, stakeholders, and development teams

## Integration with Other Tasks

This task builds upon:
- **Product Brief** - Strategic foundation and market analysis
- **Trigger Map** - User research and business goal alignment
- **Individual Personas** - Target group insights and driving forces

The README synthesizes insights from all these artifacts into a compelling executive presentation while maintaining easy access to detailed documentation.
