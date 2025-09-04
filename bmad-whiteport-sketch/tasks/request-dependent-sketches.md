# request-dependent-sketches

## Task Description
Enthusiastically identify and request all sketches connected to pages being modified in the current development task using professional, cheerful tone with clear search paths in bullet list format. Present clear warnings if visual guidance is missing or unclear, as visual design intent cannot be conveyed through written specifications alone.

## Purpose
Ensure proper visual design implementation by consulting sketches that provide essential spatial relationships, component integration patterns, visual hierarchy, and user experience flow that are impossible to describe in text specifications.

## Critical Understanding
**Visual design intent cannot be conveyed through written specifications alone.** Sketches provide:
- **Spatial Relationships**: Exact positioning and layout of elements
- **Component Integration**: How elements nest, flow, and connect visually
- **Visual Hierarchy**: Importance and relationship of UI elements
- **User Experience Flow**: How users will actually interact with the interface
- **Design Intent**: The "why" behind positioning and visual decisions

## Steps

### 1. Story Analysis for UI Components
- Identify all UI components mentioned in the story requirements
- List all pages or views that will be modified or created
- Identify existing components that will be enhanced or modified
- Document any new UI elements that need to be positioned

### 2. Scenario Documentation Search
- Search scenario documentation for references to the identified pages/components
- Look for scenario steps that mention the UI elements being developed
- Identify sketch files referenced in scenario documentation
- Map which sketches correspond to which story requirements

### 3. Sketch Request Formation
- Create specific list of sketch files needed for complete visual guidance
- Identify the exact UI elements or page sections that each sketch should show
- Prioritize sketches based on implementation dependency order
- Format enthusiastic, professional request with clear search paths in bullet list format
- Use cheerful, smooth tone while maintaining professionalism

### 4. Visual Guidance Assessment
- Review available sketches for completeness and clarity
- Identify any UI positioning that is unclear or ambiguous in sketches
- Document any conflicts between sketch design and story requirements
- Assess if sketches provide sufficient detail for implementation

### 5. Gap Identification and Warning
- **CRITICAL**: If sketches are missing for UI components, present this as a BLOCKER
- Document specific visual guidance gaps that prevent proper implementation
- Warn about potential implementation divergence without proper visual guidance
- Request clarification for any unclear positioning or integration patterns

### 6. Implementation Guidance Extraction
- Extract exact positioning requirements from sketches
- Document component integration patterns shown in visual design
- Identify styling requirements and visual relationships
- Map user interaction patterns depicted in sketches

## Output Requirements
- **Sketch Request List**: Specific sketches needed with clear identification of what they should show
- **Visual Guidance Assessment**: Evaluation of available sketch completeness
- **Implementation Roadmap**: How sketches will guide implementation decisions
- **Gap Warnings**: Clear warnings about missing or unclear visual guidance
- **Blocker Identification**: Any missing sketches that prevent proper implementation

## Request Format Example
```
## 🎨 Fantastic! Let's Get Started with [TASK NAME]! 🚀

Hey there! 😊 I'm excited to work on [TASK DESCRIPTION]! 

Following our enhanced WPS2C methodology, I need to consult the relevant sketches before I dive into the implementation. This ensures I get the placement exactly right from the start! 

**Could you please make these sketches available for me to analyze?** 📋

### 🎯 Required Sketches for [FEATURE NAME]:

• **`sketch-filename.jpg`**  
  **Search Path**: `path/to/sketch/location/sketch-filename.jpg`  
  **Purpose**: Description of what this sketch should show

[Additional sketches as needed]

This will help me understand the exact spatial relationships, visual hierarchy, and design intent! 

Once I can see the design, I'll be able to implement with perfect sketch compliance! 🎯✨

**Ready to make this awesome!** 💪
```

## Warning Protocols

### Missing Sketch Warning
```
⚠️ VISUAL GUIDANCE WARNING ⚠️
Missing sketches for [SPECIFIC UI ELEMENTS]. 
Visual design intent cannot be conveyed through written specifications alone.
Implementation may diverge from design intent without proper visual guidance.
REQUEST: Please provide sketches showing [SPECIFIC REQUIREMENTS].
```

### Unclear Positioning Warning  
```
⚠️ POSITIONING AMBIGUITY WARNING ⚠️
Sketch shows [SPECIFIC ELEMENT] but positioning relative to [OTHER ELEMENTS] is unclear.
Need clarification on [SPECIFIC POSITIONING QUESTIONS].
```

## Success Criteria
- ✅ All UI components have corresponding sketch guidance
- ✅ Positioning and integration patterns are clearly defined in sketches
- ✅ Any missing visual guidance is flagged as blocker before implementation
- ✅ Implementation approach is confirmed against visual design intent
- ✅ Designer is informed of any visual guidance gaps

## Professional Standards
- **Never proceed with UI implementation without proper sketch consultation**
- **Always flag missing visual guidance as blocker rather than making assumptions**
- **Respect the collaborative investment in design specifications and sketches**
- **Ensure implementation matches design intent rather than developer assumptions**
