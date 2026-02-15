<div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:8px;">
<h1 style="margin:0;">Privacy Policy</h1>
<div style="display:flex;align-items:center;gap:4px;">
<span style="display:inline-block;width:24px;height:24px;border-radius:50%;background-color:#4A90D9;"></span>
<span style="display:inline-block;width:22px;height:22px;border-radius:50%;background-color:#B794F6;margin-left:-10px;"></span>
<span style="display:inline-block;width:18px;height:18px;border-radius:50%;background-color:#7DD3FC;margin-left:-8px;"></span>
<span style="font-size:15px;font-weight:700;color:#000;letter-spacing:2px;margin-left:8px;">ARETE</span>
</div>
</div>

**Last Updated:** February 13, 2026

**ARETE** ("we," "us," or "our") operates the ARETE mobile application (the "App"). This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use the App.

By using ARETE, you agree to the collection and use of information in accordance with this policy.

---

## 1. Information We Collect

### 1.1 Information You Provide

- **Account Information:** When you sign up, we collect your email address and password (or Google account information if you use Google Sign-In). Your password is securely hashed and never stored in plain text.
- **Profile Information:** Your name and optional profile photo, if you choose to provide them.
- **Task Data:** The tasks you create, including titles, purposes, approaches, enjoyment notes, energy ratings, reflection notes, and completion status. This is the core data you enter into the App.

### 1.2 Information Collected Automatically

- **Analytics Data:** If you have analytics enabled in your privacy settings, we collect anonymous usage data through PostHog, including which features you use, screen views, and interaction patterns. This data is used to improve the App experience. You can disable this at any time in Settings > Privacy & Security.
- **Crash Reports:** If you have crash reporting enabled, we collect anonymous crash logs through Sentry to identify and fix bugs. These logs contain technical information about the error (device type, OS version, stack trace) but no personal content. You can disable this at any time in Settings > Privacy & Security.
- **Device Information:** Basic device information (device type, operating system version) collected as part of analytics and crash reporting.

### 1.3 Information Processed by Third Parties

- **AI-Generated Insights:** Your task data (titles, purposes, approaches, enjoyment notes, energy ratings) is sent to OpenAI's API to generate personalized weekly insights. This data is sent in aggregate form (weekly summary) and is not used by OpenAI to train their models. See OpenAI's [API data usage policy](https://openai.com/policies/api-data-usage-policies) for details.
- **Voice Transcription:** If you use the voice input feature, your audio recordings are sent to OpenAI's Whisper API for transcription. Audio is processed in real-time and not stored by OpenAI.

---

## 2. How We Use Your Information

We use the information we collect to:

- Provide, operate, and maintain the App
- Create and manage your account
- Store and sync your tasks across devices
- Generate AI-powered weekly insights based on your task patterns
- Send transactional emails (account confirmation, password resets) via Resend
- Send optional lifecycle emails (weekly digest, progress nudges, re-engagement) via Resend — you can unsubscribe from these at any time by replying "unsubscribe" to any marketing email
- Analyze usage patterns to improve the App (when analytics is enabled)
- Identify and fix technical issues (when crash reporting is enabled)
- Respond to your requests or inquiries

---

## 3. Data Storage and Security

### 3.1 Where Your Data Is Stored

- **Account and task data** is stored in Supabase (hosted on AWS infrastructure). Data is encrypted in transit (TLS) and at rest.
- **Authentication** is managed by Supabase Auth with secure session handling.
- **Local data** is cached on your device using AsyncStorage for offline access and performance.
- **Analytics data** is stored in PostHog's cloud infrastructure (US/EU).
- **Crash reports** are stored in Sentry's cloud infrastructure.

### 3.2 Security Measures

- All data transmitted between the App and our servers uses HTTPS/TLS encryption.
- Passwords are hashed using industry-standard algorithms (bcrypt via Supabase Auth).
- Row Level Security (RLS) is enabled on all database tables, ensuring users can only access their own data.
- API keys and secrets are stored securely and never exposed in client-side code.

---

## 4. Third-Party Services

We use the following third-party services to operate the App:

| Service | Purpose | Data Shared |
|---------|---------|-------------|
| **Supabase** | Authentication, database, file storage | Account info, task data, profile photos |
| **OpenAI** | AI weekly insights, voice transcription | Anonymized task summaries, audio recordings |
| **PostHog** | Product analytics (opt-in) | Anonymous usage events, device info |
| **Sentry** | Crash reporting (opt-in) | Anonymous crash logs, device info |
| **Resend** | Transactional and marketing emails | Email address, email content |
| **Google** | OAuth sign-in (optional) | Email, name, profile photo (from Google account) |

Each third-party service has its own privacy policy governing how they handle data. We encourage you to review their respective policies.

---

## 5. Your Rights and Choices

### 5.1 Privacy Controls

You can manage the following in Settings > Privacy & Security:

- **Analytics:** Toggle on/off to control whether anonymous usage data is collected via PostHog.
- **Crash Reporting:** Toggle on/off to control whether anonymous crash logs are sent via Sentry.

### 5.2 Email Preferences

- **Transactional emails** (account confirmation, password reset) are required for account functionality and cannot be opted out of.
- **Marketing emails** (weekly digest, nudges, re-engagement) can be opted out of by replying "unsubscribe" to any marketing email.

### 5.3 Account and Data

- **Access your data:** All your task data is visible within the App at all times.
- **Delete your account:** You can request account deletion by contacting us at hello@aretetodo.com. Upon deletion, all your personal data (profile, tasks, analytics associations) will be permanently removed within 30 days.
- **Export your data:** Contact us at hello@aretetodo.com to request an export of your data.

### 5.4 Rights Under GDPR/CCPA

If you are a resident of the European Economic Area (EEA) or California, you have additional rights including:

- The right to access, correct, or delete your personal data
- The right to data portability
- The right to restrict or object to processing
- The right to withdraw consent at any time

To exercise these rights, contact us at hello@aretetodo.com.

---

## 6. Data Retention

- **Account data** is retained for as long as your account is active.
- **Task data** is retained for as long as your account is active.
- **Analytics data** is retained for up to 12 months, then automatically deleted.
- **Crash reports** are retained for up to 90 days.
- Upon account deletion, all personal data is permanently removed within 30 days.

---

## 7. Children's Privacy

ARETE is not intended for children under the age of 13. We do not knowingly collect personal information from children under 13. If we discover that a child under 13 has provided us with personal information, we will delete it promptly. If you believe a child under 13 has provided us with personal data, please contact us at hello@aretetodo.com.

---

## 8. Changes to This Policy

We may update this Privacy Policy from time to time. When we do, we will update the "Last Updated" date at the top of this page. We encourage you to review this policy periodically. Continued use of the App after changes constitutes acceptance of the updated policy.

---

## 9. Contact Us

If you have questions or concerns about this Privacy Policy, please contact us:

- **Email:** hello@aretetodo.com
- **Website:** https://aretetodo.com

---

ARETE — The to-do list that actually gets done.
