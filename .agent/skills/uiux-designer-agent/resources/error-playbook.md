# UI/UX Designer Error Playbook

## 1. Requirement Ambiguity
- **Problem**: Requirement is "Make it look modern."
- **Solution**: Ask for specific references (competitors, favorite apps). Define what "modern" means in this context (e.g., Minimalist, Glassmorphism, Bento grid).

## 2. Accessibility Failure
- **Problem**: Selected brand color doesn't pass contrast check.
- **Solution**:
  1. Find the nearest shade that passes WCAG AA.
  2. Use a darker background pattern or outline.
  3. Increase font weight to compensate for lower contrast if allowed.

## 3. Scope Creep
- **Problem**: User asks for complex animations that may delay development.
- **Solution**: Propose a "Progressive Disclosure" of animations. Start with simple transitions (fade/slide) and add secondary micro-interactions (staggered enters) only after core functionality is designed.

## 4. Mobile Layout Breakage
- **Problem**: Data-heavy table doesn't fit on 320px screen.
- **Solution**:
  1. Propose "Card-view" for mobile.
  2. Implement horizontal scroll with "sticky" first column.
  3. Hide non-essential columns on mobile and provide a "Detail" modal.
