# 💥 Laravel Reflected XSS PoC - CVE-2024-13918

This repository demonstrates a **Reflected Cross-Site Scripting (XSS)** vulnerability in Laravel (CVE-2024-13918). The bug is triggered when the Laravel application is in **debug mode** and reflects unsanitized input back in the HTTP response.

> ⚠️ **This project is intended for educational and security research purposes only. Do not use this on systems you do not own or have permission to test.**

---

## 📖 CVE Details

- **CVE ID:** CVE-2024-13918  
- **Type:** Reflected XSS  
- **Affected Component:** Laravel error page in debug mode  
- **Severity:** Medium  
- **Impact:** Arbitrary JavaScript execution in the browser of the user  
- **Fix:** Disable debug mode (`APP_DEBUG=false`) or upgrade Laravel to the patched version.

---

## ⚙️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/laravel-xss-poc.git
   cd laravel-xss-poc

Install dependencies

```
composer install
```
