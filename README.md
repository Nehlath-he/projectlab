# ProjectLab — Hands-on Project Studio

A responsive, static project-learning portal designed for GitHub Pages. No build tools, framework installation, backend, or database required.

## Included in v1

- Responsive landing page with dark/light theme toggle
- Four project tracks:
  1. Data Analytics Foundation — Python, SQL, EDA and Streamlit
  2. Supervised Machine Learning
  3. Unsupervised ML & Recommendation Systems
  4. RAG Application
- Search and difficulty filters
- Project detail workspace with guided roadmap, prerequisites, deliverables, engineering/deployment steps and troubleshooting
- Google Colab and GitHub source-code link slots
- Print-friendly project guide

## Run locally

Open `index.html` in a browser. For a local web server, run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a GitHub repository, for example `projectlab`.
2. Upload `index.html`, `styles.css`, `app.js`, and this README to the repository root.
3. Open **Settings → Pages**.
4. Under Build and deployment, select **Deploy from a branch**.
5. Select `main` and `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site.

Your site URL will typically be `https://YOUR-USERNAME.github.io/projectlab/`.

## IMPORTANT: Replace the placeholder links

Open `app.js`. Each project currently uses generic placeholder links:
- `notebook`: replace with the GitHub-hosted `.ipynb` opened through Google Colab.
- `source`: replace with the relevant source-code repository URL.

Example Colab URL:

`https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO/blob/main/notebooks/01_guided.ipynb`

The buttons currently open general Colab/GitHub pages until you replace these URLs.

## Suggested repository layout for project learning materials

```text
projectlab/
├── index.html
├── styles.css
├── app.js
└── learning-materials/
    ├── data-analytics-foundation/
    │   ├── notebooks/
    │   │   ├── 01_guided.ipynb
    │   │   ├── 02_complete.ipynb
    │   │   └── 03_challenge.ipynb
    │   ├── data/
    │   ├── source-code/
    │   └── README.md
    ├── supervised-ml/
    ├── unsupervised-recommendation/
    └── rag-application/
```

For each project, aim to provide three notebook variants:
1. **Guided notebook** — explanations, runnable code, checkpoints and TODOs.
2. **Complete notebook** — full reference implementation.
3. **Challenge notebook** — independent tasks with selected TODO sections.

## Version 2 ideas

- Learner sign-in and cohort access
- Quiz and knowledge checks
- Saved progress and completion tracking
- Submission links and mentor review
- Backend/database for centralized learner progress

GitHub Pages hosts static files. Do not put API keys, passwords, private datasets, or learner personal data in this public repository. Use a backend and secure secret management if you later add authenticated learner features or live AI API calls.
