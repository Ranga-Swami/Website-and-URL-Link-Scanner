# Website-and-URL-Link-Scanner
## 🔍 Overview

**Website-and-URL-Link-Scanner** is a Python-based tool that scans websites and individual URLs for:

* Malicious or suspicious links
* Broken links (404 errors)
* Redirect chains
* External/internal links
* Basic security headers

This tool is useful for SEO professionals, developers, security analysts, and anyone looking to audit a website for link integrity or safety.

---

## 🚀 Features

* ✅ Extract all links from a web page
* ⚠️ Detect broken or redirected URLs
* 🛡️ Check for basic security headers
* 🌐 Distinguish between internal and external links
* 📄 Generate summary reports

---

## 📦 Requirements

* Python 3.7+
* `requests`
* `beautifulsoup4`
* `tldextract`
* `urllib3`
* `colorama` (for colored CLI output, optional)

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🛠️ Usage

### Basic URL Scan

```bash
python scanner.py --url https://example.com
```

### Scan with Report Output

```bash
python scanner.py --url https://example.com --output report.json
```

### Options

| Argument    | Description                             |
| ----------- | --------------------------------------- |
| `--url`     | The URL of the website to scan          |
| `--depth`   | Depth of crawl (default is 1)           |
| `--output`  | File to save results (JSON or CSV)      |
| `--timeout` | Request timeout in seconds (default 10) |

---

## 📁 Example Output

```json
{
  "url": "https://example.com",
  "total_links": 56,
  "broken_links": 3,
  "redirects": 2,
  "external_links": 19,
  "security_headers": {
    "Content-Security-Policy": "missing",
    "X-Frame-Options": "DENY"
  }
}
```

---

## 🧪 Sample Command-Line Output

```
[+] Scanning https://example.com ...
[!] Broken Link: https://example.com/missing-page (404)
[→] Redirect: http://example.com → https://example.com
[✓] Valid Link: https://example.com/about
```

---

## 🔐 Security Headers Checked

* `Content-Security-Policy`
* `X-Frame-Options`
* `Strict-Transport-Security`
* `X-Content-Type-Options`
* `Referrer-Policy`

---

## 📜 License

MIT License. See [LICENSE](LICENSE) for details.

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are welcome! Please fork the repo and submit a pull request.

---

## 👨‍💻 Author

Developed by \[Your Name or GitHub Handle]
GitHub: [github.com/yourhandle](https://github.com/yourhandle)
