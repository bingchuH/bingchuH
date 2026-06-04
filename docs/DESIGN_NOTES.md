# Design notes

This profile uses local SVG assets for Apple-like rounded cards, soft shadows, gradients, and glass-style surfaces. GitHub README markdown does not allow arbitrary CSS to reliably style native blocks, so the premium visual treatment is embedded inside SVG files under `assets/`.

Avoid native Markdown headings, horizontal rules, and tables in `README.md` for visual sections; GitHub injects default margins, borders, and line-height that break the continuous background. Use section-level SVG panels such as `assets/product-focus.svg` and `assets/github-signal.svg` instead.

Keep the dynamic stats workflow under `.github/workflows/update-stats.yml`. The README still references `profile/*.svg`, so the GitHub Action can update stats without turning the entire profile into one static long image.

Before publishing, replace `your-email@example.com` in `README.md` and `assets/contact.svg`.
