# Community

Instructions written by Accounted's users and by anyone else who does Swedish bookkeeping: workflows an AI can run, knowledge it should follow, and analyses it can work out. Everything here is reviewed by Accounted before it is merged, and published under the repository's MIT licence.

Browse them at [accounted.se/instruktioner](https://accounted.se/instruktioner), add them to your company in Accounted with one click, or copy a `SKILL.md` into any AI that reads Claude skills.

## One folder per instruction

```
community/
  manadsavstamning-bank/
    SKILL.md
```

The folder name is the instruction's permanent id: lowercase letters, digits and hyphens.

## SKILL.md

```markdown
---
name: manadsavstamning-bank
description: Stämmer av bankkontot mot banken varje månad och listar det som skiljer.
title: Månadsavstämning av banken
kind: workflow            # workflow | knowledge | analysis
author: jakobwennberg     # GitHub or Accounted handle, shown on the page
industries: []            # optional: konsult-it, bygg-hantverk, e-handel, restaurang-cafe, vard-halsa, software-saas-ai, reklambyra-marknadsforing
language: sv
---

# Månadsavstämning av banken

What it is for, in one or two sentences.

## Steg            <!-- workflow: numbered steps -->
1. …

<!-- knowledge: the rules, as plain paragraphs or a list -->
<!-- analysis: which accounts or figures, over which period, and how to read the result -->
```

`name` must match the folder name, and `description` stays under 1024 characters (Claude's limit).

## What review checks

- **No customer data**: no names of real customers or suppliers, personnummer, organisationsnummer, account numbers, amounts from real books or passwords.
- **Correct against Swedish rules**: a rule that contradicts the law (a wrong VAT rate, booking without underlag) is sent back with a comment.
- **Useful to someone else**: general enough that another company can use it as it is.
- **Safe to run**: nothing that books, sends, files or deletes without the user's approval.
