# MentorDyl

Internship alerts for CS students, straight to Discord!

The MentorDyl watches internship lists and posts new roles to a Discord channel in this case Dylan C 321 - CS 1944 as soon as they show up. Each post is sorted by role, so my students only get pinged for the jobs they actually care about.

It starts as a feed for the CS 1944 section I mentor at Virginia Tech. Hopefully this can become something bigger in the future!

## What a post shows

- Job title (links straight to the application)
- Company
- Role, season, and how long ago it was posted
- Location
- Sponsorship info, when the source has it

Master's-level roles still get posted, but only ping the Grad Students role. PhD-only and MBA-only roles and old seasons get filtered out automatically.

## Roles

Students pick the roles they want pings for:

SWE, Data Sci / Analytics, AI / ML, Cyber, Cloud / Devops, Systems / Infra, Hardware, Prod / Design, FDE, Quant, Masters

Jobs are sorted by keywords in the title first, then by the source's category if nothing matches. A job can ping more than one role.

## Sources

- [x] [Simplify](https://github.com/SimplifyJobs/Summer2027-Internships)
- [ ] [vanshb03](https://github.com/vanshb03/Summer2027-Internships)
- [ ] Jobright
- [ ] speedyapply
- [ ] Greenhouse, Lever, and Ashby job boards

## Roadmap

- [x] Sort jobs into roles
- [x] Post to Discord with role pings
- [x] Separate pings for Master's-level roles
- [ ] Remember posted jobs so nothing gets posted twice
- [ ] Mark posts as closed when applications close
- [ ] Pull from more sources
- [ ] Clearance info from job descriptions
- [ ] Intern pay, new grad pay, and return offer info
- [ ] Run on Google Cloud every 15 minutes

## Running it locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Create a `.env` file with your Discord webhook URL:

```
DISCORD_WEBHOOK_URL=your_webhook_url_here
```

Then post a few sample jobs:

```bash
python post_sample.py
```