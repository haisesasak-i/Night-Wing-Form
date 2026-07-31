# NightWing 🦇

A stylish, superhero-themed sign-up page inspired by Nightwing. Built with semantic HTML5 and modern CSS (custom properties, nesting, `backdrop-filter`), featuring a responsive split-screen layout, glassmorphism form card, and real-time password validation.

## ✨ Features

- **Split-screen layout** — a full-bleed hero image on the left with photo attribution, and a sign-up form on the right.
- **Glassmorphism form card** — semi-transparent background with `backdrop-filter: blur()` over a solid blue backdrop.
- **Responsive typography** — headings and labels scale fluidly with `clamp()` so the layout adapts across screen sizes.
- **Client-side validation**
  - Required fields for first name, last name, email, city, and password.
  - Password fields enforce (via regex `pattern`) a minimum of 8 characters, including at least one uppercase letter, one lowercase letter, one number, and one special character (`@$!%*?&`).
  - Visual feedback: fields glow **green** when valid and **red** when invalid, only after the user has typed something (`:not(:placeholder-shown)`).
- **Accessible form structure** — every input is paired with a `<label>`, uses correct `autocomplete` and `inputmode` attributes, and includes helpful `placeholder` and `title` (tooltip) text.
- **Custom "Turf" selector** — a dropdown for the user's city (Gotham City, Bludhaven, Metropolis, Star City, Central City, or Other).
- **Google Fonts integration** — uses the [Poppins](https://fonts.google.com/specimen/Poppins) typeface with `preconnect` for faster font loading.

## 📁 Project Structure

```
NightWing/
├── index.html              # Main sign-up page markup
├── stylesheets/
│   ├── style.css            # Core styles (layout, theme, form design)
│   └── reset.css            # CSS reset
├── images/
│   ├── NightWing.jpg        # Hero background image
│   └── logo.png             # NightWing logo
└── submit.php               # Form submission handler (backend, not included)
```

## 🛠️ Tech Stack

- **HTML5** — semantic, accessible markup
- **CSS3** — custom properties (variables), nesting, flexbox, `clamp()`, `backdrop-filter`
- **Google Fonts** — Poppins
- **PHP** — form submission endpoint (`submit.php`, to be implemented)

## 🚀 Getting Started

1. Clone or download this repository.
2. Make sure the following assets exist:
   - `images/NightWing.jpg` — background photo
   - `images/logo.png` — logo image
   - `stylesheets/style.css` and `stylesheets/reset.css`
3. Open `index.html` in a browser to preview the page.
4. To handle real form submissions, implement `submit.php` (or swap the `action`/`method` on the `<form>` for your own backend/API).

> **Note:** The included `<script>` currently calls `event.preventDefault()` on submit, so the form won't actually POST anywhere yet — this is meant as a placeholder while the page is in development. Remove or update it once `submit.php` (or another endpoint) is ready.

## 🎨 Customization

Most of the visual design is controlled through CSS custom properties defined at the top of `style.css` (`:root`), including:

| Variable | Purpose |
|---|---|
| `--background-color-body` | Page background color |
| `--left-image-width` / `--left-image-height` | Size of the hero image panel |
| `--font-family` | Global font stack |
| `--font-size-header-main` / `--font-size-header-sub` | Fluid heading sizes |
| `--border-radius` | Corner rounding for inputs |

Tweak these values to reskin the page without touching the layout rules.

## 🔒 Form Validation Rules

| Field | Rule |
|---|---|
| First / Last Name | Required, free text |
| Email | Required, valid email format |
| Turf (City) | Required, must select an option |
| Password / Confirm Password | Required, min 8 characters, must include uppercase, lowercase, number, and special character (`@$!%*?&`) |

## 📸 Credits

- Background photo by [Edytka](https://www.pinterest.com/nightwingsavedmylife/) via [Pinterest](https://www.pinterest.com/pin/769623023864892795/).
- Nightwing is a DC Comics character — this project is an unofficial fan-made design and is not affiliated with or endorsed by DC Comics.

## 📄 License

This project is intended for personal/educational use. Update this section with your preferred license (e.g., MIT) if you plan to distribute it.