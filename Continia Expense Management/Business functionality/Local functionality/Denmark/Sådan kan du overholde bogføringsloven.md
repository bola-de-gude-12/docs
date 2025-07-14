---
title: Sådan kan du overholde bogføringsloven
date: 24-05-2024
description:  
id: EM-228
lang: en
---

# Sådan kan du overholde bogføringsloven

> [!NOTE]
> This is the Danish version of the article. You can find the English version here: [How to Comply with the Danish Bookkeeping Act](@EM-227).

> [!IMPORTANT]
> Understøttelse af den nye danske bogføringslov er fuldt implementeret i Continias løsninger fra og med version 12.02.

## Business Central online eller on-premises

Bogføringsloven kræver, at danske virksomheder skal bruge et digitalt bogføringssystem. Dette kan være et standardsystem, som IT-leverandøren har valgt at registrere og få godkendt hos Erhvervsstyrelsen, eller det kan være et ikkeregistreret digitalt bogføringssystem, hvor virksomheden selv er ansvarlig for, at systemet overholder loven.

### Business Central online

**Microsoft Dynamics 365 Business Central online** er af Microsoft registreret og godkendt hos Erhvervsstyrelsen som standardsystem til digital bogføring. Virksomheder, som ønsker at effektivisere deres administration yderligere, kan anvende Continia Document Capture, Continia Expense Management, Continia Document Output og Continia Payment Management i tillæg til det registrerede system, uden at dette påvirker Erhvervsstyrelsens godkendelse.

Læs mere om baggrunden for ovenstående her: [Continias produkter påvirker ikke Erhvervsstyrelsens godkendelse af Business Central online](@EM-229).

Du kan finde oplysninger om Business Centrals godkendelse her: [Compliance with the bookkeeping act in Denmark](https://learn.microsoft.com/en-us/dynamics365/business-central/localfunctionality/denmark/compliance-denmark#main-requirements----15-no-2) (Microsoft-artikel).

### Business Central on-premises (lokal installation)

Business Central on-premises er også et digitalt bogføringssystem, men det er *ikke* registreret og godkendt af Erhvervsstyrelsen. Dermed skal virksomheder, der anvender dette system, selv tage ansvar for, at systemet anvendes på en måde, hvor det opfylder loven.

Den nyeste version af Business Central on-premises er i alle bogføringsmæssige sammenhænge helt det samme system som onlineudgaven.<a href="#footnote-1"><sup>1</sup></a> Alle kravene til bogføringssystemets funktioner vil således være overholdt. Også på den lokale version kan virksomheder, som ønsker at effektivisere deres administration yderligere, anvende Document Capture, Expense Management, Document Output og Payment Management i tillæg til Business Central.

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Visse funktioner kan kræve installation af tilføjelsesprogrammer (apps) eller aktivering ved hjælp af Feature Management.</li>        
  </ol>
</div>
</small>

## Hvordan opbevares digitale bilag bedst?

Bogføringsloven kræver, at danske virksomheder opbevarer bilag vedrørende køb og salg digitalt. Med Document Capture og Expense Management kan den enkelte virksomhed vælge den opbevaringsmåde, som passer dem bedst.

> [!NOTE]
> Document Capture, Expense Management og Document Output kan alle opsættes med krav om, at bilag skal findes lagret ved bogføring af salgs- og købstransaktioner. Virksomhederne kan således med Continias produkter sikre, at de overholder bogføringslovens krav om digitale bilag.

### Business Central Online

For danske virksomheder, der anvender Business Central online, vil det fra d. 1. juli 2024 være et krav fra Microsoft, at købsbilag lagres i tabellen **Indgående bilag**. Med Document Capture og Expense Management er dette enkelt, da alle købsbilag automatisk kopieres til denne tabel ved brug af disse løsninger. Virksomhederne vil således ikke mærke det nye krav.

Opbevarer virksomheden de købsbilag, der registreres via Document Capture og Expense Management, i Business Central-databasen, vil bilagene forekomme dobbelt i databasen. Dette er en bekvem og enkel metode, men den kan for visse virksomheder optage uhensigtsmæssigt meget databaseplads, da bilagene vil findes i både Continias tabeller og Microsofts **Indgående bilag**. Disse virksomheder kan vælge i stedet at opbevare købsbilagene fra Document Capture og Expense Management ved hjælp af Azure Blob Storage. Du kan finde flere oplysninger i [Setting up Azure Blob Storage](@EM-230).

### Business Central on-premises

Anvender virksomheden en lokalt installeret version af Business Central, kan virksomheden vælge at opbevare digitale købsbilag på følgende måder:

* I Continias tabeller i Business Central-databasen
* Ved hjælp af Azure Blob Storage
* Lokalt på virksomhedens server

Virksomheden kan også vælge, at Document Capture og Expense Management automatisk skal kopiere alle købsbilag til Business Central-tabellen **Indgående bilag**. Dette kan være en fordel, hvis virksomheden i dag opbevarer købsbilag ved hjælp af Azure Blob Storage eller lokalt på virksomhedens server, da bilagene således bliver omfattet af sikkerheden i databasen og de backup-rutiner, der er konfigureret for denne.

> [!IMPORTANT]
> Virksomheder, der anvender en lokalt installeret version af Business Central, skal selv sikre, at der minimum ugentligt tages en automatisk fuld sikkerhedskopi af bogføringstransaktioner og digitale bilag. Sikkerhedskopien skal opbevares på en server i et EU- eller EØS-land hos en ikke nærtstående part, som må formodes at opfylde anerkendte standarder for IT-sikkerhed.

## Continias løsninger og bogføringsloven

Bogføringsloven kræver, at danske virksomheder anvender systemer, der understøtter automatisering af virksomhedens administrative processer. Dette er hele formålet med Document Capture, Expense Management, Document Output og Payment Management. Herudover gør Continias løsninger det også enklere for virksomhederne at opfylde bogføringslovens krav om følgende:

* Løbende og nøjagtig registrering af transaktioner
* Digital opbevaring af købs- og salgsbilag
* Sikring af kontrolspor
* Afsendelse og modtagelse af elektroniske fakturaer
* Afstemning af den enkelte virksomheds bankkonti

Continias løsninger er bygget på Business Central og påvirker hverken det digitale bogføringssystems grundlæggende funktioner eller opbevaringen af data. Efter dialog med Erhvervsstyrelsen kan det fastslås, at Continias produkter kan anvendes sammen med Business Central online, uden at dette påvirker systemets status som registreret standardsystem til digital bogføring.
