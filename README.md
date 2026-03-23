<<<<<<< HEAD
# STP Viewer - Offline CAD Model Viewer

A powerful offline STP/STEP file viewer built with Three.js and OpenCASCADE.

## Features

- **3D CAD Visualization**: View STP/STEP files in your browser
- **Measurement Tools**: Distance, diameter, radius, and angle measurements
- **Color Customization**: Apply colors to individual parts
- **Parts Management**: Show/hide/isolate parts with floating tree panel
- **Theme Support**: Light, dark, and system theme options
- **Responsive Design**: Works on desktop and mobile devices

## Local Development

### Quick Start
1. Double-click `start_server.bat` (Windows) or run `start_server.sh` (Linux/Mac)
2. Open http://localhost:8000 in your browser
3. Drag and drop your .STP or .STEP files to view them

### Manual Server Start
```bash
cd "stp-viewer-offline"
python -m http.server 8000
```

Then visit: http://localhost:8000

## Online Deployment

### Option 1: GitHub Pages (Free)
1. Create a GitHub repository
2. Upload all files from this folder
3. Go to Settings → Pages → Source: main branch
4. Your site will be available at: https://yourusername.github.io/repository-name

### Option 2: Netlify (Free)
1. Sign up at netlify.com
2. Drag and drop the entire folder to deploy
3. Get a free HTTPS URL instantly

### Option 3: Vercel (Free)
1. Sign up at vercel.com
2. Connect your GitHub repo or upload files
3. Automatic deployments with custom domain support

## Browser Compatibility

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## File Support

- .STP files
- .STEP files
- Standard CAD exchange formats

## Usage

1. Load a model by dragging files or clicking the upload area
2. Use mouse controls: orbit (left drag), pan (right drag), zoom (scroll)
3. Click parts to select and color them
4. Use measurement tools from the floating toolbar
5. Manage parts visibility with the floating tree panel

## Controls

- **Orbit**: Left mouse drag
- **Pan**: Right mouse drag
- **Zoom**: Mouse wheel
- **Fit View**: F key
- **Top View**: T key
- **Front View**: Y key
- **Select Part**: Left click on model
- **Measure**: Click measurement tools then click on model

## License

=======
# STP Viewer - Offline CAD Model Viewer

A powerful offline STP/STEP file viewer built with Three.js and OpenCASCADE.

## Features

- **3D CAD Visualization**: View STP/STEP files in your browser
- **Measurement Tools**: Distance, diameter, radius, and angle measurements
- **Color Customization**: Apply colors to individual parts
- **Parts Management**: Show/hide/isolate parts with floating tree panel
- **Theme Support**: Light, dark, and system theme options
- **Responsive Design**: Works on desktop and mobile devices

## Local Development

### Quick Start
1. Double-click `start_server.bat` (Windows) or run `start_server.sh` (Linux/Mac)
2. Open http://localhost:8000 in your browser
3. Drag and drop your .STP or .STEP files to view them

### Manual Server Start
```bash
cd "stp-viewer-offline"
python -m http.server 8000
```

Then visit: http://localhost:8000

## Online Deployment

### Important: WebAssembly Configuration Required

For the CAD viewer to work online, you need to configure your hosting platform to serve WebAssembly files correctly. The following files have been added to fix this:

- `vercel.json` - Configuration for Vercel
- `_headers` - Configuration for Netlify

### Option 1: Vercel (Recommended)
1. Sign up at [vercel.com](https://vercel.com)
2. Connect your GitHub repository or upload the files
3. The `vercel.json` file will automatically configure the correct headers
4. Your site will be available at: `https://your-project.vercel.app`

**Troubleshooting Vercel:**
- Make sure all files in the `libs/` folder are uploaded
- Check that `occt-import-js.wasm` (21MB) uploaded successfully
- The `vercel.json` handles MIME types and CORS automatically

### Option 2: Netlify
1. Sign up at [netlify.com](https://netlify.com)
2. Drag and drop the entire folder to deploy
3. The `_headers` file will automatically configure headers
4. Get a free HTTPS URL instantly

### Option 3: GitHub Pages
1. Create a GitHub repository
2. Upload all files from this folder
3. Go to Settings → Pages → Source: main branch
4. **Note:** GitHub Pages has stricter CORS policies - may not work reliably with WebAssembly

### Manual Header Configuration

If your hosting platform doesn't support the config files, add these headers manually:

**For .wasm files:**
```
Content-Type: application/wasm
Cross-Origin-Embedder-Policy: require-corp
Cross-Origin-Opener-Policy: same-origin
```

**For all files in /libs/:**
```
Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: GET, POST, OPTIONS
Access-Control-Allow-Headers: Content-Type
```

## Browser Compatibility

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## File Support

- .STP files
- .STEP files
- Standard CAD exchange formats

## Usage

1. Load a model by dragging files or clicking the upload area
2. Use mouse controls: orbit (left drag), pan (right drag), zoom (scroll)
3. Click parts to select and color them
4. Use measurement tools from the floating toolbar
5. Manage parts visibility with the floating tree panel

## Controls

- **Orbit**: Left mouse drag
- **Pan**: Right mouse drag
- **Zoom**: Mouse wheel
- **Fit View**: F key
- **Top View**: T key
- **Front View**: Y key
- **Select Part**: Left click on model
- **Measure**: Click measurement tools then click on model

## License

>>>>>>> 110eaba (Update viewer UI + sidebar toggle + webassembly headers)
This project is open source and available under the MIT License.