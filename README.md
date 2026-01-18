# 🎓 Interactive Educational Simulators

A collection of interactive simulators designed to explain complex concepts through visual and engaging interaction.

**Note**: These are qualitative simulations created for educational purposes. They demonstrate core principles using simplified models and exaggerated parameters to make concepts visible and understandable at human timescales.

## 🎯 Goal

Make learning more accessible through interactive visualizations that allow you to explore step-by-step how complex systems work.

## 📚 Available Simulators

| Simulator | Description | Try | Download |
|-----------|-------------|-----|----------|
| ❤️ [Heart](./heart/) | How the human heart works: the cardiac cycle in 7 steps | [Open](https://paolodalprato.github.io/interactive-simulators/heart/heart-simulator.html) | [ZIP](https://github.com/paolodalprato/interactive-simulators/releases/latest/download/heart-simulator.zip) |
| 🌌 [Gravity](./gravity/) | Explore gravitational attraction and emergent behavior from simple physical rules | [Open](https://paolodalprato.github.io/interactive-simulators/gravity/gravity-simulator.html) | [ZIP](https://github.com/paolodalprato/interactive-simulators/releases/latest/download/gravity-simulator.zip) |
| 🍽️ [Digestion](./digestion/) | Follow food through the digestive system and see how nutrients are absorbed | [Open](https://paolodalprato.github.io/interactive-simulators/digestion/digestion-simulator.html) | [ZIP](https://github.com/paolodalprato/interactive-simulators/releases/latest/download/digestion-simulator.zip) |

> **Note**: Branching Navigator has been moved to its own repository: [paolodalprato/branching-navigator](https://github.com/paolodalprato/branching-navigator)

## ✨ Common Features

- **Language support**: Each simulator handles languages independently (see individual READMEs)
- **Interactive**: click, adjust parameters, and explore
- **Educational**: designed with pedagogical principles
- **Responsive**: works on desktop, tablet, and mobile
- **No installation**: runs directly in the browser
- **Open source**: MIT licensed, free to use and modify

## 🚀 How to Use

### Online

Visit the links in the table above directly.

### Embed in Your Website

You can embed any simulator via iframe:

```html
<iframe 
  src="https://paolodalprato.github.io/interactive-simulators/heart/heart-simulator.html" 
  width="100%" 
  height="900" 
  frameborder="0"
  style="border: none; border-radius: 12px;">
</iframe>
```

### Locally

1. Clone the repository: `git clone https://github.com/paolodalprato/interactive-simulators.git`
2. Open the HTML file of the desired simulator in your browser

## 🛠️ Technologies

- HTML5 / CSS3
- React 18 (via CDN)
- Tailwind CSS (via CDN)
- Canvas 2D / SVG animations
- No build process required

## 📖 Educational Use

These simulators are designed for:
- **Classroom demonstrations**: visual aids for teachers
- **Self-study**: interactive exploration for students
- **Corporate training**: process visualization and onboarding
- **Public engagement**: science communication and outreach

Each simulator includes:
- Clear learning objectives
- Suggested usage scenarios
- Language support for accessibility (varies by simulator)
- Scientifically accurate content (within pedagogical simplifications)

## 📄 License

This project is released under the **MIT License** - see the [LICENSE](./LICENSE) file for details.

You are free to use, modify, and distribute these simulators, even for commercial purposes, as long as you credit the original author.

## 👤 Author

**Paolo Dalprato**

- 🌐 Website: [ai-know.pro](https://ai-know.pro)
- 📰 Substack: [paolodalprato.substack.com](https://paolodalprato.substack.com)
- 🐙 GitHub: [@paolodalprato](https://github.com/paolodalprato)

---

## 🤝 Contributing

Suggestions, corrections, and new ideas are welcome! Open an issue or a pull request.

*Have suggestions? Open an issue!*

## 🏗️ Development

Each simulator is:
- A single self-contained HTML file
- Self-documented with README in its folder
- Built following a consistent simulator-builder methodology
- Tested for accessibility and cross-browser compatibility

For developers interested in creating similar simulators, see the individual README files for technical implementation details.
