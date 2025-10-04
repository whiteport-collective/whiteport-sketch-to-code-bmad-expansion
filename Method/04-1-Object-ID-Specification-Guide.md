**Related Phase**: [← Phase 4: Conceptual Documentation](04-Conceptual-Documentation.md)

---

# Object ID Specification Guide
## *Systematic Element Identification for Traceable Implementation*

---

## Purpose

Object IDs create traceable references between:
- **Conceptual Documentation** - specifications and requirements
- **HTML Prototypes** - id attributes for testing
- **Production Code** - component props and data attributes
- **Testing Frameworks** - reliable automation targets
- **Design Tools** - element identification in Figma/Sketch
- **Analytics Systems** - event tracking and user behavior

Every interactive element needs a unique, traceable identifier that bridges design, development, testing, and analytics.

---

## Format Standard

### Basic Element

#### [Button Primary](/docs/Components/Button.md) - Submit Button
**OBJECT ID**: `profile-setup-button-submit`
- **ShadCN/UI Component**: `<Button variant="default">` from `@/components/ui/button`
- **HTML Implementation**: `<button id="profile-setup-button-submit" name="submitProfile">`
- **API Data Field**: `submitProfile` (camelCase for JavaScript)
- **Content**:
  - SE: "Spara Profil"
  - EN: "Save Profile"
- **Behavior**: onClick → validate form, save data, navigate
- **Position**: Bottom of form, full width

### Element with Error Messages

#### [Input](/docs/Components/Input.md) - First Name
**OBJECT ID**: `profile-setup-input-firstname`
- **ShadCN/UI Component**: `<Input>` from `@/components/ui/input`
- **HTML Implementation**: `<input id="profile-setup-input-firstname" name="firstName">`
- **API Data Field**: `firstName` (camelCase)
- **Placeholder**:
  - SE: "Förnamn *"
  - EN: "First Name *"
- **Validation**: Required, 2-50 characters, letters only
- **Interaction**: onChange → validate on blur

**Error Messages**
**OBJECT ID**: `profile-setup-error-firstname`
- **Required error**:
  - SE: "Förnamn krävs"
  - EN: "First name is required"
- **Minimum length error**:
  - SE: "Förnamn måste vara minst 2 tecken"
  - EN: "First name needs at least 2 characters"
- **Maximum length error**:
  - SE: "Förnamn får inte överstiga 50 tecken"
  - EN: "First name cannot exceed 50 characters"

### Complex Component with States

#### [Toggle Switch](/docs/Components/Toggle.md) - Terms Acceptance
**OBJECT ID**: `profile-setup-toggle-terms`
- **ShadCN/UI Component**: `<Switch>` from `@/components/ui/switch`
- **HTML Implementation**: `<button id="profile-setup-toggle-terms" class="toggle-switch">`
- **Default State**: OFF (unchecked)
- **Interaction**: onClick → toggle acceptance state

**Toggle Label**
**OBJECT ID**: `profile-setup-label-terms`
- **Content**:
  - SE: "Jag accepterar villkoren"
  - EN: "I accept the terms and conditions"
- **Interaction**: onClick → toggle switch

**Toggle Error**
**OBJECT ID**: `profile-setup-error-terms`
- **Content**:
  - SE: "Du måste acceptera villkoren för att fortsätta"
  - EN: "You must accept the terms and conditions to continue"
- **Display**: Conditional, shown when validation fails

---

## Naming Convention

### Object ID Pattern
`{page}-{section}-{element}`

**Format Rules**:
- Use kebab-case (lowercase with hyphens)
- Maximum 3 segments for clarity
- Descriptive but concise
- Unique within scenario/page

**Examples**:
- `profile-setup-input-firstname` (input field)
- `profile-setup-error-firstname` (error message)
- `profile-setup-button-submit` (submit button)
- `start-header-logo` (header logo)
- `signin-google-button` (Google sign-in)
- `family-modal-close` (modal close button)

### API Data Field Pattern
camelCase for JavaScript/JSON compatibility:

**Examples**:
- `firstName` (not `first_name` or `FirstName`)
- `phoneNumber` (not `phone_number`)
- `termsAccepted` (not `terms_accepted`)
- `emailAddress` (not `email_address`)

**Rationale**: JavaScript conventions favor camelCase for object properties, making API integration seamless.

---

## Implementation Mapping

### HTML Element
```html
<!-- Standard implementation with Object ID -->
<input 
  id="profile-setup-input-firstname" 
  data-object-id="profile-setup-input-firstname"
  name="firstName"
  type="text"
  class="internal-input"
/>

<!-- Error message element -->
<p 
  id="profile-setup-error-firstname" 
  data-object-id="profile-setup-error-firstname"
  class="error-message hidden"
>
  First name is required
</p>

<!-- Button with Object ID -->
<button
  id="profile-setup-button-submit"
  data-object-id="profile-setup-button-submit"
  type="submit"
  class="btn-primary"
>
  Save Profile
</button>
```

### JavaScript Access
```javascript
// Access element using Object ID
const input = document.getElementById('profile-setup-input-firstname');
const value = input.value;

// Show error using Object ID
const errorElement = document.getElementById('profile-setup-error-firstname');
errorElement.classList.remove('hidden');
errorElement.textContent = 'First name is required';

// API data uses camelCase
const profileData = {
  firstName: value,        // camelCase for API
  lastName: lastNameValue,
  email: emailValue
};

// Send to backend
await fetch('/api/profile', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(profileData)
});
```

### React Component
```jsx
import { Input } from '@/components/ui/input';
import { useState } from 'react';

function ProfileForm() {
  const [formData, setFormData] = useState({ firstName: '' });
  const [errors, setErrors] = useState({});

  return (
    <div>
      <Input
        id="profile-setup-input-firstname"
        data-object-id="profile-setup-input-firstname"
        name="firstName"
        value={formData.firstName}
        onChange={(e) => setFormData({ ...formData, firstName: e.target.value })}
        placeholder="First Name *"
      />
      {errors.firstName && (
        <p 
          id="profile-setup-error-firstname"
          data-object-id="profile-setup-error-firstname"
          className="error-message"
        >
          {errors.firstName}
        </p>
      )}
    </div>
  );
}
```

### Test Automation
```javascript
// Cypress example
cy.get('[data-object-id="profile-setup-input-firstname"]')
  .type('John');

cy.get('[data-object-id="profile-setup-button-submit"]')
  .click();

cy.get('[data-object-id="profile-setup-error-firstname"]')
  .should('not.be.visible');

// Playwright example
await page.locator('[data-object-id="profile-setup-input-firstname"]')
  .fill('John');

await page.locator('[data-object-id="profile-setup-button-submit"]')
  .click();

await expect(
  page.locator('[data-object-id="profile-setup-error-firstname"]')
).toBeHidden();
```

---

## Element Types & Patterns

### Input Fields
**Pattern**: `{page}-input-{fieldname}`
- `profile-setup-input-firstname`
- `profile-setup-input-email`
- `signin-input-password`

### Buttons
**Pattern**: `{page}-button-{action}`
- `profile-setup-button-submit`
- `profile-setup-button-cancel`
- `signin-button-google`

### Error Messages
**Pattern**: `{page}-error-{fieldname}`
- `profile-setup-error-firstname`
- `profile-setup-error-email`
- `signin-error-login`

### Modal Elements
**Pattern**: `{page}-modal-{element}`
- `profile-setup-modal-overlay`
- `profile-setup-modal-title`
- `profile-setup-modal-close`

### Navigation Elements
**Pattern**: `{page}-{section}-{element}`
- `start-header-logo`
- `start-header-signin`
- `start-footer-contact`

### Toggle/Switch Elements
**Pattern**: `{page}-toggle-{feature}`
- `profile-setup-toggle-terms`
- `settings-toggle-notifications`
- `preferences-toggle-darkmode`

---

## Best Practices

### DO:
✅ **Use consistent kebab-case** for Object IDs
✅ **Place Object ID immediately** after #### heading in specs
✅ **Use camelCase for API data** fields in documentation
✅ **Document both** Object ID and API field name
✅ **Include data-object-id attribute** for testing reliability
✅ **Create separate Object IDs** for error messages
✅ **Use descriptive names** that reveal purpose
✅ **Keep IDs unique** within the page/scenario
✅ **Reference Object IDs** in design tool layers (Figma/Sketch)
✅ **Use Object IDs in analytics** event tracking

### DON'T:
❌ **Mix naming conventions** within same project
❌ **Use spaces or underscores** in Object IDs
❌ **Forget error message Object IDs** for form fields
❌ **Skip Object IDs** for interactive elements
❌ **Create overly long IDs** (keep to 3 segments)
❌ **Use generic names** like `button-1` or `input-field`
❌ **Change Object IDs** after implementation without migration plan
❌ **Duplicate Object IDs** across different elements
❌ **Use camelCase in HTML** id attributes (use kebab-case)
❌ **Forget to document** Object IDs in specifications

---

## Benefits by Role

### For Developers
- ✅ Clear element targeting in code
- ✅ Consistent naming across team
- ✅ Easy test automation setup
- ✅ Fast debugging with searchable IDs
- ✅ Reduced naming conflicts
- ✅ Clear API data structure

### For Visual Designers
- ✅ Precise element identification in design tools
- ✅ Clear design-to-code traceability
- ✅ Visual regression testing with specific element targets
- ✅ Design review feedback with exact Object ID references
- ✅ State variations clearly documented per element
- ✅ Design system consistency validation
- ✅ Handoff documentation matches implementation
- ✅ Easy identification of missing design specifications

### For QA Engineers
- ✅ Reliable test selectors
- ✅ Automated testing support
- ✅ Bug reporting precision
- ✅ Regression test stability
- ✅ Cross-browser test consistency
- ✅ Visual diff testing targets

### For Product Managers
- ✅ Feature tracking by ID
- ✅ Analytics event tagging
- ✅ A/B test implementation
- ✅ User behavior analysis
- ✅ Conversion funnel tracking
- ✅ Feature usage metrics

### For UX/Content Designers
- ✅ Specifications match implementation
- ✅ Easy content updates via ID
- ✅ Clear component relationships
- ✅ Design system traceability
- ✅ Localization string mapping
- ✅ Content audit efficiency

---

## Common Patterns

### Form Validation Flow
```markdown
#### [Input](/docs/Components/Input.md) - Email Address
**OBJECT ID**: `profile-setup-input-email`
- **API Data Field**: `email`
- **Validation**: Required, valid email format
- **Interaction**: onChange → validate on blur

**Error Messages**
**OBJECT ID**: `profile-setup-error-email`
- **Required error**: "Email is required"
- **Format error**: "Please enter a valid email address"
```

### Modal Pattern
```markdown
**Modal Overlay**
**OBJECT ID**: `terms-modal-overlay`
- **Interaction**: onClick → close modal

**Modal Title**
**OBJECT ID**: `terms-modal-title`
- **Content**: "Terms of Service"

**Modal Content**
**OBJECT ID**: `terms-modal-content`
- **Purpose**: Scrollable terms text

**Modal Close Button**
**OBJECT ID**: `terms-modal-close`
- **Interaction**: onClick → close modal
```

### Navigation Pattern
```markdown
#### Logo
**OBJECT ID**: `start-header-logo`
- **Behavior**: Links to home page

#### Sign In Button
**OBJECT ID**: `start-header-signin`
- **Content**: "Sign in" / "Logga in"
- **Behavior**: Navigate to sign-in page

#### Language Selector
**OBJECT ID**: `start-header-language`
- **Behavior**: onChange → toggle language
```

---

## Migration Strategy

### Updating Existing Projects

**Step 1: Document Current State**
- List all interactive elements without Object IDs
- Identify existing id attributes being used
- Map elements to proposed Object IDs

**Step 2: Create Object ID Registry**
- Document all new Object IDs
- Ensure no conflicts with existing IDs
- Get team approval before implementation

**Step 3: Implement Gradually**
- Start with new features using Object IDs
- Update high-priority pages first
- Maintain backward compatibility with old IDs

**Step 4: Update Tests**
- Migrate test selectors to use data-object-id
- Run regression tests to ensure stability
- Update test documentation

**Step 5: Update Documentation**
- Add Object IDs to all conceptual documentation
- Update component specifications
- Create team reference guide

---

## Troubleshooting

### Issue: Duplicate Object IDs
**Problem**: Two elements share the same Object ID
**Solution**: Add more context to distinguish them
```
❌ Bad: `button-submit`, `button-submit`
✅ Good: `profile-setup-button-submit`, `checkout-button-submit`
```

### Issue: Object ID Too Long
**Problem**: `user-profile-account-settings-form-input-firstname`
**Solution**: Simplify to 3 segments
```
❌ Bad: `user-profile-account-settings-form-input-firstname`
✅ Good: `account-input-firstname` or `settings-input-firstname`
```

### Issue: Naming Conflicts
**Problem**: Object ID conflicts with CSS class or framework ID
**Solution**: Add project prefix or use data-object-id
```
✅ Option 1: `dogweek-profile-setup-input-email`
✅ Option 2: Use data-object-id attribute exclusively for Object IDs
```

### Issue: Multi-language Content
**Problem**: Should Object IDs change per language?
**Solution**: No, Object IDs stay the same, content changes
```
✅ Correct:
<button id="profile-setup-button-submit">
  {language === 'en' ? 'Save Profile' : 'Spara Profil'}
</button>
```

---

## Tools & Integration

### Design Tools
- **Figma**: Name layers with Object IDs for handoff clarity
- **Sketch**: Use symbol names matching Object IDs
- **Adobe XD**: Component names should reference Object IDs

### Analytics
```javascript
// Track interactions using Object IDs
analytics.track('Button Clicked', {
  objectId: 'profile-setup-button-submit',
  page: 'profile-setup',
  action: 'submit'
});
```

### A/B Testing
```javascript
// Target elements for variant testing
optimizely.activate('profile_form_test', {
  variations: {
    control: { 
      'profile-setup-button-submit': { text: 'Save Profile' }
    },
    variant: { 
      'profile-setup-button-submit': { text: 'Complete Setup' }
    }
  }
});
```

---

## Summary

**Object IDs are the bridge between:**
- Design specifications and implementation
- Documentation and working code
- Manual testing and automation
- Analytics and user behavior
- Team communication and collaboration

**When properly implemented, Object IDs provide:**
- 📋 **Traceability** from specs to production
- 🤖 **Automation** for testing and deployment
- 📊 **Analytics** for data-driven decisions
- 🎨 **Design-dev alignment** through shared vocabulary
- ⚡ **Efficiency** in debugging and maintenance

**The investment in systematic Object IDs pays dividends throughout the entire product lifecycle.**

---

**Related Phase**: [← Phase 4: Conceptual Documentation](04-Conceptual-Documentation.md)

---

*This guide ensures consistent Object ID implementation across all WPS2C projects, enabling seamless collaboration between design, development, testing, and analytics teams.*

**Created by**: Whiteport Sketch-to-Code Method  
**Reference**: [WPS2C GitHub Repository](https://github.com/whiteport-sketch-to-code-bmad-expansion)  
**Documentation follows**: WPS2C Zero Tolerance Parentheses Policy & Professional Naming Conventions

