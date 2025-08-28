# Scenario & Page Creation Checklist

## Purpose
Ensure proper file structure, professional naming conventions, and comprehensive link management when creating new scenarios or pages. Based on real-world project experience and stakeholder feedback.

## ✅ Pre-Creation Verification

### 1. Repository Boundary Verification (CRITICAL)
- [ ] **MANDATORY: Run `pwd` command**: Verify current working directory before ANY file creation
- [ ] **MANDATORY: Confirm repository location**: Must be inside `echovoice-concept/` or `whiteport-sketch-to-code-bmad-expansion-latest/`
- [ ] **MANDATORY: Never create files at workspace root**: Files outside repositories require manual intervention to fix
- [ ] **Run `git status`**: Confirm you're in a valid git repository before proceeding
- [ ] **Confirm project docs folder**: Verify you're in the correct location (e.g., `echovoice-concept/docs/C-Scenarios/`)
- [ ] **Check existing structure**: Review current folder organization and naming patterns
- [ ] **Validate permissions**: Ensure write access to target directories

### 2. Naming Convention Planning
- [ ] **Apply Title-Case-With-Dashes**: All folder and file names must use this format (e.g., `01-User-Onboarding`)
- [ ] **URL-safe verification**: No spaces, special characters, or case-sensitive issues
- [ ] **Logical naming**: Pages vs Dialogs distinction (e.g., `1.4-Confirmation-Dialog` for modals)

## ✅ File Structure Standards

### 3. Professional Organization
- [ ] **Main specification prominence**: `.md` file must be immediately visible to project managers
- [ ] **Create Sketches/ subfolder**: Always create dedicated `Sketches/` subfolder when setting up new scenario steps
- [ ] **Sketches/ organization**: All visual assets organized in dedicated `Sketches/` subfolders
- [ ] **Scalable structure**: Ready for future `Visual-Design/` and `Code-Snippets/` folders
- [ ] **Consistent hierarchy**: Follow established patterns from existing scenarios

### 4. Navigation Flow Creation
- [ ] **Previous/Next links**: Update navigation links in adjacent pages 
- [ ] **Header navigation**: Add navigation at top and bottom of each page
- [ ] **Scenario overview**: Update main scenario index with new pages
- [ ] **Complete chain testing**: Verify unbroken flow through entire scenario

## ✅ Content Standards

### 5. Documentation Quality
- [ ] **Page context foundation**: Describe page features before individual objects
- [ ] **Success criteria**: Include success metrics after page overview
- [ ] **No parentheses**: Use clear explanations instead of parenthetical notes
- [ ] **Integrated technical requirements**: Embed in relevant sections, not separate blocks
- [ ] **Sketch reference included**: Add sketch image reference right after main page title
- [ ] **Bilingual text format consistency**: Use established SE/EN pattern from other scenario pages

### 6. Link Management Excellence
- [ ] **Component references**: Update all component usage examples with new paths
- [ ] **Cross-scenario links**: Verify links from other scenarios still work
- [ ] **Relative path optimization**: Use appropriate relative paths for components
- [ ] **Comprehensive verification**: Search for all references to changed paths

## ✅ Cross-Reference Updates

### 7. System-Wide Updates
- [ ] **Update main README**: Add scenario to project overview and progress tracking
- [ ] **Update component references**: Link any new components created for the scenario  
- [ ] **Update persona references**: Ensure scenario aligns with defined user personas
- [ ] **Check trigger map alignment**: Verify scenario supports business goals from trigger map

## ✅ URL-Safe Naming Standards

### 8. File and Folder Naming Convention
- [ ] **Use dashes instead of spaces**: All folder names must use dashes not spaces for URL compatibility
- [ ] **Scenario folders**: Use format `01-User-Registration/` not `01. User Registration/`
- [ ] **Page folders**: Use format `1.1-Landing-Page/` not `1.1 Landing Page/`
- [ ] **Consistency check**: Ensure all folder names follow URL-safe naming patterns
- [ ] **No special characters**: Avoid periods, spaces, and other URL-problematic characters in folder names
- [ ] **File names match**: Ensure `.md` file names match folder naming convention

## ✅ Quality Assurance

### 9. Comprehensive Review
- [ ] **Link integrity testing**: Click through all navigation links to verify they work
- [ ] **Image path verification**: Ensure all images load correctly from `Sketches/` folders
- [ ] **Cross-browser compatibility**: Verify paths work in different environments
- [ ] **Stakeholder usability**: Test from PM perspective - are main files immediately visible?

### 10. Documentation Standards Compliance
- [ ] **Title-Case-With-Dashes everywhere**: Verify naming consistency across all new files
- [ ] **Professional appearance**: Ensure documentation meets enterprise standards
- [ ] **Scalability validation**: Confirm structure can accommodate future expansion
- [ ] **Tool compatibility**: Verify paths work in IDEs, web servers, and file browsers

## ✅ Bilingual Documentation Standards

### 11. Swedish/English Interface Text
- [ ] **English structural labels**: All headers, sections, and functional elements use English names
- [ ] **Bilingual text format**: Use established pattern from existing scenario pages
- [ ] **Correct format example**: 
  ```
  **Button Label**:
  - SE: "Logga in för att spara"
  - EN: "Log in to save"
  ```
- [ ] **Avoid incorrect mixing**: Never use inline format like "SE: text | EN: text"
- [ ] **Nested structure for categories**: English label first, then indented SE/EN text labels
- [ ] **Consistency check**: Compare with 1.1 Start Page format for reference pattern

## ✅ Final Validation

### 12. Repository Safety Verification
- [ ] **Final location check**: Run `pwd` to confirm all files were created in correct repository
- [ ] **Git tracking verification**: Run `git status` to ensure all new files are properly tracked
- [ ] **No orphaned files**: Verify no files exist outside repository boundaries in workspace root
- [ ] **Repository integrity**: Confirm `.git` folder is present and accessible

### 13. Complete Flow Testing
- [ ] **End-to-end navigation**: Test complete scenario flow from start to finish
- [ ] **All images loading**: Verify all visual assets display correctly
- [ ] **No broken links**: Comprehensive check for any missing or incorrect references
- [ ] **Professional presentation**: Confirm documentation meets stakeholder expectations
- [ ] **Bilingual format consistency**: Verify all SE/EN text follows established patterns
- [ ] **Sketch inclusion verified**: Confirm sketch image displays correctly and is properly positioned

## Real-World Insights

### Lessons from Project Experience:
- **PM Feedback Critical**: Project managers need main documentation files immediately visible without visual clutter
- **URL Safety Essential**: Spaces and special characters break web deployment and tool compatibility  
- **Link Management Complex**: Renaming requires systematic updates across entire documentation system
- **Professional Structure Scales**: Well-organized projects grow more efficiently and maintain quality over time

### Common Mistakes to Avoid:
- **CRITICAL: Creating files outside repository boundaries** - requires manual intervention and causes git tracking issues
- **CRITICAL: Not verifying working directory before file creation** - leads to misplaced files
- Creating folders/files with spaces in names
- Forgetting to update navigation links in adjacent pages
- Placing images at root level where they obscure main documentation
- **Forgetting to create Sketches/ subfolder during initial setup** - leaves sketches without proper organization structure
- Using inconsistent naming conventions across the project
- Missing cross-references when reorganizing files
- Forgetting to include sketch image reference after main title
- Using inconsistent bilingual text formatting across pages
- Mixing Swedish and English text in single line with pipes
- Using parentheses to demote information instead of clear explanations

---

**Remember**: File structure errors require manual intervention to fix. Prevention through this checklist is critical for maintaining professional, scalable documentation that serves stakeholders effectively.
