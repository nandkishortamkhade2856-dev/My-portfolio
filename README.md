# Nandkishor Rahul Tamkhade — Portfolio

A personal portfolio built with React and Vite. Static output, no backend, no API keys.

## Run locally

```bash
npm install
npm run dev        # development server (http://localhost:5173)
npm run build      # production build into /dist
npm run preview    # serve the production build locally
```

Requires Node 18 or newer.

## Editing your content

Almost everything lives in **`src/data/siteData.js`**:

| What | Where in the file |
| --- | --- |
| Name, title, headline, email, GitHub, LinkedIn, phone | `profile` |
| About paragraphs | `about` |
| Skills | `skillGroups` (add a group for frameworks/tools) |
| Projects | `projects` |
| Education, certifications, achievements, milestones | `education` |
| Resume PDF | `resume.file` |

### Things left for you to fill in
Anything marked `TODO` or set to `null` / `[]` shows as "to be added" on the site rather than a made-up value:

- Each project's **contribution**, **stack** (except Project D's tools), **repo** and **demo** links, and **status**
- **Graduation year**
- **Phone** (`profile.phone`, hidden while `null`)
- **Certifications, achievements, milestones**

### Adding your resume
1. Put your PDF in `public/`, e.g. `public/resume.pdf`.
2. In `siteData.js` set `resume.file = './resume.pdf'`.

The button switches from "Resume coming soon" to a real download automatically.

### Changing the photo
Replace `public/images/profile-720.jpg` (and `.webp`) and `profile.jpg`. If the face sits differently in the frame, adjust `profile.photo.position` (CSS `object-position`). Your unedited original is kept in `originals/` and is not published.

### Project visuals
The four project visuals are abstract **concept diagrams**, labelled as such. To use real screenshots later, add them to `public/images/` and replace `ProjectVisual` in `src/components/Projects.jsx` for that project.

## Deploying (when you are ready)

`npm run build` produces `dist/`, which works on any static host (the Vite `base` is relative).

- **Netlify / Vercel:** import the GitHub repo; build command `npm run build`, output directory `dist`.
- **GitHub Pages:** push the repo, build locally, and publish the contents of `dist/` (or use a Pages workflow that runs `npm run build`).

## Notes

- There is deliberately **no contact form**: a form needs a real submission service. The email link opens the visitor's mail app.
- Motion uses transforms and opacity, and is disabled when the visitor prefers reduced motion.
- Fonts (Fraunces, Inter, JetBrains Mono) load from Google Fonts. Self-host them if you want zero third-party requests.
