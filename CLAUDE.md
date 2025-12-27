# Interactive Simulators

Educational interactive simulators as single HTML files.

**Author**: Paolo Dalprato (https://ai-know.pro)  
**License**: MIT  
**Repository**: https://github.com/paolodalprato/interactive-simulators

## Project-Specific Architecture

Each simulator must follow these patterns:

- **Single HTML file** - no build process
- **React 18 + Tailwind CSS** via CDN (unpkg)
- **Bilingual** - EN default, IT toggle
- **User-controlled pacing** - no autoplay animations for learning content
- **Credits footer** linking to ai-know.pro
- **README.md** in each simulator folder (English only)

## File Structure

```
/{simulator-name}/
├── {simulator-name}-simulator.html
└── README.md
```

## Code Conventions

- Section separators: `// ============ SECTION ============`
- Data structures at top of file
- Components ordered: data → helpers → child components → main component
- ReactDOM.render at bottom

## When Reviewing Simulators

Check specifically for:
- Probabilistic values (absorption rates, timing) - must be documented
- SVG coordinates - should be commented or centralized
- Translation completeness - all UI text in both languages
- Scientific accuracy disclaimer - should be visible in UI, not just README

## Current Simulators

| Name | Type | Status |
|------|------|--------|
| heart | Discrete state (SVG) | Complete |
| gravity | Continuous physics (Canvas) | Complete |
| digestion | Discrete state with particles (SVG) | Complete, not yet on GitHub |
