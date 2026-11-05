# Zoom Lens Simulator

An interactive side view of a 24-70 mm zoom lens on a mirrorless body, cut in half along its axis. It shows how the focal length changes the angle of view and how the aperture changes the depth of field, one setting at a time.

## 📥 Download

**[Download ZIP](https://github.com/paolodalprato/interactive-simulators/releases/latest/download/zoom-lens-simulator.zip)** — Extract the archive, then open the single HTML file directly in a browser. No installation or network connection is required.

## 🎯 What You'll Learn

- How the focal length changes in the model: a rotating cylinder with two slots moves two lens groups along the axis by different amounts
- How the diagonal angle of view narrows from 84° at 24 mm to 34° at 70 mm
- How the aperture blades close and widen the zone in focus around a subject at 2 m
- Why the depth of field depends on the focal length as well as on the f-number

## 🚀 Try It

**[Open the simulator →](https://paolodalprato.github.io/interactive-simulators/zoom-lens/zoom-lens-simulator.html)**

**Embed in your website**:

```html
<iframe
  src="https://paolodalprato.github.io/interactive-simulators/zoom-lens/zoom-lens-simulator.html"
  width="100%"
  height="1200"
  frameborder="0"
  style="border: none; border-radius: 12px;">
</iframe>
```

## 🎮 How to Use

1. Choose **Focal length** or **Aperture** with the buttons at the top left.
2. Move the pointer sideways across the figure (drag on touch screens, or use the left and right arrow keys).
3. With **Focal length** selected, the lens groups move and the cone of the angle of view opens or closes. The zone in focus stays visible but dimmed, because it also changes with the focal length.
4. With **Aperture** selected, the iris blades close from f/2.8 to f/16 and the zone in focus grows.
5. Read the values at the bottom right: the ones that change with the selected setting are in bold.
6. Switch between English and Italian with the **EN** and **IT** buttons.

## 🔬 The Model Behind the Drawing

The simulator is a qualitative representation. It shows how a zoom lens works, not the exact values of a real lens.

- **Optics**: the lens is simplified to two lens groups, a negative front group and a positive rear group, which move along the axis as the zoom ring turns.
- **Angle of view**: full-frame sensor (36 × 24 mm), diagonal angle of view. These values are the geometry of any 24-70 mm lens on full frame.
- **Depth of field**: the zone in focus around a subject at 2 m shows how the depth of field changes with the aperture and the focal length.
- **Scale**: the space in front of the lens is drawn at 1:40 against the lens.

## 🛠️ Technical Details

- One self-contained HTML file with embedded CSS, SVG and JavaScript
- Drawn with the Anatomy skill for Claude (isometric kit used here in a side view)
- Bilingual English and Italian interface
- No external runtime dependency or remote service
- Responsive layout for desktop and mobile screens

## 📄 License and Credits

MIT License — see [LICENSE](../LICENSE). Created by [Paolo Dalprato](https://www.ai-know.pro/) and developed with Claude Opus 5.5.
