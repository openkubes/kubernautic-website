# Kubernautic website localization

English remains the default language at `/`. German pages use `/de/` and the same slugs:

| English | German |
| --- | --- |
| / | /de/ |
| /platform/ | /de/platform/ |
| /agentic-ai/ | /de/agentic-ai/ |
| /architecture/ | /de/architecture/ |
| /open-source/ | /de/open-source/ |
| /enterprise/ | /de/enterprise/ |
| /console/ | /de/console/ |
| /contact/ | /de/contact/ |

The shared `src/layouts/Base.astro` detects language from the route. It renders locale-aware navigation/footer, a language-switch link preserving the current page, `html lang`, per-locale canonical URLs and reciprocal `hreflang` links. Astro's sitemap integration discovers both sets of static routes automatically.

`CTA.astro` and `Network.astro` display language-dependent labels. German versions of the interactive `ArchitectureExplorer` and `IncidentExplorer` are under `src/components/de/`; examples remain synthetic and read-only. English components remain unchanged.

## Validation before merge

1. `npm ci && npm run build`
2. Verify `dist/de/index.html` and all seven `dist/de/*/index.html` exist.
3. Review header/footer language switch on desktop and mobile, particularly long German strings.
4. Run the architecture and incident demos in each language and confirm all labels and controls.
5. Inspect `hreflang`, canonical and sitemap output. English URLs must remain stable.
6. Check security-related text and claims before publishing.

No automatic geo/IP language redirect is used; visitors switch languages explicitly.
