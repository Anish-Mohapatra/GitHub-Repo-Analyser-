🔍 GitHub Repository Analyzer
A Python command-line tool that fetches and analyzes any public GitHub user's repositories using the GitHub REST API. Get insights on top repos, programming languages, stars, activity, and more — all in your terminal.
🚀 Features
👤 Fetch and display user profile details
⭐ Show top repositories by star count
🧑‍💻 Breakdown of most-used programming languages
📊 Overall stats: total stars, forks, watchers
🕐 Recently active repositories
💾 Optional JSON export of the full report
🛠️ Tech Stack
Language: Python 3
Libraries: requests, json, collections, datetime
API: GitHub REST API v3
⚙️ Installation & Setup
Clone the repository
git clone https://github.com/your-username/github-repo-analyzer.git
cd github-repo-analyzer
Install dependencies
pip install -r requirements.txt
Run the analyzer
python github_analyzer.py <github_username>
🧑‍💻 Usage
Basic analysis:
python github_analyzer.py torvalds
With JSON export:
python github_analyzer.py torvalds --export
Sample Output
════════════════════════════════════════════════════════════
  👤 GitHub Profile: @torvalds
════════════════════════════════════════════════════════════
  Name        : Linus Torvalds
  Location    : Portland, OR
  Followers   : 218,000
  Public Repos: 8
  Joined      : Apr 04, 2011
────────────────────────────────────────────────────────────

  📊 Repository Overview
────────────────────────────────────────────────────────────
  ⭐ Total Stars     : 198,000
  🍴 Total Forks     : 57,000
  🗂️  Original Repos  : 7

  🧑‍💻 Top Programming Languages
────────────────────────────────────────────────────────────
  C                  ████████████████     80.0%  (6 repos)
  Python             ████                 20.0%  (2 repos)
📁 Project Structure
github-repo-analyzer/
│
├── github_analyzer.py          # Main application
├── requirements.txt            # Dependencies
├── <username>_github_report.json  # Auto-generated export (optional)
└── README.md                   # Documentation
⚠️ API Rate Limiting
The GitHub API allows 60 requests/hour for unauthenticated users. If you hit the limit, you can add a personal access token:
# In github_analyzer.py, update HEADERS:
HEADERS = {
    "Accept": "application/vnd.github.v3+json",
    "Authorization": "token YOUR_GITHUB_TOKEN"
}
Get a token at: github.com/settings/tokens
💡 What I Learned
Consuming a REST API with Python requests
Parsing and processing JSON data
Working with pagination for large data sets
CLI argument handling with sys.argv
Writing modular, well-structured Python code
📌 Future Improvements
[ ] Add GitHub token support via .env file
[ ] Compare two users side-by-side
[ ] Generate an HTML report
[ ] Plot language charts using matplotlib
📄 License
MIT License — feel free to use and modify!