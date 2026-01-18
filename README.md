# TechSlayers Docs (Mintlify)

This folder contains the Mintlify-powered documentation site for TechSlayers.

## Local preview

```bash
cd techslayers-docs

# Ensure you're on Node >= 20.17
nvm install 20.17.0
nvm use

# Start Mintlify locally (prints the local URL)
npx -y mintlify@latest dev --no-open
```

If you already have the correct Node version, `nvm use` will automatically pick it up from `.nvmrc`.

## Useful checks

```bash
# Check internal links
npx -y mintlify@latest broken-links

# Accessibility scan (colors + MDX checks)
npx -y mintlify@latest a11y
```

## Hosting (Mintlify)

Mintlify deployments are typically hosted directly by Mintlify from your GitHub repo.

1. Create / open your project in the Mintlify dashboard.
2. Connect this GitHub repo and select the `main` branch.
3. Set the custom domain (e.g. `docs.yourdomain.com`) in the project settings.
4. Add the DNS record Mintlify provides (usually a CNAME for `docs`), then wait for verification/SSL.

After this, pushes to `main` will trigger a redeploy automatically.

## Pushing changes

Repo: `https://github.com/00-Aakash-00/techslayers-docs`

```bash
cd techslayers-docs

git status
git add -A
git commit -m "Update docs"
git push
```

## Source references

- OpenAPI specs are stored in `techslayers-docs/openapi/` and were pulled from the existing product Swagger/OpenAPI endpoints.
- Legba source pages are stored in `techslayers-docs/legba-source/` as reference material.
# techslayers-docs

