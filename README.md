# Whiteport Sketch-to-Code for Bmad method

> **Transform hand-drawn sketches into production-ready applications through AI-powered collaborative design workshops. Conceptual developement, UX-Design and project management extension pack BMad Expansion Pack for the BMad method**

## What This Expansion Pack Provides

When you combine the **BMad AI agent framework** with the **Whiteport Sketch-to-Code expansion pack**, you get:

### Enhanced Value Proposition
- **From Sketches to Code**: Transform hand-drawn UI concepts directly into technical specifications and implementation plans
- **Collaborative Workshops**: Structured facilitation that builds requirements through dialogue rather than assumptions
- **Design-First Development**: Start with user experience and visual concepts, then systematically derive technical requirements

### What You Gain Over Standard BMad
- **Complete Agile AI Agent Framework**: BMad provides end-to-end project management, development, and testing capabilities through specialized AI agents working in coordinated workflows
- **3 New Specialized AI Agents**: Business Analyst, PM, and UX Expert with design-focused capabilities that integrate seamlessly with BMad's agile agent ecosystem
- **Proven Workshop Methodologies**: Effect Mapping for trigger maps, structured product brief discovery, systematic persona development
- **Professional Documentation Standards**: Executive-ready artifacts with embedded visualizations and consistent terminology
- **Sketch Documentation Pipeline**: From hand-drawn concepts through component libraries to implementation specifications

## The Whiteport Method

This expansion pack introduces a comprehensive design-driven development methodology that enhances BMad with specialized workflows for transforming visual concepts into production applications.

### [📋 Complete Method Overview](Method/00-whiteport-method.md)

#### 🎯 [01. Product Brief Discovery](Method/01-product-brief-discovery.md)
**Purpose**: Foundation-setting through conversational discovery  
**Process**: Adaptive questioning with progressive document building  
**Outcome**: Strategic project foundation with market analysis and technical architecture  

#### 🗺️ [02. Trigger Map Workshop](Method/02-trigger-map-workshop.md)  
**Purpose**: Align business goals with user needs through Effect Mapping AND create detailed personas  
**Process**: Strict step-by-step collaborative elicitation plus persona development  
**Outcome**: Visual map connecting business objectives to user driving forces PLUS prioritized personas with alliterative names and detailed usage goals  

#### 📱 [03. Sketch-to-Spec](Method/03-sketch-to-spec.md)
**Purpose**: Transform hand-drawn UI into systematic component specifications  
**Process**: Atomic design principles with reusability focus  
**Outcome**: Organized component specifications for development  

### Core Philosophy

**Design-First Development**: Start with visual concepts and user experience sketches, then systematically transform them into technical requirements and implementation code.

**Collaborative Workshop Approach**: Structured elicitation processes that build requirements through step-by-step dialogue rather than assumptions.

**Geographic-Aware Documentation**: Specialized for location-based applications with geo-tagging and proximity-based features.

## Expansion Pack Components

### Enhanced Agents

#### Whiteport Business Analyst (`whiteport-analyst.md`)
- **Primary Role**: Project discovery and user research coordination
- **Key Enhancement**: Collaborative workshop methodology with mandatory step-by-step elicitation
- **New Commands**: `create-product-brief`, `create-trigger-map`, `create-executive-readme`
- **Workflow**: Foundational discovery → Product brief creation → Trigger map development → Persona definition

#### PM Agent (`whiteport-pm.md`)
- **Primary Role**: Sketch-to-Code Product Manager
- **Key Enhancement**: Technical requirements from user research
- **Commands**: `create-prd-from-research`, `create-backend-foundation`, `parallel-backend-setup`

#### UX Expert (`ux-expert.md`)
- **Primary Role**: Design analysis and component extraction
- **Key Enhancement**: Hand-drawn sketch interpretation and systematic UI component library creation

### Core Methodology

#### 1. Product Brief Creation
- **Purpose**: Strategic foundation and project scoping
- **Process**: Conversational discovery with adaptive follow-up questions
- **Output**: Comprehensive project brief with market analysis, technical architecture, user types
- **Location**: `Docs/A. Product Brief/brief.md`

#### 2. Trigger Map Workshop
- **Purpose**: Business goal alignment with user needs and driving forces
- **Process**: Strict step-by-step collaborative elicitation
- **Method**: Effect Mapping methodology adapted for digital products
- **Outputs**: 
  - Trigger map document (`Docs/B. Trigger Map/00-trigger-map.md`)
  - Visual trigger map poster (`Docs/B. Trigger Map/00-trigger-map-poster.md`)
  - Individual persona profiles (numbered 01, 02, 03...)

#### 3. Persona Development
- **Standards**: Alliterative naming convention (e.g., "Sture Social", "Ellen Entrepreneur")
- **Classification**: Each persona maps to user types defined in project brief
- **Structure**: User type, demographics, usage goals (positive/negative driving forces)
- **Location**: `Docs/B. Trigger Map/` (numbered by priority)

#### 4. Scenario Documentation
- **Structure**: Numbered scenario-based organization
- **Location**: `Docs/C. Scenarios/1. Signup/1.1 Public-start-page/`
- **Content**: Page sketches, user flows, interaction specifications

#### 5. Component Library
- **Structure**: Atomic design principles
- **Location**: `Docs/D. Components/`
- **Content**: Reusable UI components extracted from scenarios

### Documentation Standards

#### File Organization
```
Docs/
├── A. Product Brief/
│   ├── brief.md
│   └── user-generated-content-strategy.md
├── B. Trigger Map/
│   ├── 00-trigger-map.md
│   ├── 00-trigger-map-poster.md
│   ├── 01-primary-persona.md
│   ├── 02-secondary-persona.md
│   └── ...
├── C. Scenarios/
│   ├── 1. Signup/
│   │   ├── 1.1 Public-start-page/
│   │   └── 1.2 Registration-form/
│   └── 2. Dashboard/
└── D. Components/
    ├── atomic/
    ├── molecular/
    └── organisms/
```

#### Writing Style Guidelines
- **No Parentheses**: Use dashes, colons, or separate sentences instead
- **Progressive Building**: Documents grow incrementally during workshops
- **Positive Reflection**: Acknowledge and build upon user input
- **Clear Terminology**: Consistent vocabulary throughout documentation

#### Mermaid Diagram Standards
- **GitHub Compatibility**: Light gray color palette, left-to-right flow
- **Structure**: Business goals → Platform → Target groups → Driving forces
- **Styling**: Professional monochromatic appearance
- **Placement**: Diagrams at top of poster documents, under headlines

### Key Methodological Innovations

#### Multiple Target Groups per User Type
Instead of "persona splitting," define multiple target groups from the same user type when they have different needs and driving forces. Example: Both "Active Community Connector" and "Time-Pressed Parent" are Reader user types but represent distinct target groups.

#### Draft-First Trigger Map Option
When substantial project brief information exists, offer users the choice between:
- **Traditional Step-by-Step**: Complete workshop elicitation process
- **Draft-First Approach**: Create initial trigger map from brief, then refine collaboratively

#### Executive-Ready Documentation
All major artifacts include executive summary README files with embedded visualizations serving as project dashboards and navigation hubs.

## Installation & Setup

### Prerequisites
- **BMad Framework v2.0+**: This expansion requires the core BMad AI agent framework
- **Compatible IDE**: Tested with Cursor, VSCode, and other BMad-compatible environments

### Installation Steps
1. **Install BMad Core**: Ensure the base framework is properly configured
2. **Download Expansion Pack**: Clone or download this repository to your BMad expansion directory
3. **Activate Whiteport Method**: Use `@whiteport-analyst.md` to begin with enhanced capabilities

### ⚠️ Important: Expansion Pack Precedence
**This Whiteport expansion pack OVERRIDES default BMad functionality**. When active:
- Uses alphabetized folder structure: `A. Product Brief/`, `B. Trigger Map/`, `C. Scenarios/`, `D. Components/`
- Whiteport task instructions take precedence over standard BMad tasks
- File naming and organization follows Whiteport standards as specified in templates
- Agent commands use enhanced collaborative workshop approach

## Implementation Guidelines

### For Development Teams
1. **Verify BMad Installation**: Ensure core framework is properly configured
2. **Load Expansion Pack**: Place in BMad expansion directory
3. **Start with Product Brief**: Always begin foundational discovery with enhanced Analyst
4. **Follow Method Sequence**: Product Brief → Trigger Map → Personas → Scenarios → Components

### For Project Managers
1. **Start with Product Brief**: Always begin with foundational discovery
2. **Use Collaborative Approach**: Follow step-by-step elicitation, never assume answers
3. **Build Progressively**: Documents grow during workshops, not after
4. **Validate Continuously**: Confirm user satisfaction before proceeding to next phase

### For UX Designers
1. **Sketch-First Approach**: Hand-drawn concepts drive technical requirements
2. **Component Thinking**: Extract reusable elements systematically
3. **User-Centered Documentation**: All decisions traced back to persona needs
4. **Geographic Awareness**: Consider location-based features in all designs

## Quality Assurance

### Workshop Effectiveness
- **One Question at a Time**: Never flood users with multiple questions
- **Mandatory Stops**: Wait for user input before proceeding to next step
- **Positive Acknowledgment**: Reflect on and appreciate each user response
- **Progress Indicators**: Keep users engaged with remaining question counts

### Documentation Quality
- **Alliterative Persona Names**: Ensures memorability and professional consistency
- **User Type Mapping**: All personas connect to business model user types
- **Poster Creation**: Always update trigger map visualization with trigger map changes
- **GitHub Compatibility**: All Mermaid diagrams render properly on GitHub

### Technical Integration
- **WordPress Optimization**: Templates optimized for WordPress development
- **Social Stream Plugin**: Integration with Whiteport Social Stream Plugin
- **Geo-tagging Support**: Geographic features as first-class citizens
- **AI Agent Architecture**: Designed for AI monitoring and content generation workflows

## Version History

See [RELEASES.md](RELEASES.md) for detailed version information and updates.

## Support & Documentation

- **Method Questions**: Refer to task files in `.bmad-core/tasks/`
- **Template Customization**: Modify templates in `.bmad-core/templates/`
- **Agent Behavior**: Review agent configurations in `.bmad-core/agents/`
- **Data Standards**: Check `.bmad-core/data/` for methodology guidelines

## License & Attribution

This expansion pack builds upon the BMad framework and incorporates methodologies from:
- Effect Mapping (Inuse, Sweden)
- Atomic Design Principles
- Whiteport AB design methodologies

---

**Developed by**: Whiteport AB  
**Compatible with**: BMad Framework v2.0+  
**Last Updated**: 2024
