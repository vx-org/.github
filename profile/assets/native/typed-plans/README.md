# Reusable VX typed MCP inputs

Each JSON file is the complete `document_build` input: `output_file` plus `plan` with `canvas` and bounded typed nodes. No absolute machine path, executable script or raw SVG/XML payload is included. Output filenames are workspace-relative and must be fresh.

The native plan keeps approved path `d`, paint and fill rules, adding named layer/group parents. CurrentColor inputs deliberately replace fills with the literal `currentColor` token. The 16/24 px inputs use the approved four-path symbol and retain its 512-unit viewBox. Native creation/export is owned by the actual Inkscape MCP operator, not by a standalone XML writer.

Discover the current tool instance before calling the inputs. See the parent native README and sanitized evidence for the actual verified production chain, export arguments and incomplete GUI acceptance.
