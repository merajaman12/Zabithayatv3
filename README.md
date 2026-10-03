# Zabit Hayat Tele

GitHub Pages-ready single-page website.

## Features
- 8 post slots.
- Each post supports title, description, purchase/link URL, image or video.
- Admin can select a local image/video from the admin device; it is converted to browser storage for this static version.
- Telegram purchase CTA.
- Social usernames/links are editable.
- Responsive design.

## Hidden Admin Panel
There is **no visible Admin link** on the public website.

Open the special URL:

`YOUR-GITHUB-PAGES-URL/#zht-admin`

Then enter the admin password.

### Important security limitation
GitHub Pages is a static public website. A hidden URL is **not real security**, and a password stored in frontend JavaScript/localStorage can be discovered by someone who knows how to inspect the site.

For a genuinely private admin panel with secure authentication and uploads that work for every visitor, use a backend such as Supabase/Firebase. The current UI is structured so that this can be connected later.

## Media
For GitHub Pages, small images/videos selected in the browser are stored as browser data in localStorage. This is suitable for testing/personal use but not ideal for large media.

For production:
- store media in Supabase Storage/Firebase Storage,
- store post metadata in a database,
- authenticate the admin server-side.
