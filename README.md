# Ropafadzo Mwanza — Student Profile

A responsive student profile and mini-portfolio page built with semantic HTML5, custom CSS, and Tailwind utility classes.

## Responsive Notes

- The existing profile, About, Skills, Contact, portrait, navigation, and contact form have been retained. Semantic landmarks, navigation targets, heading hierarchy, portrait alt text, and label-to-control associations are in place. The Projects link points to a brief section that transparently notes that project examples are not included yet.
- `style.css` owns the mobile-first page background, typography, box model, content cards, skills grid, and overall responsive content layout. The page starts with one column and changes to a two-column layout at the `48rem` custom breakpoint. The contact card spans both columns.
- CSS Grid is used for the main content and skills list, using `fr`, `repeat()`, `minmax()`, and `gap`. Flexbox is used for the wrapping navigation and footer alignment.
- Tailwind utility classes style the header, navigation, and contact form. Responsive `sm:` variants adjust header typography and spacing, form columns, and button/message layout.
- The styles have separate responsibilities: custom CSS controls the page-wide layout and visual foundations, while Tailwind controls the header/navigation and form presentation. Tailwind is loaded with its Play CDN because this project has no build setup; the browser needs an internet connection for those utilities.

## Testing

The page was opened in the browser preview and checked at the following CSS viewport widths:

| Viewport | Browser preview results |
| --- | --- |
| 375px mobile | Single-column page and form; no horizontal overflow |
| 768px tablet | Two-column page; contact card spans both columns; no horizontal overflow |
| 1280px desktop | Two-column page; contact card spans both columns; no horizontal overflow |

The preview also confirmed that the portrait loads and fits, Tailwind utility styles apply, every navigation link has a matching target, and all form fields have associated labels. The HTML was parsed with Python's built-in `HTMLParser`, and `git diff --check` passed.

**Still to verify manually before submission:** check the browser developer console for errors, run the page through an HTML validator, and repeat the viewport checks in the browser's device toolbar. The contact form is presentation-only and has no submission service configured.
