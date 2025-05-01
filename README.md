# achievementAnnoncement

# 📣 Slack Weekly Highlights Generator

This Google Sheets + Google Apps Script tool dynamically generates a weekly Slack message for fellows, recognizing top appliers, interview activity, and overall job search stats. The message is automatically enhanced using OpenAI and can be previewed or posted directly to Slack.

---

## 🚀 Features

- ✅ Pulls data from 3 Google Sheets tabs:
  - `Top Appliers`: Names and number of applications
  - `Pong Ceremony`: Interview activity details
  - `Company List`: Names of companies applied to
- ✨ AI-enhanced message formatting using OpenAI GPT-4
- 📊 Calculates total applications and unique companies
- 🎯 Filters and celebrates fellows who applied to 25+ jobs
- 🧠 Motivation quote and call-to-action
- 🔁 Optional: Sends message directly to Slack via webhook

---

## 📂 Sheet Structure

### `Top Appliers`
| Name         | Application Count |
|--------------|-------------------|
| Alex Rivera  | 52                |
| Taylor Kim   | 10                |

### `Pong Ceremony`
| Name         | Round | Date       | Company   | Position                  |
|--------------|-------|------------|-----------|---------------------------|
| Taylor Kim   | 1     | 5/2/2025   | YouTube   | OTT Live Video Engineer   |

### `Company List`
| Company          |
|------------------|
| Google           |
| Meta             |
| YouTube          |

---

## 🧑‍💻 Setup Instructions

1. **Open Google Sheets** → `Extensions` → `Apps Script`
2. Paste in the `Code.gs` (from this repo)
3. Save and **Reload the Sheet**
4. You will see a new menu: `Slack Generator`
5. Select **"Generate & Send Slack Message"**
6. A preview will display before posting to Slack

---

## 🔐 Configuration

Update the following variables in your script:

```js
const SLACK_WEBHOOK_URL = 'YOUR_SLACK_WEBHOOK_URL';
const OPENAI_API_KEY = 'YOUR_OPENAI_API_KEY';

---
 ## Example Output 

 @channel
:sparkles: Special Recognition :sparkles:

:dizzy: Sending Positive Vibes to Fellows Currently Interviewing:
:star2: @Taylor Kim – 1 Round at YouTube (OTT Live Video Engineer) on 05/02/2025

:muscle::skin-tone-5: Application Perseverance :clap::skin-tone-5:
Huge shoutout to our Top Applier, @Alex Rivera, for an impressive 52 applications last week! :rocket::clap:

:bar_chart: Fellow Stats
We had 499 applications go out to 343 unique companies last week! :tada::fire:

:white_check_mark: Action Time!
Drop a ✅ if you’ve added at least 5 jobs today!

