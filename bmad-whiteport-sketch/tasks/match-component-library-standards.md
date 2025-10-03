# Task: Match Component Library Standards

## Overview
When building a design system on top of an existing component library (like ShadCN/UI, Material UI, Ant Design, etc.), maintaining visual consistency with the library's standards creates a more cohesive experience. This task explores patterns for making custom components match the base library's styling approach.

**Note**: This is about achieving visual harmony, not strict adherence. Your project's unique needs always take priority.

## Purpose

### **Visual Cohesion Benefits**

Some teams find value in matching their custom components to the base library's aesthetic:
- **Familiar Patterns**: Users recognize consistent interaction patterns
- **Easier Maintenance**: Aligned styling conventions reduce cognitive overhead
- **Library Updates**: Easier to adopt library updates when conventions match
- **Developer Experience**: Consistent patterns make code more predictable

### **When This Matters**

**High Value**:
- Building admin dashboards with many standard components
- Extending existing library with custom variations
- Team has developers familiar with the base library
- Design system will evolve alongside library updates

**Lower Priority**:
- Highly branded, unique design language
- Custom design system from scratch
- One-off components with specific requirements
- Library is just a starting point, not a foundation

## Approach Patterns

### Pattern 1: Study the Base Library First

Before creating custom components, spend time understanding the library's conventions:

**What to Observe**:
- **Border Philosophy**: Does it use 1px or 2px borders? Solid or subtle?
- **Color Approach**: Neutral grays for defaults? When does color appear?
- **Focus Indicators**: Rings? Outlines? What color? What offset?
- **Spacing Rhythm**: 4px, 8px, 12px, 16px rhythm? Or 6px, 12px, 18px?
- **Border Radius**: Sharp? Slightly rounded (4-6px)? Very rounded (8-12px)?
- **State Transitions**: Instant? Subtle ease? Spring animations?

**Example: ShadCN/UI Patterns**
```
Border: 1px solid (subtle, gray-300)
Focus: Blue ring, 3px, offset 2px
Radius: 6-8px (moderately rounded)
Spacing: 8px rhythm (8, 16, 24, 32)
Transitions: 0.2s ease
Colors: Neutral-first, color for states
```

### Pattern 2: Input Field Styling Alignment

Input fields are often the most noticeable mismatch. Here's one approach to alignment:

**Common Library Pattern** (like ShadCN/UI):
```css
/* Typical library input styling */
.input {
  height: 40-48px;          /* Touch-friendly
  padding: 0 12px;           /* Horizontal padding
  border: 1px solid #d1d5db; /* Subtle gray border
  border-radius: 6-8px;      /* Moderate rounding
  font-size: 16px;           /* Prevent iOS zoom
  background: white;
  transition: border-color 0.2s ease;
}

.input:focus {
  border-color: #3b82f6;     /* Brand blue
  outline: none;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1); /* Focus ring
}

.input:disabled {
  background: #f3f4f6;       /* Slight gray
  color: #9ca3af;
  cursor: not-allowed;
}
```

**What Makes It Feel "Library-Standard"**:
- Subtle default styling (doesn't compete for attention)
- Clear focus state (accessibility-first)
- Consistent spacing (aligns with buttons, other inputs)
- Standard font sizing (prevents mobile zoom issues)

### Pattern 3: Checkbox & Form Control Consistency

Form controls benefit especially from consistency:

**Alignment Checklist**:
- [ ] Size matches other form controls (20x20px common)
- [ ] Border weight matches inputs (1px or 2px)
- [ ] Border radius style consistent (sharp, moderate, or round)
- [ ] Focus ring matches inputs (same color, width, offset)
- [ ] Checked state uses primary brand color
- [ ] Disabled state uses same grays as other inputs

**ShadCN/UI-Style Checkbox Example**:
```css
.checkbox {
  width: 20px;
  height: 20px;
  border: 2px solid #d1d5db;  /* Slightly bolder than input
  border-radius: 4px;          /* Less rounded than inputs
  background: white;
}

.checkbox:checked {
  background: #3b82f6;         /* Matches input focus color
  border-color: #3b82f6;
}

.checkbox:focus {
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1); /* Same as inputs
}
```

### Pattern 4: Button Hierarchy Alignment

If the library has button variants, custom buttons should follow similar patterns:

**Common Button Hierarchy**:
- **Primary**: Filled with brand color, white text
- **Secondary**: Outlined or ghost style, colored text/border
- **Destructive/Danger**: Red/error color
- **Ghost/Link**: Minimal styling, only text color

**Matching Approach**:
```css
/* If library uses solid primaries and outlined secondaries... */
.btn-custom-action {
  /* Match primary styling pattern */
  padding: 12px 24px;          /* Same as library buttons */
  border-radius: 8px;          /* Same as library */
  font-weight: 600;            /* Same emphasis */
  transition: all 0.2s ease;   /* Same timing */
  /* But use your custom color */
  background: #10b981;         /* Custom green, not blue */
}

.btn-custom-action:hover {
  background: #059669;         /* Darker shade, same pattern */
}
```

### Pattern 5: Animation & Transition Consistency

Subtle but noticeable—match transition timing and easing:

**Library Inspection**:
- Find any animated component in the library
- Check browser dev tools for transition properties
- Note the timing function (ease, ease-in-out, cubic-bezier)
- Note the duration (0.15s, 0.2s, 0.3s?)

**Apply Consistently**:
```css
/* If library uses this... */
transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);

/* Use the same for custom components */
.custom-toggle {
  transition: background 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.custom-card:hover {
  transition: transform 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}
```

## Practical Workflow

### Step 1: Extract Library Conventions

**Quick Audit Method**:
1. Open library documentation or demo
2. Inspect 3-5 core components (Button, Input, Checkbox)
3. Note patterns in browser dev tools
4. Document conventions in a reference file

**What to Document**:
```markdown
## [Library Name] Conventions

### Spacing
- Padding rhythm: 8px, 12px, 16px, 24px
- Margin rhythm: 8px, 16px, 24px, 32px

### Borders
- Default: 1px solid #e5e7eb
- Focus: 2px solid #3b82f6
- Radius: 6px standard, 8px for larger elements

### Colors
- Primary: #3b82f6
- Text: #1f2937
- Text secondary: #6b7280
- Background: white / #f9fafb
- Border: #e5e7eb

### Transitions
- Standard: 0.2s ease
- Cubic: cubic-bezier(0.4, 0, 0.2, 1)
```

### Step 2: Create Custom Components with Pattern Matching

When building a new custom component:

1. **Start with library base** (if possible)
2. **Match visual conventions** (spacing, borders, colors)
3. **Preserve library patterns** (focus states, transitions)
4. **Customize functionality** (add your unique behavior)

**Example: Custom Phone Input**
```tsx
// Use library's Input as base
import { Input } from '@/components/ui/input'
import { Select } from '@/components/ui/select'

export function PhoneInput() {
  return (
    <div className="flex gap-2">
      {/* Library Select - matches styling automatically */}
      <Select>
        <option>🇸🇪 +46</option>
        <option>🇺🇸 +1</option>
      </Select>
      
      {/* Library Input - matches styling automatically */}
      <Input 
        type="tel"
        placeholder="70 123 45 67"
      />
    </div>
  )
}
```

### Step 3: Visual Comparison Testing

**Side-by-Side Check**:
- Place library component next to custom component
- Check if borders look the same weight
- Verify padding feels consistent
- Test focus states together
- Compare hover effects

**Quick Test Page**:
```html
<div class="comparison-grid">
  <!-- Library component -->
  <div>
    <label>Library Input</label>
    <input class="library-input" />
  </div>
  
  <!-- Custom component -->
  <div>
    <label>Custom Input</label>
    <input class="custom-input" />
  </div>
</div>
```

Should feel like siblings, not strangers.

## When to Deviate from Library Standards

**Good Reasons to Diverge**:
- Brand requirements demand specific styling
- Accessibility needs require different approach
- Library pattern doesn't work for specific use case
- Custom component serves completely different purpose

**Example Acceptable Deviation**:
```
Library uses 1px borders universally.
Your brand requires bolder 2px borders for accessibility.
→ Apply 2px consistently to all components (library and custom).
```

**Remember**: Consistency within your own design system matters more than matching the library perfectly.

## Common Mismatches to Avoid

### Border Inconsistency
```css
/* Library pattern */
.library-input { border: 1px solid #d1d5db; }

/* Accidental mismatch - feels "off" */
.custom-input { border: 2px solid #ccc; }

/* Better alignment */
.custom-input { border: 1px solid #d1d5db; }
```

### Focus State Variation
```css
/* Library pattern */
.library-input:focus { 
  outline: none;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
}

/* Mismatch - different color and size */
.custom-input:focus {
  outline: 2px solid red;
}

/* Better */
.custom-input:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
}
```

### Padding Rhythm Break
```css
/* Library uses 8px rhythm */
.library-button { padding: 8px 16px; }
.library-input { padding: 0 12px; height: 40px; }

/* Breaks rhythm */
.custom-card { padding: 15px; }

/* Aligns with rhythm */
.custom-card { padding: 16px; } /* or 24px */
```

## Success Indicators

You know you've achieved good alignment when:
- [ ] Developers can't tell which components are custom vs. library
- [ ] All form controls feel like part of the same family
- [ ] Focus states are consistent across all components
- [ ] Spacing feels rhythmic and predictable
- [ ] Border weights and radii are harmonious
- [ ] Colors follow same semantic patterns
- [ ] Transitions feel unified

## Tools & Techniques

**Browser Dev Tools**:
- Inspect computed styles of library components
- Copy border, padding, color values exactly
- Note CSS class patterns and naming

**Design Tokens Extraction**:
- Some libraries publish design tokens
- Use tokens directly in your custom components
- Guarantees alignment automatically

**Visual Regression Testing**:
- Screenshot library and custom components
- Overlay them to check alignment
- Catches subtle differences

## Related Resources

**See Also**:
- `integrate-figma-components.md` - Syncing designs with code
- `create-design-system-preview.md` - Presenting components consistently
- `component-library-attribution-patterns.md` - Documenting library usage

---

**Remember**: This task is about creating visual harmony, not rigid rules. The best design system serves your users and your team's needs. Match library standards where it adds value, diverge where it serves your project better.

