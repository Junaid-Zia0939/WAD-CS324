# InternshipSeekers website scope

## Current prototype

The prototype uses separate pages for the main student and employer flows:

1. `index.html` — homepage, how-it-works section, and an empty internship state until real listings are added.
2. `login.html` — sign-in form.
3. `register.html` — student sign-up form.
4. `employer-register.html` — employer sign-up form.
5. `profile-builder.html` — academic details, structured skills, and portfolio links.
6. `student-dashboard.html` — student profile summary and example internships.

`styles.css` contains the shared responsive styling. `matching-illustration.svg` is a local homepage image. The student journey links from the homepage to account creation/login, then to profile setup, and back to the internship list.

The prototype is static and has no backend. Student registration, profile setup, and employer registration validate inputs and create temporary profile previews in the same browser using `localStorage`. Demo passwords are hashed in the browser for the sample login flow; this is not secure authentication. Sample internship and candidate recommendations demonstrate matching, and applications are stored locally. The selected resume's filename is recorded, but its contents are not uploaded.

## Suggested future implementation sequence

1. Review the page layouts and content against the assignment wireframes.
2. Connect sign-up and login to an authentication service and validate profile form data.
3. Add a relational database for users, student profiles, skills and levels, companies, internships, required skills, source links, and review timestamps.
4. Seed company and career-page records from verified first-party sources, recording the date each link was checked.
5. Add an admin review flow before importing any externally sourced job listings.
6. Pilot a crawler only for sources that permit automated access; keep raw records separate from approved listings, deduplicate canonical URLs, and retain attribution and application links.
7. Add explainable skills matching after profile and internship data are reliable. Start with normalized skill levels and compare match quality before considering vector search.
