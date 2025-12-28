# Branching Navigator

An interactive branching narrative framework for creating decision-tree based experiences. Perfect for educational scenarios, corporate training, onboarding flows, and interactive storytelling.

## ✨ Features

- **Interactive Decision Trees**: Create multi-path narratives where user choices shape the journey
- **Visual Journey Map**: Real-time tree visualization showing visited paths and current position
- **Bilingual Support**: Built-in English/Italian support (easily extensible to other languages)
- **JSON-Based Content**: Easy-to-edit scenario files, no coding required for content changes
- **Visual Scenario Editor**: Dedicated tool for creating and managing scenarios
- **Resource Attachments**: Add downloads, links, and videos to any node
- **Progress Tracking**: Visual indicators for visited paths and current step
- **Backtracking**: Users can navigate back through their journey
- **No Build Process**: Single HTML files, works directly in browsers
- **Fully Responsive**: Works on desktop and mobile devices

## 🎯 Use Cases

- **Corporate Training**: Onboarding flows, compliance training, process walkthroughs
- **Education**: Interactive lessons, decision-making exercises, case studies
- **Product Tours**: Feature exploration, user onboarding
- **Interactive Stories**: Choose-your-own-adventure narratives
- **Process Documentation**: Visual workflow exploration

## 📁 Project Structure

```
branching-navigator/
├── config.json                 # Configuration (scenario file, languages)
├── branching-navigator.html    # Main navigator engine
├── scenario-editor.html        # Visual editor for creating scenarios
├── scenario-quiz.json          # Example: bilingual quiz scenario
├── scenario-workflow.json      # Example: monolingual workflow scenario
├── start-navigator.bat         # Quick start for navigator (Windows)
├── start-editor.bat            # Quick start for editor (Windows)
├── README.md                   # This file
├── LICENSE                     # MIT License
└── docs/                       # Folder for downloadable resources
    └── (your PDF, DOC files)
```

## 🚀 Quick Start

### Option 1: Using Start Scripts (Windows)

- Double-click `start-navigator.bat` to run the navigator
- Double-click `start-editor.bat` to run the editor

### Option 2: Manual Start

1. Open a terminal in the project folder
2. Start a local server:
   ```bash
   python -m http.server 8000
   ```
3. Open in your browser:
   - Navigator: `http://localhost:8000/branching-navigator.html`
   - Editor: `http://localhost:8000/scenario-editor.html`

### Option 3: Deploy to Web Server

Upload all files to any web server or static hosting (GitHub Pages, Netlify, Vercel).

> ⚠️ **Important**: The navigator requires a web server due to JSON loading. It won't work by opening the HTML file directly (`file://` protocol).

## ⚙️ Configuration

The `config.json` file controls which scenario to load and available languages:

```json
{
    "scenario": "scenario-quiz.json",
    "languages": ["en", "it"]
}
```

| Field | Description |
|-------|-------------|
| `scenario` | JSON file containing the scenario data |
| `languages` | Array of language codes. Use `["en", "it"]` for bilingual, `["en"]` for English only |

To switch scenarios, simply change the `scenario` value and refresh.

## 🎨 Using the Scenario Editor

The visual editor makes it easy to create and modify scenarios without editing JSON manually.

### Accessing the Editor

```
http://localhost:8000/scenario-editor.html
```

### Editor Features

- **Welcome Screen**: Start with a new scenario or open an existing file
- **Node List View**: See all nodes with their level and status (START, END, orphan)
- **Visual Map View**: Interactive tree visualization of your scenario
- **Inline Node Creation**: Create new nodes directly from the choice dropdown
- **Choice Text Validation**: The editor requires button text when creating nodes (prevents invisible choices)
- **Bilingual/Monolingual**: Automatically adapts to languages defined in `config.json`
- **Resource Management**: Add downloads, links, and videos to any node

### Workflow

1. Start the local server and open the editor
2. Click **New Scenario** or **Open File** to load an existing JSON
3. Select a node from the sidebar to edit it
4. Add choices with **+ Add Choice**
5. Use **+ Create new node...** in the Target dropdown to create child nodes
6. Click **Save** to download the updated JSON
7. Copy the saved file to the project folder, replacing the old version
8. Hard refresh (Ctrl+Shift+R) the navigator to see changes

### ⚠️ Important: Node Deletion

When deleting a node that has child nodes connected to it:

- The child nodes become **orphans** (disconnected from the tree)
- They remain visible in the editor but **invisible in the navigator**
- They appear in the Map view with a red border and "orphan" badge

**Best practice**: Delete nodes from the leaves (end nodes) upward, or manually reconnect orphaned nodes to other parent nodes before saving.

## 📝 JSON Structure

The scenario is defined in a simple JSON format:

```json
{
    "meta": {
        "title": { "en": "Scenario Title", "it": "Titolo Scenario" },
        "description": { "en": "Description", "it": "Descrizione" },
        "author": "Author Name"
    },
    "translations": {
        "en": { "step": "Step", "restart": "Start Over", ... },
        "it": { "step": "Passo", "restart": "Ricomincia", ... }
    },
    "startNode": "start",
    "nodes": {
        "start": {
            "content": {
                "en": "# Welcome\n\nThis is **markdown** content.",
                "it": "# Benvenuto\n\nQuesto è contenuto **markdown**."
            },
            "choices": [
                { "text": { "en": "Option A", "it": "Opzione A" }, "next": "node_a" },
                { "text": { "en": "Option B", "it": "Opzione B" }, "next": "node_b" }
            ],
            "resources": []
        }
    }
}
```

### Monolingual Scenarios

For single-language scenarios, set `"languages": ["en"]` in config.json. The editor will show single input fields instead of language pairs.

### Supported Markdown

- `# Heading 1` and `## Heading 2`
- `**bold**` and `*italic*`
- `- list items`
- `> blockquotes`

### Resource Types

| Type | Description | Icon |
|------|-------------|------|
| `download` | Downloadable file (PDF, DOC, etc.) | 📥 |
| `link` | External URL (opens in new tab) | 🔗 |
| `video` | Video link | 🎬 |

## 🌐 Deployment

### GitHub Pages

1. Push your files to a GitHub repository
2. Go to Settings → Pages
3. Select "Deploy from a branch" and choose `main`
4. Your navigator will be available at `https://username.github.io/repo-name/branching-navigator.html`

### Multiple Instances

For multiple training modules, create separate folders with independent config files:

```
/training-portal/
├── onboarding/
│   ├── config.json
│   ├── branching-navigator.html
│   └── scenario-onboarding.json
├── compliance/
│   ├── config.json
│   ├── branching-navigator.html
│   └── scenario-compliance.json
```

### Embedding via iframe

```html
<iframe 
    src="https://your-domain.com/branching-navigator.html" 
    width="100%" 
    height="600" 
    frameborder="0">
</iframe>
```

## 📋 Technical Details

- **Framework**: React 18 (via CDN)
- **Styling**: Tailwind CSS + custom CSS
- **No build process**: Everything runs directly in the browser
- **Dependencies**: None (all loaded via CDN)

### Browser Compatibility

Chrome, Firefox, Safari, Edge (all modern versions)

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 👤 Author

**Paolo Dalprato**
- Website: [ai-know.pro](https://ai-know.pro)
- Substack: [paolodalprato.substack.com](https://paolodalprato.substack.com)
