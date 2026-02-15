## 2025-01-24 - [Accessibility in Avalonia]
**Learning:** Explicitly disabling `FocusAdorner` for all buttons in a global style without providing a clear alternative focus state (like a high-contrast border or background change) breaks keyboard navigation accessibility. Adding `AutomationProperties.Name` to icon-only buttons or buttons with symbolic content (like ◀/▶) is essential for screen reader support in Avalonia.
**Action:** When working with Avalonia, ensure every interactive element has a perceptible focus state and descriptive `AutomationProperties.Name` if its purpose isn't clear from text content alone.

## 2025-01-25 - [Cohesive Accessibility Labeling]
**Learning:** In complex editor UIs with many unlabeled inputs (like stats or IDs), adding `AutomationProperties.Name` provides a massive accessibility boost with zero visual impact. For grid-based data like Pokémon slots, reusing existing tooltip summary properties for `AutomationProperties.Name` ensures consistency between visual and screen reader feedback.
**Action:** Always check symbol-based controls (like markings) and input-dense grids for missing programmatic labels.
