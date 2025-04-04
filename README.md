# Academic Personal Homepage

A modern, responsive academic personal website template with clean design and JSON-powered dynamic content loading. This template is perfect for researchers, professors, and PhD students looking to showcase their academic achievements.


## Features

- 📱 Fully responsive design that works seamlessly on all devices
- 🎨 Clean, modern UI with intuitive navigation
- 📊 JSON-powered content for easy updates (publications and news)
- 🔍 Publications section with filtering capability (All/Preprints/Accepted/First Author)
- 📰 News section with "View All" capability 
- 🌟 Interactive elements with smooth transitions
- 🔗 Social media and contact integration

## Table of Contents

1. [Getting Started](#getting-started)
2. [Project Structure](#project-structure)
3. [Customization Guide](#customization-guide)
   - [Basic Information](#basic-information)
   - [Profile Photo](#profile-photo)
   - [Education](#education)
   - [Research Interests](#research-interests)
   - [Publications](#publications)
   - [News](#news)
   - [Honors & Awards](#honors--awards)
   - [Services](#services)
   - [Contact Information](#contact-information)
   - [Social Media Links](#social-media-links)
4. [Advanced Customization](#advanced-customization)
   - [Color Scheme](#color-scheme)
   - [Font Changes](#font-changes)
   - [Section Ordering](#section-ordering)
5. [Deployment](#deployment)
6. [License](#license)

## Getting Started

To use this template for your own academic website:

1. Clone this repository:
```bash
git clone https://github.com/yourusername/academic-homepage.git
```

2. Navigate to the project directory:
```bash
cd academic-homepage
```

3. Open the files in your preferred code editor and begin customizing according to the guide below.

4. Test your changes by opening `index.html` in a web browser.

## Project Structure

```
├── index.html              # Main homepage file
├── styles.css              # CSS styling
├── script.js               # JavaScript functionality
├── assets/                 # Images and other static assets
│   ├── profile.jpg         # Your profile photo
│   ├── cityu-logo.jpeg     # University logo examples
│   └── bit-logo.png        # University logo examples
├── data/                   # JSON data files
│   ├── news.json           # News items data
│   └── publications.json   # Publications data
└── pages/                  # Additional pages
    └── all-news.html       # Page displaying all news items
```

## Customization Guide

### Basic Information

Edit the `index.html` file to update your basic information:

1. **Name**: Replace "SENKANG 'FOREST' HU 🍀" with your name in the header section.
2. **Title/Affiliation**: Update the subtitle with your position, university, and lab affiliations.
3. **Short Bio**: Replace the text in the Biography section with your own introduction.

Example:
```html
<h1>YOUR NAME</h1>
<p class="subtitle">PhD Student @ Your University</p>
```

### Profile Photo

1. Replace the `profile.jpg` in the `assets` folder with your own photo.
2. Make sure your photo is properly cropped to a square or similar aspect ratio for best results.
3. The recommended size is 500x500 pixels.

### Education

Update the education timeline in `index.html`:

1. For each educational experience, modify the following template:
```html
<div class="timeline-item">
    <div class="timeline-marker"></div>
    <div class="timeline-content">
        <div class="edu-content-wrapper">
            <div class="edu-text">
                <h3>Degree @ University Name</h3>
                <p class="timeline-date">Start Date - End Date</p>
                <p>Major/Department</p>
                <p>Additional information</p>
            </div>
            <div class="school-logo">
                <img src="assets/university-logo.png" alt="University Name" class="edu-logo">
            </div>
        </div>
    </div>
</div>
```

2. Add your university logos to the `assets` folder and update the image paths.

### Research Interests

Modify the research interests section in `index.html`:

1. Each research area follows this structure:
```html
<div class="research-area">
    <i class="fas fa-icon-name"></i> <!-- Choose an appropriate Font Awesome icon -->
    <h3>Research Area Title</h3>
    <ul class="research-list">
        <li><strong>Subfield:</strong> Description of your work in this subfield.</li>
        <!-- Add more subfields as needed -->
    </ul>
</div>
```

2. You can find suitable Font Awesome icons at [Font Awesome](https://fontawesome.com/icons).

### Publications

Publications are loaded dynamically from `data/publications.json`:

1. Edit this JSON file to include your publications.
2. Each publication should follow this structure:
```json
{
  "number": 1,
  "title": "Your Publication Title",
  "authors": "<strong><u>Your Name</u></strong>, Co-author One, Co-author Two",
  "type": "preprint",  // or "accepted"
  "isFirstAuthor": true,  // or false
  "venue": "Conference or Journal Name",  // optional, for accepted papers
  "tags": [
    {
      "text": "Tag Label",
      "class": "tag-class",
      "link": "https://link-to-paper.com"  // optional
    }
  ]
}
```

3. Highlight your name using `<strong>` and `<u>` tags.
4. Set `isFirstAuthor` to true for papers where you are the first author or have equal contribution.

### News

News items are loaded from `data/news.json`:

1. Edit this file to include your news items:
```json
{
  "date": "Month YYYY",
  "title": "News Title",
  "content": "News content description",
  "links": [
    {
      "text": "Link Text",
      "url": "https://link-url.com"
    }
  ]
}
```

2. You can include HTML in the title and content fields if needed.
3. The most recent news items will appear on the homepage, with all items available on the all-news page.

### Honors & Awards

Update the honors and awards section in `index.html`:

```html
<div class="honor-item">
    <div class="honor-year"><span class="year-highlight">YYYY</span></div>
    <div class="honor-content">
        <h3>Award Name</h3>
        <p>Awarding Organization</p>
        <p>Additional information about the award</p>
    </div>
</div>
```

### Services

Modify the services section in `index.html` to list your professional services:

```html
<div class="service-category">
    <h3>Category Title</h3>
    <ul class="service-list">
        <li>Service Item 1</li>
        <li>Service Item 2</li>
        <!-- Add more items as needed -->
    </ul>
</div>
```

### Contact Information

Update your contact information in the header and location sections:

1. **Email**: Replace the email address in the contact links.
2. **Address**: Update your office address in the location section.
3. **Map**: Replace the Google Maps iframe with your location coordinates.

### Social Media Links

The template includes social media icon links in the header. Modify as needed:

```html
<div class="contact-info">
    <p><a href="mailto:your.email@example.com"><i class="fas fa-envelope"></i></a></p>
    <p><a href="assets/wechat.jpg" target="_blank"><i class="fab fa-weixin"></i></a></p>
    <p><a href="https://scholar.google.com/citations?user=YOUR_ID" target="_blank"><i class="fas fa-graduation-cap"></i></a></p>
    <p><a href="https://www.linkedin.com/in/your-profile/" target="_blank"><i class="fab fa-linkedin"></i></a></p>
</div>
```

## Advanced Customization

### Color Scheme

To change the color scheme, edit the CSS variables in the `styles.css` file:

```css
:root {
    --primary-color: #0066cc; /* Main accent color */
    --secondary-color: #f8f9fa; /* Background color for sections */
    --text-color: #333; /* Main text color */
    --light-text: #757575; /* Secondary text color */
    --border-color: #e0e0e0; /* Border color */
}
```

### Font Changes

To change fonts:

1. Update the Google Fonts link in the `<head>` section of your HTML files:
```html
<link href="https://fonts.googleapis.com/css2?family=YourChosenFont:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

2. Update the font-family in the `styles.css` file:
```css
body {
    font-family: 'YourChosenFont', sans-serif;
}
```

### Section Ordering

To reorder sections:

1. Rearrange the `<section>` elements in the `index.html` file.
2. Update the navigation links accordingly to maintain proper scrolling.

## Deployment

To deploy your website:

1. **GitHub Pages**:
   - Push your repository to GitHub
   - Enable GitHub Pages in the repository settings
   - Your site will be available at `https://yourusername.github.io/repository-name`

2. **Netlify**:
   - Create an account on [Netlify](https://www.netlify.com/)
   - Drag and drop your project folder to deploy
   - Your site will be given a Netlify subdomain with option to use a custom domain

3. **University Web Space**:
   - Many universities provide web hosting for faculty and students
   - Contact your university's IT services for information on how to upload your files

## License

This project is available under the MIT License. You are free to use, modify, and distribute this template for both personal and commercial purposes.
