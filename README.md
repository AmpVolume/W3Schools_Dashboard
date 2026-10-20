# 🎓 W3Schools Learning Dashboard

**W3Schools Learning Analytics Dashboard — Independent Extension**  
**Created:** October 19, 2026

An automated learning analytics dashboard that retrieves publicly available W3Schools profile statistics, generates a custom SVG visualization using Python, and publishes updates to a GitHub repository through GitHub Actions.

Built as an independent, code-driven extension to the W3Schools learning experience, this project displays learning progress directly in a GitHub profile README without requiring a separate HTML website or web application.

**Technologies:** Python, JSON, SVG, HTTP, YAML, Git, GitHub, and GitHub Actions.

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

- **Automated statistics retrieval:** Fetches publicly available learning statistics from the W3Schools profile API.
- **Programmatic SVG generation:** Uses Python to create a dashboard image from the retrieved data.
- **Custom visual design:** Features W3Schools branding, a dark background, green accents, metric cards, and vector icons.
- **Scheduled updates:** GitHub Actions runs the workflow on a six-hour schedule, subject to GitHub's scheduling availability.
- **Automatic publishing:** Commits and pushes the generated SVG when its contents change.
- **GitHub profile integration:** Displays the generated dashboard directly in a GitHub profile README.
- **Credential-free public data access:** Retrieves publicly accessible profile information without requiring W3Schools login credentials.

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| Python 3 | Retrieves profile data, processes statistics, and generates the SVG |
| JSON | Represents the data returned by the W3Schools profile API |
| HTTP | Sends requests to retrieve public profile statistics and download the logo |
| SVG | Defines the dashboard's visual elements as scalable vector graphics |
| YAML | Configures the GitHub Actions workflow |
| Git | Tracks changes and manages commits |
| GitHub | Hosts the repository and generated dashboard |
| GitHub Actions | Executes the automated workflow on a schedule or manual trigger |

## ⚙️ How It Works

1. **Workflow trigger:** GitHub Actions starts the workflow on its scheduled interval or when manually triggered.
2. **Repository checkout:** The workflow retrieves the project files so the automation can run.
3. **API request:** Python sends an HTTP request to the W3Schools public profile endpoint.
4. **JSON parsing:** Python parses the response into native data structures, such as dictionaries and lists.
5. **Data extraction:** Python extracts the available learning statistics from the response.
6. **SVG generation:** Python builds the dashboard's SVG markup, including its layout, metric cards, icons, and styling.
7. **File output:** The generated image is saved as `w3schools-dashboard.svg`.
8. **Change detection:** Git checks whether the generated SVG differs from the existing version.
9. **Publishing:** If the image has changed, the workflow commits and pushes the updated file to the repository.
10. **Profile display:** GitHub renders the SVG in the profile README that references it.

## 📊 Dashboard Metrics

The dashboard displays the following learning statistics when they are available in the API response:

- Lessons read
- Total points
- Exercise points
- Quiz points
- Current learning streak
- Completed challenges

The displayed values depend on the data returned by the public profile API and the fields extracted by the Python workflow.

## 📁 Project Structure

```text
W3Schools_Dashboard/
├── .github/
│   └── workflows/
│       └── w3schools-dashboard.yml
├── README.md
└── w3schools-dashboard.svg
```

- `.github/workflows/w3schools-dashboard.yml` — configures the automation schedule, execution steps, and publishing process.
- `w3schools-dashboard.svg` — generated dashboard image.
- `README.md` — documents the project and embeds the dashboard.

## 🚀 Running the Workflow

1. Open the [GitHub Actions tab](https://github.com/AmpVolume/W3Schools_Dashboard/actions).
2. Select the **Update W3Schools Dashboard** workflow.
3. Click **Run workflow** and select the `main` branch.
4. Wait for the workflow to finish.
5. Review the workflow logs and generated SVG to verify the result.

The workflow is also scheduled to run every six hours. GitHub may delay scheduled executions, so updates are not guaranteed at an exact time.

## 🔒 Data and Limitations

- The project uses publicly accessible W3Schools profile statistics.
- It does not require W3Schools account credentials.
- It depends on the availability and structure of the public profile API.
- API changes or outages may cause the workflow to fail until the integration is updated.
- The dashboard is a static SVG image, not an interactive web application.
- Statistics reflect the most recent successful update, not necessarily real-time activity.
- Scheduled execution and publishing depend on GitHub Actions permissions and availability.

## 🎯 Learning Objectives

This project demonstrates practical experience with:

- HTTP requests and API integration
- JSON parsing and Python dictionaries
- Extracting and processing structured data
- Programmatic file generation
- SVG markup and vector graphics
- YAML workflow configuration
- Git version control and repository synchronization
- Continuous integration and automated publishing
- Debugging automation and API-related failures

## 👨‍💻 Author

**AmpVolume**

[GitHub Profile](https://github.com/AmpVolume) · [W3Schools Profile](https://www.w3profile.com/AmpVolume/)
