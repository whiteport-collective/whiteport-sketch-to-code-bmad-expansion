# Task: Create HTML Preview from Specifications

## Overview
This task guides the UX Expert through creating interactive, standalone HTML previews from completed scenario specifications. These previews serve as a critical learning and refinement tool, enabling rapid iteration before production development begins. The previews use the selected design system components and can be opened directly in a browser for immediate validation.

## Purpose in WPS2C Workflow

### **The Missing Link Between Specification and Development**
HTML previews bridge the gap between written specifications and production code:
- **Visual Validation**: See specifications come to life immediately
- **Interactive Testing**: Test user flows and interactions locally
- **Design Refinement**: Discover gaps, edge cases, and improvements
- **Specification Feedback**: Learn what works and what needs adjustment
- **Stakeholder Review**: Share clickable prototypes for quick approval
- **Component Discovery**: Identify missing components and patterns

### **"Create as Needed" Philosophy**
Don't create all previews upfront - build them when:
- Specifications are complete enough to visualize
- Stakeholder review is needed before development
- Design decisions need visual validation
- User flow needs interactive testing
- Component behavior is unclear from specs alone

## Workflow

### Step 1: Specification Analysis and Preview Planning
**UX Expert Action**: Analyze specifications and plan preview structure
**Duration**: 10-15 minutes
**Prerequisites**: Scenario specifications complete, sketches available

**Analysis Process**:
1. **Review Specifications** (5 minutes)
   - Read complete scenario page specifications
   - Identify all UI components and interactions
   - Review Object ID/Position ID structure
   - Note multilingual content requirements
   - List external dependencies (images, icons)

2. **Design System Component Mapping** (5 minutes)
   - Map specification components to Design System
   - Identify components that exist in Design System
   - Note components that need to be added to Design System
   - Plan how to integrate Design System styles
   - Verify Design System preview is up to date

3. **Preview Structure Planning** (5 minutes)
   - Plan folder structure: `[Scenario]/Frontend/`
   - Determine file naming: `[Step]-Preview.html`, `[Step]-Preview.css`, `[Step]-Preview.js`
   - Plan asset dependencies (images in `Assets/` folder)
   - Plan navigation links between preview pages
   - Decide on standalone vs. linked preview approach

### Step 2: HTML Structure Creation
**UX Expert Action**: Create semantic HTML matching specifications
**Duration**: 20-30 minutes per page
**Output**: `[Step]-Preview.html` with complete markup

**HTML Creation Process**:
1. **Document Foundation** (5 minutes)
   - Create HTML5 document with proper `<!DOCTYPE>` and metadata
   - Link external CSS file: `<link rel="stylesheet" href="[Step]-Preview.css">`
   - Link external JS file: `<script src="[Step]-Preview.js"></script>`
   - Set viewport for responsive behavior
   - Add language selector data attributes for multilingual content

2. **Header and Navigation** (5 minutes)
   - Create header with logo, navigation, and language selector
   - Use Object IDs from specifications (e.g., `data-object-id="start-header-logo"`)
   - Implement clickable navigation links to other preview pages
   - Add "Page not outlined yet" popups for unbuilt pages
   - Ensure mobile-responsive navigation

3. **Main Content Structure** (10 minutes)
   - Build semantic HTML structure matching sketch
   - Use Position IDs for dynamic content slots (e.g., `data-position-id="hero-card-position-1"`)
   - Implement all form fields with proper labels and placeholders
   - Add buttons, inputs, and interactive elements
   - Include multilingual content using `data-lang` attributes

4. **Footer and Secondary Elements** (5 minutes)
   - Add footer content if in scope
   - Include modals, tooltips, and overlays
   - Add loading spinners and feedback elements
   - Ensure all elements have proper Object/Position IDs

### Step 3: CSS Styling with Design System Integration
**UX Expert Action**: Create external CSS file with Design System styles
**Duration**: 25-35 minutes per page
**Output**: `[Step]-Preview.css` with complete styling

**CSS Creation Process**:
1. **Design System Import** (5 minutes)
   - Import Design System base styles if available
   - Use CSS custom properties (design tokens) from Design System
   - Reference Design System color palette, typography, spacing
   - Ensure consistency with Design System preview

2. **Component Styling** (15 minutes)
   - Style all components to match sketch and Design System
   - Implement button styles (`.btn-primary-large`, `.btn-secondary-medium`, etc.)
   - Create input field styles (`.input-field`, floating labels, error states)
   - Add card, modal, and layout styles
   - Implement hover, focus, and active states

3. **Responsive Design** (10 minutes)
   - Implement mobile-first responsive styles
   - Add media queries for tablet and desktop breakpoints
   - Ensure touch-friendly sizing for mobile elements
   - Test responsive behavior across device sizes

4. **Animations and Transitions** (5 minutes)
   - Add smooth transitions for interactive elements (buttons, inputs, modals)
   - Implement modal animations using CSS transitions with transform properties
   - Create loading indicator animations with SVG and CSS keyframes
   - Add subtle hover effects using transform for visual elevation
   - Ensure all animated elements are properly sized and functional

### Step 4: JavaScript Interaction Implementation
**UX Expert Action**: Create external JS file with all interactions
**Duration**: 20-30 minutes per page
**Output**: `[Step]-Preview.js` with complete functionality

**JavaScript Creation Process**:
1. **Page Navigation** (5 minutes)
   - Implement clickable links between preview pages
   - Add popup alerts for "Page not outlined yet" dead links
   - Ensure language selector triggers content updates
   - Handle browser back/forward navigation

2. **Form Validation** (10 minutes)
   - Implement field validation (email format, required fields, phone number)
   - Show error messages on blur or form submission (not on page load)
   - Validate checkboxes (e.g., Terms and Conditions)
   - Enable submit button only when all validations pass (or trigger errors on click)

3. **Interactive Elements** (10 minutes)
   - Implement toggles, checkboxes, and radio buttons
   - Add modal open/close functionality
   - Create country selector for phone input
   - Implement loading states and spinners
   - Add language toggle functionality

4. **Multilingual Content Switching** (5 minutes)
   - Implement language selector to toggle `data-lang` visibility
   - Update all text content based on selected language
   - Persist language selection in `sessionStorage`
   - Ensure smooth content switching

### Step 5: Asset Integration and Standalone Setup
**UX Expert Action**: Integrate assets and ensure standalone functionality
**Duration**: 10-15 minutes per page
**Output**: Fully standalone, browser-ready preview

**Asset Integration**:
1. **Image Assets** (5 minutes)
   - Place images in `Frontend/Assets/` folder
   - Link images using relative paths: `Assets/img-boy-with-dog.jpg`
   - Use actual sketch images when appropriate
   - Optimize images for web (size and format)

2. **Icon and Font Assets** (5 minutes)
   - Include necessary icons (inline SVG or icon fonts)
   - Load web fonts from Google Fonts or local files
   - Ensure icons are accessible (alt text, ARIA labels)

3. **Standalone Verification** (5 minutes)
   - Test preview by opening HTML file directly in browser (`file://` URL)
   - Verify all CSS and JS loads correctly
   - Test all interactions and navigation
   - Ensure no external dependencies fail

### Step 6: Cross-Page Navigation and Flow Testing
**UX Expert Action**: Link previews together for user flow testing
**Duration**: 10-15 minutes (one-time setup + per page)
**Output**: Clickable prototype flow across all preview pages

**Navigation Setup**:
1. **Link Existing Pages** (5 minutes)
   - Update navigation links to point to built preview pages
   - Ensure logical forward navigation through the user journey
   - Remove back buttons where backward navigation doesn't make sense
   - Simplify authentication flows for preview testing purposes
   - Test complete user flow from start to end

2. **Dead Link Handling** (5 minutes)
   - Add popup alerts for pages not yet built: "Page not outlined yet"
   - Keep links visible but non-functional for future pages
   - Update popups as new pages are created

3. **Flow Validation** (5 minutes)
   - Walk through entire user journey in browser
   - Test all clickable elements and transitions
   - Verify logical flow matches scenario structure
   - Document any gaps or issues discovered

### Step 7: Learning and Specification Refinement
**UX Expert Action**: Use preview to discover improvements and gaps
**Duration**: 15-30 minutes (iterative)
**Output**: Updated specifications and Design System components

**Refinement Process**:
1. **Visual Review** (10 minutes)
   - Compare preview to original sketch
   - Identify visual mismatches or improvements
   - Test color, typography, and spacing consistency
   - Note any Design System inconsistencies

2. **Interaction Testing** (10 minutes)
   - Test all user interactions and form submissions
   - Verify validation messages and error states
   - Test loading states and animations
   - Identify missing or unclear interactions

3. **Component Discovery** (10 minutes)
   - Identify new components not yet in Design System
   - Note variations needed for existing components
   - Document component patterns discovered during preview
   - Update Design System specifications and preview

4. **Specification Update** (Iterative)
   - Refine scenario specifications based on learnings
   - Add missing Object/Position IDs
   - Clarify unclear component descriptions
   - Update multilingual content as needed
   - Document interaction patterns discovered

### Step 8: Design System Synchronization
**UX Expert Action**: Add discovered components to Design System
**Duration**: 15-30 minutes (as needed)
**Output**: Updated Design System specifications and preview

**Synchronization Process**:
1. **Component Extraction** (10 minutes)
   - Identify reusable components from preview
   - Extract component HTML structure
   - Extract component CSS styles
   - Document component variants and states

2. **Design System Integration** (10 minutes)
   - Add new components to appropriate Design System folder
   - Update `Design-System.html` consolidated preview
   - Add component specifications to `.md` files
   - Include ShadCN/UI references and usage examples

3. **Cross-Reference** (10 minutes)
   - Link scenario specifications to Design System components
   - Update "Example of use" sections in Design System
   - Ensure consistent naming across specs and previews
   - Document component relationships

## Quality Checklist

### HTML Quality
- [ ] Semantic HTML5 structure
- [ ] All Object IDs and Position IDs from specifications are implemented
- [ ] Proper accessibility attributes (ARIA labels, alt text)
- [ ] Multilingual content with `data-lang` attributes
- [ ] External CSS and JS files properly linked
- [ ] All images and assets properly linked

### CSS Quality
- [ ] External CSS file with same name as HTML file
- [ ] Design System design tokens and styles referenced
- [ ] Consistent component styling (buttons, inputs, cards)
- [ ] Responsive design with mobile-first approach
- [ ] Smooth transitions and animations
- [ ] All interactive states (hover, focus, active, disabled)

### JavaScript Quality
- [ ] External JS file with same name as HTML file
- [ ] Clean, modular, well-commented code
- [ ] All form validations working correctly
- [ ] Error messages shown on blur or submit (not on page load)
- [ ] Navigation links working correctly
- [ ] Multilingual content switching functional
- [ ] Loading states and animations working

### Standalone Quality
- [ ] Preview opens directly in browser via `file://` URL
- [ ] No external dependencies fail to load
- [ ] All interactions work without a server
- [ ] Images and assets load correctly from relative paths

### Design System Integration
- [ ] All components match Design System specifications
- [ ] New components added to Design System as discovered
- [ ] Consistent naming and styling across all previews
- [ ] Design System preview updated with new components

### User Flow Quality
- [ ] All built pages are linked together
- [ ] Navigation flow is logical and matches scenario structure
- [ ] Dead links have appropriate "Page not outlined yet" popups
- [ ] User can click through entire built journey

## Examples

### Dog Week Project Example

**File Structure**:
```
docs/C-Scenarios/01-Customer-Onboarding/
├── 1.1-Start-Page/
│   ├── 1.1-Start-Page.md (specifications)
│   ├── Sketches/
│   │   └── 1.1-Start-Page_Mobile-Web_Concept.jpg
│   └── Frontend/
│       ├── Assets/
│       │   └── img-boy-with-dog.jpg
│       ├── 1.1-Start-Page-Preview.html
│       ├── 1.1-Start-Page-Preview.css
│       └── 1.1-Start-Page-Preview.js
├── 1.2-Sign-In/
│   ├── 1.2-Sign-In.md
│   ├── Sketches/
│   └── Frontend/
│       ├── 1.2-Sign-In-Preview.html
│       ├── 1.2-Sign-In-Preview.css
│       └── 1.2-Sign-In-Preview.js
└── 1.3-Profile-Setup/
    ├── 1.3-Profile-Setup.md
    ├── Sketches/
    └── Frontend/
        ├── 1.3-Profile-Setup-Preview.html
        ├── 1.3-Profile-Setup-Preview.css
        └── 1.3-Profile-Setup-Preview.js
```

**Example HTML with Object IDs** (`1.1-Start-Page-Preview.html`):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>1.1 Start Page - Dog Week Preview</title>
    <link rel="stylesheet" href="1.1-Start-Page-Preview.css">
</head>
<body>
    <header data-object-id="start-header">
        <div class="header-left">
            <img src="Assets/logo.png" alt="Dog Week" data-object-id="start-header-logo">
        </div>
        <div class="header-right">
            <button class="btn-secondary-medium" data-object-id="start-header-signin" onclick="navigateTo('1.2-Sign-In-Preview.html')">
                <span data-lang="en">Sign In</span>
                <span data-lang="sv">Logga in</span>
            </button>
            <select data-object-id="start-header-language-selector" onchange="changeLanguage(this.value)">
                <option value="en">🇬🇧 English</option>
                <option value="sv">🇸🇪 Svenska</option>
            </select>
        </div>
    </header>

    <main>
        <section data-object-id="start-hero">
            <img src="Assets/img-boy-with-dog.jpg" alt="Boy with dog" data-object-id="start-hero-image" class="full-width-image">
            <div class="hero-content">
                <p class="pre-header" data-object-id="start-hero-preheader">
                    <span data-lang="en">Never ask who's time it is</span>
                    <span data-lang="sv">Aldrig fråga vems tur det är</span>
                </p>
                <h1 data-object-id="start-hero-headline">
                    <span data-lang="en">Start sharing dog walks</span>
                    <span data-lang="sv">Börja dela hundpromenader</span>
                </h1>
                <p data-object-id="start-hero-description">
                    <span data-lang="en">Coordinate your family's dog walking schedule with ease</span>
                    <span data-lang="sv">Koordinera familjens hundpromenader enkelt</span>
                </p>
                <button class="btn-primary-large" data-object-id="start-hero-cta" onclick="navigateTo('1.2-Sign-In-Preview.html')">
                    <span data-lang="en">Start planning</span>
                    <span data-lang="sv">Börja planera</span>
                </button>
            </div>
        </section>
    </main>

    <script src="1.1-Start-Page-Preview.js"></script>
</body>
</html>
```

**Example CSS** (`1.1-Start-Page-Preview.css`):
```css
/* Design System Design Tokens */
:root {
    --color-primary-blue: #0066CC;
    --color-primary-green: #28A745;
    --color-neutral-gray-100: #F8F9FA;
    --color-neutral-gray-900: #212529;
    --font-family-primary: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    --spacing-xs: 4px;
    --spacing-sm: 8px;
    --spacing-md: 16px;
    --spacing-lg: 24px;
    --spacing-xl: 32px;
}

/* Base Styles */
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
    font-family: var(--font-family-primary);
    color: var(--color-neutral-gray-900);
    line-height: 1.6;
}

/* Header */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: var(--spacing-md);
    background: white;
}
.header-right { display: flex; gap: var(--spacing-sm); align-items: center; }

/* Buttons (from Design System) */
.btn-primary-large {
    background: var(--color-primary-blue);
    color: white;
    border: none;
    border-radius: 8px;
    padding: 16px 32px;
    font-size: 18px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
}
.btn-primary-large:hover { background: #0052A3; transform: translateY(-2px); }
.btn-secondary-medium {
    background: transparent;
    color: var(--color-primary-blue);
    border: 2px solid var(--color-primary-blue);
    border-radius: 6px;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.2s;
}

/* Hero Section */
.full-width-image { width: 100%; height: auto; display: block; }
.hero-content {
    padding: var(--spacing-xl);
    text-align: center;
}
.pre-header {
    font-size: 14px;
    text-transform: uppercase;
    color: var(--color-neutral-gray-600);
    margin-bottom: var(--spacing-sm);
}
h1 {
    font-size: 32px;
    font-weight: 700;
    margin-bottom: var(--spacing-md);
}

/* Multilingual content */
[data-lang] { display: none; }
[data-lang].active { display: inline; }
```

**Example JavaScript** (`1.1-Start-Page-Preview.js`):
```javascript
// Initialize language on page load
document.addEventListener('DOMContentLoaded', () => {
    const savedLang = sessionStorage.getItem('dogweek-language') || 'en';
    changeLanguage(savedLang);
});

// Language switching
function changeLanguage(lang) {
    sessionStorage.setItem('dogweek-language', lang);
    document.querySelectorAll('[data-lang]').forEach(el => {
        el.classList.remove('active');
    });
    document.querySelectorAll(`[data-lang="${lang}"]`).forEach(el => {
        el.classList.add('active');
    });
    const selector = document.querySelector('[data-object-id="start-header-language-selector"]');
    if (selector) selector.value = lang;
}

// Navigation between preview pages
function navigateTo(page) {
    const builtPages = ['1.1-Start-Page-Preview.html', '1.2-Sign-In-Preview.html', '1.3-Profile-Setup-Preview.html'];
    if (builtPages.includes(page)) {
        window.location.href = page;
    } else {
        alert('Page not outlined yet');
    }
}
```

## Success Criteria

- [ ] Preview accurately reflects specifications and sketch
- [ ] All Object IDs and Position IDs are implemented
- [ ] Preview opens directly in browser without errors
- [ ] All interactions and validations work correctly
- [ ] Multilingual content switches properly
- [ ] Navigation between preview pages works
- [ ] Preview leads to specification refinements and improvements
- [ ] New components are added to Design System
- [ ] External CSS and JS files are properly structured
- [ ] Preview is visually consistent with Design System

## Common Pitfalls to Avoid

### File Organization Pitfalls
- [ ] Don't use inline CSS/JS for previews - always use external files with matching names
- [ ] Don't place assets outside `Frontend/Assets/` - keep dependencies local
- [ ] Don't use absolute paths - use relative paths for portability
- [ ] Don't mix preview and production code - keep previews in `Frontend/` within scenario folders

### Design System Pitfalls
- [ ] Don't create components without checking Design System first
- [ ] Don't forget to add new components back to Design System
- [ ] Don't use inconsistent styling - always reference Design System tokens
- [ ] Don't skip updating Design System preview when adding components

### Interaction Pitfalls
- [ ] Don't show validation errors on page load - only on blur or submit
- [ ] Don't disable submit button - keep it enabled to trigger validation
- [ ] Don't show errors sequentially - display all field errors simultaneously on submit
- [ ] Don't forget to handle loading states - show indicators for async actions
- [ ] Don't skip multilingual content - implement language switching if required
- [ ] Don't forget dead link handling - add appropriate placeholders
- [ ] Don't rely solely on keyframe animations - use transitions for smoother interactions
- [ ] Don't forget to make toggles and checkboxes fully functional

### Form Field Pitfalls
- [ ] Don't pre-fill demo data - keep fields empty unless specifications require defaults
- [ ] Don't use static labels - implement floating labels for better UX
- [ ] Don't overcrowd mobile layouts - use single-column layouts for forms
- [ ] Don't use limited option lists - provide comprehensive selections where appropriate
- [ ] Don't create static indicators - ensure loading animations are functional

### Animation Pitfalls
- [ ] Don't use only keyframe animations - combine with transitions for smooth interactions
- [ ] Don't create oversized elements - constrain sizes appropriately
- [ ] Don't forget to test animations - ensure they render and perform as expected
- [ ] Don't over-animate - subtle effects enhance rather than distract

### Navigation Pitfalls
- [ ] Don't add illogical navigation - consider the user journey flow
- [ ] Don't require full authentication in previews - simplify for testing purposes
- [ ] Don't forget to test all navigation links - verify functionality
- [ ] Don't use inconsistent messaging - standardize placeholder text

### Refinement Pitfalls
- [ ] Don't skip the learning phase - use preview to discover issues
- [ ] Don't forget to update specifications - feed learnings back into specs
- [ ] Don't skip stakeholder review - share previews early for feedback
- [ ] Don't treat previews as final code - they're learning tools, not production

## Integration with WPS2C Workflow

### **Phase 4 Enhancement: Sketch → Specification → Preview → Refinement**
This task adds a critical refinement loop to Phase 4:

**Traditional Flow**:
1. Sketch → 2. Specification → 3. Development

**WPS2C Flow with Previews**:
1. Sketch → 2. Specification → 3. **HTML Preview** → 4. **Refinement** → 5. Development

**The Learning Loop**:
- Preview reveals gaps in specifications
- Interaction testing uncovers edge cases
- Visual validation improves design decisions
- Component discovery enriches Design System
- Stakeholder feedback comes early and cheap
- Specifications are refined before expensive development

### **When to Create Previews**
- **During Specification**: Create preview as specifications mature
- **Before Development**: Validate design before handing off to developers
- **For Stakeholder Review**: Share clickable prototypes for quick approval
- **When Uncertain**: Use preview to test assumptions and resolve ambiguity
- **For Complex Interactions**: Validate multi-step flows and form behavior

### **Next Steps After Preview**
1. **Refine Specifications**: Update scenario `.md` files with learnings
2. **Update Design System**: Add discovered components and patterns
3. **Stakeholder Approval**: Share preview for design sign-off
4. **Development Handoff**: Provide refined specifications + working preview
5. **Create Next Preview**: Build next scenario page, repeating the cycle

## Key Takeaways

### **HTML Previews Are Learning Tools**
- Not production code, but prototype for discovery
- Cheap and fast to create, easy to iterate
- Reveal specification gaps and design issues
- Enable early stakeholder feedback
- Bridge the gap between design and development

### **External CSS/JS for Maintainability**
- Always use external files: `[Step]-Preview.css`, `[Step]-Preview.js`
- Enables reusability and easier updates
- Scales better as project grows
- Easier to debug and refactor
- Cleaner HTML structure

### **Design System as Single Source of Truth**
- Always reference Design System for components
- Add new components back to Design System
- Keep Design System preview updated
- Ensure consistency across all previews
- Use design tokens for styling

### **"Create as Needed" Philosophy**
- Don't build all previews upfront
- Create when specifications are mature enough
- Use as refinement tool, not documentation burden
- Iterate based on learnings and feedback
- Focus on high-value, complex scenarios first

---

**This task represents the missing link in the WPS2C methodology - the iterative preview/refinement phase that transforms good specifications into great ones.**

