# api-specs

Collection of OpenAPI specifications, browsable via Swagger UI on GitHub Pages.

## Viewing the docs

The site is served by GitHub Pages from the `main` branch. Open the Pages URL
(see the repo's **About** section or `gh repo view --json url`), pick a spec
from the dropdown in the top bar, and it renders in Swagger UI.

You can deep-link to a spec with `?spec=specs/<file>.yaml`.

## Adding a new spec

1. Drop the OpenAPI file (`.yaml` or `.json`) into `specs/`.
2. Register it in `specs/specs.json`:

   ```json
   {
     "name": "My API",
     "url": "specs/my-api.yaml"
   }
   ```

3. Commit and push — Pages redeploys automatically.

## Current specs

| Spec | File |
| --- | --- |
| Deployment API | [specs/deployment-api.yaml](specs/deployment-api.yaml) |

## Validating a spec locally

```sh
npx @redocly/cli lint specs/deployment-api.yaml
```
