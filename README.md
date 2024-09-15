# kmxtaylor.github.io

This is my personal website made with Hugo, based on the theme `terminal`.

After installing the [Hugo prerequisites](https://gohugo.io/getting-started/quick-start/#prerequisites), you can build and run the site on a hot-reloading dev server via `hugo server`.

The project structure is as follows:

- `config.toml` contains site configurations (including configs for nav bar and multilingual page support).
- `archetypes/` contains markdown templates that act like schema for new content.
- `content/` contains [page bundles](https://gohugo.io/content-management/page-bundles/) of markup files and other page resources that populate the site.
  - Index files in each directory determine the page content served at the URL corresponding to said directory path.
- `layouts/` contains HTML [templates](https://gohugo.io/templates/) to organize content, data and resources into an actual website. Most of these are sourced from the theme. I've defined a few directly in the project.
- `public/` contains the published website.
  - It gets regenerated when you build the site with `hugo`, `hugo server` or `hugo --minify`.
  - It doesn't need to be pushed, since GitHub Actions builds the site (thus generating this directory) upon deployment with `hugo --minify`.
- `resources/` contains cached output from Hugo's asset pipelines.
  - It gets regenerated when you build the site with `hugo` or `hugo server` (NOT included with `hugo --minify` but also not required in order to host site)
- `static/` contains files that will be copied to `public/` when you build the site.
  - (Currently contains the site's images, but I may decide to move them to their corresponding page bundles in the future, entailing changes to the image file paths based on the structure of the `public/` generated files.)
- `themes/` contains the site's theme(s), which are managed as their own separate git repo(s).
  - For my site, assets and most of the layouts are sourced from the theme directory (which is also an npm package), and I've been committing changes to them in my fork of the theme repo.

I've chosen to [handle translation by filename](https://gohugo.io/content-management/multilingual/#translation-by-file-name).

I've set-up a [GitHub Actions workflow](/.github/workflows/gh-pages.yml) to automate the deployment pipeline so that every push to the main branch (after development in dev) attempts a build and a deployment to the live site.
