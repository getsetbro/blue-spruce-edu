# Blue Spruce High School Website

Blue Spruce High School is a simple static HTML website featuring information about a homeschool high school. The website is designed to be served directly as static files with no build process or dependencies.

**ALWAYS** reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the information provided here.

## Working Effectively

### Repository Structure and Key Files
- **index.html**: Main website file containing all HTML, CSS, and content inline
- **README.md**: Minimal project description
- **LICENSE**: Mozilla Public License 2.0
- **.gitignore**: Standard ignore file (includes node_modules, build, dist directories)

### Development Environment Setup
- **No build process required** - This is a static HTML website
- **No dependencies to install** - All styling is inline CSS, no external packages
- **No compilation needed** - Ready to serve directly

### Running the Website Locally
Run the following commands to serve the website locally:

```bash
cd /path/to/blue-spruce-edu
python3 -m http.server 8000
```

- **Access**: Open browser to `http://localhost:8000`
- **Expected load time**: Instant (< 1 second)
- **NEVER CANCEL**: The HTTP server runs indefinitely until manually stopped with Ctrl+C

### Alternative Local Server Options
If Python is not available, use any of these alternatives:

**Using Node.js (if available):**
```bash
npx http-server . -p 8000
```

**Using PHP (if available):**
```bash
php -S localhost:8000
```

## Validation and Testing

### Manual Testing Scenarios
**ALWAYS** perform these validation steps after making any changes to index.html:

1. **Visual Validation**:
   ```bash
   python3 -m http.server 8000
   # Open http://localhost:8000 in browser
   ```
   - Verify header displays "Welcome to Blue Spruce H.S." with blue background (#2a5d67)
   - Confirm tagline "Small but mighty, focused and ready to compete!" is visible
   - Check that the blue spruce tree SVG icon renders correctly (200x200px)
   - Validate "About Us" and "Our Mission" sections are readable
   - Ensure footer shows "© 2025 Blue Spruce High School. All rights reserved."

2. **Responsive Design Testing**:
   - Test on mobile viewport (320px width)
   - Test on tablet viewport (768px width) 
   - Test on desktop viewport (1024px+ width)
   - Verify text remains readable at all sizes (minimum 24px font-size)

3. **Accessibility Testing**:
   - Confirm SVG has proper `aria-label="Blue Spruce Tree"`
   - Verify heading hierarchy (h1 -> h2 structure)
   - Check color contrast (dark text on light background)

### HTML Validation
Run basic HTML syntax validation:
```bash
python3 -c "import html.parser; p = html.parser.HTMLParser(); p.feed(open('index.html').read()); print('HTML syntax is valid')"
```
- **Expected result**: "HTML syntax is valid" 
- **If validation fails**: Fix HTML syntax errors before proceeding

### Content Validation
Verify these elements are present in index.html:
- DOCTYPE html declaration
- UTF-8 charset meta tag
- Responsive viewport meta tag
- Title: "Blue Spruce High School"
- All inline CSS styles intact
- SVG icon with proper path definition
- All text content matches expected school information

## Common Tasks

### Making Content Changes
**Do NOT modify**:
- DOCTYPE declaration
- Meta tags (charset, viewport)
- CSS structure and styling
- SVG path definition

**Safe to modify**:
- Text content within HTML elements
- Color values in CSS (while maintaining readability)
- Padding/margin values for layout adjustments

### Testing Content Changes
After any content modification:
1. Run HTML validation (see above)
2. Start local server: `python3 -m http.server 8000`
3. Visually verify changes at `http://localhost:8000`
4. Test responsive behavior
5. Stop server with Ctrl+C

### Repository Information Reference

**Repository root contents:**
```
.
├── .git/           # Git repository data
├── .gitignore      # Git ignore rules
├── .github/        # GitHub configuration (includes this file)
├── LICENSE         # Mozilla Public License 2.0
├── README.md       # Project description
└── index.html      # Main website file
```

**File sizes (approximate):**
- index.html: ~2.5KB
- README.md: ~24 bytes
- LICENSE: ~16.7KB

## Deployment and Hosting

### Static Hosting Options
This website is ready for deployment to any static hosting service:
- GitHub Pages
- Netlify  
- Vercel
- AWS S3 + CloudFront
- Any web server with static file serving

### GitHub Pages Setup (if needed)
1. Navigate to repository settings
2. Enable GitHub Pages from main branch
3. Website will be available at: `https://getsetbro.github.io/blue-spruce-edu/`

## Important Notes

### What NOT to Do
- **Do NOT** add package.json, node_modules, or any build tools
- **Do NOT** separate CSS into external files (keep inline for simplicity)
- **Do NOT** add JavaScript unless absolutely necessary
- **Do NOT** modify the SVG path without visual verification

### What to ALWAYS Do
- **ALWAYS** test locally before committing changes
- **ALWAYS** validate HTML syntax after modifications
- **ALWAYS** verify responsive design works
- **ALWAYS** maintain the school's brand colors (#2a5d67, #2a4967, #f4f4f9)

### Color Scheme Reference
- Primary blue: `#2a5d67` (header background, h2 text)
- Dark blue: `#2a4967` (SVG fill)
- Light background: `#f4f4f9` (body background)
- Text: `#333` (main text color)
- White: `white` (header text, footer background)

This website requires no build process, no dependencies, and no compilation. It is designed to be simple, fast-loading, and easy to maintain.