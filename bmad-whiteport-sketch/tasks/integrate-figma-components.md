# Task: Integrate Figma Components

## Overview
This task guides the UX Expert through using Figma MCP to add missing components, enhance existing static components, and create a complete design system integration. This bridges the gap between design tools and development implementation.

## Workflow

### Step 1: Figma Integration Setup
**UX Expert Action**: Set up Figma MCP integration for component enhancement
**Duration**: 10-15 minutes
**Prerequisites**: Static components created, Figma MCP available

**Setup Process**:
1. **Figma MCP Configuration** (5 minutes)
   - Configure Figma MCP connection
   - Set up design system file access
   - Configure component export settings
   - Test Figma API connectivity

2. **Design System Mapping** (5 minutes)
   - Map Figma components to React components
   - Identify missing components in current implementation
   - Plan component enhancement strategy
   - Document integration approach

3. **Component Export Setup** (5 minutes)
   - Set up component export from Figma
   - Configure style and asset export
   - Set up automated component generation
   - Test export functionality

### Step 2: Missing Component Identification
**UX Expert Action**: Identify components that need Figma integration
**Duration**: 15-20 minutes
**Participants**: UX Expert + Designer

**Identification Process**:
1. **Component Audit** (10 minutes)
   - Review existing static components
   - Identify components not available in design system
   - List custom components needed
   - Document component requirements

2. **Figma Component Search** (5 minutes)
   - Search Figma for existing components
   - Identify similar components that can be adapted
   - List components that need custom creation
   - Plan component creation strategy

3. **Integration Planning** (5 minutes)
   - Plan how to integrate Figma components
   - Identify components that need customization
   - Plan component variant creation
   - Document integration approach

### Step 3: Figma Component Integration
**UX Expert Action**: Integrate Figma components into static React components
**Duration**: 30-45 minutes per component set
**Output**: Enhanced components with Figma integration

**Integration Process**:
1. **Component Export** (10 minutes)
   - Export components from Figma
   - Extract styles and assets
   - Generate component code
   - Test exported components

2. **React Component Creation** (15 minutes)
   - Convert Figma components to React
   - Integrate with selected design system
   - Apply brand customizations
   - Test component functionality

3. **Component Enhancement** (10 minutes)
   - Add responsive behavior
   - Implement interactions and states
   - Add accessibility features
   - Test component integration

4. **Documentation Update** (5 minutes)
   - Document Figma integration approach
   - Update component usage examples
   - Add Figma source references
   - Create integration guidelines

### Step 4: Design System Synchronization
**UX Expert Action**: Synchronize Figma components with design system
**Duration**: 20-30 minutes
**Output**: Synchronized design system with Figma components

**Synchronization Process**:
1. **Style Synchronization** (10 minutes)
   - Sync colors, typography, and spacing
   - Update design system tokens
   - Ensure consistency across components
   - Test style consistency

2. **Component Variant Creation** (10 minutes)
   - Create component variants for different states
   - Implement responsive variants
   - Add interaction variants
   - Test variant functionality

3. **Asset Integration** (5 minutes)
   - Integrate icons and images from Figma
   - Optimize assets for web use
   - Update asset references
   - Test asset loading

4. **Quality Assurance** (5 minutes)
   - Test all integrated components
   - Verify design system consistency
   - Check accessibility compliance
   - Validate responsive behavior

## Elicitation

### Designer Collaboration Questions

**Figma Integration**:
- "Which Figma components should we prioritize for integration?"
- "Are there any custom components in Figma that we need to implement?"
- "How should we handle component variants and states?"
- "What's the preferred approach for syncing design system tokens?"

**Component Enhancement**:
- "Which components need the most customization for our brand?"
- "Are there any Figma components that don't fit our needs?"
- "How should we handle responsive variants of Figma components?"
- "What's the best approach for maintaining design system consistency?"

**Design System Sync**:
- "How often should we sync with Figma for updates?"
- "What's the process for handling design system changes?"
- "How should we manage component versioning?"
- "What's the best approach for collaborative design updates?"

### Technical Implementation Questions

**Figma MCP Setup**:
- "What's the Figma file ID for our design system?"
- "Which Figma components should we export?"
- "How should we handle component naming conventions?"
- "What's the preferred export format for assets?"

**Component Integration**:
- "Should we use Figma's generated code or create custom React components?"
- "How should we handle Figma component props and variants?"
- "What's the best approach for integrating Figma styles?"
- "How should we manage component dependencies?"

**Design System Management**:
- "How should we handle design system token updates?"
- "What's the process for component version control?"
- "How should we manage design system documentation?"
- "What's the best approach for team collaboration?"

## Quality Checklist

### Figma Integration Quality
- [ ] Figma MCP is properly configured and connected
- [ ] All required components are exported from Figma
- [ ] Component export includes all necessary assets
- [ ] Figma components integrate seamlessly with React
- [ ] Design system tokens are synchronized

### Component Integration Quality
- [ ] Figma components are properly converted to React
- [ ] Components maintain design fidelity from Figma
- [ ] Brand customizations are applied correctly
- [ ] Components work with selected design system
- [ ] Responsive behavior is implemented correctly

### Design System Sync Quality
- [ ] Colors, typography, and spacing are synchronized
- [ ] Component variants are properly implemented
- [ ] Assets are optimized and properly integrated
- [ ] Design system consistency is maintained
- [ ] Documentation is updated with Figma references

### Code Quality
- [ ] Components are properly typed and documented
- [ ] Code follows project conventions
- [ ] Components are reusable and maintainable
- [ ] Performance is optimized
- [ ] Accessibility compliance is maintained

## Examples

### Dog Week Project Example

**Figma Component Integration**:
```typescript
// Frontend/components/FigmaComponents.tsx
import { useFigmaComponents } from '@figma/mcp';
import { motion } from 'framer-motion';

export function FigmaEnhancedComponent() {
  const { components, styles, assets } = useFigmaComponents({
    fileId: 'dog-week-design-system',
    componentIds: [
      'button-primary',
      'button-secondary', 
      'card-family',
      'badge-status',
      'walk-timer',
      'family-avatar'
    ]
  });

  return (
    <div className="figma-integrated-components">
      {components.map(component => (
        <motion.div
          key={component.id}
          style={styles[component.id]}
          className="figma-component"
          whileHover={{ scale: 1.02 }}
          whileTap={{ scale: 0.98 }}
        >
          <div dangerouslySetInnerHTML={{ __html: component.html }} />
        </motion.div>
      ))}
    </div>
  );
}
```

**Figma Design System Integration**:
```typescript
// Frontend/theme/figma-theme.ts
import { createTheme } from '@mantine/core';

export const figmaTheme = createTheme({
  colors: {
    // Colors synced from Figma
    primary: ['#3b82f6', '#1d4ed8', '#1e40af'],
    secondary: ['#10b981', '#059669', '#047857'],
    accent: ['#f59e0b', '#d97706', '#b45309'],
    family: ['#8b5cf6', '#7c3aed', '#6d28d9'],
    walk: ['#06b6d4', '#0891b2', '#0e7490']
  },
  fontFamily: 'Inter, sans-serif',
  fontSizes: {
    xs: '0.75rem',
    sm: '0.875rem',
    md: '1rem',
    lg: '1.125rem',
    xl: '1.25rem'
  },
  spacing: {
    xs: '0.5rem',
    sm: '0.75rem',
    md: '1rem',
    lg: '1.5rem',
    xl: '2rem'
  },
  radius: {
    xs: '0.25rem',
    sm: '0.375rem',
    md: '0.5rem',
    lg: '0.75rem',
    xl: '1rem'
  }
});
```

**Figma Component with Variants**:
```typescript
// Frontend/components/FigmaButton.tsx
import { Button } from '@mantine/core';
import { motion } from 'framer-motion';

interface FigmaButtonProps {
  variant: 'primary' | 'secondary' | 'outline' | 'ghost';
  size: 'sm' | 'md' | 'lg';
  state: 'default' | 'hover' | 'active' | 'disabled';
  children: React.ReactNode;
  onClick?: () => void;
}

export function FigmaButton({ 
  variant, 
  size, 
  state, 
  children, 
  onClick 
}: FigmaButtonProps) {
  const getVariantStyles = () => {
    const baseStyles = {
      borderRadius: '0.5rem',
      fontWeight: 600,
      transition: 'all 0.2s ease-in-out'
    };

    const variants = {
      primary: {
        backgroundColor: '#3b82f6',
        color: 'white',
        border: 'none'
      },
      secondary: {
        backgroundColor: '#10b981',
        color: 'white',
        border: 'none'
      },
      outline: {
        backgroundColor: 'transparent',
        color: '#3b82f6',
        border: '2px solid #3b82f6'
      },
      ghost: {
        backgroundColor: 'transparent',
        color: '#3b82f6',
        border: 'none'
      }
    };

    const sizes = {
      sm: { padding: '0.5rem 1rem', fontSize: '0.875rem' },
      md: { padding: '0.75rem 1.5rem', fontSize: '1rem' },
      lg: { padding: '1rem 2rem', fontSize: '1.125rem' }
    };

    const states = {
      default: {},
      hover: { transform: 'translateY(-1px)', boxShadow: '0 4px 12px rgba(0, 0, 0, 0.15)' },
      active: { transform: 'translateY(0)', boxShadow: '0 2px 4px rgba(0, 0, 0, 0.1)' },
      disabled: { opacity: 0.5, cursor: 'not-allowed' }
    };

    return {
      ...baseStyles,
      ...variants[variant],
      ...sizes[size],
      ...states[state]
    };
  };

  return (
    <motion.button
      style={getVariantStyles()}
      onClick={onClick}
      disabled={state === 'disabled'}
      whileHover={{ scale: 1.02 }}
      whileTap={{ scale: 0.98 }}
      className="figma-button"
    >
      {children}
    </motion.button>
  );
}
```

**Figma Asset Integration**:
```typescript
// Frontend/components/FigmaAssets.tsx
import { useFigmaAssets } from '@figma/mcp';

export function FigmaAssets() {
  const { icons, images, illustrations } = useFigmaAssets({
    fileId: 'dog-week-design-system',
    assetTypes: ['icons', 'images', 'illustrations']
  });

  return (
    <div className="figma-assets">
      {/* Icons */}
      <div className="icons">
        {icons.map(icon => (
          <img
            key={icon.id}
            src={icon.url}
            alt={icon.name}
            className="figma-icon"
            style={{ width: icon.width, height: icon.height }}
          />
        ))}
      </div>

      {/* Images */}
      <div className="images">
        {images.map(image => (
          <img
            key={image.id}
            src={image.url}
            alt={image.name}
            className="figma-image"
            loading="lazy"
          />
        ))}
      </div>

      {/* Illustrations */}
      <div className="illustrations">
        {illustrations.map(illustration => (
          <img
            key={illustration.id}
            src={illustration.url}
            alt={illustration.name}
            className="figma-illustration"
            loading="lazy"
          />
        ))}
      </div>
    </div>
  );
}
```

## Figma-to-Code Synchronization Workflow

**Context**: Once your design system is established in Figma, you may want to keep component specifications synchronized with design changes. Here's one approach that some teams find effective.

### Design System as Single Source of Truth

**Philosophy**: Figma becomes the source of truth for visual design, with component specifications automatically updated to match.

**Naming Convention Pattern**:
- Figma component layer name → matches `.md` specification file name
- Example: Figma layer "Button-Primary" → `Button-Primary.md`
- Example: Figma layer "Input" → `Input.md`
- Example: Figma layer "Checkbox" → `Checkbox.md`

**Why This Works**:
- Clear 1:1 mapping between design and documentation
- Easy to identify which spec needs updating
- Scalable as design system grows

### Practical Sync Workflow

When a designer updates a component in Figma:

#### **Step 1: Extract Specifications from Figma**

**What to Copy from Figma Inspect Panel**:
- **Dimensions**: Width, height, min/max constraints
- **Colors**: All color values as hex codes
- **Typography**: Font family, size, weight, line-height
- **Spacing**: Padding, margins (top, right, bottom, left)
- **Border**: Border radius, border width, border color
- **Shadows**: Box-shadow values
- **States**: Hover, active, focus, disabled specifications

**Figma Inspect Panel Example**:
```
Width: 200px
Height: 48px
Padding: 12px 24px
Border Radius: 8px
Background: #3b82f6
Font: Inter
Size: 16px
Weight: 600
```

#### **Step 2: Update Component Specification**

Take the extracted values and update the `.md` file:

**Before** (outdated spec):
```markdown
### Visual Properties
- Height: 44px
- Padding: 10px 20px
- Border Radius: 6px
- Background: #2563eb
```

**After** (synced with Figma):
```markdown
### Visual Properties
- Height: 48px
- Padding: 12px 24px
- Border Radius: 8px
- Background: #3b82f6
```

#### **Step 3: Update CSS/HTML Guide**

If you have a Design System Guide (HTML preview), update the styles:

**CSS Update Example**:
```css
/* Before */
.btn-primary {
    height: 44px;
    padding: 10px 20px;
    border-radius: 6px;
    background: #2563eb;
}

/* After (synced with Figma) */
.btn-primary {
    height: 48px;
    padding: 12px 24px;
    border-radius: 8px;
    background: #3b82f6;
}
```

### Sync Workflow Checklist

**When Designer Updates Figma Component**:
- [ ] Open Figma component in Inspect Panel
- [ ] Note component name (matches `.md` file)
- [ ] Copy all visual specifications
- [ ] Copy state variations (hover, active, etc.)
- [ ] Update corresponding `.md` specification file
- [ ] Update CSS in Design System Guide (if applicable)
- [ ] Update HTML examples (if changed)
- [ ] Test changes in preview/browser
- [ ] Notify development team of changes

### What to Extract for Different Component Types

**Buttons**:
- Dimensions (width/height)
- Padding (all sides)
- Border radius
- Background color (all states)
- Text color (all states)
- Typography (font, size, weight)
- Shadow/elevation

**Inputs**:
- Height
- Padding
- Border (width, color, style)
- Border radius
- Background color
- Typography
- Placeholder color
- Focus state (border, shadow)
- Error state styling

**Colors**:
- Hex values for all shades (50, 100, 300, 500, 600, 700, etc.)
- Usage context
- Accessibility contrast ratios

**Typography**:
- Font family
- Font sizes for each level (H1, H2, body, etc.)
- Font weights used
- Line heights
- Letter spacing (if applicable)

### Automation Possibilities

**Manual Sync** (immediate, no setup):
- Designer shares Figma link
- Developer opens Inspect Panel
- Developer manually copies values
- Update specs and CSS manually

**Semi-Automated** (requires some setup):
- Use Figma Design Tokens plugin
- Export tokens as JSON
- Map JSON values to CSS variables
- Update specs from JSON

**Fully Automated** (complex setup):
- Figma API integration
- Automated token extraction
- CI/CD pipeline updates
- Automatic spec generation

**Recommendation**: Start manual, automate only if you have many frequent updates.

### Maintaining Design-Code Consistency

**Practical Tips**:
1. **Schedule regular syncs**: Weekly or after major design reviews
2. **Version control**: Commit Figma changes with spec updates together
3. **Change log**: Note what changed in commit messages
4. **Team communication**: Announce significant design updates
5. **Visual regression testing**: Compare before/after if possible

**Communication Pattern**:
```
Designer: "Updated Button-Primary in Figma"
         → Height: 44px → 48px
         → Padding: 10px → 12px
         → Border radius: 6px → 8px
         
Developer: *Updates Button-Primary.md*
          *Updates Design-System-Guide.css*
          *Tests in preview*
          "Synced! Deployed to staging"
```

### When Figma Sync Makes Sense

**Good Fit**:
- Active design iteration phase
- Multiple designers working on components
- Design system is mature and established
- Team has capacity to maintain sync

**May Not Be Worth It**:
- Design is mostly stable
- Small team with rare design changes
- Early exploration phase (design not finalized)
- Components are highly custom-coded

**Remember**: The goal is useful synchronization, not perfect automation. Manual sync with good communication often works better than complex automation that breaks frequently.

---

## Success Criteria

- [ ] Figma MCP is properly configured and connected
- [ ] All required components are exported from Figma
- [ ] Components integrate seamlessly with React and design system
- [ ] Design system tokens are synchronized with Figma
- [ ] Assets are optimized and properly integrated
- [ ] Components maintain design fidelity from Figma
- [ ] Documentation includes Figma integration details
- [ ] Components are ready for development integration

## Common Pitfalls to Avoid

### Figma Integration Pitfalls
- [ ] Don't skip MCP configuration - ensure proper connection
- [ ] Don't ignore component dependencies - export all required components
- [ ] Don't skip asset optimization - optimize for web use
- [ ] Don't forget error handling - handle Figma API errors gracefully

### Component Integration Pitfalls
- [ ] Don't skip design system integration - maintain consistency
- [ ] Don't ignore responsive behavior - implement breakpoints
- [ ] Don't skip accessibility - maintain WCAG compliance
- [ ] Don't forget testing - test all integrated components

### Design System Sync Pitfalls
- [ ] Don't skip token synchronization - keep design system updated
- [ ] Don't ignore version control - manage component versions
- [ ] Don't skip documentation - document integration approach
- [ ] Don't forget team collaboration - keep team informed of changes

## Next Steps

After Figma integration:

1. **Component Testing**: Test all integrated components thoroughly
2. **Performance Optimization**: Ensure components perform well
3. **Documentation Review**: Update documentation with Figma details
4. **Development Handoff**: Prepare components for production integration
5. **Team Training**: Train team on Figma integration workflow
