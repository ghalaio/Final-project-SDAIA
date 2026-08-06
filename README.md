# SDAIA Academy — Student Learning Portal

Project URL: https://ghalaio.github.io/Final-project-SDAIA/


## Project Overview

SDAIA Academy is a front-end prototype of a student learning portal for SDAIA's workshops and bootcamps. Students log in, see the workshop they've been accepted into, and work through a day-by-day curriculum with slides, labs, tests, attendance tracking, a certificate of completion, a workshop discussion board, and an AI study assistant. An instructor-mode toggle simulates how an instructor would unlock labs/tests and mark days complete, since the project has no real backend.

The prototype ships with a single mock workshop ("Applied AI & Machine Learning Bootcamp," 5 days) pre-loaded with sample content so the full experience is visible immediately without any setup.

## Project Structure

```
SDAIA_Academy.html        Single-file application — all HTML, CSS, and JavaScript
sdaia_logo_small.png      SDAIA logo, referenced by the HTML (must stay in the same folder)
README.md                 This file
```

The app is intentionally built as one self-contained HTML file (plus the logo image) so it can be opened directly in a browser with no build step, server, or dependencies.

## Technologies & AI Tools Used

- **HTML5, CSS3 (vanilla, CSS custom properties), JavaScript (vanilla, no frameworks)**
- **Browser `localStorage`** — persists student session, course progress, attendance, quiz scores, and discussion posts across reloads
- **Conic-gradient CSS + SVG** — used for the attendance pie chart and progress visuals
- **Rule-based "AI Study Buddy"** — an in-app assistant that answers questions about the current day's slide content (summarizing topics, giving quiz hints). It runs entirely client-side with simple keyword matching; it is **not** connected to a live LLM API, and is clearly labeled "demo" in the UI.
- **Claude (Anthropic)** — used as the AI coding agent to design and build the entire application within Cowork.

## Installation & Run Instructions

Project URL: https://ghalaio.github.io/Final-project-SDAIA/

No installation or build step is required.

1. Keep `SDAIA_Academy.html` and `sdaia_logo_small.png` in the same folder.
2. Double-click `SDAIA_Academy.html` (or open it via your browser's File → Open).
3. The app runs entirely client-side — no server, npm install, or internet connection is required (aside from optional slide thumbnail images loaded from an external placeholder image service).

## How to Use the Application

1. **Log in** with any name and email — no real authentication is performed.
2. **Overview / Dashboard** — see the workshop you're accepted into: description, dates, hours, location, instructor profile, your progress bar, attendance pie chart, quiz average, earned badges, and a cohort leaderboard.
3. **Enter the course workspace** — the left sidebar lists Day 1–5 with status colors (green = completed, blue = current, gray = locked), plus Certificate and Discussions.
4. **Attendance** — enter the code your instructor shares in class to mark yourself present for the current day.
5. **Day view** — each day has three tabs: Slides (always accessible once the day is unlocked), Project/Lab (locked until the instructor opens it), and Test (locked until the instructor opens it; auto-graded on submit).
6. **Instructor demo mode** — toggle "Instructor demo" in the top bar to reveal controls for opening a day's lab/test and marking the day complete, simulating the instructor side of the workflow.
7. **Certificate** — locked until all days are completed; shows a live requirements checklist, then unlocks a downloadable/printable certificate.
8. **Discussions** — post questions or tips to the whole cohort, tagged to a specific day or general, with likes and replies.
9. **AI Study Buddy** — click the floating 🤖 button to ask about today's slide topics, get a summary, or get a quiz hint.
10. **Sign out** — the 🚪 icon in the top bar clears the session so another student can log in.

## Future Improvements

- Replace `localStorage` with a real backend (auth, database, and a genuine instructor/student role separation instead of a demo toggle)
- Connect the AI Study Buddy to a real LLM API for open-ended Q&A instead of rule-based keyword matching
- Support multiple concurrent workshops per student, and a real admin/instructor dashboard for managing cohorts
- Real file upload for lab/project submissions instead of a link field
- Email/SMS notifications for attendance codes, unlocked content, and grading
- Accessibility and localization pass (Arabic language support, RTL layout)
- Automated testing (unit + end-to-end) and CI/CD pipeline

## GitHub Repository Link

https://github.com/ghalaio/Final-project-SDAIA.git

## SDAIA Academy GitHub Repository Link

https://github.com/SDAIAAcademy


