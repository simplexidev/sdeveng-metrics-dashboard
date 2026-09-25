# SimplexiDev Engineering Toolkit Metrics Dashboard

This directory contains a dependency-free static dashboard. The publication command copies
only manifest-approved aggregates into the generated site's `data/` directory. Serve the
generated `_site/` directory locally to preview it; opening the HTML file directly may
prevent JSON loading because of browser origin rules.

The publisher takes explicit dashboard and data directories; it does not depend on a
sibling checkout or the former metrics monorepo:

```console
dotnet run --project ../sdeveng-metrics-tooling/src/SdevEng.Metrics -- \
  publish-pages . <data-directory>/public _site
```

The dashboard consumes the versioned `publication-manifest.json` schema `1.0` copied by
the publisher. Browser paths are project-relative for the Pages target at
<https://simplexidev.github.io/sdeveng-metrics-dashboard/>. Evaluator and publisher code
remain in `sdeveng-metrics-tooling`; approved aggregates remain in
`sdeveng-metrics-data`.

## License

MIT. See [LICENSE](LICENSE).
