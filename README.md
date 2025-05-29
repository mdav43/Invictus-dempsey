# Jekyll Event Site

This site uses Jekyll to manage and display events. Events are grouped by month on the homepage, and each event has its own page.

## Prerequisites

*   Ruby
*   RubyGems
*   Jekyll and bundler gems:
    ```bash
    gem install jekyll bundler
    ```

## Running the Site Locally

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd <your-repo-name>
    ```
2.  **Install dependencies (if a Gemfile is added later):**
    ```bash
    bundle install
    ```
3.  **Build and serve the site:**
    ```bash
    bundle exec jekyll serve --livereload
    ```
    Open your browser to `http://localhost:4000` (or the address shown in the console).

## Managing Events

Events are managed as Markdown files in the `events` folder.

### Event File Format

Each event is a separate `.md` file in the `events` directory. The filename can be anything descriptive (e.g., `my-cool-event.md`).

The file must start with YAML frontmatter containing the following fields:

*   `title`: (String) The title of the event. This will be displayed prominently.
*   `contact`: (String) Contact email or relevant link for the event.
*   `start_date`: (Date) The start date of the event in `YYYY-MM-DD` format. This is used for sorting and grouping.
*   `description`: (String) A short description or summary of the event, displayed on the homepage listing.
*   `layout`: (String) Should always be `event`. This tells Jekyll to use the event-specific layout.

**Example Frontmatter:**

```yaml
---
title: "My Awesome Event"
contact: "organizer@example.com"
start_date: 2024-12-01
description: "A brief summary of what this awesome event is all about."
layout: event
---
```

### Event Content

Below the frontmatter, you can write the main content of the event using Markdown. This content will appear on the individual event's page.

**Example `events/my-awesome-event.md`:**

```markdown
---
title: "My Awesome Event"
contact: "organizer@example.com"
start_date: 2024-12-01
description: "A brief summary of what this awesome event is all about."
layout: event
---

## Welcome to My Awesome Event!

Detailed information about the event goes here. You can use standard Markdown formatting:

*   Lists
*   **Bold text**
*   *Italic text*
*   [Links](https://example.com)

### Schedule
- 10:00 AM: Doors Open
- 11:00 AM: Keynote Speech
- 01:00 PM: Workshops
```

### Adding a New Event

1.  Create a new `.md` file in the `events` folder (e.g., `events/new-years-gala.md`).
2.  Add the required YAML frontmatter (see "Event File Format" above).
3.  Write the event details in Markdown below the frontmatter.
4.  If you are running the local server (`jekyll serve`), Jekyll should automatically detect the new event and rebuild the site. You might need to refresh your browser.

## Structure

*   `_config.yml`: Jekyll site configuration, including the `events` collection setup.
*   `index.html`: The homepage, lists events.
*   `events/`: Contains all event Markdown files.
*   `_layouts/`: HTML layouts.
    *   `default.html`: Base layout for all pages.
    *   `event.html`: Layout for individual event pages.
*   `assets/css/style.css`: Main stylesheet.
```
