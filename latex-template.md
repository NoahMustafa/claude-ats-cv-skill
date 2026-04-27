# LaTeX CV Base Template

This is the base template the agent populates with user data.
Replace all `[PLACEHOLDER]` values. Remove any section entirely if the user has no data for it.

```latex
\documentclass[letterpaper,11pt]{article}

% ── Packages ──────────────────────────────────────────────────────────────────
\usepackage[left=0.6in, right=0.6in, top=0.6in, bottom=0.6in]{geometry}
\usepackage{lmodern}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{enumitem}
\usepackage[hidelinks]{hyperref}
\usepackage{titlesec}
\usepackage{parskip}

% ── Hyperlink colours (black = ATS safe) ──────────────────────────────────────
\hypersetup{
    colorlinks=true,
    linkcolor=black,
    urlcolor=black,
    citecolor=black
}

% ── Section formatting ────────────────────────────────────────────────────────
\titleformat{\section}
  {\large\bfseries\uppercase}
  {}{0em}{}
  [\titlerule]
\titlespacing{\section}{0pt}{8pt}{4pt}

% ── List spacing ──────────────────────────────────────────────────────────────
\setlist[itemize]{
  leftmargin=1.5em,
  itemsep=2pt,
  parsep=0pt,
  topsep=2pt
}

% ── No page numbers ───────────────────────────────────────────────────────────
\pagestyle{empty}

% ══════════════════════════════════════════════════════════════════════════════
\begin{document}
% ══════════════════════════════════════════════════════════════════════════════

% ── HEADER ────────────────────────────────────────────────────────────────────
\begin{center}
  {\LARGE \textbf{[FULL NAME]}} \\[4pt]
  \textit{[ROLE TITLE 1]} \textbf{|} \textit{[ROLE TITLE 2]} \textbf{|} \textit{[ROLE TITLE 3]} \\[4pt]
  [LOCATION] $\bullet$ [VISA STATUS IF ANY] $\bullet$ [PHONE] $\bullet$ \href{mailto:[EMAIL]}{[EMAIL]} \\
  \href{[LINKEDIN URL]}{linkedin.com/in/[USERNAME]} $\bullet$
  \href{[GITHUB URL]}{github.com/[USERNAME]} $\bullet$
  Nationality: [NATIONALITY]
\end{center}

\vspace{4pt}

% ── PROFESSIONAL SUMMARY ──────────────────────────────────────────────────────
\section{Professional Summary}

[2--4 line summary. No "I". No filler words. Include role title, key skills, and 1--2
quantified outcomes. Example: "Data Analyst with proven expertise delivering Power BI
dashboards and machine learning models across datasets exceeding 700K records. Skilled in
Python, SQL, and advanced analytics, with a track record of driving measurable outcomes,
including 92\% model accuracy and 51\% faster dashboard delivery."]

% ── WORK EXPERIENCE ───────────────────────────────────────────────────────────
\section{Work Experience}

% -- Role 1 (most recent first) ------------------------------------------------
\noindent
\textbf{[JOB TITLE]} \textbf{|} [COMPANY NAME] \textbf{|}
\textit{[CITY -- COUNTRY]} \textbf{|} \textit{[Start Mon YYYY -- End Mon YYYY / Present]}

\begin{itemize}
  \item [Bullet 1: verb + what + scale + result]
  \item [Bullet 2: verb + what + scale + result]
  \item [Bullet 3: verb + what + scale + result]
  \item [Bullet 4 (optional): verb + what + scale + result]
\end{itemize}

% -- Role 2 --------------------------------------------------------------------
\noindent
\textbf{[JOB TITLE]} \textbf{|} [COMPANY NAME] \textbf{|}
\textit{[CITY -- COUNTRY]} \textbf{|} \textit{[Start Mon YYYY -- End Mon YYYY]}

\begin{itemize}
  \item [Bullet 1]
  \item [Bullet 2]
  \item [Bullet 3]
\end{itemize}

% ── EDUCATION ─────────────────────────────────────────────────────────────────
\section{Education}

\noindent
\textbf{[DEGREE TITLE -- e.g. Bachelor of Engineering - Artificial Intelligence]} \textbf{|}
[INSTITUTION NAME] \textbf{|} \textit{[Country]} \textbf{|}
\textit{Graduated [Mon YYYY]} \textbf{|} GPA: [X.XX/4.0]

% Remove GPA line if below 3.5/4.0 or if user prefers not to include it.

% ── CERTIFICATIONS (remove section if none) ───────────────────────────────────
\section{Certifications}

\noindent
\textbf{[CERTIFICATION NAME]} -- [ISSUER] (\href{[LINK]}{Link})

% ── TECHNICAL SKILLS ──────────────────────────────────────────────────────────
\section{Technical Skills}

\begin{itemize}
  \item \textbf{Languages:} [e.g. Python, SQL]
  \item \textbf{Data Analysis:} [e.g. Power BI, EDA, KPI Development]
  \item \textbf{Excel:} [e.g. XLOOKUP, PivotTables, Data Validation]
  \item \textbf{ML:} [e.g. XGBoost, Random Forest, SVM, Regression]
  \item \textbf{Libraries:} [e.g. Scikit-learn, Pandas, Matplotlib, Seaborn]
  \item \textbf{[Other category]:} [skills]
\end{itemize}

% Skills can also be formatted as two columns using a tabular-free approach:
% Use two \begin{minipage} blocks ONLY IF page space is tight.
% Default: single flat list as above.

% ── KEY PROJECTS ──────────────────────────────────────────────────────────────
\section{Key Projects}

% -- Project 1 -----------------------------------------------------------------
\noindent
\textbf{[PROJECT NAME]} \textbf{|} \textit{[Tech Stack]} \textbf{|}
\href{[GITHUB LINK]}{GitHub} \textbf{|} \textit{[Start Mon YYYY -- End Mon YYYY]}

\begin{itemize}
  \item [Bullet 1]
  \item [Bullet 2]
  \item [Bullet 3]
\end{itemize}

% -- Project 2 -----------------------------------------------------------------
\noindent
\textbf{[PROJECT NAME]} \textbf{|} \textit{[Tech Stack]} \textbf{|}
\href{[GITHUB LINK]}{GitHub} \textbf{|} \textit{[Start Mon YYYY -- End Mon YYYY]}

\begin{itemize}
  \item [Bullet 1]
  \item [Bullet 2]
  \item [Bullet 3]
\end{itemize}

% ══════════════════════════════════════════════════════════════════════════════
\end{document}
% ══════════════════════════════════════════════════════════════════════════════
```

---

## Template Notes for the Agent

- **Remove** any section block entirely if the user has no content for it.
- **Duplicate** the role/project block pattern for each additional entry.
- **Skills layout**: default to the flat single-column list. Only use two-column layout
  (two minipages side-by-side) if the skill count exceeds 6 categories AND it's a 1-page CV.
- **Margins**: switch to `0.75in` all sides if the CV is 2 pages.
- **GPA**: only include if ≥ 3.5/4.0 and user confirms they want it shown.
- **Visa/nationality line**: only include if the user explicitly provided this info.
- **GitHub link**: only include in header if user has a public GitHub with relevant projects.
- **The three role titles in the header italic line**: use the user's own top 2–3 specialisms,
  not generic labels. E.g. `Data Analyst | Business Intelligence | Machine Learning`.
