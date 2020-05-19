---
title:      "Moderniser med Infrastructure-as-Code"
slug:       moderniser-med-infrastructure-as-code
author:     roberth_strand
#subtitle:   ""
date:       2020-05-18 18:15:13
background: '/img/posts/2020-05-18-moderniser-drift-med-infrastructure-as-code.jpg'
category:   Infrastruktur
tags:       Automasjon, DevOps, Infrastructure-as-Code
layout:     post
comment:    true
---

Etter at DevOps tankegangen begynte å spre seg for fullt her i Norge, så har flere store organisasjoner gått over til det som kalles for Infrastructure-as-Code (*IaC*) og av gode grunner. DevOps er kanskje enklere å forstå for de som kommer fra *Dev* delen av utrykket, men hører at flere som kommer fra den gamle SysAdmin-skaren får litt problemer når velkjente grafiske knapper skal byttes ut med kode. Er det skremmende vanskelig å begynne med IaC, og hvordan kommer man i gang med det?

## Dokumentasjon

Når man jobber med kode i lag med noen så lagrer man vanligvis koden på en sentral plass som er styrt med en eller annen form for versjonskontroll. Det mest vanlige i dag er Git, som ble laget av Linus Torvalds for å kunne jobbe i lag med andre på Linux Kernel.

Med andre ord så vil koden, som per definisjon også er din infrastruktur, være lagret på en sentral plass med versjonskontroll. Du vil derfor kunne sjekke endringer som har blitt gjort, målt opp mot hvordan det var før endringen. Dette gir bedre kontroll om noe skulle være feil, men også dokumentasjon på endringer.

Det beste med det hele er at man strengt talt ikke trenger å dokumentere på tradisjonelt vis, da koden er dokumentasjon. Og hva er ikke bedre enn å ikke trenge å dokumentere noe?

## Gjenbruk av kode

Når man skriver kode, så er gjenbruk noe som står høyt på listen over hva som er god praksis. DRY, eller **D**on't **R**epeat **Y**ourself, er vanlig innen programmering. Poenget er å ikke bruke tid på å skrive noe flere ganger, men heller skrive det slik at det er mulig å gjenbruke.

Samme prinsippet gjelder med Infrastructure-as-Code. Skriv koden din modulær, sånn at det du trenger å gjøre flere ganger ikke må skrives fra bunnen av hver gang. Hvordan dette gjøres i praksis kan fint bli en hel egen artikkel, men de fleste populære verktøyene er modulær ut av boksen. Dette kommer det til å bli skrevet mer om her på bloggen, så følg med 😉

## Lær deg koden, ikke plattformen

De fleste verktøyene i dag støtter flere plattformer. Når du lærer deg å skrive kode med ett verktøy, så lærer du deg å skrive det til alle disse plattformene. Dette gjør det enklere for deg å komme i gang uansett hvor det blir avgjort at en tjeneste skal kjøre. Dette betyr ikke at du på magisk vis kan begynne å jobbe med hvilken som helst leverandør, men om du har lært deg hvordan du leser språket i dokumentasjonen til en, så er det mye enklere å finne frem hos den andre.

De fleste verktøyene bruker deklarativ kode og kort forklart, deklarativ kode betyr at du skriver hva du vil ha. Om du vil ha en server, så trenger du kun å skrive hvordan den skal se ut og ikke hva som skal til for løse oppgaven rent teknisk. Hvordan dette ser ut i virkeligheten varierer litt, men de fleste går for noe som er i tekstformatene yaml eller json, eller sin egen variasjon. 

# Hvilket verktøy skal man lære

Her finnes det ikke ett korrekt svar. Det hjelper kanskje heller ikke på at mange er rimelig like. 

Om din arbeidsplass bruker ett type verktøy, så er jo saken ganske enkel. Viktigste er å komme i gang med den nye tankegangen bak IaC og ikke ett spesifikt verktøy. Det betyr da heller ikke at du ikke kan se på noen av alternativene og lære om de.

**Open source** - Det finnes veldig mange positive effekter av åpne kildekode, og utvikling det fremmer. Det åpner også i større grad for neste punkt på listen.

**Godt community** - Å være den eneste som jobber med noe gjør det vanskelig å finne svar. De fleste populære verktøyene i disse dager har en god fanskare, men spesielt pluss er det om initiativet kommer fra utviklerne selv.

**Ingen management server** - Jeg vil ikke måtte installere noe på plattformen for å kunne begynne å kjøre kode. Alt i disse dager har ett API for å kunne snakke direkte i lag, og vi jobber jo med å modernisere IT.

**Forståelig struktur** - Etter hvert så blir alt av infrastrukturkode overveldende stort. Da hjelper det ikke på at det var vanskelig å forstå fra begynnelsen av.

# Hvordan starter man å bruke Infrastructure-as-Code

En vanlig taktikk for å komme i gang med automasjon er å se på hva som er irritasjonsmoment i organisasjonen. Kanskje det tar tid å få opprettet en server etter bestilling? Eller kanskje det er en prosess som er veldig avansert med høy sjanse for menneskelig feil, som resulterer i mye feilretting? Da kan det definitivt være verdt å bruke tid på automasjon.

Kanskje du er i en prosess med å innføre en ny plattform, eller skal koble opp det gamle datasenteret til skyen? Det burde være en fin sjanse for å innføre nye prosesser og rutiner. Det betyr ikke nødvendigvis at du trenger å automatisere alt, det er jo bedre å starte en plass enn å ikke starte i det hele tatt.
