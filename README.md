# Simple School Events Website

This is a simple Jekyll-based website to display upcoming school events and resources.
It is designed to be hosted on GitHub Pages.

## Local Development

To run this site locally, you'll need Ruby and Bundler installed.

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd <your-repo-name>
    ```

2.  **Install dependencies:**
    ```bash
    bundle install
    ```

3.  **Run the Jekyll server:**
    ```bash
    bundle exec jekyll serve
    ```

    The site will typically be available at `http://localhost:4000`.

## Content Management

-   **Events:** To add or update events, edit the `_data/events.yaml` file.
-   **Resources:** To change the resource links, edit the `index.html` file in the root directory.
