# Ghost CMS Widget for Scriptable

A custom iOS widget built using [Scriptable](https://scriptable.app) that displays the total number of members from your [Ghost](https://github.com/TryGhost) blog. The widget supports small, medium, and large sizes, with graphs showing member growth over the last 30 days for medium and large sizes. More features to come.

## Features

✨ Display total members count.
✨ Graph showing member growth over the last 30 days for medium and large widgets.
✨ Customizable with widget parameters: base URL, API key, and cache duration.
✨ Automatic light/dark mode support with appropriate Ghost logo.

## Requirements

- iOS device with the Scriptable app.
- Admin API key from a Ghost instance.

## Installation

1. Download or copy the `ghost.js` script.
2. Open the Scriptable app and create a new script, pasting the code from `ghost.js`.
3. Repeat the first two steps with `crypto-min.js`.
4. Configure the widget (see below).
5. Add the Scriptable widget to your iOS home screen, tap "edit" and choose `ghost`.

## Configuration

To configure the widget, set the following parameters in the Configuration section of the `ghost.js` script:

- `baseUrl`: The Ghost instance URL (e.g., `https://yourghostsite.com`).
- `adminApiKey`: The Ghost Admin API key (navigate to Settings -> Integrations -> Add Custom Integration to generate a new key in Ghost).
- `cacheDuration`: Cache duration in milliseconds.

These parameters can be overwritten in the widget settings on your iOS home screen. 

E.g. if you'd like to have a widget for another instance than the default one, you could configure it using the following parameters: `baseUrl=https://anotherghostsite.com,adminApiKey=apikey`.

⚠️ The `cacheDuration` parameter assumes a value in minutes when set via the widget settings.

## Widget Layouts

- **Small Widget**: Displays the total members count.
- **Medium Widget**: Displays the total members count with a graph of members over the last 30 days.
- **Large Widget**: Displays the total members count with an extended graph of members over the last 30 days.

## Caching
The widget caches data to reduce the number of API calls. It stores member data locally in iCloud and refreshes the cache based on the configured `cacheDuration`. The default cache duration is 24 hours.

---

Enjoy your fully customizable Ghost members count widget! 🎉
