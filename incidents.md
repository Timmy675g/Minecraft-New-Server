# Incident History

This document tracks major incidents, outages, migrations, failures, and operational lessons learned during the development of SurvivalKendy.

Incidents can be seen in Main Website and Status Page :
Main Website : www.survivalkendy.systems
Status Page : status.survivalkendy.systems
---

# March 7th 2026 — First Major Incident

## Summary
While testing a new production deployment pipeline, the server data was accidentally wiped by the owner.

## Impact
- Server data loss
- Temporary server instability
- Risk of permanent player progress loss

## Resolution
Player data was successfully recovered using the latest available backup.

## Lessons Learned
- Never test production deployment pipelines directly on live infrastructure.
- Automated backups are critical.
- Always validate deployment procedures before production use.

---

# March 21st 2026 — The Great Reset Incident

## Summary
Due to low concurrent player activity, experimental unstable mods were introduced to the public server environment in an attempt to refresh gameplay.

## Impact
- Server instability
- Gameplay issues
- Community dissatisfaction

## Resolution
The unstable update was rolled back and the server returned to a stable state.

## Lessons Learned
- Production stability is more important than rushed feature deployment.
- Experimental features should be tested separately before public release.
- Community trust depends heavily on server reliability.

---

# April 8th 2026 — The Shutdown

## Summary
Due to very low concurrent player activity, the server was temporarily shut down in preparation for infrastructure migration and a new operational phase on DigitalOcean.

## Impact
- Temporary server shutdown
- Migration planning phase initiated

## Resolution
Infrastructure migration preparations began, including Docker based deployment improvements and operational restructuring.

## Lessons Learned
- Sustainable infrastructure matters more than temporary uptime.
- Migration planning is essential for long term server survival.
- Infrastructure evolution is part of maintaining a long-term project.

---

# May 12th 2026 — Website Backend Issues

## Summary
After releasing the public status page, major backend connectivity issues occurred between the frontend and backend systems.

## Impact
- Website instability
- Broken backend communication
- Status system disruptions

## Resolution
The issue was investigated and resolved after approximately 5 hours of debugging and infrastructure troubleshooting.

## Lessons Learned
- Reverse proxy and backend routing require careful validation.
- Infrastructure changes should be monitored closely after deployment.
- Logging and diagnostics are essential for backend troubleshooting.

---