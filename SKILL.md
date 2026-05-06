---
name: tasteful-frontend-designer
description: Use when building, redesigning, or improving frontend UI views, landing pages, dashboards, forms, app screens, component layouts, design systems, or any user-facing interface. Enforces tasteful visual design, UX hierarchy, spacing, typography, color restraint, responsiveness, accessibility, interaction polish, and implementation quality. Do not use for backend-only tasks.
version: 1.0.1
author: Harley Davey
license: MIT
metadata:
   tags: [frontend, design, ui, ux, visual-polish, accessibility, responsive]
   related_skills: [popular-web-designs, sketch, claude-design, test-driven-development]
---

# Tasteful Frontend Designer

## Overview

This skill prevents generic, flat, under-designed frontend output. Use it to make Codex treat visual design as a first-class requirement rather than a thin styling pass after the code works.

Every user-facing screen should feel intentionally designed: clear hierarchy, strong spacing, tasteful typography, restrained color, polished components, responsive behavior, accessible states, and small interaction details that make the interface feel finished.

The goal is not to make every product look flashy. The goal is to make every UI look coherent, professional, and appropriate for its context.

## When to Use

Use this skill for any task involving:

- Landing pages and marketing websites
- SaaS dashboards and admin panels
- Mobile or web app screens
- Forms, onboarding flows, booking flows, checkout flows, and settings pages
- Navigation, sidebars, headers, footers, tabs, cards, lists, tables, modals, drawers, empty states, loading states, and error states
- Component libraries, design systems, Tailwind themes, CSS variables, and style tokens
- Redesigns, visual polish passes, UX cleanup, or frontend code reviews

Do not use for:

- Backend-only tasks
- Data model changes with no UI surface
- CLI-only tools
- Pure infrastructure work

If the task has even one visible UI screen, this skill applies.

## Core Rule

Do not ship generic, flat, unstyled UI.

A frontend implementation is not complete until it has intentional choices for:

- Layout and alignment
- Spacing rhythm
- Visual hierarchy
- Typography scale and weight
- Color palette and contrast
- Component shape language
- Borders, shadows, and surfaces
- Hover, focus, active, disabled, loading, empty, and error states
- Responsive behavior
- Accessibility
- Copy clarity

If the screen could be mistaken for a default scaffold, raw database admin, or unstyled component demo, revise it before finalizing.

## Discovery Before Designing

Before implementing, inspect the existing project and gather visual direction.

### Ask the User When Practical

If the user has not provided design direction and the task is not urgent, ask concise questions such as:

1. What visual style should this follow?
   - Minimal SaaS
   - Premium/luxury
   - Startup/AI
   - Editorial/content-heavy
   - Apple-like
   - Linear/Vercel-style
   - Enterprise dashboard
   - Mobile-first consumer app
   - Playful/brand-heavy

2. Are there reference sites, screenshots, brands, or apps to match?

3. What shape language should the UI use?
   - Soft rounded corners
   - Moderate radius
   - Sharp technical/editorial edges

4. Are there font preferences?
   - System font
   - Geometric sans
   - Editorial serif
   - Technical/monospace accents

5. Should the UI be:
   - Light mode, dark mode, or both?
   - Spacious or dense?
   - Bold/high-contrast or quiet/subtle?
   - Mostly static or enhanced with subtle animations?

Ask only what materially affects the design. Do not turn every frontend task into a long questionnaire.

### Default When Direction Is Missing

If asking is impractical or would slow down a clear task, infer this tasteful default:

- Clean modern SaaS aesthetic
- Spacious layout with deliberate grouping
- Strong typography hierarchy
- Neutral base palette with one primary accent
- Subtle borders and soft shadows
- Moderate rounded corners
- Clear primary action
- Accessible color contrast
- Responsive desktop/tablet/mobile behavior
- Subtle 150-250ms transitions for hover/focus/reveal states

State the assumption briefly in the final response.

## Existing Project Rules

Before adding new styling:

1. Inspect existing theme files, design tokens, CSS variables, global CSS, component libraries, and shared layouts.
2. Reuse existing components and patterns before creating new ones.
3. Match the current product style unless the user explicitly asks for a redesign.
4. Do not introduce a new UI library, animation library, icon set, or font package unless it is clearly necessary.
5. Do not hardcode random one-off colors if the project has a theme system.
6. Do not create conflicting button, card, table, or form styles when shared components already exist.
7. Preserve brand colors and product conventions unless improving them is part of the task.

Tasteful design in an existing product means coherence, not novelty.

## Visual Direction Framework

Before writing code, choose a clear visual direction. A useful one-sentence design direction looks like:

- “A polished Linear-style SaaS dashboard with dark neutral surfaces, restrained yellow accents, compact cards, and crisp borders.”
- “A warm premium booking flow with generous whitespace, rounded cards, editorial typography, and calm motion.”
- “A mobile-first consumer app screen with playful color, large touch targets, soft elevation, and friendly empty states.”

Use this direction to make consistent decisions about spacing, typography, color, corners, shadows, and animation.

## Layout Standards

Every view should have:

- A clear page structure: header, main content, supporting content, and action areas
- Intentional max-widths so content does not stretch awkwardly on large screens
- Consistent horizontal and vertical spacing
- Strong alignment between headings, cards, controls, and content blocks
- Logical grouping of related content
- Enough whitespace to avoid clutter
- Responsive behavior for mobile, tablet, and desktop
- A clear primary action and secondary actions that do not compete

Avoid:

- Edge-to-edge text blocks
- Full-width content with no max-width or visual rhythm
- Cramped forms and dense controls with no grouping
- Unaligned cards, buttons, or inputs
- Random spacing values
- Dashboard views that look like raw database output
- Empty top-level pages that feel like placeholders

### Practical Layout Defaults

When no product-specific system exists:

- Use a centered max-width for marketing content.
- Use a structured grid for cards and dashboards.
- Use consistent section padding.
- Separate major regions with background shifts, borders, or whitespace.
- Keep line lengths readable.
- Make mobile layouts single-column unless there is a strong reason not to.

## Typography Standards

Use typography to create hierarchy and confidence.

Minimum expectations:

- Large, confident page headings
- Clear section titles
- Readable body text
- Muted helper text
- Consistent font weights
- Comfortable line-height
- Short labels and scannable copy

Avoid:

- Everything the same size
- Weak headings that do not anchor the page
- Tiny low-contrast labels
- Overusing bold text
- Overly long line lengths
- Decorative font choices that hurt readability

### Typography Checklist

Before finalizing, verify:

- The most important message is visually obvious within 3 seconds.
- Headings, labels, body text, and metadata have distinct treatments.
- Font sizes scale down gracefully on mobile.
- Text contrast is accessible.
- Copy is specific, not generic filler.

## Color Standards

Use a restrained, coherent palette.

Recommended palette structure:

- Neutral background
- Elevated surface color
- Subtle border color
- Primary text
- Muted text
- One primary accent
- Optional secondary accent
- Semantic success, warning, error, and info colors

Avoid:

- Too many bright colors
- Random gradients
- Low-contrast text
- Pure black on pure white unless intentional
- Brand-conflicting colors
- Multiple accents competing for attention
- Semantic colors used decoratively in ways that reduce clarity

### Gradients

Use gradients only when they fit the product style. Prefer subtle depth, glow, or background atmosphere over loud rainbow gradients. If a gradient is used, keep the rest of the palette restrained.

## Components Standards

Cards, buttons, inputs, tables, modals, tabs, and nav should feel finished.

### Buttons

Buttons should have:

- Clear primary, secondary, and destructive variants where needed
- Hover state
- Focus-visible state
- Active/pressed state when appropriate
- Disabled state
- Loading state for async actions
- Consistent height, padding, radius, and typography

Avoid tiny ambiguous buttons, unclear hierarchy between actions, and primary buttons that blend into the background.

### Inputs and Forms

Forms should have:

- Visible labels
- Helper text where useful
- Clear required/optional treatment when relevant
- Focus states
- Validation states
- Error messages near the affected fields
- Logical grouping
- Comfortable touch targets on mobile
- A clear submit action

Avoid placeholder-only labels, cramped field stacks, and validation messages that are generic or detached from the field.

### Cards and Surfaces

Cards should have:

- Consistent padding
- Consistent radius
- Border or shadow treatment that separates them from the background
- Clear internal hierarchy
- Logical actions

Avoid borderless white cards on a white background, heavy shadows everywhere, and random radius values.

### Tables and Data Views

Tables should be readable and usable:

- Align numbers and dates consistently
- Use clear headers
- Add row hover or selected states where useful
- Preserve readable spacing
- Provide empty, loading, and error states
- Handle mobile with horizontal scroll, stacked cards, or prioritized columns

Avoid dumping raw database output with no formatting, hierarchy, or responsive treatment.

### Empty, Loading, and Error States

Every meaningful async or data-dependent UI should account for:

- Empty state: what happened, why it matters, and what to do next
- Loading state: skeleton, spinner, shimmer, or optimistic placeholder
- Error state: what went wrong and how to recover

Blank white areas are not acceptable polished UI.

## Corners, Borders, and Shadows

Use one consistent shape language.

Guidelines:

- Rounded corners create a friendly, modern feel.
- Sharper corners create a technical, editorial, or enterprise feel.
- Borders create structure without excessive depth.
- Shadows should be subtle and used sparingly.
- Elevation should reflect hierarchy: modals above cards, cards above background, buttons above surfaces only when needed.

Avoid:

- Mixing sharp and highly rounded elements randomly
- Heavy shadows on every card
- Inconsistent radii between related components
- Borderless surfaces that disappear into the page

If the user explicitly mentions rounded corners versus sharp edges, apply that preference consistently to cards, buttons, inputs, modals, and charts.

## Motion Standards

Use motion to improve perceived quality, not to distract.

Good uses:

- Hover transitions
- Button press states
- Modal or drawer enter/exit transitions
- Accordion expand/collapse
- Skeleton loading
- Small reveal animations for marketing sections
- Subtle chart or metric entrance animations

Avoid:

- Excessive animation
- Slow transitions
- Motion that blocks usability
- Animating every element
- Large parallax effects unless explicitly requested

Default motion:

- 150-250ms
- ease-out or equivalent
- Animate opacity, transform, border, background, and shadow
- Respect reduced-motion preferences when possible

## UX Standards

Every screen should answer:

1. What is this?
2. What matters most?
3. What should the user do next?
4. What happens after the user acts?
5. What could go wrong, and how is that handled?

### Landing Pages

A polished landing page should:

- Lead with a specific value proposition
- Show outcomes, not just features
- Use strong CTA hierarchy
- Include trust signals where appropriate
- Make sections visually distinct
- Use specific, believable copy
- Avoid generic AI/startup filler language
- End with a clear next step

### Dashboards

A polished dashboard should:

- Prioritize the most important metric or action
- Use cards and sections to organize complexity
- Make status, trends, and exceptions obvious
- Use visual hierarchy so not every card competes
- Include helpful empty and loading states
- Avoid looking like a raw admin database table

### Forms and Flows

A polished form should:

- Group fields logically
- Ask only for necessary information
- Use clear labels and validation
- Keep the primary action visible
- Explain consequences before destructive actions
- Show progress for multi-step flows
- Preserve user input when errors occur

### Navigation

Navigation should:

- Make current location obvious
- Keep labels concise
- Group related items
- Avoid overcrowding
- Work on mobile
- Provide clear affordances for menus, drawers, and tabs

## Accessibility Standards

Tasteful UI must also be usable.

Minimum expectations:

- Semantic HTML where possible
- Visible keyboard focus states
- Sufficient color contrast
- Labels associated with inputs
- Buttons for actions and links for navigation
- Alt text for meaningful images
- ARIA only when semantic HTML is insufficient
- Reduced-motion consideration for non-essential animation
- Touch targets large enough for mobile interaction

Do not sacrifice accessibility for visual novelty.

## Implementation Standards

When coding:

- Prefer semantic HTML and accessible primitives
- Reuse project components and design tokens
- Keep styling maintainable and consistent
- Avoid deeply nested brittle markup
- Avoid one-off CSS unless justified
- Keep components reusable where the pattern will repeat
- Test responsive states
- Keep business logic separate from presentation when practical
- Avoid introducing dependencies for simple styling
- Do not break existing tests, routes, or data behavior while polishing UI

## Frontend Quality Workflow

For any UI task, follow this sequence:

1. Inspect existing style system and UI conventions.
2. Identify the screen’s purpose, primary user action, and visual hierarchy.
3. Choose or confirm a design direction.
4. Implement layout and structure first.
5. Apply typography, spacing, color, surface, and component polish.
6. Add interaction states: hover, focus, active, disabled, loading, empty, error.
7. Check responsive behavior at mobile, tablet, and desktop sizes.
8. Check accessibility basics.
9. Self-review visually before finalizing.

## Tasteful Defaults by Surface

### SaaS Dashboard

- Neutral background with elevated cards
- Compact but readable spacing
- Clear metric cards and status indicators
- Muted borders instead of heavy shadows
- One accent color for primary actions and important states
- Tables with readable rows, alignment, and empty states

### Marketing Page

- Strong hero section
- Specific headline and supporting copy
- Clear CTA pair
- Alternating sections with visual rhythm
- Feature cards with differentiated icons or treatments
- Trust indicators or proof points when available
- Responsive, polished mobile hero

### App Screen

- Clear top-level title and primary action
- Comfortable touch targets
- Reduced cognitive load
- Persistent or obvious navigation
- Friendly empty/loading/error states
- Smooth but restrained transitions

### Admin Panel

- Dense enough for productivity, not cramped
- Strong information architecture
- Consistent tables, filters, badges, and actions
- Status colors that are semantic and restrained
- Clear destructive action confirmation

## Common Pitfalls

1. Generic scaffold UI
   - Symptom: looks like default Tailwind/bootstrap/shadcn examples pasted together.
   - Fix: add product-specific hierarchy, spacing, copy, surfaces, and state treatment.

2. Visual noise
   - Symptom: gradients, shadows, icons, badges, and accent colors all compete.
   - Fix: reduce palette, remove decorative elements, make one thing primary.

3. Inconsistent shape language
   - Symptom: pills, sharp cards, rounded modals, and square inputs mixed randomly.
   - Fix: choose one corner philosophy and apply it consistently.

4. Weak hierarchy
   - Symptom: user cannot tell what matters first.
   - Fix: increase heading confidence, group content, mute secondary elements, and clarify primary action.

5. Cramped spacing
   - Symptom: forms and cards feel like raw admin output.
   - Fix: add section spacing, card padding, row gaps, and readable line-height.

6. Overly stretched desktop layouts
   - Symptom: text and tables span the entire screen.
   - Fix: add max-widths, grids, side panels, or content containers.

7. Broken mobile experience
   - Symptom: desktop layout collapses awkwardly or overflows.
   - Fix: design mobile stacking, responsive grids, and table alternatives.

8. Missing interaction states
   - Symptom: UI looks okay in screenshot but feels unfinished in use.
   - Fix: add hover, focus, active, disabled, loading, empty, and error states.

9. Inaccessible polish
   - Symptom: beautiful but low-contrast, keyboard-hostile, or label-less.
   - Fix: restore contrast, semantic markup, labels, and focus-visible styles.

10. Ignoring the existing product language
    - Symptom: new view looks better in isolation but mismatched in the app.
    - Fix: reuse tokens and components; improve within the system unless redesigning.

## Self-Review Checklist

Before finalizing frontend work, answer these questions:

- [ ] Does the page look intentionally designed rather than scaffolded?
- [ ] Is the hierarchy obvious within 3 seconds?
- [ ] Is spacing consistent across sections and components?
- [ ] Are typography sizes, weights, and line-heights deliberate?
- [ ] Are colors restrained, accessible, and brand-aligned?
- [ ] Are buttons, inputs, cards, tables, and nav polished?
- [ ] Are hover, focus, active, disabled, loading, empty, and error states handled where relevant?
- [ ] Is mobile usable and not an afterthought?
- [ ] Is desktop not overly stretched?
- [ ] Are accessibility basics covered?
- [ ] Does the implementation match existing project conventions?
- [ ] Would this look acceptable in a professional portfolio or production SaaS product?

If any major answer is no, revise before presenting the result.

## Output Expectations

When responding after implementation:

- Briefly explain the visual direction used
- Mention the main UI/UX improvements
- Mention files changed
- Mention any assumptions made
- Mention verification performed
- Do not over-explain obvious styling details

A good final note sounds like:

“Used a clean modern SaaS direction with spacious cards, restrained neutral surfaces, one blue accent, clearer hierarchy, and polished form states. Updated the dashboard layout, shared card styles, and responsive table behavior. Assumed light mode only because the project has no dark theme. Verified desktop/mobile breakpoints and keyboard focus states.”
