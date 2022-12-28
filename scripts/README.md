- python3 scripts/fetch.py
    - Downloads my mod readme files (at `/docs/mods`) and parts of the WrapperLib wiki (at `/docs/wrapperlib`). 
        - These are not committed in this repo so the script must be run once before the Docusaurus build.
    - Some third party gists are downloaded as well (at `/docs/mirror`). 
        - These only download when run locally on my computer (not in cloudflare).
        - They are committed to the repo so I can review changes before publishing them.
- python3 scripts/redirects.py
    - Generates additions to the `/static/_redirects` file (used by cloudflare)
        - Converts from old site paths, so external links from before Docusaurus migration still work. 
- npm run build
    - Builds the Docusaurus site (at `/build`).
    - sidebar.js
        - Defines the different navigation lists shown on the sides of Docusaurus pages.