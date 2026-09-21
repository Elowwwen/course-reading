# Extraction and assembly for difficult readings

## Long readings

For readings too long for one pass (often 30+ pages), split at section boundaries and keep an explicit shared format specification: section headings, native table rows, module-level PDF links, figure/table ownership, and fragment paths. Process sequentially by default; parallel subagents are optional only when available and authorized by the user's environment/instructions. Do not require delegation to complete a reading.

Use cached extracted text with `===== PAGE N =====` markers and correct tricky reading order, including multi-column dialogues, before translating. Fragments may use `%%FIG:figure-id%%` placeholders. Assign captions once; assemble fragments with code, replace placeholders with full vault-relative figure embeds and captions, restore genuine source tables, and add titles/frontmatter. Verify no placeholders remain and all planned sections, figures, tables, and five recall callouts are present. Follow the selected language mode throughout.

## Local extraction and figures

Discover a working Python/PDF runtime rather than assuming a machine-specific executable. When PyMuPDF is available, probe each page's size and counts of text, raster images, and vector drawings to identify scanned pages and figure-heavy layouts. Scans with no text require available OCR rather than fabricated extraction.

Extract text once with page boundaries. For figures, locate caption text with `page.search_for()` or text blocks; inspect adjacent raster rectangles from `page.get_image_info()` and vector bounds from `page.get_drawings()`. Exclude background scans and tiny decorative shapes; combine nearby candidates based on page geometry, not a universal size threshold. Captions can be above or below the image. Use `page.get_pixmap(dpi=220, clip=rect)` or a suitable higher scale for vector clips; extract raster images at native resolution with a pixmap/xref when appropriate. Avoid baking the caption into a crop if it is also rendered as Markdown. Visually inspect representative crops for clipping, unrelated content, resolution, and caption duplication.

## Final placement and embed verification

Re-list the destination at the end: the user or another session may have moved a reading into a shared week folder during processing. Resolve the current canonical location before finalizing full vault-relative links. Verify every embed path exists and every PDF jump refers to the correct document. Do not create a duplicate folder merely because Unicode normalization differs: compare NFC-normalized sibling names and investigate ambiguity without silently merging unrelated folders.
