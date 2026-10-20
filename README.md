# FitConnect

**Smart Yoga & Fitness Awareness for a Healthier Community**
*Move Better. Live Better.*

FitConnect is a simple web app built for a Community Engagement Project. People often know that exercise and yoga are good for them, but that awareness rarely becomes a daily habit. FitConnect closes that gap by combining three things in one place: **Learn**, **Track** and **Join**.

> Status: working prototype for demonstration and academic use.

---

## The problem

Long hours of sitting and screen use, little regular activity, and limited awareness of safe yoga practice are common in students and office workers. Existing options each miss something:

| Option | Good at | Missing |
|---|---|---|
| Videos / social media | Free tutorials and tips | One-way, no tracking |
| Fitness apps | Plans and tracking | Individual, no community |
| Yoga apps | Guided sessions | No local interaction |
| Offline classes | Instructor-led | Fixed time and place |

FitConnect brings guidance, tracking and community together in one simple platform.

## Features

- **Learn:** yoga library with 6 beginner poses (steps, benefits, cautions), topic filters (posture, back care, stress relief) and a daily tip.
- **Track:** log activity type, minutes and water intake; delete entries.
- **Dashboard:** 7-day chart, progress toward a 150-minute weekly goal, streak and active days.
- **Join:** 7-day community challenge with daily tasks and check-ins.
- **Survey:** before / after survey with a comparison chart, used to measure the project's impact.

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript (Jinja templates) |
| Backend | Python, Flask |
| Database | SQLite (created automatically) |
| Charts | Chart.js (bundled locally, works offline) |
| Version control | Git and GitHub |

## Screenshots

<!-- Add your own screenshots after running the app, for example:
![Home](screenshots/home.png)
![Dashboard](screenshots/dashboard.png)
-->

## Getting started

**Requirements:** Python 3.9 or newer.

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/FitConnect.git
cd FitConnect

# 2. Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate            # Windows
# source venv/bin/activate       # macOS / Linux

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the app
python app.py
```

Open **http://127.0.0.1:5000** in your browser, register an account and explore.

To stop the server, press `Ctrl + C`.

## Project structure

```
FitConnect/
├── app.py              # Flask routes and SQLite schema
├── requirements.txt
├── templates/          # HTML pages (Jinja)
├── static/
│   ├── css/            # Styles
│   ├── js/             # Chart.js and small UI script
│   └── img/            # Images
└── instance/           # SQLite database (created on first run, git-ignored)
```

## How it works

1. A user registers and logs in.
2. They read the yoga library and the daily tip.
3. They log activity, and the dashboard shows daily and weekly consistency.
4. They join the 7-day challenge and check in each day.
5. Before and after the community activities, participants fill in the survey, and the results chart shows what changed.

## Data and evidence

The need for the project was illustrated with a sample analysis of the Kaggle **Sleep Health and Lifestyle** dataset (374 records, synthetic data):
https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset

In that sample, the least active group (45 minutes or less per day) reported the lowest average sleep quality, although the overall correlation was weak (r = 0.19). This is only a reference sample; the project's own before / after survey provides the real community results.

## Limitations

- This is a prototype. Set a `SECRET_KEY` environment variable for any real deployment.
- No CSRF protection, email verification or password reset yet.
- Yoga content is basic guidance, **not medical advice**. Have it reviewed by a qualified instructor before real use.
- The optional AI pose-feedback module (OpenCV and MediaPipe) is not included.

## Future scope

- Mobile app
- Wearable integration
- AI pose assistance (OpenCV and MediaPipe)
- Multi-language content
- Expert-reviewed content
- Community leaderboard

## Team

- Name 1 (roll no.)
- Name 2 (roll no.)

Department of Computer Engineering, *College name*
Guided by: *Sir / Madam name*

## License

Add a license of your choice (for example MIT) by creating a `LICENSE` file, or remove this section for a purely academic project.
