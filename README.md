# Liu Peng Personal Website

This is the source code for Liu Peng's personal website, built with Jekyll and GitHub Pages.

## ✨ Features
- Modern, responsive design with dark mode (follows OS preference)
- Mobile-friendly hamburger navigation menu
- About Me, Projects, and Home pages
- Card-based layout for experience, skills, awards, projects, and interests
- Data-driven content using YAML files for easy updates
- Reusable Jekyll includes for maintainability
- Clean, readable markdown for main content
- Compact About Me page with expandable experience section
- Two-column layout for education and awards sections
- Interests & Activities section with cards and Font Awesome icons
- Active navigation highlighting based on current page
- Accessible: ARIA labels on interactive elements
- Automatic deployment via GitHub Pages

## 🗂️ Project Structure

- `_data/` — All experience, skills, awards, projects, and interests stored as YAML files
- `_includes/` — Reusable HTML components for experience, skills, awards, project cards, and interest cards
- `pages/aboutme.md` — About Me page (uses data and includes, pretty URL: `/aboutme/`)
- `pages/projects.md` — Projects page (uses data and includes, pretty URL: `/projects/`)
- `index.html` — Homepage
- `assets/css/style.css` — Main stylesheet (CSS custom properties, dark mode, responsive)
- `_layouts/default.html` — Main layout (navigation, header, footer, hamburger JS)

## 🛠️ How to Edit Content
- **Experience:** Edit `_data/experience.yml`
- **Skills:** Edit `_data/skills.yml`
- **Awards:** Edit `_data/awards.yml`
- **Projects:** Edit `_data/projects.yml`
- **Interests:** Edit `_data/interests.yml` (uses Font Awesome icon classes, e.g. `fas fa-camera-retro`)

## 🎨 Theming & Design
The stylesheet uses CSS custom properties defined in `:root` for all colours, shadows, and radii. Dark mode is applied automatically via `@media (prefers-color-scheme: dark)` — no JavaScript required. To customise the colour scheme, edit the variables at the top of `assets/css/style.css`.

## 🧑‍💻 Local Development
1. Install Ruby and Bundler
2. Run `bundle install`
3. Start the server: `bundle exec jekyll serve --livereload`
4. Visit [http://localhost:4000](http://localhost:4000)

## 🚀 Deployment
The site is hosted on **GitHub Pages** at [www.liupeng.eu](https://www.liupeng.eu) (custom domain configured via `CNAME`). Pushing to the `master` branch triggers an automatic Jekyll build and deploy — no CI/CD configuration required.

## 📝 License
MIT License

