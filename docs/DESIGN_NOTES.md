# Design notes

This profile uses one local SVG asset for Apple-like rounded cards, soft shadows, gradients, and glass-style surfaces. GitHub README markdown does not allow arbitrary CSS to reliably style native blocks, so the static visual treatment is embedded in `assets/readme-overview.svg`.

Avoid native Markdown headings, horizontal rules, and tables in `README.md` for static visual sections; GitHub injects default margins, borders, and line-height that break the continuous background. Keep those sections inside `assets/readme-overview.svg`.

Keep the dynamic stats workflow under `.github/workflows/update-stats.yml`. The README still references `profile/*.svg`, so the GitHub Action can update stats without turning the entire profile into one static long image.

Before publishing, replace `outloo0ok@outlook.com` in `README.md` and `assets/readme-overview.svg`.
