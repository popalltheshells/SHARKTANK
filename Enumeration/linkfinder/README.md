# LinkFinder
is used to identify hardcoded endpoints of your target application, sometimes these yield things such as

- S3 bucket endpoint
- API endpoints (unauth)
- Private pages, etc.

### To build
``` docker build -t linkfinder . ```

### To execute
``` docker run -it linkfinder https://target.com/example.js -o cli ```
