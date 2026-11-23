# Awesome-Data-Science-Presentation-Notebook-VIZ

## Top Data Science Presentation & Notebook Viz Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Reactive Notebooks, Interactive Data Apps & Publication-Quality Reporting*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Science Presentation & Notebook Visualization**. These tools help data scientists turn exploratory notebooks into shareable dashboards, interactive web apps, and presentation-ready reports—covering everything from cloud-hosted notebook environments to open-source frameworks that render live Jupyter notebooks as standalone applications.

**Examples** include Marimo, Streamlit, Hex, Deepnote, Observable, Quarto, Voila, and JupyterLab (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted data apps, open-source notebook publishing, and community-driven visualization—ideal for data teams seeking reproducibility, avoiding per-seat SaaS pricing, and owning their presentation pipeline end to end. The open-source landscape is genuinely functional: **Marimo** guarantees reproducible notebooks with no hidden state , **Streamlit** turns Python scripts into shareable data apps in minutes , and **Quarto** produces publication-quality documents from Markdown and notebooks .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global data science and machine learning platform market is estimated at ~$100B–$130B+ (projected to exceed $500B by the 2030s at an ~18–25% CAGR), driven by enterprise generative AI mandates and demand for interactive data products. The sector is **moderately to highly fragmented** rather than a winner-take-all monopoly: while hyperscalers (Google Cloud, AWS, Azure) and unified data platforms (Snowflake, Databricks) command enterprise infrastructure, specialized vendors and open-source ecosystems (Hex, Deepnote, Observable, Marimo) thrive by solving specific developer ergonomics, reactive compute, and collaborative presentation workflows.

## SaaS/Hosted Platforms

| Platform | Company Size (Valuation / Revenue) | Starting Paid Tier Pricing | Free Tier Limits | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Google Colab](https://colab.research.google.com/)** | **Parent: Alphabet / Google** (~$2.1T+ Market Cap, $350B+ Annual Revenue) | **$9.99/month** (Colab Pro, 100 compute units; or $9.99 Pay-As-You-Go) | **Free forever**: Limited shared compute (T4 GPU subject to dynamic availability and quotas); max 12h runtime; idle timeouts after short inactivity. | Cloud-hosted Jupyter environment for ML experimentation, quick prototyping, and GPU/TPU compute. |
| **[Streamlit Community Cloud](https://streamlit.io/cloud)** | **Parent: Snowflake** (~$800M Acquisition; Snowflake ~$50B+ Market Cap, $3.5B+ Annual Revenue) | **Free Community Cloud** / Streamlit in Snowflake (SiS) starts via Snowflake Virtual Warehouses at **~$2.00–$3.00/credit-hour** (XS Warehouse consumes 1 credit/hr) | **Free forever**: Unlimited public apps; 1 private app; up to 2.7 GB RAM and 2 vCPUs per app container; apps sleep after 12h inactivity. | Rapid deployment platform converting Python scripts into interactive, shareable data applications and internal tools. |
| **[Hex.tech](https://hex.tech/)** | **$1.2B Valuation** ($272M+ Funding, ~$6M–$15M+ ARR) | **$36/editor/month** (Professional tier, billed annually) | **Free forever**: 1 editor seat, up to 5 published apps, small shared compute profile, limited monthly AI actions. | Collaborative workspace combining SQL, Python, and reactive visual components into interactive stakeholder data apps. |
| **[Observable Cloud](https://observablehq.com/)** | **~$142M Valuation** ($46.1M Funding, ~$5M+ ARR) | **$22/month** (Pro tier, billed annually; or $25 month-to-month) | **Free forever**: Unlimited public notebooks, unlimited editors/viewers on Free Teams; strictly public data only (no private notebooks/connections). | Collaborative data canvas and reactive notebook environment for D3/Observable Plot visualizations and interactive reports. |
| **[Deepnote](https://deepnote.com/)** | **~$80M Valuation** ($23.8M Funding, ~$3M+ ARR) | **$39/editor/month** (Team tier, billed annually; or $59/editor/month billed monthly) | **Free forever**: Up to 3 editors, unlimited viewers, up to 5 projects, Basic compute (2 vCPUs, 5 GB RAM), 7-day revision history, limited AI credits. | Real-time collaborative cloud Jupyter notebook environment designed for data science teams and dashboard deployment. |
| **[Saturn Cloud](https://saturncloud.io/)** | **~$25M–$50M Valuation** ($9.5M Funding, ~$2M–$5M ARR) | **Pay-As-You-Go** starting at **$0.04/hour** (CPU, e.g. t3.medium) / **$0.53/hour** (T4 GPU); $0.10/GB-month storage | **Free forever**: 30 hours of free compute per month, access to JupyterLab, RStudio, and Dask clusters; subject to inactivity timeouts. | Managed cloud data science platform offering auto-scaling GPU/CPU clusters, Dask pipelines, and dashboard hosting. |
| **[Marimo (molab)](https://marimo.io/)** | **Acquired by CoreWeave** (Pre-acquisition $5M Seed; CoreWeave ~$19B–$23B Valuation) | **Free in Public Preview** (molab cloud service); open-source enterprise/self-hosted configurations | **Free forever (preview)**: 4 vCPUs, 32 GB RAM per notebook; opt-in NVIDIA RTX Pro 6000 GPU access; 12-hour session limit; 90-minute idle timeout. | Reactive, deterministic Python notebook platform running without hidden state; deploys notebooks as interactive web apps. |

## Open-Source GitHub Projects

- **[Marimo](https://github.com/marimo-team/marimo)**  
  **The most reproducible open-source notebook for data science.** **Apache-2.0**, Python. **No hidden state**: code, outputs, and program state are guaranteed consistent—run a cell and dependent cells re-run automatically; delete a cell and its variables are scrubbed . **Deterministic execution order** based on variable references, not cell position. **Built-in package management** with automatic venv isolation. **Interactive dataframes** for paging/filtering millions of rows without code. **SQL cells** that return Python dataframes. **Deploy as web app** (`marimo run`), execute as script (`python notebook.py`), or **convert Jupyter notebooks** (`marimo convert`). **Testable**: run pytest on notebooks. **Best for teams wanting reproducible, git-friendly notebooks** that double as apps and scripts without Jupyter's hidden-state pitfalls .

- **[Streamlit](https://github.com/streamlit/streamlit)**  
  **The most popular open-source framework for turning Python scripts into data apps.** **Apache-2.0**. **Write apps the same way you write plain Python scripts**—Streamlit reruns the entire script on every interaction, with `@st.cache_data` to skip costly computations . **Magic commands** let you write variables on their own line and they render automatically. **30+ built-in components** including dataframes, charts (Altair, Plotly, Matplotlib, ECharts), media, and layout columns/grids . **Deploy anywhere**—local, Streamlit Community Cloud, or self-hosted. **Best for quick dashboards, internal tools, and demos** where development speed matters more than fine-grained state control .

- **[Quarto](https://github.com/quarto-dev/quarto-cli)**  
  **The open-source scientific and technical publishing system for data scientists.** **MIT licensed**, built on Pandoc. **Author in Markdown** with embedded code from Python, R, Julia, and JavaScript via Jupyter, Knitr, and Observable . **Rich technical writing features**: cross-references, sub-figures, callouts, citations, and numbered equations. **Project system** for rendering websites and books from multiple documents. **Visual Markdown editor** for long-form composition. **Output to HTML, PDF, Word, and presentations**. **Best for publication-quality reports, books, and reproducible research** where the notebook is the source but the output must be polished .

- **[Voila](https://github.com/voila-dashboards/voila)**  
  **Turns Jupyter notebooks into standalone web applications.** **BSD-3-Clause**. **Each user gets a dedicated Jupyter kernel** that executes callbacks to widget changes . **By default, disallows execute requests from the frontend** (security) and **strips input cells** from the rendered app. **JupyterLab preview extension** installed automatically. **Language-agnostic**—works with C++ (xeus-cling), R, and other kernels . **Best for sharing existing Jupyter notebooks as interactive dashboards** without rewriting them as Streamlit apps .

- **[JupyterLab](https://github.com/jupyterlab/jupyterlab)**  
  **The next-generation web interface for Project Jupyter.** **BSD-3-Clause**, **19.5K+ stars** (Bokeh) / active development . **Modular, extensible IDE** for notebooks, terminals, text editors, and custom components. **Extension ecosystem** for everything from git integration to debugging. **Best for teams already on Jupyter** wanting a full IDE experience with the option to add Voila for app publishing .

- **[Jupyter Book](https://github.com/jupyter-book/jupyter-book)**  
  **Build publication-quality books and documents from computational material.** **Open-source**, maintained by the Executable Book Project. **Write in Markdown or Jupyter notebooks**, include code cells, run embedded code, cache outputs, and convert to **web-based interactive books and PDF** . **Jupyter Book 1.x is in maintenance**; **Jupyter Book 2.x** is being built on MyST-MD . **Best for textbooks, documentation, and research compilations** where narrative and computation must live together .

- **[Evidence](https://github.com/evidence-dev/evidence)**  
  **Business intelligence as code—build reports with SQL and Markdown.** **MIT licensed**. **Create reports in code** using SQL queries and Markdown; **self-host or publish on Evidence Studio** . **Agent-ready**: develop with Evidence's Agent or Claude Code/Cursor . **Best for data analysts wanting version-controlled, code-based BI reports** without a drag-and-drop tool .

### Additional Strong Open-Source Options

- **[Panel](https://github.com/holoviz/panel)** — **Powerful data exploration and web app framework for Python** (BSD-3-Clause). Build tools, dashboards, and complex apps entirely in Python; works with Bokeh, Plotly, Matplotlib, Altair, and more. Deploy as web app, standalone Pyodide app, or static HTML . **Best for Python-native interactive dashboards** with rich widget support.
- **[Plotly Dash](https://github.com/plotly/dash)** — **Analytical web apps in Python** (MIT). Callback-based interactivity, Plotly charts, and Dash Enterprise for deployment. **Best for production dashboards** needing fine-grained callback control.
- **[Gradio](https://github.com/gradio-app/gradio)** — **Build and share ML demos in Python** (Apache-2.0, 43.7K stars). `gr.Interface` wraps any Python function with inputs/outputs; share links in seconds . **Best for model demos and quick UI prototypes**.
- **[Observable Plot](https://github.com/observablehq/plot)** — **JavaScript chart library** for exploratory data visualization. Works in Observable notebooks, vanilla HTML, npm, React, and Vue . **Best for web-native interactive charts** embedded in custom apps.
- **[nteract](https://github.com/nteract/nteract)** — **Desktop notebook editor** (Tauri + React) with a background daemon (`runtimed`), CLI (`runt`), and **MCP server for AI agents** to run code and collaborate in real time . **Best for teams wanting a local-first desktop notebook** with agent integration.

**Frameworks for building custom systems**: Combine **Marimo** for reproducible notebooks that deploy as apps, **Streamlit** or **Panel** for interactive dashboards, and **Quarto** for publication-quality reports. Use **Voila** to surface existing Jupyter notebooks as web apps without rewriting them.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data science presentation tools may expose datasets and model outputs to web audiences; enforce access controls and validate that dashboards do not leak sensitive data through interactive filters or parameter manipulation.
- **Tool choice depends on whether you need reproducibility, rapid app building, or publication output.** **Marimo solves Jupyter's hidden-state problem**—code, outputs, and state stay consistent, and notebooks double as scripts and apps . **Streamlit is the fastest path to a working data app** but reruns the whole script on every interaction—fine for dashboards, less ideal for expensive computations . **Quarto is for publication-quality output**, not interactive apps—use it when the deliverable is a report or book, not a dashboard . **Voila turns existing notebooks into apps** without rewriting, but inherits Jupyter's hidden-state risks . **Marimo's molab and Streamlit Community Cloud offer free cloud hosting**, but self-hosting eliminates vendor dependency. Validate whether you need interactive apps (Streamlit, Panel), reproducible notebooks (Marimo), or polished reports (Quarto) before committing.

---

**Made for data scientists, analysts, and teams building reproducible data presentation infrastructure.**  
Let's make data science presentation and notebook visualization more open, reproducible, and shareable.
