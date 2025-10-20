# AI Prompts to Kickstart Your Charity: Water Landing Page

## Basic Page Structure
Create a simple HTML layout for a nonprofit landing page with sections for a hero, a story, and a call-to-action.

## Style with Brand Identity
Write CSS using a color palette of [insert your brand colors] and fonts that feel [insert tone, e.g., bold and modern].

## Build the Hero Section
Create a hero section with a centered headline, subheadline, and full-width background image that grabs attention.

## Add Story + CTA Sections
Add a section for a real-world impact story with text and an image, and a donation section with a bold 'Donate Now' button.

## Make It Responsive
Add CSS media queries so this landing page looks good on both desktop and mobile devices. Add code comments to help explain why we use media queries.

## How to upload and use background images for the landing page:

1. Add the image file to the project
   - VS Code: open the Explorer and drag & drop the image into the img/ folder.
   - GitHub web: go to the repo → Add file → Upload files → choose image → Commit.
   - Terminal: use curl/wget to download or scp to copy:
     - curl -L -o img/hero-background.jpg "https://example.com/path/to/image.jpg"
     - scp user@host:/path/to/image.jpg img/

2. Reference the image in your CSS (relative path recommended):
   - Example:
     ```css
     /* filepath: styles.css */
     .hero {
       background-image: url('img/hero-background.jpg');
       background-size: cover;
       background-position: center;
       background-repeat: no-repeat;
       background-color: #003366; /* fallback color */
     }
     ```

3. Improve readability with an overlay:
   - Example:
     ```css
     .hero::before {
       content: "";
       position: absolute;
       inset: 0;
       background: rgba(0,0,0,0.45); /* dark overlay */
       pointer-events: none;
       border-radius: inherit;
     }
     ```

4. Best practices
   - Resize/optimize images (1–2MB max; prefer 1000–2000px wide for hero).
   - Use web-friendly formats (webp or jpeg).
   - Commit and push images to your repo so the deployed site can access them.