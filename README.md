# Swedish accounting skills

Agent skills for Swedish bookkeeping law, tax and reporting: reference knowledge an AI agent loads when the question comes up.
They work in any agent that reads the Agent Skills format (Claude Code, Codex, Cursor, OpenClaw and others) and need no Accounted account.

## Install

```bash
npx skills add erp-mafia/accounted-skills                      # choose from the list
npx skills add erp-mafia/accounted-skills --skill swedish-vat  # one skill
npx skills add erp-mafia/accounted-skills -a codex             # into one agent: claude-code, codex, cursor, openclaw, ...
```

Or clone the repository: Claude Code loads `.claude/skills/` when you work inside the directory.

## Skills

| Skill | Covers |
| --- | --- |
| [`swedish-accounting-compliance`](.claude/skills/swedish-accounting-compliance/SKILL.md) | Swedish accounting law and compliance reference for developers building accounting software |
| [`swedish-asset-accounting`](.claude/skills/swedish-asset-accounting/SKILL.md) | Swedish fixed asset accounting (anläggningsredovisning) reference |
| [`swedish-cash-register`](.claude/skills/swedish-cash-register/SKILL.md) | Swedish cash register (kassaregister), staff ledger (personalliggare) and the bookkeeping of daily takings |
| [`swedish-daily-bookkeeping`](.claude/skills/swedish-daily-bookkeeping/SKILL.md) | Practical kontering of everyday Swedish transactions (löpande bokföring): booking bank lines and receipts to BAS 2026 accounts with the right momsbehandling |
| [`swedish-e-invoicing`](.claude/skills/swedish-e-invoicing/SKILL.md) | Swedish e-invoicing (e-fakturering) reference |
| [`swedish-ef-skatteplanering`](.claude/skills/swedish-ef-skatteplanering/SKILL.md) | Swedish tax planning for enskild firma (sole proprietorship) |
| [`swedish-financial-reporting`](.claude/skills/swedish-financial-reporting/SKILL.md) | Swedish financial reporting: årsredovisning structure (K2/K3 uppställningsform, noter, förvaltningsberättelse, underskrifter) |
| [`swedish-inventory`](.claude/skills/swedish-inventory/SKILL.md) | Swedish inventory accounting (varulager): valuation and bookkeeping |
| [`swedish-invoice-compliance`](.claude/skills/swedish-invoice-compliance/SKILL.md) | Swedish invoice compliance (fakturering) reference |
| [`swedish-k3-k4-judgment`](.claude/skills/swedish-k3-k4-judgment/SKILL.md) | Swedish K3 (BFNAR 2012:1) in depth, K4 (IFRS/RFR 2) at a high level, and the professional judgment around them |
| [`swedish-payroll`](.claude/skills/swedish-payroll/SKILL.md) | Swedish payroll (lön & arbetsgivaravgifter) compliance reference for developers building payroll or accounting software |
| [`swedish-project-accounting`](.claude/skills/swedish-project-accounting/SKILL.md) | Swedish project accounting (projektredovisning) covering dimensional tagging of bokföringsposter with project codes, WIP accounting (pågående arbeten) |
| [`swedish-sie-import-export`](.claude/skills/swedish-sie-import-export/SKILL.md) | Swedish SIE4 file format: parsing, validation, generation, troubleshooting |
| [`swedish-sru-filing`](.claude/skills/swedish-sru-filing/SKILL.md) | Swedish SRU file generation for Skatteverket digital tax filing (INK2, INK2R, INK2S declarations for aktiebolag) |
| [`swedish-tax-planning`](.claude/skills/swedish-tax-planning/SKILL.md) | Swedish corporate tax planning (skatteplanering AB) for aktiebolag and fåmansbolag |
| [`swedish-travel-expenses`](.claude/skills/swedish-travel-expenses/SKILL.md) | Swedish travel expenses (resekostnader, tjänsteresor) end to end for 2026: when a trip qualifies (50 km, övernattning, tjänsteställe, tremånadersregeln) |
| [`swedish-vat`](.claude/skills/swedish-vat/SKILL.md) | Swedish VAT (moms) compliance reference |
| [`swedish-year-end-closing`](.claude/skills/swedish-year-end-closing/SKILL.md) | Swedish year-end closing (bokslut) for AB and Enskild firma |

### Also in this repository

Skills written in this repository, not generated from Accounted's source.

| Skill | Covers |
| --- | --- |
| [`swedish-industry-bygg`](.claude/skills/swedish-industry-bygg/SKILL.md) | Swedish accounting for construction and trades (bygg och hantverk) |
| [`swedish-industry-ehandel`](.claude/skills/swedish-industry-ehandel/SKILL.md) | Swedish accounting for e-commerce (e-handel) |
| [`swedish-industry-restaurang`](.claude/skills/swedish-industry-restaurang/SKILL.md) | Swedish accounting for restaurants and cafés (restaurang och café) |
| [`swedish-industry-saas`](.claude/skills/swedish-industry-saas/SKILL.md) | Swedish accounting for SaaS and software companies |
| [`swedish-industry-vard`](.claude/skills/swedish-industry-vard/SKILL.md) | Swedish accounting for healthcare, dental care and beauty services (vård, tandvård, skönhet) |

## Community

Instructions shared by Accounted's users and others live in [`community/`](community/README.md): workflows, knowledge and analyses, each reviewed by Accounted before it is merged.
Browse them at [accounted.se/instruktioner](https://accounted.se/instruktioner). To share your own, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Source

Generated from Accounted's canonical Swedish accounting skills.
Edit the source in erp-mafia/accounted; the skill files in this repository are a read-only mirror.

For live corrected instructions, connect your AI to Accounted over MCP.
A checkout is a snapshot and does not receive withdrawals until updated.

## License

MIT. See [LICENSE](LICENSE).
