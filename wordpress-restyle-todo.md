# To-Do: WordPress Site Restyle (Tools & Table)

This document outlines the steps required to transition `toolsandtable.com` to its new visual identity, using the recently created SVG assets.

## Phase 1: Preparation & Safeguards
- [ ] **Full Site Backup**: Create a complete backup of the database and files (e.g., using UpdraftPlus or Duplicator).
- [ ] **Staging Environment**: Set up a staging site (via host or LocalWP) to test changes without affecting live traffic.
- [ ] **Asset Audit**: Inventory existing images and media that need updating or replacing to match the new style.

## Phase 2: Branding & Identity
- [ ] **Finalize Logo Selection**: Choose between `logo-minimalist.svg`, `logo-traditional-rustic.svg`, or `logo-playful-bold.svg`.
- [ ] **Define Color Palette**: Extract primary and secondary hex codes from the chosen SVG to set as CSS variables or Global Styles.
- [ ] **Typography Selection**: Pair the logo with appropriate Google Fonts (e.g., *Montserrat* for Minimalist, *Playfair Display* for Rustic).
- [ ] **Update Favicon**: Generate and upload a 512x512px site icon derived from the logo symbol.

## Phase 3: Theme & Layout Configuration
- [ ] **Theme Selection**: Install a lightweight, block-based theme (e.g., Astra, GeneratePress, or Twenty Twenty-Four).
- [ ] **Global Styles Setup**: Configure global colors, typography, and button styles in the WordPress Site Editor.
- [ ] **Header/Footer Overhaul**:
    - [ ] Upload the new SVG logo to the header.
    - [ ] Update navigation menus for better "Cooking Guide" structure.
    - [ ] Refresh footer with new branding and copyright info.

## Phase 4: Content & Aesthetic Updates
- [ ] **Homepage Redesign**: Update the hero section to align with the new brand voice and visuals.
- [ ] **Post Templates**: Adjust the layout for recipes and guides to ensure high readability and clean "Table" presentation.
- [ ] **Block Patterns**: Create reusable patterns for "Tools Needed" or "Recipe Highlights" sections.
- [ ] **Image Refresh**: Replace outdated featured images with high-quality photography that fits the new aesthetic.

## Phase 5: Technical Optimization
- [ ] **SVG Support**: Ensure a plugin (like *SVG Support*) is active to allow the new logo files to be used safely.
- [ ] **Performance Audit**: Run a PageSpeed Insights check; optimize image loading and caching (WP Rocket or similar).
- [ ] **SEO Review**: Update Meta Titles/Descriptions if the "Tools & Table" brand positioning has shifted.

## Phase 6: Launch
- [ ] **Cross-Browser Testing**: Verify layout on Chrome, Safari, and Firefox.
- [ ] **Mobile Responsiveness**: Check all new styles on various mobile screen sizes.
- [ ] **Go Live**: Sync changes from staging to production.
- [ ] **Post-Launch Check**: Verify all forms and navigation links are functional.
