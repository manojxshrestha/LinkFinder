# 🔗 LinkFinder

**LinkFinder** is a powerful tool for discovering endpoints and hidden URLs within JavaScript files — a critical step in reconnaissance and web application security testing.

## 🚀 Installation

If not already installed:
```bash
git clone https://github.com/GerbenJavado/LinkFinder.git
cd LinkFinder
pip install -r requirements.txt
```

---

## 📘 Basic Command Structure

```bash
linkfinder -i <input> -o <output_format>
```

- `<input>`: Target JavaScript file, directory, or URL.
- `<output_format>`: `cli` for terminal output or `html` for file output.

---

## 🔍 Usage Examples

### 1. Analyze a Single JavaScript File
```bash
linkfinder -i /path/to/your/file.js -o cli
```

### 2. Save Results to an HTML File
```bash
linkfinder -i /path/to/your/file.js -o html -o output.html
```

### 3. Scan a Directory of JavaScript Files
```bash
linkfinder -i /path/to/your/directory -o cli -d
```

- `-d`: Recursively scan all `.js` files in the directory.

### 4. Use Regular Expressions to Refine Search
```bash
linkfinder -i /path/to/file.js -r "regex_pattern" -o cli
```

### 5. Scan a Website Directly
```bash
linkfinder -i https://example.com -o cli
```

### 6. Save Website Scan Results to HTML
```bash
linkfinder -i https://example.com -o html -o results.html
```

### 7. Scan a Specific Web Page
```bash
linkfinder -i https://example.com/page.html -o cli
```

### 8. Exclude Specific Files During Directory Scan
```bash
linkfinder -i /path/to/directory -o cli -d --exclude somefile.js
```

### 9. Enable Verbose Output
```bash
linkfinder -i /path/to/file.js -o cli -v
```

### 🔄 10. Use with Burp Suite

1. Export JavaScript files from Burp.
2. Analyze them with:
   ```bash
   linkfinder -i /path/to/burp_exported.js -o cli
   ```

---

## 🧪 Example: Find All Links in a JS File
```bash
linkfinder -i /var/www/html/app.js -o cli
```

### 🌐 Example: Output Results in HTML
```bash
linkfinder -i /var/www/html/app.js -o html -o results.html
```

---

## 💡 Pro Tips
- Combine with tools like `gau`, `waybackurls`, or `jsfinder` for better enumeration.
- Always check JS files for juicy endpoints like `/api/`, `/admin/`, tokens, or hidden routes.

---

