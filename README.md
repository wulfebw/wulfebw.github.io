# Personal Blog

## Running Locally

```bash
hugo server
```

Visit `http://localhost:1313` to preview your site.

## Configuration

Edit `config.yml` to customize:
- Site title and description
- Social media links (LinkedIn, GitHub, Twitter, Google Scholar)
- Navigation menu items
- Other PaperMod theme settings

Edit `content/_index.md` for your homepage/about page content.

## Adding Blog Posts

Create a new post:
```bash
hugo new posts/your-post-name.md
```

Edit the post in `content/posts/your-post-name.md`

## Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions when you push to the `main` branch.

The workflow (`.github/workflows/hugo.yml`) builds the Hugo site and deploys to GitHub Pages.
