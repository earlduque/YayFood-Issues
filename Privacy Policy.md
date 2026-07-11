# YayFood Privacy Policy

**Last updated: July 11, 2026**

YayFood is a personal food-rating diary developed and published by Earl Duque ("the Developer"). This policy explains what information the app handles, where it is stored, who can see it, and your choices — including how to delete your account.

---

## The short version

- **Personal use (no household):** Your data lives **on your device** and in **your private iCloud account** (via Apple CloudKit). We do not run a server for it, and we cannot see it.
- **Shared households (optional, opt-in):** When you create or join a household, the data in that shared pool is stored on **our private hosted backend (Supabase)** so your household members can see it. This is the only situation in which your data leaves your device/iCloud for our infrastructure.
- We do **not** sell your data, show ads, or use third-party analytics or tracking SDKs.

## 1. What we store, and where

### On your device + your private iCloud (always)

Restaurants, dishes, ratings, people, photos, and notes you create are saved locally in the app and synced to **your own** iCloud account through Apple CloudKit. Apple's handling of iCloud data is governed by Apple's privacy policy. We have no access to your iCloud data.

Notes are stored as plain text (not encrypted) within the app's protected storage. Please don't put sensitive information in notes.

### On our hosted backend — only for shared households (Supabase)

If you opt in to a household:

- **Account/identity:** When you sign in with **Sign in with Apple**, we receive an opaque Apple user identifier and the name you choose to share. We store this to identify you as a household member. We do **not** receive your Apple password, and if you use Apple's "Hide My Email," we only ever see the relay address.
- **Shared content:** Restaurants (including their names, addresses, and map coordinates), dishes, ratings, people, notes, and dish photos in your household pool are stored in our Supabase project (database + private photo storage) so other members of your household can view them. Each rating is attributed to the member who authored it.
- **Notes are stored unencrypted:** Notes on shared restaurants and dishes are stored as **plain (unencrypted) text on the server**, visible to your household members. Avoid putting sensitive personal information in notes you share with a household.
- **Photos:** Shared dish photos are uploaded to a private storage bucket accessible only to members of your household. Photos are stripped of EXIF metadata (including GPS and device info) before upload.
- Access is enforced by row-level security: a member can only read or write data for households they belong to.

We use the backend solely to provide household sharing. We don't mine it for advertising or sell it.

### Optional image lookup (Pexels)

If you leave "auto-fetch dish images" enabled, the app may send a dish name to our image proxy to fetch a stock photo from Pexels. No personal identifiers are sent — only the search term. You can turn this off in Settings; the app works fully without it.

## 2. Data retention and deletion

- **Delete individual data:** Remove restaurants, dishes, ratings, etc. in the app at any time. Deletions of shared data propagate to your household members.
- **Leave a household:** You can leave a household at any time. Your past contributions remain in that household's shared pool (so the remaining members' history stays intact), and your device keeps a private copy.
- **Delete your account (in-app):** Settings → Household → **Delete Account**. This revokes your Sign in with Apple authorization and permanently deletes your account identity from our backend. Your authored contributions remain in any household pool you participated in (attributed to your past identity), and your device keeps its private local copy. After deletion you cannot sign back into that account; a new sign-in creates a new identity. Account deletion requires an internet connection.
- **Export your data:** Settings → Data Management lets you export your diary as JSON or text at any time.

## 3. Children's privacy

YayFood is not directed at children under 13 (or the equivalent minimum age in your jurisdiction) and we do not knowingly collect their information.

## 4. Third-party services

The app relies on the following third-party services, each governed by its own privacy policy:

| Service | Purpose | Privacy Policy |
|---|---|---|
| Apple (iCloud/CloudKit, Sign in with Apple, App Store) | Private sync, optional sign-in, distribution & tips | https://www.apple.com/legal/privacy/ |
| Supabase | Hosted backend for optional household sharing (our data processor) | https://supabase.com/privacy |
| Pexels | Optional stock food images (receives only a search term) | https://www.pexels.com/privacy-policy/ |

We do not use advertising networks or analytics/tracking SDKs.

## 5. Your rights and choices

- Use the app entirely locally: without joining a household, no data reaches our infrastructure at all.
- Turn off Pexels image fetching in Settings for a fully offline experience (or use text-only mode).
- Export, correct, or delete your data in the app at any time; delete your account in-app as described above.
- Depending on where you live (for example, the EEA/UK under GDPR, or California under the CCPA/CPRA), you may have additional statutory rights. Contact us to exercise them.

## 6. Changes to this policy

We may update this policy as the app evolves. When we do, we will revise the "Last updated" date at the top of this document. Material changes will be noted in the app's release notes.

## 7. Contact

Questions? Open an issue at https://github.com/earlduque/YayFood-Issues or contact the developer at earliodookie+yayfood@gmail.com.

---

*This policy applies to the YayFood iOS application only.*
