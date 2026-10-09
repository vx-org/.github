# VX additive resource variants

These files are an additive review set around the approved VX v2 identity. The existing production files one directory above remain unchanged.

- `svg/`: actual native Plain SVG exports, including matching light/dark lockups, symbols, literal currentColor variants and symbol-only 16/24 px candidates.
- `png/light/` and `png/dark/`: nine actual native transparent PNG sizes, 1024/512/256/128/64/48/32/24/16.
- `icons/`: real light/dark ICO and ICNS containers assembled from the native PNG bytes; ICO has seven entries, ICNS eleven standard/retina PNG chunks. Header, payload and decoded pixel read-back passed. Native Windows Shell and macOS icon-opening acceptance is not claimed.
- `favicon.svg`: an actual native export with literal `currentColor` fills. An external favicon resource uses its own color context; it should not be assumed to inherit the host page's CSS color. External favicon appearance on light/dark browser chrome has not been verified by the inline currentColor test.
- `review/vx-avatar-candidate.png`: an actual native 512 px candidate. It is not an organization-account setting change or a replacement for the current approved avatar.

Palette: Graphite `#101713`, Chartreuse `#D7FF3F`, Soft White `#F4F6F2`. Use light artwork on light backgrounds and dark artwork on Graphite; preserve proportions and spacing. The approved guidance retains a 16 px symbol minimum and a 160 px lockup minimum.

Inline currentColor SVGs inherit a visible CSS `color` from their context. A standalone PNG resolves a fixed color and cannot retain currentColor. Actual inline theme computation passed in Chromium 151.0.7922.34. The relevant QA report and screenshot are in `../native/qa/`.

The approved larger geometry is preserved at 16/24 px; separate small-source canvases make the symbol-only intent explicit. Actual 1x and nearest-neighbor display observations found no shape-breaking defect requiring a geometry change. The native GUI review remains blocked by the official UI metadata `protocol_mismatch`. User acceptance, account-avatar adoption and production replacement remain separate decisions.

See [manifest](../manifest.json), [native source](../native/README.md) and [brand rights](../BRAND-RIGHTS.md).
