# Jiffy-Rolling-CX-Dashboard-
📊 JiffyShirts CX Queue Dashboard
A lightweight, browser-based dashboard for monitoring the live support queue throughout the day. No login required — just upload a CSV export from Zendesk and go.


How to Use
1. Pull a CSV from Zendesk
Export your queue view as a CSV from Zendesk. This is your snapshot — a point-in-time picture of everything currently in the queue.
2. Upload at the start of your shift (6am)
Drag and drop (or click to browse) your CSV into the Current Snapshot box. This first upload of the day automatically becomes the baseline — the starting point all day totals are measured against.

⚠️ The 6am snapshot is critical. Everything else builds from it. If no one uploads at 6am, the first upload of the day becomes the baseline instead.
3. Upload every ~2 hours throughout the day
Each time someone uploads a new current snapshot, the dashboard:

Updates all live queue metrics (SLA status, oldest ticket, issue breakdown, etc.)
Adds any newly removed ticket IDs to the running worked total
Logs the snapshot in the day tracker

You don't need to coordinate who uploads — anyone can do it. The totals just keep building.
4. Use the Previous Snapshot for interval comparisons
If you want to see what changed in just the last 2 hours, upload your previous CSV into the Previous Snapshot box. This shows the interval comparison (worked this interval, new arrivals, net change) separately from the full-day running total.
5. Screenshot and share
When sharing with the wider team, take a screenshot of the full dashboard and post it to Slack or wherever your team communicates.


What the Numbers Mean
Day Totals (top section)
Metric
What it means
Total Worked Today
All ticket IDs that were in the baseline but are no longer in the current queue — regardless of why they left (resolved, on hold, merged, etc.)
New Arrivals Today
Ticket IDs that came into the queue after the baseline was set
Net Change
Current queue size minus baseline size
Baseline Size
How many tickets were in the queue at the first upload of the day
Current Size
How many tickets are in the queue right now


Important: "Worked" does not mean "solved." It means any ticket that was pulled out of this queue — whether it was resolved, put on hold, had first contact made, or had any other action taken. This reflects true team workload.
Current Queue State
Live metrics from the most recently uploaded snapshot — SLA health, oldest ticket, new tickets in today vs yesterday.
Interval Comparison
Only shows when a Previous Snapshot is uploaded. Shows what changed between your last two check-ins specifically.
Priority Buckets
Tickets grouped by age in 2-hour bands. Red = already past SLA. Yellow = getting close. Green = healthy.


Day Tracker (top banner)
Shows:

Baseline Set — when the first upload of the day happened
Snapshots Today — how many CSVs have been uploaded
Baseline Queue Size — queue size at start of day
Last Upload — when the most recent snapshot was added
Dots — one dot per snapshot uploaded today; hover each dot to see the timestamp, size, and filename


Important Notes
The dashboard resets automatically at midnight CST. You don't need to do anything — the next morning's first upload sets a fresh baseline.
Use the Reset Day button only if you need to manually clear everything mid-day (e.g. if the wrong file was uploaded as the baseline).
All times are CST/CDT. The dashboard converts Zendesk timestamps automatically.
Browser storage is used to track the running total. This means the running total is tied to the browser being used. For best results, one person should handle uploads from the same machine throughout the day, then screenshot and share.
The previous snapshot upload does not affect the day total — it's only for the interval comparison view.


CSV Format
The dashboard expects a standard Zendesk queue export with these columns:

Column
Required
ID
✅ Yes
Ticket status
✅ Yes
Requested
✅ Yes (for SLA and age calculations)
Updated
Recommended
Issue
Recommended (for issue breakdown chart)
Subject, Requester, Assignee, SLA, Order Num, VIP Level, Intent
Optional



Questions?
Reach out to your CX Supervisor.

**
