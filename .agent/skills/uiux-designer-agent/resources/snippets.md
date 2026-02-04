# UI/UX Design Snippets (Style Manifest Templates)

The Designer Agent should provide a specific manifest like these for the Frontend Agent:

## Manifest A: "The High-Trust Professional" (FinTech/SaaS)

```css
:root {
  /* Logic: Neutral backgrounds, strong semantic colors */
  --bg-primary: #f8fafc;
  --bg-surface: #ffffff;
  --text-main: #0f172a;
  --accent-primary: #2563eb; /* Trust Blue */
  --border-subtle: #e2e8f0;
  
  --radius-strict: 4px;
  --shadow-flat: 0 1px 3px rgba(0,0,0,0.1);
}
```

## Manifest B: "The Immersive Dark" (Gaming/Creative)

```css
:root {
  /* Logic: Deep backgrounds with atmospheric glow */
  --bg-primary: #050505;
  --bg-surface: #121212;
  --text-main: #e2e2e2;
  --accent-glow: #a855f7; /* Neon Violet */
  --border-glass: rgba(255, 255, 255, 0.1);
  
  --glass-blur: blur(12px);
  --shadow-glow: 0 0 20px rgba(168, 85, 247, 0.3);
}
```

## Manifest C: "The Playful Learning" (EdTech/Kids)

```css
:root {
  /* Logic: High saturation, rounded corners, soft shadows */
  --bg-primary: #fffbeb;
  --text-main: #1e293b;
  --accent-pop: #f43f5e; /* Rose */
  
  --radius-bouncy: 24px;
  --shadow-soft: 0 8px 0 rgba(0,0,0,0.05); /* 3D effect shadow */
}
```

## Reusable Interaction Snippet (Context-Aware)

```css
/* Every manifest should define a standard focus ring for A11y */
:focus-visible {
  outline: 2px solid var(--accent-primary, var(--accent-glow, var(--accent-pop)));
  outline-offset: 2px;
}
```
