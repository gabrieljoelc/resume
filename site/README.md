# site

Renders `profile.yaml` to a one-page HTML resume and a PDF, deployed to Vercel at gabrielchaney.com.

Stub: roadmap step 4 picks the stack and adds the build, CI, and deploy.

Constraints for that step:

- The only input is `profile.yaml`. The build never reads `data/`.
- Deterministic: the same `profile.yaml` always produces the same output. No AI calls in the build.
- The PDF comes from the same source as the HTML. Don't use wkhtmltopdf; the project is archived.
