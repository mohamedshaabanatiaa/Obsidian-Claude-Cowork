# Morning Daily Briefing — Mohamed Shaaban
**Task name:** `morning-daily-briefing`
**Schedule:** Every day at 9:00 AM (Asia/Dubai, GMT+4)
**Cron:** `0 9 * * *`

---

## Objective

Run a comprehensive morning briefing for Mohamed Shaaban (mshaaban@obsidiansecurity.com), Sr. Regional Solutions Consultant – META at Obsidian Security. Pull data from Gmail, Google Calendar, Slack, and Jira, then compile everything into a structured briefing with action items, a new contacts CSV, and conditional follow-up drafts.

---

## Step-by-Step Instructions

### 1. 📬 Email Digest (Gmail)

Search Gmail for all emails received in the last 24 hours using the query `after:YYYY/MM/DD` (yesterday's date). Read each relevant email and categorize:

- 🔴 **ACTION REQUIRED** — emails needing Mohamed's direct response or decision
- 🟡 **FYI** — informational updates, no action needed
- 🔵 **FOLLOW-UP** — emails Mohamed has sent that are awaiting a reply

**Key rules:**
- For emails related to the **SAHARA reseller/partner opportunity**, note that **Sayed Shamshuddin (sshamshuddin@obsidiansecurity.com) should respond**, not Mohamed. Flag these as Sayed's responsibility.
- For any HR or payroll disputes (e.g., medical insurance deductions, phone/internet allowances with Rippling or HR), check whether a reply has been received. If no reply exists to Mohamed's last sent message on the thread, **create a Gmail draft** (do NOT send) for Mohamed to review and send as a follow-up. The draft should be professional, referencing prior correspondence.
- Exclude automated digests (Gong daily, Notion newsletters, Zoom join notifications) from the ACTION REQUIRED category — place them under FYI.

---

### 2. 👤 New Contacts CSV

Extract all **external** contacts (non-@obsidiansecurity.com) who appear in yesterday's emails — both senders and recipients. For each, collect: Full Name, Given Name, Family Name, Work Email, Company/Organization.

Save a CSV file to the outputs folder at:
`/outputs/new_contacts_YYYY-MM-DD.csv`

Format the CSV using Google Contacts import format with headers:
`Name, Given Name, Family Name, E-mail 1 - Type, E-mail 1 - Value, Phone 1 - Type, Phone 1 - Value, Organization 1 - Type, Organization 1 - Name, Organization 1 - Title`

Present the file with a download link.

---

### 3. 🗓️ Today's Calendar (Google Calendar)

Fetch all events for today from Google Calendar. Display all meetings in **Dubai time (Asia/Dubai, GMT+4)**, sorted chronologically. For each meeting include:
- Start and end time
- Meeting title
- Link (Zoom, Teams, etc.) if available
- Organizer
- RSVP status (✅ Accepted / ⚠️ Tentative / ❌ Declined / ❓ Needs Action)
- Key attendees (external ones especially)

Flag the following:
- ⚠️ **Scheduling conflicts** (overlapping meetings)
- ⚠️ **Unanswered RSVPs** — meetings still marked Tentative or Needs Action that need a decision

Omit personal focus blocks (Prayer Time, Lunch Time) from any conflict warnings — those are non-negotiable.

---

### 4. 💬 Slack Highlights

Open the Obsidian Security Slack workspace (workspace ID: T01D4P8A0FY, URL: https://app.slack.com/client/T01D4P8A0FY) using the browser. Check the following channels for notable messages from the past 24 hours:

- **#product-updates** → Summarize any new product/feature announcements. Draft a LinkedIn post based on the most notable update (professional tone, 2–3 sentences, suitable for Mohamed to post).
- **#social** → If a LinkedIn post has been shared or drafted by the team, reference it.
- **#sales** → Surface any key deal updates, customer wins, or blockers.
- **#team-technical-field-organization** → Surface any technical enablement updates or field team announcements.
- **#high-risk-alerts-customers-and-prospects** → Highlight any high-risk alerts related to Mohamed's accounts or the META region.
- **#boom** → Surface any wins or announcements.

If Slack is not accessible, note each channel as "unavailable" rather than skipping them.

---

### 5. 📋 All Tasks & Action Items

Compile a **complete list of all tasks** (not a top 3 — every actionable item) across all sources. Group by priority:

**🔴 Urgent / Action Today**
**🟡 Follow up / Monitor**
**🔵 Pending Response (sent, waiting)**

Include tasks from emails, calendar prep needs (e.g., meetings needing preparation), Slack items, and any ongoing threads. For each task, note the source (email, calendar, Slack, etc.).

---

### 6. 🎯 Jira Issues

Search Jira (cloud ID: `0977b327-0fc4-4447-ba92-50319c0e8e00`) for any open issues assigned to `currentUser()` where `statusCategory != Done`, ordered by `updated DESC`. If there are open issues, list them with status and priority. If none, note "No open Jira issues."

---

## Output Format

Present the briefing inline in the chat using clear markdown sections with the headers above. Save the new contacts CSV to the outputs folder and provide a download link. Any Gmail drafts created should be noted with the subject line and recipient so Mohamed can review them in Gmail Drafts.

Do NOT include an Obsidian Security threat alerts section.

---

## Key Contacts & Context

- **Mohamed Shaaban** — mshaaban@obsidiansecurity.com | Sr. Regional Solutions Consultant – META | Based in Dubai (UAE)
- **Sayed Shamshuddin** — sshamshuddin@obsidiansecurity.com | Mohamed's colleague, handles SAHARA partner communications
- **SAHARA partner opportunity** — Sayed owns this thread. Mohamed is CC'd but Sayed should respond.
- **Tamkeen Security / Beta IT** — Partner enablement in Saudi Arabia (Mohammed Hamed, m.hamed@tamkeensecurity.sa)
- **Aramco** — Recurring weekly stand-up with Rahaf Alnufaiee (rahaf.nafay@aramco.com)
- **Mashreq** — Active POV (proof of value) engagement
- **GBM** — Account mapping partner sessions
