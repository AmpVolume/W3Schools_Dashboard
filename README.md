# 🎓 W3Schools Learning Dashboard

An automated learning analytics dashboard that retrieves public W3Schools profile statistics, generates a custom SVG visualization using Python, and displays the results on my GitHub profile.

<p align="center">
  <a href="https://www.w3profile.com/AmpVolume/">
    <img src="https://raw.githubusercontent.com/AmpVolume/W3Schools_Dashboard/main/w3schools-dashboard.svg" alt="W3Schools Learning Dashboard" width="100%" />
  </a>
</p>

<p align="center">
  <a href="https://www.w3profile.com/AmpVolume/">W3Schools Profile</a> ·
  <a href="https://github.com/AmpVolume/W3Schools_Dashboard/actions">Automation Workflow</a>
</p>

## ✨ Features

- **Automated statistics retrieval:** Fetches public profile data from the W3Schools profile API.
- **Dynamic SVG generation:** Uses Python to create a dashboard image from the latest available statistics.
- **Custom visual design:** Features W3Schools branding, a dark background, green accents, metric cards, and vector icons.
- **Scheduled updates:** GitHub Actions attempts to refresh the dashboard every six hours.
- **Automatic publishing:** Commits and pushes the generated SVG when its contents change.
- **GitHub profile integration:** Displays the generated dashboard directly in my profile README.

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| Python 3 | Retrieves data and generates the dashboard |
| JSON | Represents the API response data |
| REST-style HTTP request | Retrieves public profile statistics |
| SVG / XML-based markup | Defines the dashboard's visual elements |
| YAML | Configures the GitHub Actions workflow |
| Git and GitHub | Version control and publishing |
| GitHub Actions | Runs the scheduled automation |

## ⚙️ How It Works

1. GitHub Actions starts the workflow on a schedule or when manually triggered.
2. The workflow checks out the repository.
3. Python sends an HTTP request to the W3Schools public profile endpoint.
4. The response is parsed from JSON into Python data structures.
5. Python extracts the learning statistics and generates SVG markup.
6. The SVG is written to `w3schools-dashboard.svg`.
7. Git checks whether the generated file has changed.
8. If changes exist, the workflow commits and pushes the updated dashboard.
9. GitHub renders the SVG inside the profile README.

## 📊 Dashboard Metrics

The dashboard displays these available profile statistics:

- Lessons read
- Total points
- Exercise points
- Quiz points
- Current learning streak
- Completed challenges

The displayed values depend on the data returned by the public profile API.

## 📁 Project Structure

```text
W3Schools_Dashboard/
├── .github/
│   └── workflows/
│       └── w3schools-dashboard.yml
├── README.md
└── w3schools-dashboard.svg
```

- `w3schools-dashboard.yml` — defines the automation schedule, execution steps, and publishing process.
- `w3schools-dashboard.svg` — generated dashboard image.
- `README.md` — project documentation and dashboard display.

## 🚀 Running the Workflow

1. Open the repository's **Actions** tab.
2. Select **Update W3Schools Dashboard**.
3. Click **Run workflow** and select the `main` branch.
4. Wait for the workflow to complete.
5. Inspect the generated SVG and workflow logs.

The workflow also runs on a six-hour schedule. GitHub may delay scheduled runs, so updates are not guaranteed at an exact minute.

## 🔒 Data and Limitations

- The dashboard uses publicly accessible profile statistics; it does not require W3Schools login credentials.
- It depends on the availability and structure of the public profile API.
- If the API changes or becomes unavailable, the workflow may fail until the integration is updated.
- The dashboard is a static SVG image, not an interactive web application.
- The displayed statistics reflect the most recent successful refresh, not necessarily real-time activity.

## 🎯 Learning Objectives

This project demonstrates practical experience with:

- HTTP requests and API integration
- JSON parsing and Python dictionaries
- Generating files programmatically
- SVG markup and vector graphics
- YAML configuration
- Git version control
- Continuous integration and automated publishing
- Debugging workflow failures and Git synchronization

## 👨‍💻 Author

**AmpVolume**

[GitHub Profile](https://github.com/AmpVolume) · [W3Schools Profile](https://www.w3profile.com/AmpVolume/)

---

*Built as a learning project to practice Python automation, API integration, SVG generation, and GitHub Actions.*
