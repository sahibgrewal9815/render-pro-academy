# Render Pro Academy

Website for Render Pro Academy: online architectural rendering course (SketchUp, D5 Render, Filmora), models and materials store, Render Pro Detail Lab, Render Review and student gallery.

Live at **https://rpa.visionforge.co.in**

## How it works
- **This repo** holds the website (one `index.html` plus app icons). GitHub Pages serves it on the custom domain in `CNAME`.
- **Supabase** (project "Render Pro Academy", Mumbai) holds the database, logins, files and server functions:
  - `student-login`: Login ID + password, locked to one device
  - `admin-api`: create course logins, change passwords, delete students (admins only)
  - `secure-file`: short-lived download links for lesson files and store packs
- The key in `index.html` is Supabase's public (anon) key. That's safe to publish: every table is protected by row-level security.

## Logins
- **Admin dashboard / Content studio:** `#admin` or `#studio`, log in with the admin email and an 8-digit email code.
- **Course students:** `#learn`, Login ID + password created in the admin dashboard.
- **Customers:** `#account`, email code; name and mobile number are required at sign-up.

## Still to connect
- Resend (email codes to all customers)
- Bunny Stream (lesson and Detail Lab videos)
- Razorpay (online payments)
