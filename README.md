# electrical-pdf-backend (Electrical segment)

**CID Leg 2 — Electrical segment.** Renders ACORD + supplemental PDFs from CID_HomeBase templates (Electrical uses SUPP_ELECTRICAL), emails via Gmail API. Same RSS pattern as HVAC and Plumber.

* **Segment:** `electrical` (set via `SEGMENT` env; default `electrical`).
* **Canonical bundle:** `ELECTRICAL_INTAKE` = SUPP_ELECTRICAL + ACORD125, 126, 130, 140. Config in `src/config/bundles.json`.
* **Intake (Netlify):** `Netlify/index.html` posts to **CID-PDF-API** `POST /submit-quote` with `ELECTRICAL_INTAKE`.
* **Templates:** CID_HomeBase (cloned on Render Docker build).

Deploy: Docker (Render). Netlify hosts the public quote form at `electricalinsurancedirect.com`.
