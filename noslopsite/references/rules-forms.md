---
description: "Form UX, validation, accessibility, and polish rules."
connections: [rules-a11y, rules-interaction]
---

# Forms Rules

### forms-proper-labels
**Priority**: critical  
**Applies to**: frontend  
**Why it matters**: Placeholders are not labels.  
**How to detect**: Inputs with only placeholder text.  
**How to fix**: Always use visible `<label>` elements associated with inputs.

### forms-inline-validation
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Users shouldn't have to submit to see errors.  
**How to detect**: Validation only on submit.  
**How to fix**: Validate on blur or as user types (with debounce), show errors immediately.

### forms-error-messages
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Vague errors frustrate users.  
**How to detect**: Generic "Invalid input" messages.  
**How to fix**: Specific, helpful error messages that explain how to fix the problem.

### forms-error-summary
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Screen reader users and long forms need a summary.  
**How to detect**: Errors only next to fields.  
**How to fix**: Add an error summary at the top of the form that links to fields.

### forms-autofill
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Browser autofill saves time and reduces errors.  
**How to detect**: Missing or wrong `autocomplete` attributes.  
**How to fix**: Use correct autocomplete values (email, name, tel, etc.).

### forms-disabled-submit
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Prevents incomplete submissions.  
**How to detect**: Submit always enabled.  
**How to fix**: Disable submit until form is valid, or show clear validation on attempt.

### forms-loading-submit
**Priority**: high  
**Applies to**: frontend  
**Why it matters**: Users need feedback during submission.  
**How to detect**: No loading state on submit button.  
**How to fix**: Show loading spinner + disable button during submission.

### forms-success-feedback
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Users need confirmation that it worked.  
**How to detect**: Form just disappears or page reloads with no message.  
**How to fix**: Show clear success message or redirect with confirmation.

### forms-multi-step-progress
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Long forms need progress indication.  
**How to detect**: Multi-step forms without progress indicator.  
**How to fix**: Add step indicator and persist state.

### forms-password-manager
**Priority**: medium  
**Applies to**: frontend  
**Why it matters**: Password managers need proper attributes.  
**How to detect**: Missing autocomplete or wrong input types.  
**How to fix**: Use `type="password"`, proper autocomplete, and avoid preventing paste.
