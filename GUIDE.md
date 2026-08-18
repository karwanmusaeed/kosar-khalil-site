# Kosar Khalil — Website Setup Guide

This project has three parts:
- **index.html** — the website itself (the design)
- **data/** — two data files: `site.json` (collections & photos) and `settings.json` (site texts)
- **admin/** — the control panel (Decap CMS), opened at `yoursite.com/admin`
- **images/uploads/** — the photos

Everything is free, except an optional custom domain.

---

## Part 1 — Create a GitHub account and upload the project

1. Go to **github.com** → **Sign up** → create an account with your email.
2. After logging in, click the **+** button (top right) → **New repository**.
3. Name the repository `kosar-khalil-site` — make sure **Public** is selected → **Create repository**.
4. On the new page, click **uploading an existing file**.
5. **Drag & drop** the contents of the project folder (extracted from the zip) onto the page — that means: `index.html`, `netlify.toml`, and the `admin`, `data`, `images` folders.
   - ⚠️ Note: don't upload the `kosar-khalil-website` folder itself — upload what's **inside** it.
6. Click **Commit changes** at the bottom and wait for the upload to finish (the images take a little while).

## Part 2 — Deploy on Netlify

1. Go to **netlify.com** → **Sign up** → choose **Sign up with GitHub** (easiest).
2. From the dashboard: **Add new site** → **Import an existing project** → **GitHub**.
3. Allow Netlify to access your account, then pick the `kosar-khalil-site` repository.
4. Change nothing (Build command empty, Publish directory `.`) → **Deploy site**.
5. After about a minute your site is live at an address like `random-name-12345.netlify.app`.
   - To change the name: **Site configuration → Site details → Change site name** → set it to `kosarkhalil` so it becomes `kosarkhalil.netlify.app`.

## Part 3 — Enable the control panel (one time only)

1. In Netlify, on your site's page: **Site configuration → Identity** → click **Enable Identity**.
2. Still under Identity: **Registration** → set it to **Invite only** (so nobody else can register).
3. Still under Identity, further down: **Services → Git Gateway** → click **Enable Git Gateway**.
4. Go to the **Integrations → Identity** tab (or the top of the page) → **Invite users** → enter your own email → **Send**.
5. Open your email → click **Accept the invite** → it takes you to your site and asks you to **set a password** — set one.

## Part 4 — Daily use

Go to: **kosarkhalil.netlify.app/admin** → log in with your email and password.

**Adding a new photo:**
1. Open **Website Content → Photos & Collections**.
2. In the **Photos** section → **Add Photos** → upload the image, fill in Title and Price.
3. In the **Collection ID** field, type the collection's ID (one of these): `citadel` · `sandstorm` · `babylon` · `nocturne` · `mist` · `legends`
4. Click **Publish → Publish now** at the top.
5. Wait 30–60 seconds — the site updates automatically.

**Changing a photo's title/price:** same place → click the photo in the Photos list → edit it → Publish.

**Deleting a photo:** in the Photos list, use the **⋮** icon or X on the item to remove it → Publish.

**Editing the site texts:** **Website Content → Texts & Settings** → change any text (site name, descriptions, email, Instagram/Behance links...) → Publish.

**Creating a new collection:**
1. In **Photos & Collections → Collections → Add Collections**.
2. Type an **ID** in English, lowercase, no spaces (example: `portraits`).
3. Fill in the title, description and the right-side text lines → Publish.
4. Now in Photos you can assign photos to that collection by typing the same ID.

⚠️ **Important:** a photo's Collection ID field must exactly match a collection's ID — if it's misspelled, the photo won't appear.

## Part 5 — Custom domain (optional)

If you want to buy `kosarkhalil.com` (~$10–15/year from Namecheap or Porkbun):
Netlify → **Domain management → Add a domain** → follow the on-screen instructions. HTTPS is added automatically.

---

## Technical notes

- The site has no real checkout yet — the Add to Cart button is only a counter. Once you decide on a payment method (Gumroad, Payhip...), the payment part gets wired in.
- If you open `index.html` directly on your computer (without a server), the data won't load — that's normal; it works fully on Netlify.
- The `data/site.json` file holds all the content — Netlify and GitHub keep their own copies, so nothing gets lost.
