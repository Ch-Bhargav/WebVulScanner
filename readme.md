### README.md Template

#### Project Title

Web Vulnerability Scanner

#### Description

This Python script scans web pages for potential Cross-Site Scripting (XSS) vulnerabilities by analyzing HTML forms and injecting test payloads.

#### Features

- Parses HTML forms from a given URL.
- Checks each form for XSS vulnerabilities using test payloads.
- Detects vulnerable forms and outputs results to the console.

#### Prerequisites

- Python 3.x
- `requests` library (`pip install requests`)
- `beautifulsoup4` library (`pip install beautifulsoup4`)

#### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/web-vulnerability-scanner.git
   ```

2. Navigate to the project directory:

   ```bash
   cd web-vulnerability-scanner
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

#### Usage

1. Modify `url` in `web_vulnerability_scanner.py` to specify the target URL you want to scan:

   ```python
   url = 'http://testphp.vulnweb.com'
   ```

2. Run the scanner script:

   ```bash
   python web_vulnerability_scanner.py
   ```

3. The script will:

   - Fetch the HTML content of the specified URL.
   - Parse the HTML using BeautifulSoup to find all `<form>` elements.
   - Check each form for XSS vulnerabilities by injecting a test payload (`<script>alert(1)</script>`).
   - Output a message if a vulnerability is detected.

#### Example Output

```
Form at http://testphp.vulnweb.com/vulnerabilities/sqli/ is vulnerable to XSS.
```

#### Notes

- Ensure you have permission to scan and test websites for vulnerabilities.
- Customize the XSS payload (`'<script>alert(1)</script>'`) in `check_vulnerabilities()` for more sophisticated tests.

#### License

This project is licensed under the MIT License - see the LICENSE file for details.

#### Acknowledgments

- Inspired by ethical hacking and web security practices.

