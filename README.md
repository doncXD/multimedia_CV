# Multimedia CV website: Dylan Doncaster

**Live site:** https://doncXD.github.io/multimedia_CV/

The CV to download is a generic one to avoid personal data on internet

**Figma design:** https://www.figma.com/design/3heakflUNVsSxkzJ4ujUZv/Untitled?node-id=0-1&t=RmhDviKaVfSFujjG-0
(If teacher needs edit access I can modify it without any problem. Only reason is to avoid outside people messing around with the design)

## Project Analysis:

### User profile:

| | |
|---|---|
| **Name** | John Smith |
| **Age** | 34 |
| **Role** | Technical Recruiter at a mid-size embedded systems and defense-tech company in Barcelona |
| **Tech comfort** | Medium. Understands the stack well enough to screen candidates, but is not an engineer. |
| **Devices** | Laptop at the office (mostly), phone when commuting or between meetings |

**Background.** John screens around 40 candidates for each internship or junior opening. He reads CVs in batches and decides in roughly 30 seconds whether a candidate goes to the "maybe" pile. When a candidate links a personal website, he opens it only if the link looks professional, and she leaves quickly if the page is slow or cluttered.

**Goals**
- Quickly understand who the candidate is and what they are studying.
- Verify technical skills with evidence (real projects, not just a list of keywords).
- Find contact details and a downloadable CV without hunting for them.
- Pass promising candidates to the engineering team with a link they can inspect.

**Frustrations**
- Walls of text and vague claims such as "passionate team player".
- Skill lists with no proof behind them.
- Pages that break on mobile or take too long to load.
- Having to search for an email address or the repositories.

**What he expects to find**
1. A clear one-line summary of the candidate and their specialization.
2. A short list of relevant technologies.
3. Two or three projects with a short description and a link to the code.
4. Education and any experience, in reverse chronological order.
5. An obvious way to contact the candidate.

**Quote:** *"Show me what you've built, and make it easy to reach you."*


### 1.2 Information Architecture

The site is a single page, so the architecture is the order of the sections and how users move between them. The order follows John's reading pattern: he decides quickly, so the most decisive information comes first and the detail follows for anyone who keeps reading.

1. **Intro.** Name, title ("Computer Engineering student"), a one-sentence value statement, and two calls to action: *View projects* and *Contact*. This answers "who is this?" within the first screen. 
2. **About.** A short paragraph (3-4 sentences) covering studies, interests and the specialization the candidate is aiming for, such as embedded systems and signal processing. It adds personality without taking much space.
3. **Skills.** Grouped by category (Languages, Systems and Embedded, Tools, Spoken languages) instead of one long list. Grouping makes it quick to scan and shows that the candidate understands how the technologies relate.
4. **Projects.** The core of the page. Each project is a card with a title, a one-line description, the technologies used and a link to its repository. It comes right after the skills so that every claim above is immediately backed by evidence.
5. **Education.** The degree at the Universitat de Girona, with the most relevant courses (operating systems, computer architecture, software engineering).
6. **Experience.** Work, volunteering or other relevant activity, in reverse chronological order. It sits below the projects because, for a student, projects carry more weight than jobs.
7. **Contact.** Email, GitHub, LinkedIn and a button to download the PDF CV, placed at the end as the natural next step after reading.

A fix navigation bar with links to every section lets users jump directly to where they want. The contact section is also reachable from the intro button, so a recruiter who has already decided never needs to scroll to the bottom.

### 1.3 Visual Design

The goal is a visual identity that feels technical and clean without looking like a generic template. It should say "engineer" and still be pleasant to read.

**Colour palette.** A dark navy base (`#0B132B`) with an off-white text colour (`#B3B3B3`), which reduces eye strain and gives a modern, technical look. A single accent colour, electric teal (`#1DE9B6`), is used for links, buttons and highlights, so the user's attention always goes to interactive elements. A muted grey-blue (`#8892B0`) is used for secondary text. All text and background combinations were checked against WCAG AA contrast ratios.

**Typography.** Two Fonts: **Inter** is used for headings and body text because it is highly legible on screens at every size. **JetBrains Mono** is used for small details such as section labels, tags and technology chips (a subtle way to reference coding). If the browser doesnt have them it loads the system sans-serif and monospace, which on a macOS is San Francisco and SF Mono, and on Windows Segoe UI and Cascadia Code, on Linux whatever is installed. The page looks slightly different per device but it loads faster and has no external dependency...

**Layout.** A centred layout with a maximum width of about 1000px keeps line lengths comfortable. Sections are separated by generous whitespace instead of heavy dividers. Projects and skills use a CSS Grid of cards that collapses from three columns to two to one as the screen narrows. The design is mobile-friendly (it uses rem (Root EM) that multiplies the root font size by that. Keeping everythin proportional).

**Inspiration.** Developer portfolios such as [Brittany Chiang's site](https://brittanychiang.com) (side navigation, restrained palette) and several minimalist dark-theme portfolios found on Awwwards and GitHub. The idea taken from them is that restraint and strong typography communicate competence better than heavy decoration.

**Interaction.** Smooth scrolling between anchors, and no animation that delays access to the content.
(the radar is not interactive, it was a subtle decoration used to make the page more attractive).


----

## 2. Technologies

| Technology | Why |
|---|---|
| **HTML5** | Semantic structure (`header`, `nav`, `main`, `section`, `footer`) for accessibility and clarity. |
| **CSS3** | Flexbox and Grid for layout, CSS custom properties for the palette, media queries for responsiveness. |
| **GitHub Pages** | Free hosting directly from the repository. |
| **Figma** | Design prototype before implementation. |

No CSS framework (Bootstrap, Tailwind) was used. The layout is simple enough to write by hand, and doing so keeps the code small, readable and fully under my control.

AI was used to "vibecode" the svg radar that fitted the colour palette to give some "life" to the page. An alternative would have been an open source gif-svg that would have not fitted with the colour choices.

---

## 3. Project Structure

```
.
├── index.html
├── css/
│   └── style.css
├── assets/
│   ├── img/
│   └── CV.pdf
└── README.md
```

---

## 5. Author

**Dylan Doncaster**, Software-Computer Engineering, Universitat de Girona
GitHub: [@doncXD](https://github.com/doncXD)
