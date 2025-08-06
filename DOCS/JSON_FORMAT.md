# JSON FORMAT



### 🖌️ Card-Level Metadata

Each card can have:

- id: Unique identifier
- name: Designer-defined label
- color: Background or accent color for the card itself
- tags: Array of keywords or labels for categorization


### 🧩 Content Type Summary

| Type        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `palette`   | Defines color scheme. Can be named keys (`primary`, `accent`, etc.) or array of hex codes |
| `font`      | Sets font via Google Fonts or custom link. Includes `name` and `link`       |
| `h1`–`h6`    | Headings for structure and hierarchy                                        |
| `p`         | Paragraph text for descriptions or notes                                    |
| `checkbox`  | Task item with label and checked state                                      |
| `date`      | ISO-formatted date string (e.g. `"2025-09-10"`)                             |
| `timezone`  | IANA timezone string (e.g. `"Europe/Berlin"`, `"Asia/Tokyo"`)               |




### 🎨 Designer-Friendly JSON Format
```json
{
  "cards": [
    {
      "id": "card-001",
      "name": "Brand Identity",
      "color": "#FCE4EC",
      "content": [
        {
          "type": "palette",
          "colors": {
            "primary": "#E91E63",
            "secondary": "#F8BBD0",
            "accent": "#C2185B"
          }
        },
        {
          "type": "palette",
          "colors": ["#E91E63", "#F8BBD0", "#C2185B", "#880E4F"]
        },
        {
          "type": "font",
          "name": "Playfair Display",
          "link": "https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap"
        },
        { "type": "h1", "text": "Visual Language" },
        { "type": "p", "text": "This palette evokes elegance and femininity." }
      ]
    },
    {
      "id": "card-002",
      "name": "UI Checklist",
      "color": "#E3F2FD",
      "content": [
        {
          "type": "font",
          "name": "Inter",
          "link": "https://fonts.googleapis.com/css2?family=Inter&display=swap"
        },
        { "type": "h2", "text": "Design QA" },
        { "type": "checkbox", "label": "Check contrast ratios", "checked": true },
        { "type": "checkbox", "label": "Verify spacing consistency", "checked": false }
      ]
    }
  ]
}
```

### 🧾 Finalized JSON Sample (with `tags` as metadata)
and date and timezone samples
```json
{
  "cards": [
    {
      "id": "card-006",
      "name": "Design Sprint",
      "color": "#E3F2FD",
      "tags": ["Sprint", "UX", "Team A"],
      "content": [
        {
          "type": "date",
          "value": "2025-09-10"
        },
        {
          "type": "timezone",
          "value": "Europe/Berlin"
        },
        {
          "type": "palette",
          "colors": {
            "primary": "#2196F3",
            "secondary": "#BBDEFB"
          }
        },
        {
          "type": "font",
          "name": "Nunito",
          "link": "https://fonts.googleapis.com/css2?family=Nunito&display=swap"
        },
        { "type": "h2", "text": "Goals for the Week" },
        { "type": "p", "text": "Focus on user flows and wireframes." },
        { "type": "checkbox", "label": "Sketch onboarding screens", "checked": false },
        { "type": "checkbox", "label": "Review with stakeholders", "checked": true }
      ]
    }
  ]
}
```




---

copyright: 2025 by sleet.near