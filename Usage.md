# 🛠️ Usage Guide - StealthJS

**StealthJS** is a bash-based script that extracts JavaScript links, paths, and URLs from websites and subdomains for recon and bug bounty hunting.

---

## Usage with Target Domain

```bash
# Extract JS links and save
./StealthJS.sh -t <domain.com> -j

# Extract URLs from JS (no filter)
./StealthJS.sh -t <domain.com> -f

# Extract URLs from JS (optimized)
./StealthJS.sh -t <domain.com> -f -o

# Extract Paths from JS (no filter)
./StealthJS.sh -t <domain.com> -p

# Extract Paths from JS (optimized)
./StealthJS.sh -t <domain.com> -p -o

# Use Proxy
-x http://127.0.0.1:8080

# Use Chromium Headless Browser
-c chromium_headless_browser
```

---

## Usage with Subdomain List

```bash
# Extract JS links and save
./StealthJS.sh -s subdomains.txt -j

# Extract URLs from JS (no filter)
./StealthJS.sh -s subdomains.txt -f

# Extract URLs from JS (optimized)
./StealthJS.sh -s subdomains.txt -f -o

# Extract Paths from JS (no filter)
./StealthJS.sh -s subdomains.txt -p

# Extract Paths from JS (optimized)
./StealthJS.sh -s subdomains.txt -p -o
```

---

## Usage with JS Links List

```bash
# Extract URLs from JS (no filter)
./StealthJS.sh -l js_links.txt -f

# Extract URLs from JS (optimized)
./StealthJS.sh -l js_links.txt -f -o

# Extract Paths from JS (no filter)
./StealthJS.sh -l js_links.txt -p

# Extract Paths from JS (optimized)
./StealthJS.sh -l js_links.txt -p -o
```

---

## Install Required Packages

```bash
sudo ./StealthJS.sh -z
```

---

## Flags Summary

```text
-t, --target                 Target domain
-s, --subdomain_list, --subs    Subdomain list file
-l, --jslist, --jl          JavaScript file list
-j, --javascript            Extract JS links
-f, --fullurls, --url       Extract full URLs
-p, --url_paths, --paths    Extract only path segments
-o, --optimize, --opt       Optimize output
-x                          Use proxy (http/s)
-c                          Use Chromium headless browser
-z                          Install dependencies
-i, --secrets, --secret     Scan JS for secrets
-r, --raw                   Output raw results
-h, --help                  Show help message
```

---


