# YayFood Privacy Policy

_Last updated: June 23, 2026_

YayFood is a personal food-rating diary. This policy explains what information the app handles, where it is stored, and your choices — including how to delete your account.

## The short version

- **Personal use (no household):** Your data lives **on your device** and in **your private iCloud account** (via Apple CloudKit). We do not run a server for it, and we cannot see it.
- **Shared households (optional, opt-in):** When you create or join a household, the data in that shared pool is stored on **our private hosted backend (Supabase)** so your household members can see it. This is the only situation in which your data leaves your device/iCloud for our infrastructure.
- We do **not** sell your data, show ads, or use third-party analytics/tracking SDKs.

## What we store, and where

### On your device + your private iCloud (always)
Restaurants, dishes, ratings, people, photos, and notes you create are saved locally in the app and synced to **your own** iCloud account through Apple CloudKit. Apple's handling of iCloud data is governed by Apple's privacy policy. We have no access to your iCloud data.

Notes are stored as plain text (not encrypted) within the app's protected storage. Please don't put sensitive information in notes.

### On our hosted backend — only for shared households (Supabase)
If you opt in to a household:
- **Account/identity:** When you sign in with **Sign in with Apple**, we receive an opaque Apple user identifier and the name you choose to share. We store this to identify you as a household member. We do **not** receive your Apple password, and if you use Apple's "Hide My Email," we only ever see the relay address.
- **Shared content:** Restaurants, dishes, ratings, people, and dish photos in your household pool are stored in our Supabase project (database + private photo storage) so other members of your household can view them. Each rating is attributed to the member who authored it.
- **Photos:** Shared dish photos are uploaded to a private storage bucket accessible only to members of your household. Photos are stripped of EXIF metadata (including GPS and device info) before upload.
- Access is enforced by row-level security: a member can only read/write data for households they belong to.

We use the backend solely to provide household sharing. We don't mine it for advertising or sell it.

### Optional image lookup (Pexels)
If you leave "auto-fetch dish images" enabled, the app may send a dish name to our image proxy to fetch a stock photo from Pexels. No personal identifiers are sent — only the search term. You can turn this off in Settings; the app works fully without it.

## Data retention and deletion

- **Delete individual data:** Remove restaurants, dishes, ratings, etc. in the app at any time.
- **Leave a household:** You can leave a household at any time. Your past contributions remain in that household's shared pool (so the remaining members' history stays intact), and your device keeps a private copy.
- **Delete your account (in-app):** Settings → Household → **Delete Account**. This revokes your Sign in with Apple authorization and permanently deletes your account identity from our backend. Your authored contributions remain in any household pool you participated in (attributed to your past identity), and your device keeps its private local copy. After deletion you cannot sign back into that account; a new sign-in creates a new identity. Account deletion requires an internet connection.
- **Export your data:** Settings → Data Management lets you export your diary as JSON or text at any time.

## Children

YayFood is not directed at children under 13 and we do not knowingly collect their information.

## Third parties

- **Apple** (iCloud sync, Sign in with Apple) — governed by Apple's privacy policy.
- **Supabase** (hosted backend for household sharing) — our data processor; data is stored in their infrastructure under our project.
- **Pexels** (optional stock images) — receives only a search term when image fetching is enabled.

We do not use advertising networks or analytics/tracking SDKs.

## Changes

We may update this policy as the app evolves. Material changes will be reflected by the "Last updated" date above.

## Contact

Questions? Open an issue at https://github.com/earlduque/YayFood-Issues or contact the developer at earliodookie+yayfood@gmail.com.
