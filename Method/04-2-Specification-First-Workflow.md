# 04-2 Specification-First Workflow

## Quality Control for Implementation

---

## Core Principle

**Specifications are the single source of truth.**

All implementation must flow from documented specifications. Never implement features, content, styling, or behavior that exists only in code. 

**Why this matters:** When everyone works from the same documented specifications, the team stays aligned, design decisions are preserved, and future developers understand the intent behind every choice. This prevents costly rework and maintains quality.

---

## The Specification-First Workflow

### Step 1: Check the Specification 📋

Before implementing any feature or making any code change:

1. **Locate the relevant specification document**
   - Navigate to the appropriate `.md` file in `docs/C-Scenarios/`
   - Find the specific Object ID or section

2. **Read the specification thoroughly**
   - Content (all language variants)
   - Styling (visual properties, Tailwind classes)
   - Behavior (interactions, state changes)
   - Technical requirements (validation, APIs, data flow)

3. **Assess completeness**
   - Is all necessary information present?
   - Are there gaps, ambiguities, or placeholders?
   - Does the spec provide enough detail for implementation?

---

### Step 2: Flag Missing Information 🚨

When you notice incomplete or missing information, **stop and alert the designer/PM**. This prevents implementing features that will need to be rebuilt later and ensures everyone stays aligned.

**Alert template:**

```
📋 Specification Review Needed

Object ID: [object-id]
Location: [file-path, line number]

Current specification:
[quote current spec]

To implement this accurately, it would be helpful to have:
- [ ] Content copy (SE/EN) - Ensures consistent messaging
- [ ] Styling details (colors, spacing, typography) - Maintains design system
- [ ] Interaction behavior (onClick, onChange, validation) - Creates expected UX
- [ ] Error states/messages - Helps users recover from issues
- [ ] Success states/feedback - Confirms actions to users
- [ ] Technical requirements (API calls, data structure) - Enables proper integration

Reason this matters:
[Brief explanation of why this information helps create better implementation]

Would you like me to propose specification updates based on best practices?
```

**Information that's often helpful to clarify:**
- Placeholder text that might need actual content
- Generic descriptions that could benefit from specific details
- Language variants to ensure bilingual consistency
- Styling specifics to maintain design system integrity
- Interaction patterns to create intuitive user experiences
- Error messages to support users when things go wrong
- Data structures to ensure proper technical integration

---

### Step 3: Propose Specification Updates 💡

Once flagged, propose specific, actionable updates:

```
PROPOSED SPECIFICATION UPDATE

File: [path-to-file.md]
Section: [section-name]
Object ID: [object-id]

Add/Update:

**[Object Component Name]**
**OBJECT ID**: `object-id`
- **Content**:
  - SE: "[Swedish text]"
  - EN: "[English text]"
- **Styling**: [Specific Tailwind classes or CSS properties]
- **Purpose**: [Why this element exists, what problem it solves]
- **Interaction**: [onClick/onChange/onBlur behavior, what happens]
- **States**: [Default, hover, active, disabled, error, success]
- **Validation**: [Rules, error messages per language]
- **Technical**: [API endpoints, data structure, dependencies]

Rationale:
[Why these specific details, UX considerations, business logic]
```

**Wait for approval before proceeding.** This ensures the specifications reflect the team's shared vision and prevents implementing something that will need to change.

---

### Step 4: Update Specification First ✅

After approval:

1. **Update the `.md` file**
   - Add all approved content
   - Follow existing formatting and structure
   - Place content in the correct section with proper Object IDs
   - Ensure language variants are on separate lines

2. **Verify completeness**
   - All required information is now documented
   - Follows WPS2C documentation standards
   - Links to relevant components in Design System

3. **Commit specification changes**
   - Clear commit message: "docs: Add [feature] specification to [file]"
   - Separate commit from implementation

---

### Step 5: Implement Based on Specification 💻

Now and only now, write code:

1. **Reference the specification**
   - Quote relevant Object IDs
   - Cite specific content, styling, and behavior from spec
   - Example: *"Implementing `profile-setup-preview-terms` as specified in 1.3-Profile-Setup.md:275-281"*

2. **Implement exactly what's documented**
   - Use specified content verbatim
   - Apply documented styling
   - Follow specified interaction patterns
   - Implement all states and validations

3. **Implement exactly what's specified**
   - Don't add features not in the spec
   - Don't change wording or styling
   - Don't skip documented requirements
   - When you have ideas for improvements, propose them as spec updates first
   
   **Why this matters:** Staying true to specifications maintains team alignment and ensures everyone reviewed and approved what gets built.

4. **Add implementation notes**
   - Comment code with Object IDs for traceability
   - Note any technical decisions made within spec constraints
   - Document any libraries or dependencies used

---

## Examples

### ❌ Don't Do This

**Scenario:** Designer asks "Is there copy for this part?"

```
Designer: "Is there copy for this part?"

AI: *Immediately writes HTML/JS with new content*
AI: "I've added this text: [content]"
```

**Why this doesn't work:**
- No specification check means no alignment
- Content only in code can't be reviewed by the team
- Design decisions are lost
- Future developers won't understand the intent

---

### ✅ Do This Instead

**Scenario:** Designer asks "Is there copy for this part?"

```
Designer: "Is there copy for this part?"

AI: "📋 Let me check the specification...

⚠️ SPECIFICATION INCOMPLETE

Object ID: profile-setup-preview-terms
Location: 1.3-Profile-Setup.md:275-278

Current specification:
'Visual representation: Horizontal gray lines (skeleton text)'

Missing information:
- [ ] Actual content copy (SE/EN)
- [ ] Styling details (font size, color, line spacing)
- [ ] Purpose explanation

Reason: Users need actual preview text to understand what 
they're accepting, not just placeholder lines.

Should I propose specification updates?"

Designer: "Yes, please propose."

AI: "PROPOSED SPECIFICATION UPDATE

File: 1.3-Profile-Setup.md
Section: Terms Acceptance
Object ID: profile-setup-preview-terms

Update lines 275-278:

**Terms Preview Display**
**OBJECT ID**: `profile-setup-preview-terms`
- **Content**:
  - SE: 'Genom att använda Dog Week godkänner du att dela 
        schemaläggningsinformation med dina familjemedlemmar. 
        Vi skyddar din integritet och kommer aldrig att sälja 
        dina uppgifter. Du kan radera ditt konto när som helst.'
  - EN: 'By using Dog Week, you agree to share scheduling 
        information with your family members. We protect your 
        privacy and will never sell your data. You can delete 
        your account at any time.'
- **Styling**: Small text (text-xs), gray color (text-gray-600), 
              relaxed line spacing
- **Purpose**: Shows brief summary of key terms to give users 
              context before accepting
- **Interaction**: Static display, changes with language selector

Rationale: Transparency and user trust. Users should see a 
clear summary of what they're accepting, not skeleton placeholders.

Should I proceed with this update?"

Designer: "Yes, approved."

AI: "✅ Specification updated in 1.3-Profile-Setup.md
Now implementing based on specification..."
```

---

## Checklist for AI Agents & Developers

### Before Writing Any Code

- [ ] I have read the complete specification for this feature
- [ ] All content (SE/EN) is documented in the spec
- [ ] All styling details are specified
- [ ] All interaction behaviors are documented
- [ ] All error states and messages are defined
- [ ] All validation rules are specified
- [ ] I have flagged any missing information
- [ ] I have received approval for any proposed spec updates
- [ ] Specifications are updated and committed

### During Implementation

- [ ] I am implementing exactly what's in the specification (no additions, no changes)
- [ ] I am using Object IDs as specified
- [ ] I am using content verbatim from the spec
- [ ] I am applying styling as documented
- [ ] I am implementing interactions as specified
- [ ] I am not adding undocumented features
- [ ] I am referencing the spec in my code comments

### After Implementation

- [ ] My code matches the specification exactly
- [ ] No content exists only in code (all content is in specs)
- [ ] No styling decisions exist only in code (all styling is in specs)
- [ ] No behavior exists only in code (all behavior is in specs)
- [ ] Object IDs are traceable from spec to code
- [ ] I can point to spec sections for every implementation decision

---

## Why This Matters

### For Designers
- **Design decisions are preserved** - Your intent is documented, not lost in code
- **Consistent implementation** - Developers build exactly what you specified
- **Future changes are traceable** - Know what was intended vs. what was built

### For Developers
- **Clear requirements** - No guessing, no assumptions
- **Implementation confidence** - Spec tells you exactly what to build
- **Maintenance clarity** - Understand why things were built this way

### For Project Managers
- **Traceability** - Requirements → Spec → Code is clear
- **Quality assurance** - Easy to verify implementation matches spec
- **Team alignment** - Everyone works from same source of truth

### For Future AI Agents
- **Context preservation** - Understand design decisions without reverse-engineering
- **Consistent behavior** - Follow documented patterns, not code patterns
- **Quality maintenance** - Uphold standards across sessions

---

## Integration with WPS2C Phases

This workflow primarily applies to:

- **Phase 4: Conceptual Documentation** - Where specifications are created
- **Phase 5: PRD-2 Functional Requirements** - Where technical specs are defined
- **Phase 7: Development Workflow** - Where implementation happens

**Key principle:** Never skip Phase 4 or Phase 5 to jump directly to Phase 7.

---

## Tools & Templates

### Specification Completeness Check Template

```markdown
## Specification Review: [Feature Name]

**File:** [path-to-spec.md]
**Section:** [section-name]
**Object IDs:** [list-of-object-ids]

### Completeness Assessment

#### Content
- [ ] All text content documented (SE/EN)
- [ ] Placeholders replaced with actual copy
- [ ] All language variants present

#### Styling
- [ ] Visual design specified (colors, spacing, typography)
- [ ] Tailwind classes documented or CSS properties defined
- [ ] Responsive behavior specified

#### Behavior
- [ ] All interactions documented (onClick, onChange, etc.)
- [ ] State changes defined (hover, active, disabled)
- [ ] Transitions/animations specified if applicable

#### Validation & Errors
- [ ] Validation rules documented
- [ ] Error messages defined (SE/EN)
- [ ] Success feedback specified

#### Technical
- [ ] API endpoints/data structure documented
- [ ] Dependencies listed (libraries, components)
- [ ] Performance requirements noted

### Missing Information
[List anything incomplete or unclear]

### Proposed Updates
[Detailed proposals for spec updates]
```

---

## 🚨 Specification Red Flags

**Stop and propose spec updates when you see:**

| Pattern | Why It's a Problem | What to Do |
|---------|-------------------|------------|
| "Lorem ipsum" or placeholder text | Real content is needed to assess layout and length | Propose actual content or flag for copywriting |
| "TBD" or "To be determined" | Creates ambiguity and rework | Resolve before implementing |
| "Styled appropriately" | Too vague for consistent implementation | Define specific styling (colors, spacing, typography) |
| "When user clicks..." without outcome | Interaction is incomplete | Define what happens, including states and feedback |
| Generic errors like "Error occurred" | Doesn't help users recover | Specify error messages per scenario (SE/EN) |
| Missing language variants | Incomplete translations | Ensure both SE and EN are defined |
| Skeleton UI without content plan | Layout needs real content | Define actual text to reveal spacing needs |
| "Similar to X" without details | Creates assumptions | Specify explicitly, even if similar to existing |
| Undefined validation rules | Unpredictable user experience | Define rules, error messages, and formatting |
| Missing API contracts | Integration will be guesswork | Document endpoints, data structure, responses |

---

## Success Criteria

**Specification-First workflow is successful when:**

✅ Any developer/AI can read spec and know exactly what to build
✅ No questions about content, styling, or behavior
✅ Implementation can be verified against spec
✅ Design intent is clear and preserved
✅ Future changes can reference original specifications
✅ No "hidden" features exist only in code

---

## Next Steps

After mastering this workflow:

1. Review [04-Conceptual-Documentation.md](04-Conceptual-Documentation.md) for specification writing guidelines
2. Review [04-1-Object-ID-Specification-Guide.md](04-1-Object-ID-Specification-Guide.md) for Object ID standards
3. Apply this workflow to all implementation tasks
4. Train team members on specification-first approach
5. Conduct specification reviews before implementation sprints

---

**Remember:** Taking time to update specifications saves far more time in implementation, maintenance, and future changes. Specifications are not overhead—they are the foundation of quality.

