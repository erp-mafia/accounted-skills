---
name: fortnox-uppsagning
description: Granskar Fortnox-abonnemang, licenser, Fortnox Access, bindningstid, förnyelser och fakturor, exporterar bokföringen inför flytten, säger upp det användaren godkänner och kontrollerar att det faktiskt blev uppsagt. Använd när någon vill säga upp Fortnox, byta bokföringsprogram, bli av med Fortnox Access eller stoppa Fortnox-kostnader.
title: Säga upp Fortnox
kind: workflow
author: emil-froberg
industries: []
language: sv
---

# Säga upp Fortnox

Fortnox gör det medvetet så svårt de kan att lämna. De döljer vad saker faktiskt kostar, gömmer bindningstiden så att användare låses in i långa avtal, och gör det extremt krångligt att säga upp. Man får verkligen, verkligen kämpa, och för en vanlig människa är det i praktiken nästan omöjligt. Men med hjälp av komplexa AI-modeller ska det tekniskt sett gå att säga upp sina abonnemang, om man verkligen jobbar hårt för det.

I praktiken betyder det: lita aldrig på att en enskild sida visar hela bilden. I oktober 2026 stod det **Du har inga produkter att säga upp** medan Fortnox Access fortfarande debiterades, programsumman visade 0 kr på ett betalt abonnemang, och **Säg upp allt** fyllde bara i ett formulär. Utgå från att en kostnad finns kvar tills du har sett den upphöra.

Målet är att hitta varje företags faktiska åtaganden, säkra bokföringen, säga upp det användaren godkänner och tydligt skilja på vad som är uppsagt, vad som fortfarande kostar och vad som inte gick att nå. Instruktionen ger i sig inget godkännande att säga upp, betala, radera konton eller kontakta support.

## Innan du börjar

Arbetet kräver en webbläsare som du själv kan styra: logga in på fortnox.se, klicka och läsa sidorna. Kontrollera det först. Saknas ett sådant verktyg, säg det direkt och föreslå att användaren byter till en miljö som har det, eller erbjud att guida steg för steg medan användaren klickar själv och berättar vad som syns. Påstå aldrig att något är granskat eller uppsagt som du inte själv har sett.

Låt användaren logga in själv. Spara aldrig inloggningsuppgifter, sessionslänkar, tenant-tokens eller personliga faktureringsuppgifter i instruktionen eller i ett överlämningspaket.

## Steg

1. **Logga in och kartlägg företagen.** Gå till https://www.fortnox.se och följ **Logga in**. Under **Välj företag**, anteckna varje företag du når och de som kräver **Be om åtkomst**: företagsnamn, abonnemangsnummer om det syns, och om användaren är systemadministratör. Att ett företag syns på grund av en registrerad roll betyder varken åtkomst eller personligt betalningsansvar. Begär inte åtkomst utan godkännande. Syns flera företag, fortsätt läsa medan du reder ut vilka som ska sägas upp. Åtkomst till en arbetsgivares eller ett delat företag är inget godkännande att säga upp det.

2. **Håll isär de tre sakerna.** **Fortnox ID** är inloggningen. Företagets abonnemang är en sak, **Fortnox Access** en annan, och Access kan ha en egen löpande avgift. Anta inte att ID:t orsakade en faktura, eller att det avslutar företagets abonnemang om man raderar ID:t.

3. **Granska varje företag.** Via företagsmenyn och **Mitt abonnemang**, sedan **Abonnemang** där det finns:
   - **Översikt**: Fortnox Access separat från programlicenser, antal och månadspriser. 0 kr i programsumma betyder inte att abonnemanget är gratis.
   - Avtalsperiod, bindningstid, sista dag för uppsägning, faktureringsdatum, förnyelseperiod och betalningsansvar, för både abonnemang och **Plustjänster**.
   - **Kommande avtalsperiod**: kommande produkter, beräknade kostnader och förnyelsedatum.
   - **Fakturor**: obetalda belopp, fakturanummer, förfallodatum och betalstatus.
   - **Plustjänster**: användningsavgifter och förbetalda saldon. Förbetalda krediter och rader med 0 kr är inga extra abonnemang.

   Anteckna uttryckligen det som saknas. Ett företag som heter "Test" är inget bevis på gratis tjänst. Leder **Mitt abonnemang** bara till **Mina program** och **Fråga om fler program** är det ingen faktureringsöversikt: rapportera att åtkomsten är begränsad i stället för att säga att inget abonnemang finns.

4. **Exportera bokföringen innan något avslutas.** Räkenskapsinformation ska sparas i sju år efter utgången av det kalenderår då räkenskapsåret avslutades (BFL 7 kap), men i oktober 2026 angav Fortnox att bokföringsdata raderas 18 månader efter avslut. Ansvaret ligger på företaget, inte på Fortnox. Fråga var filerna ska sparas och exportera för varje räkenskapsår som finns i Fortnox:
   - SIE4-fil (hela bokföringen med verifikationer)
   - verifikationer med underlag och bilagor
   - grundbok (verifikationslista) och huvudbok
   - årsredovisningar och bokslut
   - kund- och leverantörsfakturor, och löneunderlag om lön körts i Fortnox

   Följ Fortnox nuvarande exportfunktioner i stället för gamla menyvägar. Kontrollera att varje fil öppnas och att alla år finns med. Påminn om att en säkerhetskopia ska förvaras åtskild från originalet. Vill användaren hoppa över exporten, notera det som en öppen risk i rapporten. För import till nästa system, se `swedish-sie-import-export`.

5. **Säg upp via abonnemanget.** Vägen i oktober 2026 var **Abonnemang → Hantera uppsägning**. Etiketter kan ändras, så följ det som faktiskt syns. Sidan kan säga **Du har inga produkter att säga upp** medan Fortnox Access fortfarande kostar; öppna då **Avsluta abonnemang** för att avsluta det underliggande abonnemanget.
   1. Läs varningen och anteckna exakt vilka konsekvenser och datum den anger. I oktober 2026 försvann åtkomsten vid periodens slut och bokföringsdata raderades efter 18 månader. Kontrollera det varje gång.
   2. Innan du skickar: förklara konsekvensen för användaren, bekräfta att exporten i steg 4 är klar eller medvetet bortvald, och få uttryckligt godkännande för raderingen. Ett godkännande att stoppa kostnader är inte ett godkännande att radera data. Fråga inte igen om samma konsekvens redan är godkänd.
   3. Gå vidare med **Gå vidare med uppsägningen**, välj en sann orsak och skicka med **Säg upp**. Hitta aldrig på nedläggning, konkurs eller byte av leverantör som inte stämmer. Välj **Annan orsak** eller den sanna orsak som ligger närmast.

6. **Säg upp äldre licenser.** Den äldre vägen är företagsmenyn → **Administrera användare → Mer → Säg upp program**. **Säg upp allt** fyller bara i antal. Välj **Abonnemang används ej** om det stämmer, sedan **Säg upp produkter → Bekräfta uppsägning**, och läs varningarna innan du bekräftar. Att alla licenser är uppsagda betyder inte att abonnemanget eller alla löpande kostnader har upphört.

7. **Gör inget utöver uppdraget.** Betala eller bestrid inte fakturor, skicka inga meddelanden till support och radera inte Fortnox ID bara för att användaren bad om en uppsägning.

8. **Kontrollera resultatet.** Ett klick eller ett ifyllt formulär är inte en uppsägning. Spara en skärmbild av bekräftelsesidan och anteckna slutdatum om det visas. Gå tillbaka till abonnemangsstatus och kommande avtalsperiod och kontrollera att förnyelsen verkligen stoppades. Visas bara ett allmänt "klart"-meddelande, säg exakt vad det bekräftar och vad som fortfarande är okänt. Skicka inte om en uppsägning när utfallet är oklart; kontrollera status först. Skärmbilder sparas där användaren vill, aldrig i instruktionen.

9. **Rapportera.** Ange varje företag som **uppsagt**, **avslutas vid periodens slut**, **fortfarande aktivt**, **väntar på godkännande** eller **ej kontrollerat på grund av åtkomst**. Redovisa obetalda fakturor och exportens status separat. Säg aldrig "allt klart" förrän varje företag i uppdraget är redovisat. Saknas åtkomst, ange företaget och vad en administratör eller support behöver göra, utan att själv skicka något.

10. **Lämna över.** Ange datum för senaste kontrollen, vad som faktiskt skickades, vad som väntar på godkännande och nästa konkreta steg. Kontrollera alltid aktuell status innan du gör något nytt; gamla skärmbilder visar hur det var då, inte hur det är nu.
