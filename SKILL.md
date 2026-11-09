---
name: hr-legal-mcp-skill
description: Official Croatia (HR) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Croatia Legal Research & Multi-Tier Case Law Skill (`hr-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Croatia (HR)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:HR:VSRH:2024:100 or NN 35/05`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Općinski sudovi (Municipal Courts), Trgovački sudovi (Commercial Courts) & Upravni sudovi (Zagreb, Split, Rijeka, Osijek)
   - **Second Instance (Cantonal / Regional / Appellate):** 15 Županijskih sudova (County Courts: Zagreb, Split, Rijeka, Osijek, Varaždin, Velika Gorica, Zadar, Pula, Karlovac, Sisak, Slavonski Brod, Bjelovar, Dubrovnik, Šibenik, Vukovar), Visoki trgovački sud, Visoki upravni sud & Visoki kazneni sud RH
   - **Supreme & Constitutional Instance:** Vrhovni sud Republike Hrvatske (VSRH) & Ustavni sud Republike Hrvatske (USRH)
   - **Primary Tiered Database:** SupraNova Centralna Baza Sudske Prakse (odluke.sudovi.hr — Općinski, Županijski, Visoki & Vrhovni sud) (`https://odluke.sudovi.hr`)
