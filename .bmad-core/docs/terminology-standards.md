# Whiteport Method Terminology Standards

## Overview

Consistent terminology is critical for effective collaboration across the Whiteport Sketch-to-Code method. This guide establishes standard definitions and language patterns to ensure clarity and prevent confusion during user research, design, and development phases.

## Writing Style Standards

### Parentheses Usage
- **Avoid parentheses** in all Whiteport documentation
- Use alternative structures: dashes, colons, or separate sentences
- Replace parenthetical clarifications with more explicit language
- Example: Instead of "User research (trigger maps and personas)" write "User research including trigger maps and personas"

## Core Terminology Definitions

### User Research Terms

#### **Driving Forces** (NOT "Motivations")
**Definition**: The underlying psychological and practical factors that move a persona to action.
**Usage**: "Helena's driving forces include professional recognition and work-life balance."
**Avoid**: "Helena's motivations..." or "Helena is motivated by..."

#### **Usage Goals** (NOT "Goals" or "User Goals")
**Definition**: Specific positive and negative outcomes users seek from product interaction.
**Usage**: "Sune's usage goals include private progress tracking and avoiding social comparison."
**Context**: Always specify positive vs negative usage goals

#### **Business Visions** (NOT "Business Goals")
**Definition**: High-level strategic ambitions with measurable proof points.
**Components**: 
- **Soft Goals**: Qualitative ambitions ("Everyone should be healthy and happy")
- **Hard Goals**: Measurable proof points (☑️ "15% reduction in sick days")

#### **Target User Groups** (NOT "User Segments" or "Personas")
**Definition**: Specific user types identified in trigger map phase.
**Usage**: When referring to groups before detailed persona development
**Transition**: "Target user groups" become "personas" after deep-dive development

### Technical Architecture Terms

#### **Platform Architecture** (NOT "Technical Stack")
**Definition**: Strategic allocation of features across different platforms based on persona needs.
**Usage**: "Platform architecture reflects Helena's need for admin controls and Sune's preference for mobile privacy."

#### **Persona-Justified Decisions** (NOT "User-Centered Design")
**Definition**: Technical choices explicitly linked to specific persona research insights.
**Usage**: More specific than generic user-centered approach

## Language Pattern Standards

### Positive Usage Goals Language Patterns

**Required Starters**:
- "Wants to..." 
- "Wishes to..."
- "Prefers to..."
- "Would like to..."
- "Would love to..."
- "Seeks to..."

**Examples**:
- ✅ "Wants to feel confident about program success"
- ✅ "Would like to demonstrate ROI to leadership"
- ❌ "Needs confidence" (too vague)
- ❌ "Confident program success" (not action-oriented)

### Negative Usage Goals Language Patterns

**Required Starters**:
- "Fears..."
- "Doesn't want..."
- "Wishes to avoid..."
- "Would not have...happen"
- "Dreads..."
- "Avoids..."

**Examples**:
- ✅ "Fears being seen as hypocritical about fitness"
- ✅ "Doesn't want to create additional work for busy employees"
- ❌ "Concerns about hypocrisy" (not action-oriented)
- ❌ "No extra work" (unclear what they're avoiding)

### Business Hard Goals Language Patterns

**Required Characteristics**:
- Start with measurable action verbs
- Include specific metrics or percentages
- Use checkmark symbols (☑️) for completed format

**Action Verb Starters**:
- "Achieve..."
- "Reduce..."
- "Increase..."
- "Improve..."
- "Demonstrate..."
- "Deliver..."

**Examples**:
- ✅ "☑️ Reduce sick leave days by 15% within 12 months"
- ✅ "☑️ Achieve 60% employee participation within 6 months"
- ❌ "Better employee health" (not measurable)
- ❌ "Participation rates" (no target specified)

### Persona Description Language Standards

**Rich Context Requirements**:
- Specific ages, not ranges ("29-year-old" not "late twenties")
- Concrete job titles and company contexts
- Detailed family situations and personal circumstances
- Authentic-sounding quotes and internal thoughts

**Examples**:
- ✅ "Sune is a 29-year-old software developer who arrives late but stays even later"
- ✅ "Helena, a former spinning instructor turned HR manager with two young children"
- ❌ "A busy professional in their thirties"
- ❌ "Someone who works in HR"

## Document-Specific Terminology

### Trigger Map Documents

**Required Terms**:
- "Business Visions" (section header)
- "Target User Groups" (section header) 
- "Positive Goals" and "Negative Goals" (subsection headers)
- "Driving Forces" (when discussing user motivations)

**Avoid**:
- "Business Goals" (use "Business Visions")
- "User Stories" (use "Usage Goals")
- "Pain Points" (use "Negative Goals")

### Persona Documents

**Required Terms**:
- "Usage Goals & Driving Forces" (section header)
- "Positive Usage Goals" and "Negative Usage Goals" (subsection headers)
- "Personal Relationship to [Core Activity]" (required subsection)
- "Design Implications & User Journey Considerations" (combined section)

**Avoid**:
- "Motivations" (use "Driving Forces")
- "Goals" without "Usage" qualifier
- "Pain Points" (use "Negative Usage Goals")

### Product Brief Documents

**Required Terms**:
- "Key Assumptions" (prominent section)
- "Platform Architecture" (not "Technical Architecture")
- "Target User Summary" (with persona file references)
- "MVP Scope" (not "Phase 1 Features")

## Consistency Quality Checklist

### Cross-Document Verification

#### **Terminology Consistency Check**
- [ ] "Driving Forces" used consistently instead of "Motivations"
- [ ] "Usage Goals" specified as positive/negative throughout
- [ ] "Business Visions" with soft/hard goal structure maintained
- [ ] "Target User Groups" vs "Personas" used correctly by phase

#### **Language Pattern Check**
- [ ] Positive usage goals start with approved action words
- [ ] Negative usage goals start with approved avoidance words
- [ ] Business hard goals include measurable metrics
- [ ] Persona descriptions include rich, specific context

#### **Section Header Consistency**
- [ ] Standard section headers used across similar documents
- [ ] Required subsections included (e.g., "Personal Relationship to Core Activity")
- [ ] Combined sections labeled consistently (e.g., "Design Implications & User Journey")

### Document-Specific Checks

#### **Trigger Map Quality Check**
- [ ] "Business Visions" clearly separated from "Target User Groups"
- [ ] "Positive/Negative Goals" structure consistent across user groups
- [ ] "Driving Forces" analysis included in strategic insights

#### **Persona Quality Check**
- [ ] "Usage Goals & Driving Forces" section uses standardized language
- [ ] "Personal Relationship to [Core Activity]" subsection included
- [ ] Rich context follows persona description standards

#### **Product Brief Quality Check**
- [ ] "Key Assumptions" prominently placed
- [ ] "Platform Architecture" justified through persona analysis
- [ ] Links to persona files use correct terminology

## Team Training and Reference

### Terminology Quick Reference

**When discussing user motivations**: Use "Driving Forces"
**When discussing user outcomes**: Use "Usage Goals" (positive/negative)
**When discussing business strategy**: Use "Business Visions" (soft/hard goals)
**When discussing platform decisions**: Use "Platform Architecture"
**When referencing user research**: Use "Persona-Justified Decisions"

### Common Mistakes to Avoid

#### **Terminology Mixing**
- ❌ Using "goals" for both business and user outcomes
- ❌ Switching between "motivations" and "driving forces"
- ❌ Calling personas "user segments" after development phase

#### **Language Pattern Inconsistency**
- ❌ Positive goals that don't start with action words
- ❌ Negative goals that don't clearly state avoidance
- ❌ Business goals without measurable components

#### **Context Quality Issues**
- ❌ Generic persona descriptions without rich context
- ❌ Vague usage goals that don't guide design decisions
- ❌ Business visions without clear hard goal proof points

## Implementation Guidelines

### For Agents and Team Members

#### **Before Writing Any Document**
1. Review terminology standards for document type
2. Check language pattern requirements
3. Prepare consistent section headers
4. Plan terminology usage throughout document

#### **During Document Creation**
1. Use terminology checklist for real-time validation
2. Apply language patterns consistently
3. Cross-reference with related documents for consistency
4. Include rich context following established standards

#### **After Document Completion**
1. Run full terminology consistency check
2. Validate language patterns across all sections
3. Confirm cross-document terminology alignment
4. Document any approved terminology variations

This standardization ensures clear communication, reduces confusion, and maintains professional quality across all Whiteport method deliverables.

