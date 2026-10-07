# WoodmenLife Recruiting Copilot V6

V6 reorganizes the demo into five top-level tabs:

- Dashboard
- Applicants
- Outreach
- Jobs
- Analytics

## Key behavior
- Applicants opens with all applicants and can be filtered by job, status, or search text.
- Jobs are clickable launch points. “View applicants” opens the same Applicants workspace with the selected job filter applied.
- Outreach is independent from a specific requisition. Recruiters can use the embedded Talent Discovery Agent and optionally filter synthetic prospects by target job.
- The Applicants workspace includes the embedded Applicant Intelligence Agent.
- Both agent URLs are independently configurable.

## Run
```powershell
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173`.

## Configure agents
Edit `frontend/.env`:

```text
VITE_TALENT_DISCOVERY_AGENT_URL=...
VITE_APPLICANT_INTELLIGENCE_AGENT_URL=...
```

The supplied Copilot Studio URL is configured for both panels because only one URL was provided. Restart the Vite server after changing `.env`.

All applicant, prospect, resume, and application data is synthetic. The embedded Copilot Studio agent is live and governed by its own publishing and authentication configuration.
