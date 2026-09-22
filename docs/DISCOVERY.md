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
