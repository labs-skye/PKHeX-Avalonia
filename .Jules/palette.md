## 2025-01-24 - [Accessibility in Avalonia]
**Learning:** Explicitly disabling `FocusAdorner` for all buttons in a global style without providing a clear alternative focus state (like a high-contrast border or background change) breaks keyboard navigation accessibility. Adding `AutomationProperties.Name` to icon-only buttons or buttons with symbolic content (like ◀/▶) is essential for screen reader support in Avalonia.
**Action:** When working with Avalonia, ensure every interactive element has a perceptible focus state and descriptive `AutomationProperties.Name` if its purpose isn't clear from text content alone.

## 2025-01-24 - [Accessible Slots and Markers]
**Learning:** Interactive grid elements (like Pokemon slots) and symbolic checkboxes (like markings) are often opaque to screen readers if they only contain images or symbols. Binding `AutomationProperties.Name` to a text summary (like `ToolTipSummary`) or providing explicit labels for symbols ensures the UI remains functional for all users.
**Action:** Always bind `AutomationProperties.Name` for repetitive interactive elements that represent complex data objects.
