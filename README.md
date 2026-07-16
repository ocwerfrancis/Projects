# Login Form

A responsive, glassmorphism-style login form built with plain HTML and CSS. Features a frosted-glass card that sits over a full-page background image, letting the scenery show through while keeping all form elements clearly readable.

## Preview

The form includes:
- Social login options (Google, Apple)
- An "or" divider
- Email and password fields with a "Forgot Password" link
- A styled submit button
- A sign-up prompt

## Features

- **Glassmorphism design** — semi-transparent form background with `backdrop-filter: blur()` so the page background image shows through
- **Full-page background image** — covers the entire viewport using `background-size: cover`
- **Social login buttons** — Google and Apple options with icons, easily extendable to more providers
- **Responsive layout** — form scales to fit smaller screens using `max-width` and flexible sizing
- **Custom styling** — Montserrat font (via Google Fonts), rounded corners, subtle hover states, and a teal color scheme

## Project Structure

```
Login Form/
├── index.html
├── style.css
├── logos/
│   ├── google.png
│   └── apple.png
└── └── background.jpg
```

## Setup

1. Clone or download this project.
2. Make sure your image assets are in place:
   - Provider icons go in `logos/` (e.g. `google.png`, `apple.png`)
   - Your background photo goes in `images/` and is referenced in `style.css` under `background-image`
3. Open `index.html` directly in a browser, or serve it with a local server (recommended, since some browsers restrict local file paths):
   ```
   python -m http.server
   ```
   Then visit `http://localhost:8000`.

## Customization

- **Background image**: update the `url()` path in the `body` rule in `style.css`.
- **Transparency level**: adjust the `rgba()` alpha value and `backdrop-filter: blur()` amount on `.login-form` to make the card more or less see-through.
- **Colors**: the primary accent color (`#007A74`) is used for the button, links, and focus states — update it in `style.css` to rebrand.
- **Additional login providers**: duplicate an `.option` block in the HTML and add a matching logo to `logos/`.

## Notes

- Image paths should be relative (no leading `/`) when opening the file directly from disk, so they resolve correctly regardless of where the project folder lives.
- For best results, use a high-resolution background image (1920px+ on the longer side) to avoid blurring when scaled with `background-size: cover`.

## License

Free to use and modify for personal or commercial projects.
