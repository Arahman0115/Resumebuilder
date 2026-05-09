# Resume Building System

## Purpose
This repo stores three role-specific base resumes and generates tailored resumes for individual job applications. When you provide a job description, Claude reads all three base resumes, identifies the most relevant content, and produces a customized resume saved alongside the job description.

---

## Folder Structure

```
fakeresumefiles/
├── INSTRUCTIONS.md              ← this file
├── base-resumes/
│   ├── data-analyst/            ← your Data Analyst resume (any format: .docx, .pdf, .txt)
│   ├── business-analyst/        ← your Business Analyst resume
│   └── consultant/              ← your Consultant resume
└── applications/
    └── <company>-<role>-<YYYY-MM-DD>/
        ├── job-description.txt  ← paste the full job posting here
        └── tailored-resume.txt  ← Claude-generated tailored resume
```

---

## Setup (one-time)
Add your base resumes to the appropriate folders under `base-resumes/`. Any file format works — plain text (`.txt`) gives Claude the cleanest read. Name the file whatever you like (e.g., `resume.txt`, `ahnaf-data-analyst.txt`).

---

## Generating a Tailored Resume

1. Open this project in Claude Code (or paste the job description into the chat).
2. Tell Claude: **"Here is a job description, please generate a tailored resume."** Then paste or attach the job posting.
3. Claude will:
   - Read all three base resumes from `base-resumes/`
   - Use the job description to select and reframe the most relevant experience, skills, and bullet points
   - Create a new folder under `applications/<company>-<role>-<YYYY-MM-DD>/`
   - Save `job-description.txt` and `tailored-resume.txt` inside it

---

## Tips
- Keep base resumes comprehensive — include everything. Claude will select what's most relevant per role.
- Update base resumes whenever your experience changes; all future tailored resumes will reflect the update automatically.
- If you want a specific format or length for the tailored resume, say so when you prompt Claude (e.g., "keep it to one page" or "use a skills-first format").
