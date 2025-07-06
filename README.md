# Liu Peng Personal Website

This is the source code for Liu Peng's personal website, built with Jekyll and GitHub Pages.

## ✨ Features
- Modern, responsive design
- About Me, Projects, and Home pages
- Card-based layout for experience, skills, awards, projects, and interests
- Data-driven content using YAML files for easy updates
- Reusable Jekyll includes for maintainability
- Clean, readable markdown for main content
- Compact About Me page with expandable experience section
- Two-column layout for education and awards sections
- Interests & Activities section with cards (icons/short descriptions coming soon)
- Automatic deployment via GitHub Pages

## 🗂️ Project Structure

- `_data/` — All experience, skills, awards, and projects are stored as YAML files for easy editing
- `_includes/` — Reusable HTML components for experience, skills, awards, project cards, and (soon) interest cards
- `pages/aboutme.md` — About Me page (uses data and includes, pretty URL: `/aboutme/`)
- `pages/projects.md` — Projects page (uses data and includes, pretty URL: `/projects/`)
- `index.html` — Homepage
- `assets/css/style.css` — Main stylesheet

## 🛠️ How to Edit Content
- **Experience:** Edit `_data/experience.yml`
- **Skills:** Edit `_data/skills.yml`
- **Awards:** Edit `_data/awards.yml`
- **Projects:** Edit `_data/projects.yml`

## 🧑‍💻 Local Development
1. Install Ruby and Bundler
2. Run `bundle install`
3. Start the server: `bundle exec jekyll serve --livereload`
4. Visit [http://localhost:4000](http://localhost:4000)

## 🚀 Deployment
Pushing to the `master` branch automatically deploys the site via GitHub Pages.

## 📝 License
MIT License

