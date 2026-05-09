# PowerPoint Finder

Locates and secures publicly indexed PowerPoint files, verifies valid `.ppt` and `.pptx` downloads and records detailed manifests and logs for auditing and organization.

## Overview

Uses a Google Custom Search Engine to find publicly indexed PowerPoint files matching one or more keywords, then downloads and verifies valid `.ppt` and `.pptx` files. This application supports configuration through command-line arguments or environment variables, including search queries, result pages, request delays, output folders, dry-run mode and more. Search results are deduplicated by URL, logged and assigned metadata such as title, snippet, rank, HTTP status and download status.

Downloaded files are validated before being saved; legacy `.ppt` files are checked by their binary signature, and `.pptx` files are inspected as ZIP archives. The script writes JSON and CSV manifests summarizing all results, downloads and errors. It also creates a structured log file, making the tool useful for collecting, auditing and organizing PowerPoint files from search results.
