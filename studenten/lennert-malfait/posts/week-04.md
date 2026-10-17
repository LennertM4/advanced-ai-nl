# Week 4 — Wat kost mijn e-mailsorteerder?

## Mijn tool in cijfers

Mijn tool sorteert een Outlook-bericht in `doen`, `lezen`, `negeren` of `herhaling`. In de eerste v2-run waren 9 van 10 inputs juist (n = 10, 1 run). De enige fout was T01, een F1-fout: een aanbeveling om een laptop mee te brengen werd als verplichte actie gelezen. Na één gerichte regel en een voorbeeld in v3 gaf de tool voor T01 het juiste label `lezen` (1 op 1, n = 1, 1 run). De foutverdeling van die run is dus F1: 1; F2 tot en met F6: 0. Een volledige tweede run van alle tien inputs moet nog in verse gesprekken gebeuren.

## Wat kost één run?

De kostenmeting is voorbereid in `build/kosten.md`. De cursus vraagt eerst de context vóór de vraag en daarna het totaal van de run. Het verschil is mijn deel: de classifierprompt, de e-mail en het JSON-antwoord. In deze Codex-sessie zijn `/context` en `/cost` niet beschikbaar als meetcommando's, dus ik vul daar geen verzonnen cijfers in. De prijsaanname uit de les is $1 per miljoen inputtokens en $5 per miljoen outputtokens, omgerekend met $1 = €0,90. Bij een voorbeeldkost van €0,002 per run kost 100 berichten per maand €0,20, 1.000 berichten €2 en 100.000 berichten €200. Dat laat zien dat volume pas bij zeer grote aantallen zwaar doorweegt. Een echte API-run moet de voorbeeldkost bevestigen.

## Met de hand of met de tool?

Met de hand open ik een bericht, lees ik onderwerp en inhoud, beslis ik welk label past en verplaats ik het bericht. Ik schat dit op 55 seconden per mail: 40 seconden lezen, 10 seconden beslissen en 5 seconden verplaatsen. De bron is mijn eigen inbox en een eerste schatting. Met de tool duurt het uitvoeren naar schatting 3 seconden. Ik reken daarnaast 10 seconden menselijke controle, omdat een foutieve `doen`- of `negeren`-classificatie gevolgen kan hebben. De totale tijd wordt dan 13 seconden. De winst is 42 seconden per bericht.

Ik gebruik als scenario mijn eigen studenteninbox en schat 100 berichten per maand die echt een label nodig hebben. Dat is 1.200 berichten per jaar. De tijdswinst is ongeveer 3,5 minuten per werkdag, 17,5 minuten per week, 70 minuten per maand en 14 uur per jaar bij dit maandvolume. Bij een geschatte uurwaarde van €15 is dat €210 bruto tijdwaarde per jaar. Daar trek ik de API-kost van de tool af zodra de runmeting is ingevuld. Bij €0,002 per run blijft ongeveer €207,60 netto over. Deze berekening geldt alleen als de controle inderdaad tien seconden duurt en alle 100 berichten anders handmatig behandeld zouden worden.

## Mijn zwakste cijfer

Mijn zwakste cijfer is de handmatige 55 seconden. Ik heb die tijd nog niet met een chronometer gemeten. Als de echte tijd maar 30 seconden is, daalt de winst naar 17 seconden per bericht en wordt de jaarlijkse waarde ongeveer €85 bij hetzelfde volume en uurloon. De beslissing hangt dus meer af van de tijd die controle kost en van gemiste belangrijke mails dan van de kleine tokenkost.
