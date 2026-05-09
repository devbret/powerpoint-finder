# PowerPoint Finder

Locates and secures publicly indexed PowerPoint files, verifies valid `.ppt` and `.pptx` downloads and records detailed manifests and logs for auditing and organization.

## Overview

Uses a Google Custom Search Engine to find publicly indexed PowerPoint files matching one or more keywords, then downloads and verifies valid `.ppt` and `.pptx` files. This application supports configuration through command-line arguments or environment variables, including search queries, result pages, request delays, output folders, dry-run mode and more. Search results are deduplicated by URL, logged and assigned metadata such as title, snippet, rank, HTTP status and download status.

Downloaded files are validated before being saved; legacy `.ppt` files are checked by their binary signature, and `.pptx` files are inspected as ZIP archives. The script writes JSON and CSV manifests summarizing all results, downloads and errors. It also creates a structured log file, making the tool useful for collecting, auditing and organizing PowerPoint files from search results.

## Set Up Instructions

Below are the required software programs and initial steps for running this application on a Linux machine.

### Programs Needed

1. [Git](https://git-scm.com/downloads)

2. [Python](https://www.python.org/downloads/)

### Steps

1. Install the above programs

2. Open a terminal

3. Clone this repository: `git clone git@github.com:devbret/powerpoint-finder.git`

4. Navigate to the repo's directory: `cd powerpoint-finder`

5. Create a virtual environment: `python3 -m venv venv`

6. Activate the virtual environment: `source venv/bin/activate`

7. Install the needed dependencies for running the script: `pip install -r requirements.txt`

8. Convert the `.env.template` file into a `.env` file

9. Add values for environmental variables in the `.env` file

10. Run the Python script: `python3 app.py`

11. Downloaded `.ppt` and `.pptx` files will be saved to the `powerpoint_downloads` directory

12. Generated log files will be saved to the `manifests` directory

13. Exit the virtual environment: `deactivate`

## Other Considerations

This project repo is intended to demonstrate an ability to do the following:

- Search using a Google Custom Search Engine for `.ppt` and `.pptx` files based on one or more queries

- Download PowerPoint files, validate they are real PowerPoint presentations and save files locally

- Deduplicate search results, skip blocked or invalid downloads and record metadata for each result

- Generate `.json` and `.csv` manifest files so each run can be reviewed and audited later

If you have any questions or would like to collaborate, please reach out either on GitHub or via [my website](https://bretbernhoft.com/).
