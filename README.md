PoseDatasetHarvester2

A tiny in-browser prototype that normalizes pose/time-series files (CSV, JSON, MATLAB .mat via ArrayBuffer heuristic) into a single CSV with columns: time, module_id, position_x, position_y, position_z, orientation_w, orientation_x, orientation_y, orientation_z. Upload files or paste raw file content (or enter direct file URLs and fetch them manually in another tab then paste). Produces a provenance log and short report.

Usage:
- Open index.html in a modern browser.
- Drag files or click to upload, or paste file contents into the big text area.
- Click "Process". Download will be offered for normalized CSV and provenance log.

Limitations:
- No automatic crawling of web pages or repositories; only processes content you provide.
- .mat parsing is heuristic: recognizes simple binary MAT v5 with variable name and raw numeric data arrays only (many .mat variants won't parse). This is an exploratory prototype.

This tool is an interpretive prototype, not a validated extractor for every dataset. Extend with server-side downloads and robust MAT file parsing when needed.