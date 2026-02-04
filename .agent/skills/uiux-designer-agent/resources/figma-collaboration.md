# Figma & Human-in-the-Loop Collaboration

This protocol defines how a human Senior Designer collaborates with the UI/UX Designer Agent.

## 1. AI to Human (The Foundation)
The Agent provides the starting point for the human designer.
- **Tokens**: Use the `Style Manifest` from `design-handoff.md` to set up Figma Variables/Styles.
- **Layout**: Use the `Mermaid` flow or generated images as a structural guide.
- **Strategy**: Use the `Experience Strategy` to align on the project's creative direction.

## 2. Human to AI (The Refinement)
When a human designer improves the design in Figma, they must "sync" it back to the Agent using one of these methods:

### Method A: Visual Capture (Recommended)
1. **Screenshot**: Take a high-resolution screenshot of the Figma frame.
2. **Commentary**: Provide a brief explanation of *what* was changed and *why* (e.g., "Adjusted border-radius to 12px for a softer feel, updated primary brand color to match new guidelines").
3. **Delivery**: Share the image path or upload it to the project chat. The Agent will analyze the CSS/Styling from the image and description.

### Method B: Token Export
1. **JSON/CSS Export**: Use Figma plugins (like "Tailwind CSS" or "Design Tokens") to export variables as code.
2. **Delivery**: Paste the exported CSS/JSON into the chat.
3. **Agent Action**: The Agent will update the `design-handoff.md` and alert the Frontend Agent to sync the changes.

### Method C: Figma URL (If Access Enabled)
1. **Link Sharing**: Provide the Figma Frame URL.
2. **Agent Action**: The Agent (if it has browser/read tools enabled) will attempt to inspect the layout and update its internal model.

## 3. The "Anti-Drift" Rule
To prevent the code from drifting away from the human's design:
- Once the Human Senior Designer approves a design, the Agent must mark that version as **"LOCKED: DESIGN SOURCE"**.
- Any subsequent logic changes by the Agent must respect the established visual tokens (colors, spacing, typography).

## 4. Handoff to Implementation
After human refinement, the Agent updates the final `design-handoff.md`. The Frontend Agent MUST follow the updated manifest as the absolute source of truth.
