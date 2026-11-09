# Croatia Legal Research MCP Server (`hr-legal-mcp`)

**[Hrvatski](#lang-hr) | [English Documentation](#english-documentation)**

---

<a id="lang-hr"></a>
## Pravni MCP Poslužitelj (`hr-legal-mcp`) — Hrvatski

### O ovom repozitoriju

Ovaj repozitorij sadrži Model Context Protocol (MCP) poslužitelj koji povezuje vašu AI aplikaciju (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline ili Antigravity) sa službenim glasilima i bazama sudskih odluka za **Croatia** (prvostupanjski općinski/osnovni i trgovački sudovi, drugostupanjski županijski/kantonalni/okružni i visoki sudovi te vrhovni i ustavni sudovi).

### Brza instalacija (Odabir AI aplikacije)

1. **Preuzimanje:** Kliknite na **`<> Code` -> `Download ZIP`** i raspakirajte mapu na računalu.
2. **Pokretanje:** Dvokliknite na **`Click_Here_To_Install_Windows.bat`** (Windows) ili **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Odabir AI klijenta:** U prozoru označite AI aplikacije koje koristite (Claude, Cursor, Windsurf, VS Code, Antigravity), pokrenite instalaciju i ponovno pokrenite odabrani AI program.

**Sigurnosna napomena:** Program radi isključivo u načinu čitanja (read-only) te ne mijenja niti čita vaše osobne datoteke na računalu.

### Hijerarhija sudova i službeni izvori

| Sudski stupanj | Obuhvaćeni sudovi |
|:---|:---|
| **1. Stupanj (Prvostupanjski sudovi)** | Općinski sudovi (Municipal Courts), Trgovački sudovi (Commercial Courts) & Upravni sudovi (Zagreb, Split, Rijeka, Osijek) |
| **2. Stupanj (Županijski / Kantonalni i žalbeni sudovi)** | 15 Županijskih sudova (County Courts: Zagreb, Split, Rijeka, Osijek, Varaždin, Velika Gorica, Zadar, Pula, Karlovac, Sisak, Slavonski Brod, Bjelovar, Dubrovnik, Šibenik, Vukovar), Visoki trgovački sud, Visoki upravni sud & Visoki kazneni sud RH |
| **3. Stupanj (Vrhovni i Ustavni sud)** | Vrhovni sud Republike Hrvatske (VSRH) & Ustavni sud Republike Hrvatske (USRH) |

- **Narodne novine ELI Official Gazette Portal (narodne-novine.nn.hr):** [https://narodne-novine.nn.hr](https://narodne-novine.nn.hr) (`narodne-novine.nn.hr`, `zakon.hr`, `sabor.hr`)
- **SupraNova Centralna Baza Sudske Prakse (odluke.sudovi.hr — Općinski, Županijski, Visoki & Vrhovni sud):** [https://odluke.sudovi.hr](https://odluke.sudovi.hr) (`odluke.sudovi.hr`, `vsrh.hr`, `usud.hr`, `sudacka-mreza.hr`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Croatia (HR)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Croatia**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Općinski sudovi (Municipal Courts), Trgovački sudovi (Commercial Courts) & Upravni sudovi (Zagreb, Split, Rijeka, Osijek) |
| **Tier 2 — Regional / Cantonal / Appellate** | 15 Županijskih sudova (County Courts: Zagreb, Split, Rijeka, Osijek, Varaždin, Velika Gorica, Zadar, Pula, Karlovac, Sisak, Slavonski Brod, Bjelovar, Dubrovnik, Šibenik, Vukovar), Visoki trgovački sud, Visoki upravni sud & Visoki kazneni sud RH |
| **Tier 3 — Supreme & Constitutional** | Vrhovni sud Republike Hrvatske (VSRH) & Ustavni sud Republike Hrvatske (USRH) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Narodne novine ELI Official Gazette Portal (narodne-novine.nn.hr) — [https://narodne-novine.nn.hr](https://narodne-novine.nn.hr)
  - *Indexed Legislation Domains:* `narodne-novine.nn.hr`, `zakon.hr`, `sabor.hr`
- **Court Decisions & Jurisprudence Archives:** SupraNova Centralna Baza Sudske Prakse (odluke.sudovi.hr — Općinski, Županijski, Visoki & Vrhovni sud) — [https://odluke.sudovi.hr](https://odluke.sudovi.hr)
  - *Indexed Judicial & Open Case Law Domains:* `odluke.sudovi.hr`, `vsrh.hr`, `usud.hr`, `sudacka-mreza.hr`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Croatia. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Croatia. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Croatia. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "hr-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/hr-legal-mcp/archive/refs/heads/main.zip",
        "hr-legal-mcp"
      ]
    }
  }
}
```
</details>
