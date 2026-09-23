# Altera Roof Services: discovery

This is the launch checklist. **Confirmed** facts ship as written. Everything else is a `TODO:` in the site. Those look finished enough to demo, but they are never presented as true.

## Confirmed
| Fact | Source |
|---|---|
| Business name: **Altera Roof Services** | The logo, and the owner chose this name (confirmed) |
| Location: **Coquitlam, British Columbia** | Facebook post captions "Altera Roof Services at Coquitlam, British Columbia" (confirmed) |
| Services: residential shingle roofs, flat roofs / commercial, moss removal & maintenance, leak repair / emergency | Owner, in chat (confirmed) |
| Logo: a shield with two roof chevrons over the wordmark, in dark and light versions | Owner-supplied files (confirmed) |
| Job photos: 2 drone aerials, a moss roof before/after pair, a flat-roof skylight curb before/after pair | Owner's Facebook posts (confirmed) |
| They photograph jobs before and after, often by drone | 48-photo Facebook album (confirmed) |

## Open: blocking launch
- [ ] **Phone number.** The site uses the fictional `604-555-0142` (the reserved 555-01XX range). Replace it in `site/index.html` (search for `TODO: phone`).
- [ ] **Email address.** The site uses a placeholder `mailto:`. Replace it (`TODO: email`).
- [ ] **"Free roof check".** Confirm they offer free inspections or quotes. It's the site's main call to action.
- [ ] **Promise copy.** The owner approves the lines that describe how they work: "you get the before and after photos", the call-back promise in the FAQ, and the leak advice.
- [ ] **Service area** beyond Coquitlam (e.g. Port Coquitlam, Port Moody, Burnaby, Maple Ridge?).
- [ ] **Facebook page URL** for the footer link.
- [ ] **Hero film.** Needs Higgsfield credits (the balance was 0.08). Until then the site runs on the designed still hero. Later, replace it with real drone footage.


## Confirmed from the existing site (alteraroofservices.ca, Sep 2026)
The site itself was blocked from the build sandbox, so these facts came from search-engine snippets of it and from the [Yelp listing](https://www.yelp.ca/biz/altera-roof-services-vancouver) and [Instagram](https://www.instagram.com/alteraroofservices/). All are now used on the site (confirmed):
- Legal name **Altera Roof Services Ltd.** Tagline **"Roofing Done Right, The First Time."**
- **Repair-first**, specializing in roof leak diagnosis and targeted repairs: "finding the source of leaks, not guessing, patching blindly, or pushing unnecessary replacements."
- **Red Seal-certified** craftsmanship and **20+ years** of roofing experience.
- Works on every major roofing system and **all major membrane systems**: new installs, repairs, leak investigations, maintenance, full replacements.
- Mission: "Altera was built on one idea: do the job right and be straight with people."
- Values: no shortcuts; no surprises on the invoice; they show up when they say they will; they communicate clearly from first call to final walkthrough; "real accountability, not just a warranty on paper."
- Service area: **Lower Mainland and Fraser Valley**.
- Phone: **(604) 441-7876**. This replaces the 555 placeholder.
- The listing address (11910 220 Street) is deliberately **not** published on the new site. It may be a home address, so ask the owner first.

### Resolved from the blocking list above
- Phone: done. Service area: done. Facebook: replaced with Instagram in the footer.
- Email: still unknown. The "Email us" button was removed rather than left pointing at a placeholder.
- Privacy policy: the existing site's policy couldn't be retrieved. `site/privacy.html` is a new policy written for this site as built: no cookies, no analytics, no forms, and contact by phone or text only. **The owner must review it before launch.** Note that the old site mentions analytics cookies and this one uses none.
- Still to confirm: that the number accepts texts, and the "free roof check" offer.

## Open: nice to have
- [ ] Years in business, crew size, owner name and photo, in their own words, for an About section.
- [ ] Insurance and WorkSafeBC coverage, and warranty terms. **Do not claim any of these until confirmed.**
- [ ] Real reviews (Google, HomeStars, Facebook). **No testimonials or ratings ship until real ones exist**, and no `aggregateRating` in JSON-LD. Invented reviews for a real business are deceptive advertising under the Competition Act (s.74.01).
- [ ] Scope of the moss job (a cleaning or a re-roof?). Until then the site captions it only "Before / After".
- [ ] A leak repair photo for the services card. It currently uses a drawn icon, like the other cards.
- [ ] Higher-resolution originals of the job photos. The current ones are about 1250px wide, cropped from screenshots.

## Research: what local homeowners care about
- **Rain and moss.** Coquitlam gets about 1,800 mm of rain a year, and wet, shaded, wooded lots grow moss on roofs. ([Excel Roofing](https://www.excelroofing.ca/coquitlam/), [HomeStars](https://www.homestars.com/roofing/roofing-specialist-pros/coquitlam))
- **Roofers who disappear.** The top complaint is roofers who never call back, take weeks to quote, or leave jobs unfinished. A BC case: a roofer took $4,000 cash up front and vanished. ([Roofing Done Wright](https://www.roofingdonewright.com/blog/common-complaints-roofing-contractors/), [Penticton Herald](https://www.pressreader.com/canada/penticton-herald/20170925/281547996079908))
- **What good reviews praise.** The crew was on time, finished the job, and cleaned up. ([Penfolds](https://www.penfoldsroofing.com/locations/coquitlam-roofing), [Resilience](https://resilienceroofing.ca/))
- **What people check.** Insurance, local references, and photos of real work.

**Core argument:** *You see every step.* Altera already photographs its jobs before and after from the air. That answers the "roofers vanish" fear with proof instead of promises.

## Privacy
- Job photos are cropped from screenshots, and all metadata is stripped at export (`site/assets/*.jpg`).
- No street numbers or plates are legible at web size. Re-check this when higher-resolution originals arrive.
- The original screenshots stay in `review/` and are never deployed.
