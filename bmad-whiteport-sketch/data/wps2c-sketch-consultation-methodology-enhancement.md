# WPS2C Sketch Consultation Methodology Enhancement

## Critical Learning from Language Selector Implementation

### What We Discovered
During E01-S01-Language-Selector-Component implementation, the developer successfully created a fully functional language selector component that met all technical requirements. However, the component was positioned separately from the navigation header instead of integrated within the navigation header object as specified in the StartPage Desktop Concept sketch.

**Root Cause**: Visual design intent cannot be conveyed through written specifications alone.

## Methodology Enhancement Required

### For UX Expert Sally 🎨

#### Enhanced Responsibilities
**Sketch Provision**: 
- Ensure all UI components have corresponding sketches showing exact placement and integration
- Make sketches accessible in scenario documentation with clear file paths
- Provide sketches that show spatial relationships, component integration, and visual hierarchy

**Developer Support**:
- Respond to developer requests for sketch clarification
- Provide additional visual guidance when component placement is unclear
- Review completed implementations for sketch compliance

**Quality Assurance**:
- Verify that sketches clearly communicate design intent
- Flag when sketches may be insufficient for proper implementation
- Ensure visual consistency across all sketch-driven components

#### Template Changes for UX Expert
- Synopsis and component templates now include mandatory sketch reference sections
- Scenario documentation must include clear sketch file paths
- Visual design verification becomes equal priority to functional requirements

### For PM Sarah 📋

#### Enhanced Story Creation Requirements
**Mandatory Sketch References**:
- Every UI story MUST include specific sketch references
- Sketch consultation becomes acceptance criteria, not optional
- Visual design compliance required in definition of done

**New Story Structure**:
```
## 🎨 Sketch Consultation Requirements
⚠️ **CRITICAL**: Visual design intent cannot be conveyed through written specifications alone
**Primary Sketch**: [Path to main design sketch]
**Pre-Development Checklist**:
- [ ] **MANDATORY**: Request all dependent sketches before development
- [ ] **ANALYZE**: Visual design intent, component placement, integration patterns
```

**Blocker Protocol**:
- Missing sketches = development blocker
- No assumptions about component placement allowed
- Clear escalation path when visual guidance is insufficient

#### Epic Management Changes
- Epic templates now include sketch dependency mapping
- Visual design excellence equal priority to functional excellence
- Sketch compliance tracking for all UI stories

### For Dev Agents 💻

#### Mandatory Pre-Development Protocol
1. **Request dependent sketches** before any UI development
2. **Analyze visual design intent** through sketch consultation
3. **Verify component placement** against sketch specifications
4. **Flag missing visual guidance** as blockers immediately

#### Updated Implementation Process
- Sketch consultation becomes step 1 of UI development
- Visual design verification required before story completion
- Component positioning must match sketch specifications exactly
- Integration patterns must follow sketch-defined relationships

## Template Updates Applied

### New Templates Created
1. **`ui-story-tmpl.yaml`** - Enhanced story template with mandatory sketch consultation
2. **`ui-epic-tmpl.yaml`** - Epic template with sketch-driven development requirements

### Enhanced Agent Instructions
- **Dev Agent**: Updated core principles to prioritize sketch consultation
- **Process Documentation**: Clear methodology for sketch-first development
- **Quality Standards**: Visual design verification as acceptance criteria

## Implementation Guidelines

### For Story Creation (PM Sarah)
1. **Engage UX Expert Sally** early to ensure sketch availability
2. **Map sketch dependencies** clearly for each story
3. **Include sketch references** in acceptance criteria
4. **Make visual design verification** part of definition of done

### For Sketch Provision (UX Expert Sally)
1. **Provide comprehensive sketches** showing component placement and integration
2. **Ensure sketch accessibility** in scenario documentation
3. **Support developer questions** about visual design intent
4. **Review implementations** for sketch compliance

### For Development (Dev Agents)
1. **HALT development** if sketches are missing or unclear
2. **Request specific sketches** from UX Expert before proceeding
3. **Verify visual design intent** through sketch analysis
4. **Match sketch specifications exactly** in implementation

## Quality Assurance Protocol

### Story Level
- [ ] Sketch references included in story requirements
- [ ] Visual design verification in acceptance criteria
- [ ] Sketch consultation documented in implementation

### Epic Level
- [ ] All UI stories have sketch dependencies mapped
- [ ] Visual design consistency across epic components
- [ ] Sketch compliance verified for epic completion

### Methodology Level
- [ ] Professional development standards maintained
- [ ] Gap identification protocol followed
- [ ] Collaborative investment in sketches respected

## Success Metrics

### Prevention of Implementation Divergence
- Zero UI components positioned incorrectly relative to sketch specifications
- All visual integration patterns follow sketch-defined relationships
- Component placement matches design intent exactly

### Enhanced Collaboration
- Clear communication between UX Expert, PM, and Dev agents
- Systematic sketch consultation process
- Professional respect for design authority and specifications

### Methodology Excellence
- Sketch-first development becomes standard practice
- Visual design verification equal priority to functional requirements
- Professional documentation of design methodology compliance

## Rollout to Team

### Immediate Actions Required
1. **UX Expert Sally**: Review scenario documentation to ensure sketch accessibility
2. **PM Sarah**: Update story creation process to include mandatory sketch references
3. **Dev Agents**: Implement sketch consultation as first step of UI development

### Template Application
- Use `ui-story-tmpl.yaml` for all future UI story creation
- Apply `ui-epic-tmpl.yaml` for epics containing UI components
- Reference this methodology enhancement in agent training

### Continuous Improvement
- Monitor sketch consultation effectiveness
- Refine templates based on implementation experience
- Document additional methodology enhancements as needed

---

**This methodology enhancement ensures that visual design intent is properly communicated and implemented, preventing the functional-but-misplaced component issue we experienced with the Language Selector.**
