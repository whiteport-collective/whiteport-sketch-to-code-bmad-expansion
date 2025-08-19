# 02. Trigger Map Workshop Method

## Overview

The Trigger Map Workshop Method is a structured collaborative process for aligning business goals with user needs through Effect Mapping methodology. This method creates visual maps that connect organizational objectives to user driving forces, ensuring development priorities serve both business and user success.

## Core Principles

### Strict Step-by-Step Elicitation
- **Mandatory Stops**: Analyst MUST wait for user input before proceeding to next step
- **No Assumptions**: Never complete multiple steps or assume user answers
- **Collaborative Building**: Map emerges through dialogue, not analyst creation

### Effect Mapping Foundation
Based on methodology created by Inuse in Sweden, adapted for digital product development:
- **Business Goals**: What the organization wants to achieve
- **Target Groups**: Who will help achieve those goals through product use
- **Usage Goals**: What target groups want and wish to avoid
- **Strategic Insights**: Development priorities based on goal alignment

### Visual Communication
- **Mermaid Diagrams**: Professional trigger map posters with GitHub-compatible styling
- **Left-to-Right Flow**: Business goals → Platform → Target groups → Driving forces
- **Simultaneous Creation**: Always update poster when trigger map document changes

## Process Flow

### Initial Approach Assessment

**First Step**: Review completed product brief for existing insights about business goals, target users, success metrics, and market context.

**Offer Two Options**:

#### Option A: Draft-First Approach
"Based on the comprehensive project brief, I have enough information to create an initial trigger map draft. Would you like me to create a first version that we can then review and refine together?"

**Benefits**: Leverages existing insights efficiently, provides concrete artifact for reaction and refinement

#### Option B: Traditional Step-by-Step Workshop
"Or we can go through the traditional collaborative trigger map process step-by-step, building it from the ground up through our workshop questions."

**Benefits**: Complete collaborative development, comprehensive coverage through structured elicitation

**STOP HERE** - Wait for user to choose preferred approach before proceeding.

### Step 1: Establish Customer Pattern Understanding

**MANDATORY ELICITATION**: Start with foundational questions about customer patterns:

**Question 1**: "Do you see any patterns in your current or potential customers? Do you see any natural types of customers, users, or visitors?"

**Question 2**: "What do you call your different target groups? Are they customers, visitors, guests, users, members, subscribers, etc.? Note that different target groups can have different names."

**Purpose**: Establishes terminology and foundational understanding for entire trigger map

**STOP HERE** - Wait for user responses before proceeding.

### Step 2: Review and Refine Business Goals

**Overarching Question**: "Let's explore what you, as an organization, imagine that you will get in terms of value from building/refining this product?"

**Follow-up**: "Based on the product brief, what are the specific, measurable business goals that these [use their terminology from Step 1] should help you achieve?"

**Method**: Guide user in defining goals in tree structure:
- **Soft Goals**: Overall project ambitions in qualitative terms - "Best on the market," "Most convenient choice," "Top of mind for..."
- **Hard Goals**: Measurable proof points - "top ranking," "X number of views," "Y number of users"

**Validation**: "Do you agree that fulfilling the hard goals would be a satisfactory way to fulfill the soft goals?"

**STOP HERE** - Wait for user input to refine and quantify business goals.

### Step 3: Identify and Detail Target Groups

**Question**: "Who, in the world, will, by using the system in the intended way, ensure that the business goals are fulfilled?"

**Follow-up**: "Of the [customer types from Step 1], which ones are most critical to achieving [specific goals from Step 2]?"

**Guidelines for Target Group Definition**:
- **User Type Classification**: Each target group must map to user types defined in project brief
- **Multiple Groups per Type**: Define multiple target groups from same user type when they have different needs and driving forces
- **Memorable Naming**: Use alliterative names like "Sture Social" or "Clara Curlingmum"
- **Clear Distinction**: Ensure groups are distinguishable with real, different needs
- **Priority Focus**: Usually 3-5 most important groups to avoid distraction

**STOP HERE** - Wait for user input to define and prioritize target groups.

### Step 4: Define Usage Goals for Each Group

**Overarching Question**: "Let's now explore what your target audience will get, in terms of value, out of interacting with this product."

**For Each Group**: "Why would a [target group name] use this product? What do they want to happen and what do they want to avoid?"

**Focus on Emotional Content**: Answers should be primarily emotional, focusing on ultimate buying decisions and driving forces.

**Positive and Negative Forms**:
- **Positive Usage Goals**: "Wants to...", "Wishes to...", "Prefers to...", "Would like to..."
- **Negative Usage Goals**: "Fears...", "Doesn't want...", "Wishes to avoid...", "Would not have happen..."

**Key Insight**: "Becoming wealthy" vs "not staying poor" are technically the same but lead to radically different design, content, and imagery choices.

**STOP HERE** - Wait for user input after each target group before moving to next.

### Step 5: Create Strategic Insights

**Question**: "Based on what we've discovered, what should be our primary development focus?"

**Synthesis**: Create well-organized hierarchical list of user desired outcomes sorted by importance and impact on business.

**Priority Principle**: Most important function fulfilling goals of primary target group should be developed first.

**STOP HERE** - Wait for user input on prioritization and strategic direction.

### Step 6: Develop Individual Personas

**Process**: Transform target groups into detailed persona profiles with alliterative naming and comprehensive documentation.

#### Persona Creation Standards

##### Alliterative Naming Convention
**CRITICAL REQUIREMENT**: All personas must use alliterative names combining first name with role descriptor.

**Examples**:
- "Rita Reader" - for news readers/content consumers
- "Ellen Entrepreneur" - for business owners/advertisers  
- "Patricia Partner" - for information partners/organizations
- "Peter Public-servant" - for government officials/public servants
- "Sture Social" - for active community connectors
- "Clara Curlingmum" - for time-pressed parents

**Purpose**:
- **Memorability**: Makes personas easier to remember and reference in workshops
- **Professional Consistency**: Creates recognizable pattern across projects and teams
- **Workshop Effectiveness**: Helps teams quickly identify and discuss specific personas

##### User Type Classification
**Each persona must map to user types defined in project brief** for logical consistency between personas and business model.

**Common Classifications**:
- **Reader**: Content consumers, news readers, information seekers
- **Advertiser**: Local businesses, service providers, promotional content creators
- **Partner**: Information providers, organizations, institutional content sources
- **Public Servant**: Government officials, civic leaders, public sector representatives

#### Persona Development Process

For each target group identified in the trigger map:

##### Basic Information
- **Alliterative Name**: Following naming convention
- **User Type**: Classification mapping to project brief user types
- **Demographics**: Age, situation, key characteristics from target group analysis
- **Context**: Relevant background and circumstances

##### Detailed Usage Goals & Driving Forces
**Expand from trigger map usage goals into specific persona motivations**:

**Positive Usage Goals** - what persona wants to achieve:
- Start with action words: "Wants to...", "Wishes to...", "Prefers to...", "Would like to..."
- Focus on emotional outcomes and desired experiences
- Connect directly to trigger map insights about target group motivations

**Negative Usage Goals** - what persona wants to avoid:
- Start with avoidance words: "Fears...", "Doesn't want...", "Wishes to avoid...", "Would not have happen..."
- Identify pain points and negative scenarios
- Address concerns and friction points

##### Individual Persona Files

**File Naming Convention**: `Docs/B. Trigger Map/[priority-number]-[persona-name-slug].md`

**Examples**:
- `01-sture-social.md`
- `02-clara-curlingmum.md`  
- `03-ellen-entrepreneur.md`
- `04-patricia-partner.md`

**Content Structure**:
```markdown
# [Persona Name] - [User Type]

**User Type**: [Classification]

## Persona Overview
[Demographics, situation, context expanded from target group]

## Usage Goals & Driving Forces

### Positive Usage Goals (What [Name] wants to achieve)
- ✅ [Detailed goal from trigger map analysis]
- ✅ [Additional specific motivations]
- ✅ [Emotional outcomes desired]

### Negative Usage Goals (What [Name] wants to avoid)  
- ❌ [Specific fears from trigger map]
- ❌ [Pain points to address]
- ❌ [Negative scenarios to prevent]
```

## Document Standards

### Terminology in Final Documents
- **Business Goals Section**: Use "Business Visions" and "Hard Goals" as headings (remove "soft" label)
- **Usage Goals Format**: Structure with clear positive/negative indicators
- **Clean Presentation**: Avoid workshop terminology clutter in final documents

### Visualization Requirements
- **Always Create Poster**: Simultaneously update trigger map poster with any trigger map changes
- **Mermaid Structure**: Left-to-right flowchart with business goals → platform → target groups → driving forces
- **GitHub Compatibility**: Light gray professional color palette, avoid complexity that breaks rendering
- **Placement**: Mermaid diagram at top underneath headline

## Expected Outcomes

### Primary Deliverables
1. **Trigger Map Document** (`Docs/B. Trigger Map/00-trigger-map.md`)
2. **Trigger Map Poster** (`Docs/B. Trigger Map/00-trigger-map-poster.md`)
3. **Individual Persona Files** (numbered 01, 02, 03... by priority with alliterative names and detailed usage goals)

### Strategic Value
- **Development Prioritization**: Clear guidance on what to build first
- **Design Decision Framework**: User driving forces guide interface and content choices
- **Stakeholder Alignment**: Visual map everyone can understand and reference
- **Testing Script Foundation**: Usage goals become basis for user testing questions

## Integration with Other Methods

### Builds on Product Brief
Uses user types, business context, and strategic foundation from product brief discovery

### Creates Complete User Foundation
Delivers both strategic mapping AND detailed personas in single integrated workshop process

### Guides Technical Planning
Strategic insights, priority order, and detailed personas inform development roadmap and technical architecture

## Quality Assurance

### Process Quality
- **One Question at a Time**: Never flood users with multiple questions simultaneously
- **Mandatory Stops**: Wait for user input before proceeding to next step
- **Positive Reflection**: Acknowledge and build upon each user response
- **Complete Coverage**: All business goals, target groups, and usage goals thoroughly explored

### Output Quality
- **Visual Clarity**: Trigger map poster renders properly on GitHub and communicates effectively
- **Strategic Usefulness**: Provides clear development priorities and decision framework
- **User Connection**: All personas and goals trace back to real user needs and business objectives
- **Persona Quality**: All personas follow alliterative naming, map to user types, and have actionable usage goals
- **Executive Readiness**: Documents serve as effective communication tools for stakeholders

## Common Pitfalls to Avoid

### Workshop Process
- **Skipping Elicitation**: Never assume or create content without user input
- **Rushing Through Steps**: Maintain mandatory stops and wait for user responses
- **Generic Target Groups**: Ensure groups have distinct, real differences in needs and motivations

### Persona Development
- **Non-Alliterative Names**: Always follow first name + role descriptor naming convention
- **Missing User Type Classification**: Every persona must map to project brief user types
- **Vague Usage Goals**: Ensure goals are specific, emotional, and actionable
- **Wrong Repository**: Create persona files in project repository, not expansion pack repository

### Documentation
- **Forgetting Poster Updates**: Always update visualization when trigger map changes
- **Complex Mermaid Diagrams**: Keep diagrams simple enough to render properly on GitHub
- **Disconnected Documentation**: Ensure all personas trace back to trigger map target groups

---

**Related Methods**: [01. Product Brief Discovery](01-product-brief-discovery.md) | [03. Sketch-to-Spec](03-sketch-to-spec.md)  
**Agent**: Business Analyst with collaborative workshop capabilities  
**Foundation**: Effect Mapping methodology by Inuse, Sweden  
**Typical Duration**: 60-120 minutes depending on number of target groups and persona detail complexity
