# hematitegg/.github

The public profile of the hematitegg organisation on GitHub.

- `profile/README.md` is shown on https://github.com/hematitegg.
- `profile/assets/` holds the header in GitHub's dark and light themes. They come from the brand repo (`github/`, made by `process/generator/github.py`); update them there and copy them across.

## Why the images use absolute URLs

`profile/README.md` links its header by absolute `raw.githubusercontent.com` URL, not by relative path. github.com rewrites relative paths when it renders the page, but the GitHub mobile apps render the README from the REST API (`/repos/hematitegg/.github/readme/profile`), which leaves relative paths as they are, so the banner showed blank in the apps. Keep the URLs absolute. The `<img>` fallback is the dark header: renderers that ignore `<picture>` then show a dark banner, which still looks fine on a light screen.
