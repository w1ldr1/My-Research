# Tools & Table Developer Punch List

Date: 2026-04-20
Scope:
- homepage
- recipes archive
- tools guide
- about page
- sitewide metadata and navigation

## Priority 0: Launch Blockers

### 1. Remove sitewide `noindex, nofollow`

Status:
- observed on homepage, recipes, tools guide, and about page

Tasks:
- inspect WordPress reading settings and SEO plugin settings
- remove `noindex, nofollow` from public pages
- verify page source on:
  - `/`
  - `/recipes/`
  - `/tools-guide/`
  - `/about/`
- submit sitemap to Google Search Console after deployment

Acceptance criteria:
- public pages no longer output `meta name='robots' content='noindex, nofollow'`

### 2. Fix homepage duplicate `<title>` tags

Status:
- homepage outputs two title tags

Tasks:
- inspect theme head output and SEO plugin output
- ensure only one `<title>` is rendered
- confirm canonical is correct

Acceptance criteria:
- homepage outputs one title tag only

### 3. Replace or remove dead `#` links

Status:
- placeholder links present in homepage footer and other navigation areas

Known placeholders:
- `Old World`
- `New World`
- `Techniques`
- `Knife Guide`
- `Pans & Cookware`
- `Under $50`
- `Full Kit`
- `Beginner Series`
- `Technique Library`
- `Instagram`
- `YouTube`
- `Pinterest`

Tasks:
- map each placeholder link to a real destination
- if destination page does not exist, remove the link temporarily
- add real outbound social URLs or hide social links until accounts are ready

Acceptance criteria:
- no `href="#"` links remain on public-facing pages

## Priority 1: Credibility and Conversion

### 4. Add real imagery to featured recipe cards

Status:
- homepage recipe cards still use placeholder initials

Tasks:
- upload real images for featured homepage recipes
- ensure archive cards support featured images consistently
- define fallback only for genuinely missing images

Acceptance criteria:
- homepage featured and secondary recipe cards display real images

### 5. Add page-level meta descriptions and social metadata

Tasks:
- set meta descriptions for homepage, recipes, tools guide, and about page
- add Open Graph tags:
  - `og:title`
  - `og:description`
  - `og:image`
  - `og:url`
  - `og:type`
- add Twitter card tags

Acceptance criteria:
- each key page has a unique meta description and valid social preview metadata

### 6. Expand About page credibility blocks

Tasks:
- add founder story and editorial mission
- add tool testing methodology section
- add author or brand bio block
- add contact or contact path if appropriate

Acceptance criteria:
- About page clearly explains who is behind the site and why the advice is credible

### 7. Strengthen newsletter conversion area

Tasks:
- update newsletter copy to focus on outcome, not just cadence
- optionally add:
  - recent issue preview
  - archive link
  - subscriber count if meaningful
- validate successful and failed form states visually

Acceptance criteria:
- newsletter section communicates who it is for and why it is worth subscribing

## Priority 2: Information Architecture

### 8. Create real destination pages for brand pillars

Recommended pages:
- `/start-here/`
- `/old-world/`
- `/new-world/`
- `/techniques/`
- `/beginner-series/`

Tasks:
- create archive or landing page templates
- add intro copy to each
- connect homepage cards and footer links to them

Acceptance criteria:
- brand language maps to actual browsable content areas

### 9. Improve internal linking across content

Tasks:
- add related recipes on recipe pages
- link recipe pages to relevant tools and techniques
- link tools guides back to recipes that use those tools

Acceptance criteria:
- articles support multi-page browsing instead of dead-end sessions

## Priority 3: Technical Cleanup

### 10. Consolidate font loading and head output

Observed:
- multiple Google Fonts references on homepage
- multiple icon declarations

Tasks:
- remove duplicate font includes
- confirm only required font weights are loaded
- clean duplicate or redundant icon declarations if theme or plugin overlap exists

Acceptance criteria:
- head output is cleaner and easier to maintain

### 11. Add schema markup where appropriate

Tasks:
- recipe schema on recipe pages
- article schema for editorial pages
- organization schema for site identity if not already present

Acceptance criteria:
- structured data validates on key public pages

### 12. Audit accessibility basics

Tasks:
- confirm keyboard focus states
- verify form labeling
- check contrast on muted text and button states
- mark decorative images correctly
- confirm nav and section headings are semantically ordered

Acceptance criteria:
- major accessibility issues are removed from primary user flows

## Suggested Delivery Order

### Sprint 1

- remove `noindex, nofollow`
- fix duplicate title tag
- replace all `#` links
- add meta descriptions and social metadata
- replace placeholder recipe images

### Sprint 2

- expand About page
- improve newsletter conversion copy and trust cues
- create `Start Here`, `Old World`, `New World`, and `Techniques` pages
- add internal linking blocks

### Sprint 3

- clean head asset loading
- add schema
- accessibility pass
- analytics and event tracking

## QA Checklist

- view source confirms pages are indexable
- homepage has one title tag
- no placeholder links remain
- homepage cards show real images
- newsletter form success and failure states work
- all top-nav and footer links resolve correctly
- social sharing preview is acceptable for homepage and key pages
- mobile navigation and CTA layout still work after changes
