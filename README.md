# Linux - OSINT Guide ⚫️

## 🎯 GOAL: Start with just a name → find more info (accounts, location, contacts, etc.)

### 🔍 PROCESS: Step-by-step breakdown
> ⚠️ Please read [DISCLAIMER](DISCLAIMER.md) before using this guide.

---

## ✅ 1. **Name Recon – Filter the Noise**

* Use **exact/full name** if known (e.g., "Ravi Sharma")
* Add context if you have it:
  * Location (city, country)
  * Age group or workplace/school

**Tools**:

* Google dorking:
  ```
  "Ravi Sharma" site:linkedin.com/in
  "Ravi Sharma" site:facebook.com
  ```
* Social search engines:
  * [PeekYou](https://www.peekyou.com)
  * [Pipl](https://pipl.com) *(paid)*
  * [BeenVerified](https://www.beenverified.com) *(paid, US-focused)*

---

## ✅ 2. **Image + Face Hunting**

* Search for image matches:
  * Use Google Image Reverse
  * Yandex (better for face matching)
* If you find a profile photo, try facial search or context matching

---

## ✅ 3. **Social Media Mapping**

Try all major social networks using username permutations:

* Facebook
* Instagram
* LinkedIn
* Twitter/X
* Snapchat
* TikTok

**Automated Tools**:

* 🔧 **Sherlock** (GitHub): Finds usernames across platforms
* 🔧 **Maigret** (Alt. to Sherlock)
* 🔧 **Namechk.com** (for handle availability)

If name is uncommon – success chances go way up.

---

## ✅ 4. **Check Leaked Databases (Emails, Phones)**

If you somehow link an **email or phone**, check:

* **HaveIBeenPwned.com** – data breaches
* **Scylla.sh** or **Dehashed.com** *(paid)* – leaked credential dumps
* Telegram bot leaks (like @finduserbot or @mailsearchbot – exist in grey zones)

---

## ✅ 5. **Check Domain Ownership / Forums / GitHub**

If the person has a technical background:

* Search GitHub by name
* Check domain WHOIS (old sites they made)
* Look for posts on forums, StackOverflow, Reddit

---

## ✅ 6. **Cross-Reference Public Databases (Location Dependent)**

Depending on country:

* Voter rolls
* Property tax records
* Business registries
* Alumni databases

These are often public or semi-public.

---

## ✅ 7. **Phone Numbers & Emails to Socials**

If you have a phone or email:

* Plug into:
  * **Truecaller**
  * Telegram "Add Contact" (see profile photo, name)
  * Instagram "Find Friends" via contacts (if you import)

Also try:

* Facebook/IG password reset page → enter phone/email → if it exists, shows name/partial info

---

## 🔍 Reality Check

If they're:

* Tech-savvy
* Use aliases or burner accounts
* Hide metadata

Then it becomes **10x harder**.

But 80% of people leak **enough** to be traced **just from their name** – especially if it's unique or semi-unique.

---

## 💡 Example: You have just "Aarav Mehta"

You would:

1. Google + LinkedIn dork: `"Aarav Mehta" site:linkedin.com`
2. Look for profile matches with matching photo/location
3. Reverse search profile image via Yandex
4. Check if username "aaravmehta" exists on IG/Twitter
5. Run Sherlock/Maigret on likely usernames
6. Try @finduserbot on Telegram with likely usernames

---

# LEVEL +1 🟡

So, what you read just above is only **surface-level OSINT** – the kind anyone with persistence can figure out.

But if you're talking **serious deep-trace, digital fingerprinting, passive intel** – then yeah, there's a **lot more** under the iceberg. Here's a taste of what lies deeper:

---

## 🧠 Under the Iceberg – What Real Investigators/Threat Actors Might Use

### 🔍 1. **Cross-platform behavioral fingerprinting**

* **Same typing patterns**, emojis, slang across accounts = linked identities
* AI can cluster accounts by **language model** style (yes, it's a thing now)
* Timezone-based posting patterns = locate region

---

### 🧠 2. **Device/Browser Fingerprints**

If you ever:

* Clicked a shady link
* Visited a site with tracking scripts
* Installed an app

Then your:

* Your current OS
* Ip address
* Device model
* Screen resolution
* Fonts
* Audio stack
* Canvas fingerprint and many more

…can all be used to **track you across sessions, sites, and identities**.

Tools like:

* **Creepy**
* **FingerprintJS**
* **Amass** for subdomain tracking
* **Sn0int** or **Spiderfoot** for full OSINT profiling

---

### 📡 3. **Passive DNS, Subdomain & Infrastructure Recon**

Even if a person *hosted* something for a while:

* Passive DNS can show **historical records**
* Tools like **SecurityTrails**, **DNSDumpster**, **Shodan**, or **Censys**
* Can link emails used in SSL certs, domain WHOIS, etc.

---

### 🛰️ 4. **Wi-Fi / Geolocation Leaks**

People leak:

* Home router SSIDs in metadata
* GPS EXIF in photos (if not stripped or removed)
* Even simple web apps can use **WebRTC leaks** to get internal IPs

---

### 💥 5. **Sock Puppet Attribution**

Let's say someone uses multiple fake accounts.

By:

* Comparing browser fingerprints
* Device behavior
* Login times
* AI analysis of writing style

You can cluster them and say:

> "These 5 accounts are very likely the same human behind them."

Used by:

* Law enforcement
* Private intel firms
* Ad-tech companies

---

### 🕸️ 6. **Deep Leak Repositories**

If you know where to look (usually darkweb or invite-only forums):

* Full leak dumps (not just emails, but full profiles, photos, ID scans)
* Combo lists of usernames, IPs, and devices
* Aggregated OSINT platforms built by ex-analysts or threat actors

---

## ⚠️ But Let's Be Clear:

Yes, it's possible to go extremely deep. But:

* 90% of targets can be profiled with just **public data + time**
* The last 10% – the "invisible ones" – require **privileged access**, serious tools, or legal overreach

---

# LEVEL +2 🟠

## 0) Quick goal → end state

Start: only **name = Jordan Miles**
End: prioritized, validated profile: possible usernames, social accounts, location, employer clues, public images, emails/phones if publicly available or leaked in breaches.

---

## 1) Google dorking (fast wins)

Examples (paste into Google):

* `"Jordan Miles" site:linkedin.com`
* `"Jordan Miles" "New York" -"obituary"`
* `intitle:"Jordan Miles" site:medium.com`

---

## 2) Username hunting (automation or manual way)

Tools: **Sherlock**, **Maigret**.
Sherlock example: `sherlock "jordanmiles"`
Goal: find same handle across Twitter, IG, GitHub, TikTok.

What to validate: profile pics, bio lines, mutual connections, location strings.

---

## 3) Image reverse search

Use: **Yandex**, **Google Images**, **TinEye**.
If you find a photo, reverse it – may reveal older profiles, portfolio sites, or event photos with tags.

---

## 4) Social profile correlation

For each candidate account:

* Compare profile photo, bio, posting style, timezone, language.
* Check cross-links (Twitter → Linktree → personal site).
* Look for public friend lists, tagged posts, comments that reveal networks.

Goal: cluster accounts that are likely same person.

---

## 5) Public records & context

Depending on country, search:

* Company registries, LinkedIn company pages
* Local news archives
* University alumni pages
* Domain WHOIS for personal domains (`jordanmiles.com`)

Tools: Browser + `site:` dorks, SecurityTrails/Whois for domain history.

---

## 6) Breach / credential footprints (ethical checks)

Sites: **HaveIBeenPwned** (email only), **Dehashed/Intelx** (paid – be cautious).
If an email surfaces in public breaches, it can confirm an identity – "don't" use leaked credentials.

---

## 7) Infrastructure & historical traces

Tools: **Wayback Machine** (old versions of sites), **SecurityTrails**, **Passive DNS**.
Why: shows past email addresses, old bios, or domains that tie to other aliases.

---

## 8) Device / network signals (passive)

Look for developer assets: GitHub commits (emails in commit history), published papers, npm/pypi packages. Those often leak real emails.

---

## 9) Build the profile + confidence scoring

For each data point assign confidence:

* 3 = Strong (matching photo + same employer + unique handle)
* 2 = Probable (matching bio + overlapping network)
* 1 = Weak (same name + generic location)

Make a simple table and stop once you have a 2–3 high confidence matches.

---

## 10) Verify ethically

* Prefer cross‑references from at least **two independent public sources** before concluding.
* If you must contact: use a professional/transparent approach (not deception).

---

## Quick tool list (practical)

* Sherlock / Maigret – username sweep
* Yandex / Google Images / TinEye – reverse image
* Google dorks – targeted search
* Wayback, SecurityTrails, PassiveDNS – historical/infrastructure
* LinkedIn, Twitter, Instagram, GitHub – primary social checks
* HaveIBeenPwned – breach checks (email only)
* Maltego / SpiderFoot – automation/graphing (for large targets)

---

## Defensive checklist (if you were Jordan)

* Strip EXIF from photos before upload.
* Use unique usernames and emails per service.
* Don't reuse profile photos across public/professional accounts.
* Turn off public friend lists and limit metadata.
* Enable MFA; monitor HaveIBeenPwned for leaked emails.

---

# LEVEL +3 🔴

Okay so if you reached till here then you will get some practical catalogue of **useful OSINT tools** with one-liner examples or command snippets for each and a short note about what you'll get. No fluff, just actionable. Use responsibly and stay "legal".

# OSINT tools (practical examples)

> Quick legal note: these are **public‑source** and passive techniques. Don't perform unauthorized access, scraping that violates ToS at scale, or anything intrusive. Read each tool's docs & local law.

---

## 1) Google / Google Dorks

Example queries:

```
"Vishal Patel" site:linkedin.com
"Vishal Patel" "Mumbai" filetype:pdf
intitle:"Vishal Patel" site:medium.com
```

What you get: quick public hits, posts, PDFs, corporate mentions. Best first step.

---

## 2) Reverse image search – Google / Yandex / TinEye

Manual: upload profile photo to Yandex / Google Images / TinEye.
What you get: other places the image appears (old profiles, event galleries, portfolio).

---

## 3) Sherlock (username sweep)

Install & run:

```bash
git clone https://github.com/sherlock-project/sherlock.git
cd sherlock
python3 -m pip install -r requirements.txt
python3 sherlock.py vishalpatel --timeout 10 --output results.json
```

What you get: list of platform URLs where that username exists (helps find cross‑platform handles).

---

## 4) Maigret (modern Sherlock alternative)

Install & run:

```bash
pip install maigret
maigret vishalpatel --export json --timeout 10
```

What you get: similar to Sherlock, often with more modern site checks and exported results.

---

## 5) theHarvester (email/subdomain discovery)

Example:

```bash
theHarvester -d example.com -b google -l 200
```

What you get: harvested emails, subdomains, hostnames from public search engines and sources.

---

## 6) Recon-ng (modular OSINT)

Basic usage:

```bash
recon-ng
# inside RECON-NG
marketplace install all
use recon/domains-hosts/bing
set SOURCE example.com
run
```

What you get: modular workflow (WHOIS, DNS, recon) and built-in DB for correlation.

---

## 7) SpiderFoot (automation + graph)

Docker quick run:

```bash
docker run -v $(pwd)/sfdb:/data -p 5001:5001 spiderfoot/spiderfoot
# Open http://localhost:5001 and run a scan
```

What you get: automated scans across 100+ modules, visual graphing of linked results.

---

## 8) Maltego (graph analysis GUI)

Usage: GUI app. Create transforms (import domains, names, e‑mails) → run transforms → inspect graph.
What you get: powerful visual relationship maps (good for investigations).

---

## 9) Wayback Machine (historical snapshots)

Check history:

```bash
# web UI: https://web.archive.org/web/*/vishalpatel.com
# or use waybackpy in Python for automation
```

What you get: old site content, past bios, email addresses.

---

## 10) Whois / dig / host (domain and DNS)

Examples:

```bash
whois vishalpatel.com
dig +short TXT _dmarc:vishalpatel.com
dig +noall +answer example.com ANY
```

What you get: domain registrant info, DNS records, historical clues.

---

## 11) SecurityTrails / PassiveTotal / DNSDumpster (passive DNS)

API example (SecurityTrails):

```bash
curl -H "APIKEY: YOUR_KEY" "https://api.securitytrails.com/v1/domain/example.com/history"
```

What you get: historical DNS, subdomains, associated IPs (paid tiers more data).

---

## 12) Shodan (internet-exposed assets)

CLI:

```bash
shodan search --fields ip_str,port,org "vishalpatel"
shodan host 1.2.3.4
```

What you get: servers, exposed services, SSL certs linked to domains/emails.

---

## 13) Censys (certificate & host search)

CLI/API example:

```bash
# use API or the web UI
curl -u 'UID:SECRET' "https://search.censys.io/api/v2/hosts/search?q=parsed.names:vishalpatel.com"
```

What you get: historical certs, domains, infrastructure ties.

---

## 14) Amass / Subfinder (subdomain & footprinting)

Amass passive scan:

```bash
amass enum -passive -d example.com -o amass.txt
```

Subfinder:

```bash
subfinder -d example.com -o subfinder.txt
```

What you get: subdomain enumeration, which can reveal internal projects or personal sites.

---

## 15) GitHub / code search (commits, emails)

Google dork:

```
site:github.com "Vishal Patel"
```

GitHub search or use `git log` on repos to inspect commit emails (public).
What you get: code, commit emails, repos, username patterns.

---

## 16) HaveIBeenPwned (breach lookup – email required)

API example (requires key):

```bash
curl -s -H "hibp-api-key: KEY" "https://haveibeenpwned.com/api/v3/breachedaccount/vishal@example.com"
```

What you get: if that email appears in public breaches – can confirm identity links (don't use leaked passwords).

---

## 17) TrueCaller / Telegram / Signal discovery (phone → identity)

Manual: add number to phone contacts & open Telegram/Signal → sometimes reveals profile. Truecaller web/phone shows caller name (depends on user data).
What you get: possible name/photo associated with phone numbers.

---

## 18) Social search engines & directories (Pipl, PeekYou, Spokeo)

Examples: use their web UIs or paid APIs to run name + location lookups.
What you get: aggregated public records, social accounts, sometimes contact info (often paid).

---

## 19) Recon & OSINT Framework sites

* OSINT Framework (web UI) – maps tools by data type.
  What you get: fast pointer to niche tools for emails, people, phone, metadata.

---

## 20) Metadata / EXIF tools (image EXIF)

Command:

```bash
exiftool image.jpg
```

What you get: camera make, GPS (if not stripped), timestamps – use on images you legitimately have.

---

## 21) Browser fingerprinting / passive tracking libs

* FingerprintJS (library) – shows how sites can track devices.
  What you get: understanding of how device/browser fingerprints are constructed (useful for detection/defense).

---

## 22) Telegram / Mastodon / Niche search bots

Manual: query bots like `@usernameinfo_bot` or Mastodon search for usernames across instances. Many niche platforms have search bots or public APIs.

---

# Quick combo workflows (two examples)

**A – Name → social handles**

1. Sherlock/Maigret sweep for `vishalpatel`
2. Google dorks for full name + site:linkedin/github
3. Reverse image Yandex for any found photo

**B – Domain / email → infrastructure**

1. whois + dig + amass
2. Shodan/Censys + SecurityTrails for historic certs/IPs
3. Wayback for past website content

---

# Output & validation suggestions

* Keep results in a CSV with columns: `source,url,evidence,confidence(1-3)`.
* Require **two independent sources** for confidence ≥2.
* Track timestamps – OSINT is ephemeral.

---

# Final short defensive tips (for you or targets)

* Use unique photos & usernames for sensitive personas.
* Strip EXIF before uploading.
* Use separate emails per service and monitor breaches.
* Limit public friend/follower lists.

---

# More Comming soon...
