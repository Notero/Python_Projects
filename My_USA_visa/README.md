# 🇺🇸 US Visa Appointment Rescheduler Bot (Turkish Consulate)

## 🧾 Description
This Python script uses **Selenium WebDriver** to automatically log into the **US Visa Appointment website (Turkey region)** and attempts to reschedule an appointment as soon as a new slot becomes available.

It checks availability every **10 minutes**, selects the **first available slot**, and confirms the appointment, **updating a local file** with the new date.

## 🚀 Features
- ✅ Logs into https://ais.usvisa-info.com automatically
- ✅ Clicks through navigation and appointment pages
- ✅ Scrapes calendar for earliest available slot
- ✅ Selects the first appointment time and confirms
- ✅ Updates local `.txt` with new appointment date
- 🔁 Repeats every 10 minutes until successful

## 🛠️ Setup

### 💻 Requirements
- Python 3.x
- [Google Chrome](https://www.google.com/chrome/)
- [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/)
- Install dependencies:

      pip install selenium
🔧 Configuration
  Set your credentials:

    email = "your@email.com"
    password = "yourpassword"
  Set your ChromeDriver absolute path:

    service = Service(absolute_path="C:/Path/To/chromedriver.exe")
  Update the local path to where your script stores the last appointment:
    
    currrent Path = "/Users/akin/PycharmProjects/PythonProject1/USvize.txt"
📌 Notes
The script only picks the first available day and time. If you want to change that behavior, modify the calendar scraping logic.

The site may flag you for suspicious activity due to repeated refreshing/logins. Use cautiously.

Make sure 2FA or CAPTCHA is disabled, or handled separately.

⚠️ Warnings
❗ Never share your credentials in public repositories.

❗ Automating government services may violate site terms of service.

❗ Frequent requests may get your account locked or banned.

💡 To-Do
Add CAPTCHA handling or third-party CAPTCHA solvers

Add notification (email/text) when appointment is rescheduled

Add more intelligent slot filtering (e.g., specific days/hours)

👤 Programmed by Akin Korkmaz
📅 Script optimized for 2025 appointments (adjust logic for future use)
