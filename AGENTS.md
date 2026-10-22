# AGENTS.md

## Resume

`resumes/resume.json` (JSON Resume format) is the origin of truth for James's resume. Everything else is built atop it:

- The generated `resumes/resume.html` and `resumes/resume.pdf` (rendered with the `short` theme via `resume/`, see `.github/workflows/deploy.yml`).
- Any tailored or role-specific resume variants, cover letters, or site copy.
- Anything quoting figures from the resume, whose raw numbers live in `resumes/data/`.

Rules:

- Make content changes (roles, dates, bullets, skills, summary) in `resumes/resume.json` first, then regenerate or derive downstream artifacts from it. Never edit generated HTML/PDF by hand.
- Downstream material must not contradict the JSON. If a variant needs a different claim, update the JSON (or the data in `resumes/data/`) first.
- Back every quantified claim with data in `resumes/data/` or a clearly stated source. Prefer the conservative figure (e.g. median commits over lines added).
- `hjhart/resume` is deprecated. Do not sync from it.
