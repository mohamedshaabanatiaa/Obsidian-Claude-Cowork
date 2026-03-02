# Morning Daily Briefing — Mohamed Shaaban
**Task name:** `morning-daily-briefing`
**Schedule:** Every day at 9:00 AM (Asia/Dubai, GMT+4)
**Cron:** `0 9 * * *`

---

## Objective

Run a comprehensive morning briefing for Mohamed Shaaban (mshaaban@obsidiansecurity.com), Sr. Regional Solutions Consultant – META at Obsidian Security. Pull data from Gmail, Google Calendar, Slack, and Salesforce, then compile everything into a structured briefing with action items, a new contacts CSV, and POV follow-up status.

---

## Step-by-Step Instructions

### 1. 📬 Email Digest (Gmail)

Search Gmail for all emails received in the last 24 hours using the query `after:YYYY/MM/DD` (yesterday's date). Read each relevant email and categorize:

- 🔴 **ACTION REQUIRED** — emails needing Mohamed's direct response or decision
- 🟡 **FYI** — informational updates, no action needed
- 🔵 **FOLLOW-UP** — emails Mohamed has sent that are awaiting a reply

**Key rules:**
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

- **#sales-engineering-private** → Surface any SE updates, deal support requests, or technical blockers.
- **#announcements** → Summarize any company-wide announcements.
- **#product-updates** → Summarize any new product/feature announcements. Draft a LinkedIn post based on the most notable update (professional tone, 2–3 sentences, suitable for Mohamed to post).
- **#sales-competitive-intel** → Highlight any new competitive intelligence relevant to META deals.
- **#social** → If a LinkedIn post has been shared or drafted by the team, reference it.
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

### 6. 🔬 POV Daily Follow-Up

Check the status of all active POVs (Proof of Value engagements). For each POV, evaluate two signals and flag if either is stale (no update in 7+ days):

#### Step 1 — Salesforce POV Status
Navigate to each active POV opportunity in Salesforce using the browser. Check the **Last Modified Date** and any recent activity or notes on the opportunity record.

**Current active POVs:**
- **Mashreq Bank** — SF Opportunity: https://obsidiansecurity.lightning.force.com/lightning/r/Opportunity/006UT00000S0gf3YAB/view

If the Salesforce opportunity record has not been updated in **7 or more days**, flag it as: 🔴 **SF STALE — update needed**.

#### Step 2 — Slack POV Channel Status
Navigate to the POV's dedicated Slack channel (format: `#account-pov-internal`) and check the date of the most recent message.

**Current POV Slack channels:**
- Mashreq Bank → **#mashreqbank-pov-internal**

If the channel has had no messages in **7 or more days**, flag it as: 🔴 **SLACK STALE — update needed**.

#### Step 3 — POV Update (if stale)
If either signal is stale, draft a POV status update for Mohamed to post in the Slack channel. The update **must follow the exact cumulative format already used in that channel** — read the existing messages to understand the format, then append the new update in an identical style. Do not invent a new format; mirror what is already there precisely.

#### Output format for this section:
```
🔬 POV: Mashreq Bank
  SF Last Update: [date] — [✅ Current / 🔴 STALE]
  Slack Last Update: [date] — [✅ Current / 🔴 STALE]
  [If stale] → Draft update ready for #mashreqbank-pov-internal (see below)
```

---

## Output Format

Present the briefing inline in the chat using clear markdown sections with the headers above. Save the new contacts CSV to the outputs folder and provide a download link.

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
