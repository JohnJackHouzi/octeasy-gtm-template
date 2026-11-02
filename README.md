# Octeasy Reading Comfort for Google Tag Manager

This community template adds the Octeasy reading comfort button to a website through Google Tag Manager. The button opens a panel where each visitor adapts the display to the way they read: text size, a dyslexia-friendly font, line and letter spacing, high contrast, a soft dark mode, a reading ruler, a reading mask, a magnifier and read aloud. Their choices stay in their own browser.

## What the template does

- It sets `window.OcteasyConfig = { site: "<your site key>" }`.
- It loads `https://octeasy.com/widget.js`, once per page.

Nothing else. The template asks for two permissions only:

| Permission | Scope |
|---|---|
| Injects scripts | `https://octeasy.com/widget.js` only |
| Accesses global variables | `OcteasyConfig` only, read and write (required by `setInWindow`), no execute |

The widget then fetches your site's settings (button colour, position, panel language) from `https://octeasy.com/api/v1/config/<your site key>`. It sets no cookies and collects no personal data about your visitors.

## Setup

1. Copy your site key from your Octeasy dashboard (Installation page). It starts with `ot_`.
2. In Google Tag Manager, add a new tag and choose **Octeasy Reading Comfort** from the Community Template Gallery.
3. Paste your site key.
4. Choose the **Initialization - All Pages** trigger (or **All Pages**).
5. Check the button in Preview mode, then publish the container.

If the site key is missing or malformed, the template loads nothing and the tag reports a failure in Preview mode.

## What Octeasy does not do

Octeasy is a reading comfort tool. It does not make a site compliant with accessibility standards and does not replace an accessibility audit or fixes to the site's code and content.

## Support

Open an issue in this repository, or write to hello@octeasy.com. More information: https://octeasy.com

## License

Apache License 2.0, see `LICENSE`.
