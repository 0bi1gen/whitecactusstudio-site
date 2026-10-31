# whitecactusstudio.com

Static site for White Cactus Studio (home, Доростеф app page, privacy policy EN + SR).
No build step, no JavaScript, no cookies, no analytics, no third-party requests.

Source of truth for the policy text: `dorostef-app/docs/privacy-policy.md` (keep the HTML in sync).

## Deploy (GitHub Pages) — DRAFT, `[AWAITING VALIDATION]`
1. Create a PUBLIC GitHub repo (free Pages needs public), push this folder to `main`.
2. Repo > Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. At IONOS (Domains & SSL > whitecactusstudio.com > DNS):
   - Delete the default parking records for `@` (A and AAAA) first.
   - Add four A records for `@` (root): 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - Add four AAAA records for `@` (optional): 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153
   - Add CNAME `www` -> `<github-username>.github.io`
   - Verify the values against GitHub's current docs ("Managing a custom domain for your GitHub Pages site") before saving.
4. In Settings > Pages: custom domain `whitecactusstudio.com` (the `CNAME` file does this too), wait for the DNS check, then tick "Enforce HTTPS".
5. Check on a phone over mobile data: https://whitecactusstudio.com/dorostef/privacy/ and /sr/ load, valid HTTPS, no redirects to a login.

## Before publishing
- Update "Last updated" on both privacy pages to the publish date.
- Re-read the policy against the real app and the network audit result.
- Delete nothing from the policy that Google's forms rely on (Data safety must match it).
