# ab47techlabs.com

Corporate website for **AB47 Tech Labs Private Limited**, the company behind [Nexfinity](https://nexfinity.ai/).

Plain HTML and CSS with no build step and no dependencies. It works on any static host.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home: who we are, vision and mission, Nexfinity, who we serve, principles |
| `about.html` | Story, vision, mission, values, leadership, company facts |
| `products.html` | Nexfinity and its three products, each linking to nexfinity.ai |
| `careers.html` | Why join, open roles, hiring process |
| `contact.html` | Company contacts, with product enquiries sent to Nexfinity |
| `privacy.html`, `terms.html` | Draft legal pages for this website |
| `404.html` | Not-found page |

Shared styles are in `assets/css/styles.css`. Colours and fonts follow the brand kit in `AB47-Tech-Labs-Brand-Kit/` (open `brand-guidelines.html`): Deep Blue `#386BB3` for buttons and links, Code Blue `#6692CF` for accents, Ink `#111111` for headings and dark sections, Fira Sans for text and Jost for small uppercase labels. Change them in the `:root` block at the top of the stylesheet. The mobile menu and footer year are in `assets/js/main.js`.

## Before you go live: fill in the placeholders

Anything still missing is wrapped in `<span class="ph">…</span>` and shows with a yellow highlight. To find every one:

```bash
grep -n 'class="ph"' *.html
```

What's needed:

- **Email addresses** `hello@` and `careers@ab47techlabs.com`: set up these mailboxes, or change them
- **Legal pages**: last-updated date, Grievance Officer, jurisdiction city. Have a lawyer review both pages, then delete the yellow "Draft" notice.

Also review the draft vision, mission, values and story copy, and change anything that doesn't sound like you.

The header, nav and footer are repeated in every page. If you change one, change it in all seven pages.

## Run locally

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080.

## Deploy

Any static host works. Two free options:

- **Netlify** or **Cloudflare Pages**: drag this folder into the dashboard, or connect a Git repo with no build command and `/` as the publish directory. Then add `ab47techlabs.com` as a custom domain.
- **GitHub Pages**: push to a repo, turn on Pages for the `main` branch, and add a `CNAME` file containing `ab47techlabs.com`.

After deploying, point your domain's DNS records at the host. Each host's custom-domain screen gives the exact records.

## Link the two sites

On nexfinity.ai, change the footer line to something like:

> Nexfinity is a product of [AB47 Tech Labs Private Limited](https://ab47techlabs.com/).
