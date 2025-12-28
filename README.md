# Personal Blog

## Setup

### Prerequisites

- Hugo installed
  - Install via snap: `sudo snap install hugo --channel=extended` (this should get a newer version)

### Initial Setup

1. Initialize Hugo site (if not already done):
   ```bash
   hugo new site .
   ```

2. Add PaperMod theme as a submodule:
   ```bash
   git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
   ```

3. Test locally:
   ```bash
   hugo server
   ```
   Visit `http://localhost:1313` to preview your site.

## Configuration

- Edit `config.yml` to customize:
  - Site title and description
  - Social media links (LinkedIn, GitHub, Twitter, Google Scholar)
  - Navigation menu items
  - Other PaperMod theme settings

- Edit `content/_index.md` for your homepage/about page content

- Add your resume PDF to `static/resume.pdf` (or update the link in `_index.md`)

## Adding Blog Posts

Create a new post:
```bash
hugo new posts/your-post-name.md
```

Edit the post in `content/posts/your-post-name.md`

## Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions when you push to the `main` branch.

The workflow (`.github/workflows/hugo.yml`) will:
1. Build the Hugo site
2. Deploy to GitHub Pages

## Migration to wulfebw.github.io

When ready to go live:

1. Rename your old `wulfebw.github.io` repo to `old-blog` (this stops GitHub Pages from serving it)
2. Rename this repo to `wulfebw.github.io`
3. Update `baseURL` in `config.yml` to `https://wulfebw.github.io/`
4. Push the changes - GitHub Pages will automatically serve from the new repo

## Local Development

- Run `hugo server` to start the development server
- Run `hugo` to build the site (outputs to `public/` directory)
- The `public/` directory is gitignored and should not be committed
