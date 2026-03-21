# Task: Redesign FoodBook Prototype — Desktop-First with Sidebar

## Context
You are working on `index.html` in this repo — a single-file HTML/CSS/JS prototype for a cooking app called FoodBook. The current design is mobile-first with a phone shell and bottom navigation bar.

**Elena (the user) wants a desktop-first redesign with this layout:**

## Requirements

### Layout — Desktop (primary, min-width ~900px)
- **Left sidebar** (fixed, ~260-280px wide):
  - App logo/brand at the top (🍲 FoodBook)
  - Main navigation sections listed vertically: Home, Food Diary, My Recipes, Want to Try (Wishlist), Tips & Tricks, Cooking Tracker
  - Each section is clickable. When clicked, the section becomes active (highlighted in primary green #8B9E6B)
  - **Accordion subcategories:** When a section like "My Recipes" is clicked, subcategories expand underneath it (e.g., 🍖 Main Course, 🍰 Desserts, 🥤 Drinks, 🥗 Appetisers, 🥐 Pastry). These subcategories act as filters for the content area.
  - Sidebar has a subtle border-right or light background to separate from content
  - Sidebar background: white or very light (#FAFAF7)
- **Main content area** (right side, fills remaining width):
  - Shows the content of whatever section is active in the sidebar
  - All existing screen content (Home, Diary, Recipes, Wishlist, Tips, Tracker) should render here
  - Generous max-width (~1100px) with centered content, proper padding

### Layout — Mobile (secondary, max-width ~768px)
- Sidebar collapses into a **hamburger menu** (☰ icon top-left)
- Clicking hamburger slides the sidebar in as an overlay from the left
- Content takes full width
- Keep it functional but desktop is the priority

### Design System (KEEP these — do not change)
- Primary: #8B9E6B
- Primary Light: #E5EDDB
- Background: #FAFAF7
- Surface: #FFFFFF
- Border: #E8E5DE
- Warm Accent: #F0EBE1
- Purple Accent: #E8DFF0
- Orange Accent: #FDECD8
- Text Primary: #2C2C2C
- Text Secondary: #555555
- Text Muted: #999999
- Rating: #D4A853
- Fonts: Playfair Display (headers), Inter (body)

### Specific Changes
1. **Remove** the phone shell wrapper (`.phone-shell`) — this is a desktop app now
2. **Remove** the bottom navigation bar — sidebar replaces it
3. **Remove** the splash screen — not needed for a desktop app
4. **Adapt the recipe grid** — on desktop, use 3-4 columns instead of 2
5. **Adapt the tracker calendar grid** — can be wider, show full month nicely
6. **Keep all existing functionality**: screen switching, recipe modal, shuffle, filters, diary day strip, wishlist, tips, tracker logging, Excel import button, FAB (reposition for desktop — maybe top-right of content area or inside the relevant section)
7. **Recipe detail modal** — on desktop, render as a centered overlay modal (not bottom sheet)
8. **Diary calendar strip** — can be a horizontal week strip at top of diary content
9. **Keep all mock data** exactly as-is — this is a UI prototype

### Sidebar Accordion Behavior
- Home: no subcategories, just navigates
- Food Diary: no subcategories (diary has its own day/filter UI)
- My Recipes: subcategories expand → 🍖 Main Course, 🍰 Desserts, 🥤 Drinks, 🥗 Appetisers, 🥐 Pastry, + "All" option
- Want to Try: subcategories expand → same categories as recipes
- Tips & Tricks: no subcategories
- Cooking Tracker: no subcategories

When a subcategory is clicked, it filters the content in the main area (same as the current chip filters, but driven from sidebar).

### Quality
- Clean, professional look — think Notion, Linear, or a modern SaaS dashboard
- Smooth transitions (sidebar hover states, active indicators, screen switching)
- The prototype should look like a real app, not a toy

## What NOT to do
- Do NOT add any external dependencies or frameworks (keep it single-file HTML/CSS/JS)
- Do NOT change the mock data
- Do NOT add backend functionality
- Do NOT remove any existing features

## When finished
1. Make sure the file opens correctly in a browser
2. Test that all navigation works (sidebar clicks, subcategory filtering, modals)
3. Summarize what changed

The output should be a single `index.html` file that replaces the current one.
