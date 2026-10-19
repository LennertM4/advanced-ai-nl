# Week 4 — Wat kost mijn e-mailsorteerder?

## Mijn tool in cijfers

Mijn tool sorteert een Outlook-bericht in `doen`, `lezen`, `negeren` of `herhaling`. In de eerste v2-run waren 9 van 10 inputs juist (n = 10, 1 run). De enige fout was T01, een F1-fout: een aanbeveling om een laptop mee te brengen werd als verplichte actie gelezen. Na één gerichte regel en een voorbeeld in v3 gaf de tool voor T01 het juiste label `lezen` (1 op 1, n = 1, 1 run). Daarna heb ik v3 opnieuw getest in tien aparte Codex-sessies: 10 van 10 waren juist (n = 10, 1 run). Omdat dat 10 op 10 was, voegde ik drie moeilijke, geanonimiseerde Outlook-inputs toe: dubbelzinnig, heel kort en Engels. Die extra run was 3 op 3 juist (n = 3, 1 run). In de tweede volledige run en de extra run waren F1 tot en met F6 dus 0.

## Wat kost één run?

De kostenmeting staat in `build/kosten.md`. In een nieuwe Codex-sessie gaf de run 14.784 inputtokens, waarvan 6.656 cached, en 10 outputtokens. Met de cursusprijs als aanname ($0,10 per miljoen gewone inputtokens, $0,01 per miljoen cached inputtokens en $0,50 per miljoen outputtokens, omgerekend met $1 = €0,90) kost deze run ongeveer €0,00080. Bij 100 berichten per maand is dat ongeveer €0,08; bij 1.000 keer dat volume €79,59. Met dezelfde tokens zou GPT-6.1 Sol ongeveer €0,01532 per run kosten, of €1,53 per maand bij 100 berichten. De modelnaam was `gpt-5.6-luna`, terwijl de cursus een vergelijkbare maar anders genoemde Luna-prijs geeft. Daarom is dit een transparante schatting, geen factuurbedrag.

## Met de hand of met de tool?

Met de hand open ik een bericht, lees ik onderwerp en inhoud, beslis ik welk label past en verplaats ik het bericht. Ik schat dit op 55 seconden per mail: 40 seconden lezen, 10 seconden beslissen en 5 seconden verplaatsen. De bron is mijn eigen inbox en een eerste schatting. Met de tool duurt het uitvoeren naar schatting 3 seconden. Ik reken daarnaast 10 seconden menselijke controle, omdat een foutieve `doen`- of `negeren`-classificatie gevolgen kan hebben. De totale tijd wordt dan 13 seconden. De winst is 42 seconden per bericht.

Ik gebruik als scenario mijn eigen studenteninbox en schat 100 berichten per maand die echt een label nodig hebben. Dat is 1.200 berichten per jaar. De tijdswinst is ongeveer 3,5 minuten per werkdag, 17,5 minuten per week, 70 minuten per maand en 14 uur per jaar bij dit maandvolume. Bij een geschatte uurwaarde van €15 is dat €210 bruto tijdwaarde per jaar. De jaarlijkse toolkost is ongeveer €0,96. Er blijft dus ongeveer €209,04 netto over. Deze berekening geldt alleen als de controle inderdaad tien seconden duurt en alle 100 berichten anders handmatig behandeld zouden worden.

## Mijn zwakste cijfer

Mijn zwakste cijfer is de handmatige 55 seconden. Ik heb die tijd nog niet met een chronometer gemeten. Als de echte tijd maar 30 seconden is, daalt de winst naar 17 seconden per bericht en wordt de jaarlijkse waarde ongeveer €85 bij hetzelfde volume en uurloon. Ook de testset blijft klein: een volledige run van tien en een extra run van drie moeilijke berichten zeggen nog weinig over alle mogelijke e-mails. De beslissing hangt dus meer af van de tijd die controle kost en van gemiste belangrijke mails dan van de kleine tokenkost. Ik zou de tool voorlopig alleen gebruiken met menselijke controle.
