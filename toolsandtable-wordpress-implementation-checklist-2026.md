# Tools & Table WordPress Implementation Checklist

Date: 2026-04-20
Audience:
- WordPress developer
- site owner
- designer or content lead

Goal:
- translate the site review into WordPress-specific implementation work

## Phase 1: Make the Site Publicly Launchable

### 1. Remove `noindex, nofollow`

Check:
- `Settings -> Reading`
- SEO plugin settings if installed
- theme or custom head hooks

Tasks:
- disable any “discourage search engines” setting
- disable page-level `noindex` rules on public pages
- verify in page source for:
  - homepage
  - recipes archive
  - tools guide
  - about page

Done when:
- page source no longer includes `meta name='robots' content='noindex, nofollow'`

### 2. Fix duplicate homepage title output

Likely causes:
- custom theme hardcoded `<title>`
- SEO plugin also outputting title metadata

Tasks:
- inspect `header.php`, `wp_head()`, and theme head partials
- remove hardcoded duplicate title output
- leave a single title source in place

Done when:
- homepage source contains one `<title>` tag

### 3. Fix dead links

Tasks:
- search theme templates and menus for `href="#"` usage
- replace with real page URLs or remove the links
- update footer social links with live profiles

Useful checks:
- appearance menus
- widget or block footer content
- hardcoded theme templates

Done when:
- no public-facing dead placeholder links remain

## Phase 2: Improve Search and Sharing

### 4. Add metadata for core pages

Pages:
- homepage
- recipes archive
- tools guide
- about page

Tasks:
- set unique SEO title for each page
- set unique meta description for each page
- configure Open Graph:
  - title
  - description
  - image
  - URL
  - type
- configure Twitter card metadata

WordPress implementation options:
- SEO plugin fields
- theme support if no plugin is used

Done when:
- each page generates clean previews in social debuggers and has unique meta descriptions

### 5. Ensure canonical URLs are correct

Tasks:
- confirm canonical for each page matches preferred permalink
- avoid duplicate canonical output from theme plus plugin

Done when:
- each page has one correct canonical URL

## Phase 3: Upgrade Homepage Credibility

### 6. Replace recipe placeholders with featured images

Tasks:
- ensure recipe posts have featured images assigned
- update archive/home template to pull featured image first
- add fallback only when no image exists

Template areas to inspect:
- homepage featured recipe card
- recipe archive card component
- any custom query loops

Done when:
- featured homepage recipes show real imagery instead of placeholder letters

### 7. Improve newsletter block

Tasks:
- replace generic headline/subhead with stronger copy
- confirm submit success and error states are styled and readable
- test mobile form layout
- optionally add archive or recent issue link below form

Files or areas to inspect:
- custom homepage template
- block pattern or reusable block
- JS handling for AJAX submit

Done when:
- newsletter section clearly communicates value and works on desktop and mobile

### 8. Expand About page

Tasks:
- add sections for:
  - mission
  - founder or brand story
  - editorial standards
  - tool testing methodology
  - start-here CTA
- add real photography if available

Implementation options:
- block editor page update
- custom page template if layout demands more control

Done when:
- About page answers who, why, what, and how in a credible way

## Phase 4: Build Better Information Architecture

### 9. Create brand pillar landing pages

Recommended pages:
- `Start Here`
- `Old World`
- `New World`
- `Techniques`
- `Beginner Series`

Tasks:
- create WordPress pages or taxonomy archives
- add intro copy and featured content blocks
- update homepage cards and footer links to point to them

Implementation note:
- use pages if editorial control matters more than automation
- use categories or custom taxonomies if long-term scaling matters more

Done when:
- the brand vocabulary maps to real destination pages

### 10. Improve internal linking modules

Tasks:
- add “related recipes” block on recipe pages
- add “related techniques” and “related tools” blocks where relevant
- add reverse links from tool guides to recipes

Implementation options:
- custom query loops by taxonomy
- related-posts plugin if lightweight and controllable
- manual curation for flagship content

Done when:
- key pages encourage next clicks instead of ending the session

## Phase 5: Technical Cleanup

### 11. Consolidate font loading

Observed:
- multiple Google Fonts references on homepage

Tasks:
- review theme enqueue functions
- remove duplicate font includes
- keep only required font weights
- prefer one enqueue path

Done when:
- font CSS is loaded once in a predictable way

### 12. Clean head output

Tasks:
- inspect duplicate icon declarations
- remove redundant favicon definitions where possible
- confirm theme and plugin outputs are not overlapping unnecessarily

Done when:
- head markup is cleaner and easier to maintain

### 13. Add schema

Tasks:
- recipe schema on recipe posts
- article schema on editorial pages if appropriate
- organization schema for brand/site identity

Implementation options:
- SEO plugin schema tools
- dedicated schema plugin
- custom JSON-LD in theme if needed

Done when:
- structured data validates for core page types

### 14. Accessibility pass

Tasks:
- verify heading order
- verify keyboard tab flow
- verify visible focus states
- verify form labels and error messaging
- check contrast of muted text and rust-on-cream combinations

Useful tools:
- browser accessibility inspector
- Lighthouse
- WAVE

Done when:
- primary flows are usable without obvious accessibility failures

## Suggested Role Split

### Developer

- indexing and metadata fixes
- template and theme cleanup
- dead link removal
- image/template logic
- schema and accessibility pass

### Content Lead

- final copy approval
- About page content
- hub page intros
- tool-testing standards copy
- newsletter positioning

### Designer

- recipe image treatment
- CTA hierarchy
- mobile QA
- social preview image design

## Pre-Launch QA

- homepage source has one title tag
- no public pages contain `noindex, nofollow`
- all nav and footer links resolve
- homepage cards show real images
- social previews are configured
- newsletter submission works
- mobile layout is stable
- key pages are indexed and crawlable

## Nice-to-Have After Launch

- analytics events for CTA clicks and newsletter submits
- recipe schema enhancements
- update timestamps on buying guides
- content templates for techniques and tool reviews
