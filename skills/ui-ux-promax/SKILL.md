---
name: ui-ux-promax
description: Premium UI/UX design guidance for websites and applications. Use when designing, auditing, or improving interfaces, user flows, design systems, responsive layouts, accessibility, visual hierarchy, interaction states, or frontend handoff.
---

# UI-UX-promax

Create interfaces that are clear, distinctive, inclusive, responsive, and practical to implement. Apply this skill when a request involves a new screen, redesign, UX audit, component library, visual direction, interaction pattern, or frontend-ready specification.

## Start with product intent

Before choosing colors or components, identify:

- The primary user, job-to-be-done, and success moment.
- The platform, viewport range, input methods, and technical constraints.
- The main action and the information users need to decide.
- The content model, empty states, permissions, loading behavior, and failure recovery.
- The brand personality and any existing design language that must be preserved.

If details are missing, state concise assumptions and continue. Prefer one strong recommended direction over a list of disconnected options.

## Use a deliberate design process

1. Map the critical user flow from entry to successful completion.
2. Establish information architecture and page-level hierarchy before styling.
3. Define a small visual system: type scale, spacing rhythm, color roles, radii, elevation, borders, and motion.
4. Compose the layout around content priority and responsive behavior.
5. Specify interaction states and accessibility behavior.
6. Review the result against the checklist below and call out trade-offs.

## Make visual decisions coherent

Use semantic tokens rather than scattered values. Name colors by role (`surface`, `text-primary`, `text-muted`, `accent`, `danger`, `focus`) instead of by hue. Keep one dominant visual idea and one supporting accent; avoid decorative gradients, shadows, or effects that compete with the task.

Use a readable type hierarchy with no more than two font families. Set body text around 16px or larger where platform constraints allow, use comfortable line height, and keep line lengths near 45–80 characters for long-form content. Establish consistent spacing using a small scale, such as 4/8px increments, and use alignment to create rhythm.

Design for the product’s personality rather than defaulting to generic cards, pills, or dashboard grids. Use imagery, illustration, texture, or motion only when it improves comprehension or reinforces the brand. Every decorative element should have a reason to exist.

## Design responsive layouts

Define behavior at narrow mobile, regular mobile/tablet, and desktop widths. Prefer fluid sizing and content-driven breakpoints over device-specific assumptions. Preserve the primary action, readable order, and touch target size when space is tight. Decide explicitly what stacks, scrolls, collapses, truncates, or disappears.

For touch interfaces, target at least 44×44 CSS pixels for interactive controls with sufficient spacing between adjacent targets. Do not rely on hover to reveal essential information. Keep focus, keyboard order, and visible labels intact at every breakpoint.

## Specify components and states

For every interactive component, describe its anatomy, purpose, and states:

- Default, hover, focus-visible, pressed, disabled, loading, success, error, and empty.
- Validation rules, inline help, error recovery, and confirmation for destructive actions.
- Keyboard operation, screen-reader name/role/state, and focus return behavior.
- Content limits, truncation rules, long-label behavior, and localization considerations.

Use native controls when they provide the correct semantics. If a custom control is necessary, document its keyboard and assistive-technology behavior instead of treating visual similarity as sufficient.

## Accessibility baseline

Meet WCAG 2.2 AA intent unless the project specifies a stricter target. Ensure meaningful contrast for text and essential UI, never communicate status by color alone, provide visible focus indicators, use semantic headings and landmarks, support keyboard navigation, associate labels with inputs, and provide useful alternative text. Respect reduced-motion preferences and avoid flashing or rapidly oscillating content.

Write interface copy in plain language. Make buttons describe the action, make errors actionable, and preserve user input after recoverable failures. Treat accessibility as part of the component definition, not a final polish pass.

## Frontend handoff format

When handing work to implementation, include:

1. A short design rationale tied to user goals.
2. Layout structure and responsive rules.
3. Token table for color, typography, spacing, radius, elevation, and motion.
4. Component inventory with variants and interaction states.
5. Content and validation rules.
6. Accessibility and keyboard requirements.
7. Acceptance criteria that can be checked in the browser.

For existing code, inspect and preserve working behavior before changing styles. Prefer small, composable CSS or component changes; avoid introducing a new dependency when the current stack can express the design. Keep secrets out of client-side code and flag exposed credentials during an audit.

## Quality checklist

Before considering the work complete, verify:

- The main action is obvious within a few seconds.
- The visual hierarchy matches task priority.
- Every important state is represented, including empty, loading, error, and success.
- The design works with keyboard, touch, zoom, and reduced motion.
- Text remains readable at narrow widths and with longer localized strings.
- Contrast, focus, labels, semantics, and error messaging are adequate.
- Repeated patterns use shared tokens and components.
- The implementation path is realistic for the repository’s current stack.
- The recommendation is specific enough for another designer or developer to execute without guessing.
