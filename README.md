<h1 align="center">ScamShield</h1>

<p align="center">
  <strong>Spot the warning signs before you click, pay, or reply.</strong><br>
  A free, student-built scam checker and education platform.
</p>

<p align="center">
  <a href="https://scamshieldapp.org/pages/analyzer"><img src="https://img.shields.io/badge/Try%20the%20Analyzer-006B60?style=for-the-badge" alt="Try the Scam Analyzer"></a>
  <a href="https://www.youtube.com/watch?v=8k15kCeRCdk"><img src="https://img.shields.io/badge/Watch%20the%20Demo-274B72?style=for-the-badge" alt="Watch the demo"></a>
</p>

<p align="center">
  <a href="#what-you-can-do">Features</a> ·
  <a href="#try-it-with-a-sample">Try a sample</a> ·
  <a href="#under-the-hood">Tech stack</a> ·
  <a href="#privacy-and-limitations">Privacy</a>
</p>

<p align="center">
  <a href="https://scamshieldapp.org/">
    <img src="https://scamshieldapp.org/images/hero-images/home-banner-hero-image-laptop-display-lead-library-alert-weekly-scamshield.png" alt="ScamShield website preview showing the scam library and weekly alerts" width="760">
  </a>
</p>

## What you can do

| Feature | What you get |
| :--- | :--- |
| **[🔍 Scam Analyzer](https://scamshieldapp.org/pages/analyzer)** | Paste a message or link, or upload a screenshot. Get a risk score, a plain-language explanation, and steps you can take. |
| **[📚 Scam Library](https://scamshieldapp.org/library)** | Learn how scams such as phishing, fake job offers, and bank impersonation work, and which details give them away. |
| **[🔔 Scam Alerts](https://scamshieldapp.org/pages/alerts)** | Subscribe to the newsletter for emerging scam tactics and practical online safety tips. |
| **[🚩 Scam Reporter](https://scamshieldapp.org/pages/report-a-scam)** | Share suspicious messages, websites, or calls to help ScamShield identify patterns worth covering. |

## Try it with a sample

Open the [Scam Analyzer](https://scamshieldapp.org/pages/analyzer) and paste this fictional delivery text. It’s free and requires no account.

> Your package is on hold. Pay a $1.99 redelivery fee within two hours at `delivery-update.example`.

See whether the analysis flags the unexpected fee, the short deadline, and the unfamiliar domain. The result also gives you next steps and can offer guidance if you already responded.

## Why I built it

A fake delivery text can look ordinary when you’re expecting a package. I built ScamShield to explain what makes a message suspicious in the moment, so people can recognize the same tactics the next time they see them.

## Under the hood

The web frontend submits text, links, or images to a rate-limited `POST /analyze` endpoint. The Express backend uses Google Gemini to assess the content and returns structured results. The frontend turns them into a risk score, confidence estimate, suspected scam type, specific red flags, and next steps.

| Layer | Stack |
| :--- | :--- |
| Frontend hosting | Vercel |
| API | Node.js and Express on Render |
| AI analysis | Google Gemini |

## Privacy and limitations

Treat the analysis as an AI-generated second opinion. Verify suspicious requests through a contact method you already trust, such as the number in your bank’s app. Remove passwords, one-time codes, and other sensitive details before submitting content. Third-party services may process analyzer submissions.

[Privacy Policy](https://scamshieldapp.org/pages/privacy-policy) · [Terms of Service](https://scamshieldapp.org/pages/terms-of-service)

---

<p align="center">
  Built by <strong>Zavier Carino</strong> · <a href="mailto:outreach@scamshieldapp.org">Feedback and community outreach</a>
</p>
