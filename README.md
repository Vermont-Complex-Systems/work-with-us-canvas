# JSON Canvas Kit

A SvelteKit template for hosting interactive [JSON Canvas](https://jsoncanvas.org/) files on GitHub Pages. Edit your canvas and markdown files in Obsidian, commit your changes, and have them automatically deployed to a beautiful, interactive web viewer.

## Features

- 📝 **Obsidian Integration** - Edit canvas and markdown files directly in Obsidian
- 🎨 **Interactive Viewer** - Pan, zoom, and drag nodes on the canvas
- 🔗 **Markdown Support** - Render markdown files with full GFM support
- 🚀 **Auto-Deploy** - GitHub Actions automatically deploys to GitHub Pages on push
- 📱 **Responsive** - Works on desktop and mobile devices
- ⚡ **Fast** - Static site generation with SvelteKit

## Getting Started

### 1. Create Your Repository

Click the **"Use this template"** button at the top of this repository to create your own copy.

### 2. Clone and Install

```bash
# Clone your new repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME

# Install dependencies
npm install
```

### 3. Open in Obsidian

1. Open Obsidian
2. Click **"Open folder as vault"**
3. Navigate to and select the `static/` folder in your repository
4. Start creating your canvas!

### 4. Start Development Server

```bash
# Start the dev server
npm run dev

# Or open in browser automatically
npm run dev -- --open
```

Visit `http://localhost:5173` to see your canvas in action.

## Creating Your Canvas

### In Obsidian

1. In your Obsidian vault (the `static/` folder), create markdown files for your content
2. Create a `.canvas` file (File → New Canvas)
3. Add your markdown files as nodes by dragging them onto the canvas
4. Connect nodes with edges to show relationships
5. Save your work

### Main Canvas File

The viewer looks for `static/main.canvas` by default. Make sure your main canvas file is named `main.canvas`.

## Deploying to GitHub Pages

Deployment happens automatically via GitHub Actions whenever you push to the `main` branch.

### First-Time Setup

1. Go to your repository settings
2. Navigate to **Pages** (under "Code and automation")
3. Under "Build and deployment", set:
   - **Source**: GitHub Actions
4. Push your changes and the workflow will deploy automatically

Your site will be available at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

For organization repos:
```
https://YOUR-ORG-NAME.github.io/YOUR-REPO-NAME/
```

### Manual Deployment

If you need to trigger a deployment manually:

```bash
git commit --allow-empty -m "Trigger deployment"
git push
```

## Customizing

### Repository Name

If you change your repository name, update the `base` path in `svelte.config.js`:

```javascript
paths: {
  base: process.env.NODE_ENV === 'production' ? '/YOUR-NEW-REPO-NAME' : ''
}
```

### Canvas Styling

Edit `src/lib/canvas.css` to customize colors, fonts, and styling. The CSS variables at the top of the file control the theme:

```css
:root {
  --color-bg-1: #fff;
  --color-bg-2: #fafafa;
  --color-tx-1: #3F062D;
  --color-ui-3: #5E0641;
  /* ... */
}
```

### Adding More Canvas Files

Currently, the viewer loads `main.canvas`. To support multiple canvas files, you can modify `src/routes/+page.svelte` to accept a query parameter or create additional routes.

## Workflow

1. **Edit in Obsidian** - Open the `static/` folder as a vault and work on your canvas
2. **Preview Locally** - Run `npm run dev` to see your changes in real-time
3. **Commit Changes** - `git add . && git commit -m "Update canvas"`
4. **Push to GitHub** - `git push origin main`
5. **Auto-Deploy** - GitHub Actions builds and deploys your site automatically

## Project Structure

```
jsoncanvas-kit/
├── static/                # Obsidian vault (your canvas and markdown files)
│   ├── main.canvas       # Main canvas file
│   ├── welcome.md        # Example markdown files
│   ├── getting-started.md
│   ├── canvas.js         # Canvas interaction scripts
│   └── prism.js          # Syntax highlighting
├── src/
│   ├── routes/
│   │   └── +page.svelte  # Main viewer component
│   └── lib/
│       └── canvas.css    # Canvas styling
├── .github/
│   └── workflows/
│       └── deploy.yml    # GitHub Actions deployment
└── svelte.config.js      # SvelteKit configuration
```

## Troubleshooting

### Canvas not loading

- Ensure your main canvas file is named `main.canvas` and located in the `static/` folder
- Check that file paths in your canvas don't include the `static/` prefix (just use `filename.md`)

### Styles not appearing

- Make sure `src/lib/canvas.css` is being imported in `+page.svelte`
- Clear your browser cache and hard reload (Cmd/Ctrl + Shift + R)

### Deployment failing

- Check the Actions tab in your GitHub repository for error logs
- Ensure GitHub Pages is enabled and set to use GitHub Actions as the source

## Technical Details

- **Framework**: SvelteKit with adapter-static
- **Markdown Rendering**: svelte-exmarkdown with GFM plugin
- **Canvas Format**: JSON Canvas spec v1.0
- **Deployment**: GitHub Actions + GitHub Pages

## Contributing

Feel free to open issues or submit pull requests to improve this template!

## License

MIT

## Resources

- [JSON Canvas Specification](https://jsoncanvas.org/)
- [Obsidian](https://obsidian.md/)
- [SvelteKit Documentation](https://svelte.dev/docs/kit)
