# Digestive System Simulator

An interactive educational simulator that visualizes how different foods travel through the human digestive system.

## 📥 Download

**[Download ZIP](https://github.com/paolodalprato/interactive-simulators/releases/latest/download/digestion-simulator.zip)** - Single HTML file, no installation required

## 🎯 What It Teaches

This simulator helps users understand:

- **Digestive phases**: Mouth → Esophagus → Stomach → Small Intestine → Large Intestine
- **Nutrient absorption**: Where and how different nutrients (water, carbs, proteins, fats, fiber) are absorbed
- **Transit times**: How different foods require different digestion times
- **Organ functions**: What happens in each part of the digestive tract
- **Fat digestion**: The role of bile in emulsifying fats

## 🍽️ Available Foods

| Food | Components | Total Time | Key Learning |
|------|------------|------------|--------------|
| 💧 Water | Water only | 15-20 min | Fastest transit, full absorption in small intestine |
| 🍎 Apple | Water, carbs, fiber | 2-3 hours | Fiber reaches large intestine intact |
| 🥪 Sandwich | All nutrients | 4-6 hours | Mixed meal, fats slow digestion |
| 🥗 Salad | Water, carbs, fiber | 4-5 hours | High fiber feeds gut bacteria |
| 🧀 Cheese | Protein, fat | 5-7 hours | High fat = slow gastric emptying |
| 🍽️ Feast | All nutrients (large) | 8-12 hours | System under maximum load |

## 🎮 How to Use

1. **Select a food** from the menu
2. **Click "Next Phase"** to advance through digestion
3. **Watch the pellets** move and get absorbed
4. **Read the descriptions** to understand what's happening
5. **Compare different foods** to see how composition affects digestion

## 🔬 Scientific Accuracy

This is a **qualitative educational model** designed to illustrate digestive concepts. Key simplifications:

- Transit times are approximate ranges
- Nutrient absorption is represented probabilistically
- Anatomical shapes are simplified for clarity
- The simulator shows general principles, not exact physiology

**Accurate concepts represented:**
- Water absorption primarily in small intestine (pure water) vs. also large intestine (food water)
- Fats slow gastric emptying
- Bile is essential for fat emulsification
- Fiber passes undigested to large intestine
- Material moves as a mass through large intestine

## 🌐 Bilingual

The simulator supports both English and Italian with a language toggle.

## 💻 Technical Details

- **Single HTML file** - no build process required
- **React 18** via CDN
- **Tailwind CSS** for styling
- **SVG graphics** for the digestive tract visualization
- **CSS transitions** for smooth animations

## 📱 Embedding

```html
<iframe 
    src="https://paolodalprato.github.io/interactive-simulators/digestion/digestion-simulator.html"
    width="100%" 
    height="800"
    frameborder="0">
</iframe>
```

## 🎓 Suggested Use Cases

- **Biology classes**: Introduce digestive system anatomy
- **Nutrition education**: Show how different foods are processed
- **Health awareness**: Understand why some foods feel "heavy"
- **Self-study**: Interactive way to learn digestion basics

## 📄 License

MIT License - Free for educational and commercial use.

## 👤 Author

Created by [Paolo Dalprato](https://ai-know.pro)
