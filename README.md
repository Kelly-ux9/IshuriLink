# IshuriLink

IshuriLink — Student–Teacher collaboration platform (MVP).

## What is included
- PHP backend (simple MVC-free structure)
- MySQL schema (import to create DB)
- Frontend pages per role (school admin, teacher, student)
- File uploads for materials, assignments, submissions
- Simple forums and announcements
- Session-based authentication

## Quick install (local with XAMPP)
1. Create database `ishurilink` and import SQL from `database.sql` (SQL provided in repo root).
2. Edit `config/db.php` with your DB credentials.
3. Create folders:
   - `assets/uploads/materials/`
   - `assets/uploads/assignments/`
   - `assets/uploads/submissions/`
   Make sure they are writable by the server.
4. Place the project under your web server root (e.g., `htdocs/IshuriLink/`).
5. Open `http://localhost/IshuriLink/register_school.php` to create a school and admin account.
6. Use created admin credentials to login and add teachers/students.
7. Teachers upload materials and create assignments; students view and submit.

## Notes & improvements
- Passwords currently stored with `md5` for simplicity. For production replace with `password_hash()` and update login logic.
- Use prepared statements or an ORM to harden SQL injection prevention.
- Limit upload file types and sizes (already basic checks present).
- For GitHub Pages + remote backend, host backend on a PHP host and set correct API endpoints.
- I can convert this to a Node/Express + SQLite or MySQL stack if preferred.

## Author
MUGISHA Kelly
