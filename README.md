# Personal Website Publications System

## Overview

This website uses a JSON-based system to manage publications automatically. 
Update the JSON file and the website rebuilds the publications page dynamically.

## File Structure

- **`publications.json`** - Contains all publication data in structured format
- **`publications.html`** - Publications page that automatically loads from JSON
- **`index.html`** - Homepage
- **`css/main.css`** - Styles

## How It Works

The `publications.html` page uses JavaScript to:
1. Fetch publication data from `publications.json`
2. Automatically sort publications by year (newest first)
3. Generate HTML for each publication
4. Bold your name ("Russin, J.") automatically
5. Add "* Equal contribution" note when `equalContribution: true`

## Adding New Publications

Simply edit `publications.json` and add a new entry. The format is:

```json
{
  "title": "Your Paper Title",
  "authors": "Russin, J., Other Author, Another Author",
  "journal": "Journal or Conference Name",
  "year": 2025,
  "url": "https://link-to-paper.com",
  "doi": "https://doi.org/optional-doi",
  "equalContribution": true
}
```

## JSON Fields

### Required Fields
- **`title`** - The paper title
- **`authors`** - Author list (just use "Russin, J." - bolding is automatic)
- **`journal`** - Journal, conference, or publication venue
- **`year`** - Publication year (used for sorting)

### Optional Fields
- **`url`** - Link to the paper/preprint
- **`doi`** - DOI link (displays as a clickable DOI icon)
- **`equalContribution`** - Set to `true` to add "* Equal contribution"

## Important Notes

1. **Your name is automatically bolded** - Don't use `<strong>` tags in the JSON
2. **Equal contribution is handled separately** - Use the `equalContribution` field instead of adding "* Equal contribution" to the journal name
3. **No build step required** - Changes to the JSON file are reflected immediately when you refresh the page
4. **Works with GitHub Pages** - No special configuration needed

## Maintenance

Just edit the JSON file when you have new publications. 
Edit the index.html to change the homepage.
