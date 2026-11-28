# simplestrom Wärmepumpe – Claude plugin

Wärmepumpe planen in Deutschland, direkt im Chat: Heizlast und Kosten mit dem
[simplestrom-Heizlastrechner](https://www.simplestrom.de/rechner/heizlast), BEG-Förderung, Ersparnis, CO₂ und
unverbindliche Angebote von bis zu 3 Fachbetrieben aus der Region.

> **Keine professionelle Beratung.** Alle Ergebnisse (Heizlast, Kosten, Förderung, Ersparnis, Angebots-Check) sind
> unverbindliche Schätzungen und allgemeine Informationen. Sie sind keine Energie-, Förder-, Rechts- oder Steuerberatung
> und keine Zusage für deinen Einzelfall. Ob und in welcher Höhe du Förderung bekommst, entscheidet die KfW nach ihren
> Bedingungen; Größe und Preis der Wärmepumpe legt ein Fachbetrieb nach einem Vor-Ort-Termin fest.
>
> *Not professional advice: all outputs are non-binding estimates and general information, not energy, subsidy, legal
> or tax advice for the user's own case.*

Bundles:
- the remote MCP connector `https://www.simplestrom.de/api/mcp` (Streamable HTTP, no sign-in, MCP Apps UI), and
- the skill `waermepumpe-planen`.

## Install

- **Claude (web, desktop, mobile):** Settings → Connectors → Add custom connector → `https://www.simplestrom.de/api/mcp`
- **Claude Code:** `/plugin marketplace add ThisIsWallE/simplestrom-claude-plugin`, then `/plugin install simplestrom-waermepumpe@simplestrom`

## Tools

| Tool | Read-only | Visible to model | UI |
|---|---|---|---|
| waermepumpe_kosten_schaetzen | yes | yes | calculator click flow + result card |
| waermepumpe_lohnt_sich | yes | yes | – |
| waermepumpe_stromkosten | yes | yes | – |
| waermepumpe_foerderung_berechnen | yes | yes | – |
| waermepumpe_angebot_pruefen | yes | yes | – |
| waermepumpe_angebote_anfordern | yes | yes | quote click flow |
| angebot_absenden | no | app only (form in the view) | – |

## Not professional advice

Every tool answer ends with this line, and the skill tells Claude to keep it:
"Hinweis: Unverbindliche Schätzung und allgemeine Information, keine Energie-, Förder-, Rechts- oder Steuerberatung.
Ob und in welcher Höhe du Förderung bekommst, entscheidet die KfW nach ihren Bedingungen; Größe und Preis legt ein
Fachbetrieb nach Vor-Ort-Termin fest."

## Privacy Policy

Full policy: https://www.simplestrom.de/datenschutz#ki-apps

- **Collected:** house details for the estimate (PLZ, area, building year, heating, consumption); they are not stored.
  For a quote request only what the user types into the form in the view (name, phone, email) plus explicit consent.
  The assistant never receives contact data and cannot send a request on its own.
- **Use and sharing:** quote requests go to up to 3 matching heat-pump installers, as stated in the consent text.
- **Retention:** quote requests are kept as long as needed to handle the request and as required by law; details in the policy.
- **No chat transcripts** are requested or stored.
- **Contact:** https://www.simplestrom.de/kontakt · Impressum: https://www.simplestrom.de/impressum

## Support

https://www.simplestrom.de/kontakt · Terms: https://www.simplestrom.de/nutzungsbedingungen
