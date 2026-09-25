# Metrics dashboard development

This repository owns the dependency-free static dashboard and GitHub Pages workflow for
SimplexiDev Engineering Toolkit metrics. Keep browser assets project-relative and do not
copy evaluator implementation or committed metrics data into this repository.

Pages must assemble the site from this repository, reviewed aggregates in
`simplexidev/sdeveng-metrics-data`, and the validated publisher in
`simplexidev/sdeveng-metrics-tooling`. Never publish raw runs, prompts, responses,
transcripts, private source, logs, secrets, or unapproved JSON.

Before merging, run `dashboard-check` and `publish-pages` with the sibling repositories,
then inspect the generated site artifact.
