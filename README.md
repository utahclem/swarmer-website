# SWARMER Website

Static site — two HTML files, one images folder. Same stack as dehornmusic.com.

## File Structure

```
swarmer-website/
├── index.html
├── epk.html
└── images/
    ├── logo-white.png          ← Swarmer_Logo-White.png (rename)
    ├── band-portrait.jpg       ← Swarmer_Band_Portrait.jpeg (rename, B&W alley shot)
    ├── band-victoria-hills.jpg ← 1780933490471_IMG_4437.jpeg (rename, Victoria Hills color shot)
    ├── live-crucialfest.jpg    ← 1780933425013_057A4630.jpeg (rename, Crucialfest live shot)
    ├── shell-classic.png       ← SWARMER_SHELL.jpg (rename, classic shell logo art)
    ├── merch-1.jpg             ← any merch photo you have
    ├── merch-2.jpg             ← any merch photo you have
    └── albums/
        ├── one-pound.jpg       ← One Pound EP artwork (grab from Bandcamp or your files)
        └── foremast.jpg        ← Foremast single artwork (grab from Bandcamp or your files)
```

**Note:** Brutalist album art loads directly from Bandcamp CDN — no local copy needed.
One Pound / Foremast artwork falls back to Bandcamp CDN if local files are missing.

## Image Notes

- `logo-white.png` — Use the white wordmark-only version (Swarmer_Logo-White.png)
- `band-victoria-hills.jpg` — Used as EPK hero. The low-angle outdoor color shot.
- `band-portrait.jpg` — Used in About section on main site. The B&W alley portrait.
- `live-crucialfest.jpg` — Used in EPK live section. Photo credit: Bonneville Jones.
- Shell/death metal variants (SWARMER_DEATH_SHELL.png, SWARMER_DEATHMETAL.png) — not 
  currently used in the build but available for future use.

## Deployment (same as Dehorn)

1. Create GitHub repo: `swarmer-website` (or whatever you name it)
2. Push all files (index.html, epk.html, images/)
3. In Cloudflare Pages: create new project → connect to GitHub repo → no build command needed
4. Add custom domain: swarmermusic.com
5. In Squarespace (where swarmermusic.com is registered): update nameservers to Cloudflare

## DNS (Squarespace → Cloudflare)

Same process as Name.com for Dehorn, just done through Squarespace's domain settings:
- Log into Squarespace Domains
- Find swarmermusic.com → Settings → Nameservers
- Replace with Cloudflare nameservers (provided when you add the domain in Cloudflare)

## Fonts

Google Fonts (loaded via CDN, no local files needed):
- Bebas Neue — headings / display
- Barlow — body text
- Barlow Condensed — labels, nav, UI
- Share Tech Mono — mono labels, dates

## Colors

- Background:    #0d0b09
- Raised bg:     #131009
- Accent:        #a0442a  (deep rust)
- Text:          #e8e4de
- Text dim:      #8a8278
- Text muted:    #5a5550

## Sections

### index.html
- Nav (fixed, collapses to hamburger on mobile)
- Floating social bar (desktop only)
- Hero — Brutalist album art background, white logo, tagline, CTA buttons
- Latest Release — Brutalist with streaming links
- News & Press — 4 items (Braeburn signing, SLUG Localized, SLUG Soundwaves, City Weekly)
- Discography — grid with click-to-open modals (tracklists + streaming links)
- Merch — links to Bandcamp
- Videos — Brutalist official video embed
- Tour — placeholder with Bandsintown link
- Info/About — bio, member grid, label block, contact, band photo
- Footer

### epk.html
- Split hero (Victoria Hills band photo left / band info right)
- Pull quote banner (City Weekly)
- Bio + members
- Discography sidebar
- Listen / Follow links sidebar
- Press section (4 items)
- Live section (Crucialfest photo + booking info)
- Press assets grid (photos, logo, album art)
- Footer with contact

## To Do / Future

- Add Bandsintown widget to Tour section when shows are booked
- Mailing list integration (same options as Dehorn: Mailchimp embed, etc.)
- One Pound CD / Brutalist vinyl merch photos when available from Braeburn
- Longer bio when written
- YouTube section expansion as more videos are added
- Death metal logo/shell variants — decide if/how to incorporate
