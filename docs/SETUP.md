# Setup and reproducibility

## Review without running code

Open the original report, presentation, and dataset description from the README. The repository has no deployed application.

## Suggested environment

Python 3.11 is a proposed modernization baseline, not the original environment and not a verified compatibility claim for the legacy notebooks. The notebook metadata records older Python environments. requirements.txt is an unpinned starting manifest, not an exact historical lockfile.

```bash
git clone https://github.com/enzosafadi/Coursera-Capstone.git
cd Coursera-Capstone
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

macOS / Linux:

```bash
source .venv/bin/activate
```

Then:

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

## Before executing historical cells

1. Recover and attribute the coordinate input; replace absolute paths with project-relative paths.
2. Move Excel exports into a local outputs directory and remove obsolete encoding arguments.
3. Replace the legacy pandas import with the supported pandas.json_normalize interface where needed.
4. Add the missing GeoPy Nominatim import and handle failed lookups.
5. Remove inline pip/conda installation cells after preparing the environment.
6. Verify a supported venue-provider integration. The old v2 request function cannot be assumed compatible with a current account.
7. Load any credentials from local environment configuration, add request timeouts and error handling, and clear sensitive outputs before committing.
8. Recover the missing cross-city feature construction and model stages.

Installing packages alone will not make the complete study reproducible. Network data collection and notebook execution have not been validated by this update.

## Dependency policy

After the modernized workflow executes successfully, record exact versions in a lockfile and rerun in a clean environment. No provider SDK is required merely to review the archived material; requests appears in the historical venue function.

## Local files

Use data/raw, data/processed, and outputs for regenerated local material. These locations and .env files are ignored by Git. Publish a small permitted fixture separately if a future automated test needs one.
