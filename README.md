# Studio Poster – ordering website

Static website (one `index.html`, no build step). Customers pick posters/Polaroids, enter delivery details, and the order opens in WhatsApp addressed to **+91 7708739778**. You receive the order as a WhatsApp message and reply with payment instructions (prepaid only).

## Put it online with GitHub Pages (free)
1. Create a new repository on github.com (e.g. `studio-poster`), set it to Public.
2. Click **Add file → Upload files**, drag in everything from this folder (`index.html`, `.nojekyll`, `README.md`), then **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/studio-poster/`. Share this link with customers.

## Receiving orders
- A customer fills the form and presses **Send Order via WhatsApp**; WhatsApp opens with the full order text. The order only reaches you when they press Send.
- Photos cannot be attached automatically; the site tells customers to attach the original images in the same chat.
- Nothing is stored on a server, so keep the WhatsApp chats as your order record.

## Editing business details
Open `index.html` and edit the `CFG` block near the bottom (inside `<script>`):
- `wa` / `waShow`: WhatsApp number
- `email`: business email
- `insta`: Instagram profile URL (leave empty until the exact username is confirmed)
- `payInfo`: payment instructions shown at review (e.g. your UPI details), optional
- `delTN` / `delOther`: delivery charges (₹50 / ₹80)
- `cat`: sizes and prices (`null` price = custom quotation)
- `maxMB`: maximum photo size

On GitHub you can edit directly: open `index.html`, click the pencil icon, change values, commit.
