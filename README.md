# SRMS – Student Result Management System (Dashboard UI)

> Developed by **Mahisagarsoft**

A responsive student dashboard built with plain HTML, CSS and JavaScript in a single file. It works on phones, tablets, laptops and large monitors, and needs no build step or backend.

## Quick start

1. Put `index.html` in a folder.
2. Open it in any modern browser (double-click it, or use a local server).

```bash
# optional: serve locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is only needed to load the Poppins font from Google Fonts. Without it, the page falls back to the system font.

## Features

| Area | What works |
|------|-----------|
| **Navigation** | Sidebar with 11 pages (Dashboard, Profile, Courses, Results, Attendance, Exams, Timetable, Notice Board, Academic Calendar, Downloads, Feedback). Uses URL hashes, so the back button and refresh work. |
| **Dashboard** | Welcome banner, stat cards, recent results, notices, mini calendar, quick access tiles, performance donut. Cards and links open the matching page. |
| **Search** | Live search across pages, courses and notices. Press `/` to focus it. |
| **Notifications** | Bell with unread count and dropdown. Clicking a notice marks it read; the Notice Board has "Mark all as read". |
| **Calendar** | Previous/next month navigation, today highlight, event markers. |
| **Results** | Filter by exam type and download as CSV. |
| **Downloads** | Marksheet, timetable, exam schedule and attendance report as CSV files. |
| **Feedback** | Star rating and message form with validation and a confirmation toast. |
| **Logout** | Confirm dialog and a logged-out screen (demo only). |

## Responsive behaviour

- **Phones (up to 760px):** the sidebar becomes a slide-in menu with a backdrop, and search moves to its own row. Stat cards show two per row, and tables scroll sideways.
- **Small laptops (about 1024–1280px):** compact sidebar and stat cards, with some grids reflowing to two or three columns.
- **Laptops and desktops:** the full layout. At 1600px and above, the content is centered with a maximum width of 1560px.
- **Short screens (760px tall or less):** tighter sidebar spacing so every item stays visible.

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `/` | Focus the search box |
| `Esc` | Close dropdowns, the mobile menu or the logout dialog |
| `Tab` / `Enter` | Move between and activate menu items, cards and buttons |

## Customising the data

All sample content lives at the top of the `<script>` block in `index.html`:

| Constant | Contents |
|----------|----------|
| `RESULTS` | Subject, exam type, grade, score, date |
| `NOTICES` | Title, description, date, read status |
| `COURSES` | Code, name, faculty, credits, attendance |
| `EXAMS` | Subject, date, time, venue |
| `TT` | Weekly timetable rows |
| `EVENTS` | Calendar events keyed by `YYYY-MM-DD` |

To change the student's name, edit the welcome text in `VIEWS.dashboard`, the top bar, and `VIEWS.profile`. The "today" date is fixed to 20 May 2024 to match the design. Change it in `calHTML()` if you want the real current date.

## Project structure

```
.
├── index.html   # markup, styles and scripts (everything)
└── README.md
```

## Limitations

- Data is hard-coded sample content and nothing is saved between visits.
- Login and logout are visual demos, not real authentication.
- Icons are emoji. Swap in an icon library (Font Awesome, Lucide) if you want an exact match to the original design.

## Ideas for next steps

- Real login page and authentication
- Backend or database (Node/Express, PHP/MySQL, Firebase) for live results
- Dark mode
- PDF marksheet export
- Charts for semester-wise CGPA trends

## Credits

Designed and developed by **Mahisagarsoft**.

## License

Free to use and modify for learning and personal projects. Please keep the Mahisagarsoft credit in the footer.
# SRMS
