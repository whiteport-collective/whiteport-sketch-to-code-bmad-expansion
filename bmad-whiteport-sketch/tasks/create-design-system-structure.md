# Create Design System Structure

**Task**: Create both C-Scenarios and D-Design-System folder structures during conceptual design phase  
**Agent**: whiteport-ux-expert  
**Phase**: Conceptual Design & Sketching  
**Priority**: High

## Task Overview

The UX Expert is responsible for setting up the foundation structure for both C-Scenarios and D-Design-System, then discovering components through the sketching process. This ensures that the foundation is ready, but components emerge naturally from the sketching workflow rather than being predetermined.

## Prerequisites

- Project has completed A-Product-Brief and B-Trigger-Map phases
- Conceptual design phase has begun
- Sketches are being created or referenced

## Task Steps

### **Step 1: Set Up Foundation Structure**
1. **Create C-Scenarios Folder**: Main scenarios directory
2. **Create D-Design-System Folder**: Main design system directory
3. **Create Foundation Folders**: Design tokens structure
4. **Create Basic Component Structure**: Atomic, molecular, organism folders
5. **Create Existing Components Documentation**: Document current `/components/ui/` implementations

### **Step 2: Begin Sketching Process**
1. **Start Conceptual Sketching**: Begin the sketching workflow
2. **Identify Components as You Sketch**: Components emerge from sketching process
3. **Discuss Components as Needed**: Only when components are identified through sketching
4. **Create Component Specifications**: As components are discovered through sketches
5. **Link Sketches to Components**: Connect sketches to component specifications

### **Step 3: Create Design Tokens Foundation**
1. **Colors**: Create color palette foundation
2. **Typography**: Create typography system foundation
3. **Spacing**: Create spacing scale foundation
4. **Breakpoints**: Create breakpoint system foundation

### **Step 4: Document Existing Components**
1. **Review Current Components**: Document existing `/components/ui/` implementations
2. **Create Component Overview**: Document what components already exist
3. **Integration Planning**: Plan how to integrate with design system

### **Step 5: Component Discovery Through Sketching**
1. **Sketch and Identify**: Components emerge as you sketch
2. **Discuss as Needed**: Only discuss components when they're identified through sketching
3. **Create Specifications**: Create component specifications as discovered
4. **Link to Sketches**: Connect components to the sketches that identified them

## Folder Structures

### **C-Scenarios Structure (Example)**
```
C-Scenarios/
├── 01-[Scenario-Category-1]/
│   ├── 1.1-[Scenario-Name]/
│   │   ├── 1.1-[Scenario-Name]-Synopsis.md
│   │   ├── Sketches/
│   │   └── Frontend/
│   └── 1.2-[Another-Scenario]/
│       ├── 1.2-[Another-Scenario]-Synopsis.md
│       └── Sketches/
├── 02-[Scenario-Category-2]/
│   ├── 2.1-[Scenario-Name]/
│   └── 2.2-[Another-Scenario]/
└── 03-[Scenario-Category-3]/
    ├── 3.1-[Scenario-Name]/
    └── 3.2-[Another-Scenario]/
```

### **D-Design-System Structure**

### **Foundation (Always Created)**
```
02-Foundation/
├── 00-Foundation-Overview.md
├── 01-Colors/
│   └── Color-Palette.md
├── 02-Typography/
│   └── Typography-System.md
├── 03-Spacing/
│   └── Spacing-System.md
└── 04-Breakpoints/
    └── Breakpoint-System.md
```

### **Atomic Components (Only Referenced)**
```
03-Atomic-Components/
├── 00-Atomic-Components-Overview.md
├── 01-Buttons/
│   ├── Primary-Button-Specification.md
│   └── CTA-Button-Primary-Specification.md
├── 02-Inputs/
│   └── Text-Input-Specification.md
├── 03-Icons/
│   └── Icon-System-Specification.md
├── 04-Cards/
│   └── Basic-Card-Specification.md
├── 05-Badges/
│   └── Status-Badge-Specification.md
└── 06-Existing-Components/
    └── Existing-Components-Overview.md
```

### **Molecular Components (Only Referenced)**
```
04-Molecular-Components/
├── 00-Molecular-Components-Overview.md
└── 01-Trust-Indicators/
    └── Trust-Indicators-Specification.md
```

### **Organism Components (Only Referenced)**
```
05-Organism-Components/
├── 00-Organism-Components-Overview.md
├── 01-Hero-Section/
│   └── Hero-Section-Specification.md
└── 02-Navigation-Header/
    └── Navigation-Header-Specification.md
```

## Quality Standards

### **WPS2C Compliance**
- **Three-File Structure**: Every component has specification, sketch, and code
- **Design Tokens**: Consistent use of foundation tokens
- **Accessibility**: WCAG 2.1 AA compliance built-in
- **Swedish Focus**: Cultural sensitivity and localization

### **No Speculation**
- **Only Referenced**: Create components only if mentioned in sketches
- **No Bloat**: Avoid unnecessary components or complexity
- **Real Value**: Every component serves a specific purpose
- **Focused Approach**: Lean, practical design system

## Success Criteria

### **Structure Created**
- [ ] D-Design-System folder structure created
- [ ] Foundation design tokens implemented
- [ ] Only referenced components included
- [ ] Three-file structure for each component

### **Quality Assured**
- [ ] WPS2C compliance maintained
- [ ] Accessibility standards met
- [ ] Swedish cultural sensitivity integrated
- [ ] Design tokens used consistently

### **Documentation Complete**
- [ ] Component specifications created
- [ ] Usage guidelines documented
- [ ] Examples provided
- [ ] Testing requirements defined

## Integration with Workflow

### **During Conceptual Design**
- **Sketch Analysis**: Identify components as sketches are created
- **Structure Growth**: Add components only when referenced
- **Token Usage**: Use design tokens consistently
- **Quality Assurance**: Maintain WPS2C standards

### **During Sketching Process**
- **Component Identification**: Identify reusable components
- **Specification Creation**: Create component specifications
- **Sketch Integration**: Link sketches to specifications
- **Code Generation**: Create React components

## Examples

### **Component Creation Process**
1. **Sketch Analysis**: "This sketch shows a CTA button"
2. **Component Check**: "Is CTA button referenced in sketches? Yes"
3. **Structure Creation**: Create `03-Atomic-Components/01-Buttons/CTA-Button-Primary/`
4. **Specification**: Create `CTA-Button-Primary-Specification.md`
5. **Design Tokens**: Use foundation color and spacing tokens
6. **Accessibility**: Include WCAG compliance requirements

### **No Speculation Example**
- **Sketch Analysis**: "This sketch shows a complex dashboard"
- **Component Check**: "Is dashboard referenced in sketches? No"
- **Action**: "Do not create dashboard component yet"
- **Reason**: "Wait until dashboard is actually needed in sketches"

---

*This task ensures the design system grows organically based on actual project needs, avoiding speculation and maintaining focus on Swedish family requirements.*

*Created using Whiteport Sketch-to-Code BMad Expansion methodology with focus on practical design system development.*
