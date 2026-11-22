# Component specification — status indicator

## Purpose
Show an extension state as readable text with a matching visual treatment.

## Astryx inventory
Check whether Astryx already supplies this behavior. Prefer its exported component through @neometaharness/ui. Record the upstream component and version.

## States
- Healthy: status text and successful state.
- Degraded: status text, explanation, and accessible action.
- Off: status text and available enable control.
- Loading: meaningful progress indication.
- Error: actionable error text and retry option.

## Accessibility and themes
Use semantic status text and keyboard-reachable actions. Verify focus, contrast, and disabled appearance in both light and dark. Avoid color-only meaning.

## Verification
Capture screenshots and keyboard tests for every state. Note any missing Astryx behavior before requesting a Neo-specific component.
