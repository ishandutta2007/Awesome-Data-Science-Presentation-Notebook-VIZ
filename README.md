# Awesome-Data-Science-Presentation-Notebook-VIZ

# Top Data Science Presentation & Notebook Viz Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Reactive Notebooks, Interactive Data Apps & Publication-Quality Reporting*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Science Presentation & Notebook Visualization**. These tools help data scientists turn exploratory notebooks into shareable dashboards, interactive web apps, and presentation-ready reports—covering everything from cloud-hosted notebook environments to open-source frameworks that render live Jupyter notebooks as standalone applications.

**Examples** include Marimo, Streamlit, Hex, Deepnote, Observable, Quarto, Voila, and JupyterLab (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted data apps, open-source notebook publishing, and community-driven visualization—ideal for data teams seeking reproducibility, avoiding per-seat SaaS pricing, and owning their presentation pipeline end to end. The open-source landscape is genuinely functional: **Marimo** guarantees reproducible notebooks with no hidden state , **Streamlit** turns Python scripts into shareable data apps in minutes , and **Quarto** produces publication-quality documents from Markdown and notebooks .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Marimo (molab)](https://marimo.io/)**  
  **Reactive Python notebook with a free cloud service (molab).** **No hidden state**—running a cell automatically re-runs dependent cells, and deleting a cell scrubs its variables from memory . **Deploy as an interactive web app or slides**, run in the browser via WASM, or execute as a script. **Built-in package management** with automatic venv isolation. **AI-assisted coding** with Copilot or local models. **molab** provides a cloud notebook experience similar to Google Colab for sharing links .

- **[Streamlit Community Cloud](https://streamlit.io/cloud)**  
  **The fastest path from Python script to shareable data app.** **Free tier** for public apps with Community Cloud. **App Gallery** for discovery. **Built-in sharing** with authentication options on paid tiers. Positioned for quick demos and internal tools without infrastructure management .

- **[Hex.tech](https://hex.tech/)**  
  **Collaborative data workspace with notebook and app modes.** Combines SQL, Python, and no-code cells with AI assistance. **Publish as interactive data apps** with parameterized inputs. Positioned for teams wanting a polished, collaborative notebook-to-app workflow.

- **[Deepnote](https://deepnote.com/)**  
  **Collaborative Jupyter-compatible notebook with real-time co-editing.** **AI assistant** for code generation and debugging. **Publish as shareable apps** with interactive widgets. Positioned for teams wanting Jupyter familiarity with cloud collaboration.

- **[Observable Cloud](https://observablehq.com/)**  
  **Reactive JavaScript notebook for data visualization.** **Observable Plot** library for charts, plus **chart cell** for no-code creation with eject-to-code . **Free for public use**; Pro connects to private databases and enables private collaboration .

- **[Google Colab](https://colab.research.google.com/)**  
  **Free cloud Jupyter notebooks with GPU/TPU access.** Widely used for ML experimentation and teaching. **Limited persistence** and compute quotas on free tier; Pro/Pro+ add higher limits.

- **[Saturn Cloud](https://saturncloud.io/)**  
  **Managed data science platform with Jupyter, RStudio, and Dask.** **Auto-scaling GPU/CPU clusters** for model training and batch jobs. Positioned for teams wanting managed infrastructure without DevOps overhead.

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
