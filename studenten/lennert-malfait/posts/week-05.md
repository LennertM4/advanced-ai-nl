# Week 5 — Mijn score schommelt

Deze week testte ik de zekerheid van mijn e-mailsorteerder. De tool gebruikt `doen`, `lezen`, `negeren` en `herhaling`.

## Mijn foutmarge

Ik draaide v2 en v3 elk drie keer op dezelfde tien cases. V2 scoorde 8/10, 9/10 en 7/10. V3 scoorde 9/10, 8/10 en 7/10. De foutmarge is dus voor beide versies 7–9 op 10, met n = 10 per run. De bereiken overlappen volledig.

Mijn eerdere claim dat de gerichte v3-regel een bewezen verbetering gaf, trek ik daarom in. De regel helpt T01, maar de totale verbetering is niet bewezen. In verschillende runs wisselden vooral T04, T07 en T08 van label. Een score van 10/10 uit één run zou hier een te sterk verhaal vertellen.

## Model en effort

Mijn gok vooraf was dat lage effort voldoende zou zijn. De drie setups gebruikten hetzelfde model en dezelfde cases: medium scoorde 8/10, low 9/10 en high 8/10. Alle drie vallen binnen de foutmarge. Ik kies voorlopig low effort, omdat de score niet aantoonbaar slechter is en de taak eenvoudig is. De omgeving bood geen kleiner of groter Codex-model aan, dus dit is geen volledige modelvergelijking.

De CLI gaf geen betrouwbaar apart output-tokenveld. Daarom noteer ik de kost als benadering: ongeveer €0,00080 per run volgens de week-4-meting. Bij 1.200 runs per jaar is dat ongeveer €0,96.

## Mijn value chain, met de foutmarge erin

Handmatig schat ik 55 seconden per mail: 40 seconden lezen, 10 seconden beslissen en 5 seconden verplaatsen. Met de tool duurt draaien en nakijken 13 seconden. Bij 70% juist moet gemiddeld nog 30% van 55 seconden worden hersteld: samen 29,5 seconden. Bij 90% juist is dat 18,5 seconden. De winst is dus 25,5–36,5 seconden per mail.

Bij 100 berichten per maand is dat ongeveer 8,5–12,2 uur per jaar. Met €15 per uur als eigen aanname is de waarde €127,50–€182,50. Na de geschatte €0,96 toolkost blijft €126,54–€181,54 over. Mijn zwakste cijfer blijft de handmatige 55 seconden: die heb ik niet met een chronometer gemeten.

## De 20 nieuwe inputs

Ik heb de 20 kandidaten uit mijn inbox verwerkt tot een aparte geanonimiseerde
week-5-testset in `build/test-set.md`. Daarin staan per input een korte
samenvatting, het type bericht en het verwachte label. Ik heb geen letterlijke
mailteksten, namen, adressen, links of codes opgeslagen. Deze twintig cases zijn
nog niet in de score van 7–9/10 gebruikt; de score blijft dus gebaseerd op de
oude T01–T10-set. De volgende meting moet de twintig inputs eerst apart draaien,
zodat de uitbreiding niet stilzwijgend met de oude resultaten wordt vermengd.

## Mijn dashboard

De cijfers staan in `build/dashboard.html`. De belangrijkste boodschap staat bovenaan: v2 en v3 liggen allebei tussen 7 en 9 op 10. De dashboardlink wordt `https://raw.githack.com/LennertM4/advanced-ai-nl/week-05/studenten/lennert-malfait/build/dashboard.html` na het pushen.

## Mijn AI-ismen

- Week 2: “Daardoor kan ik de uitkomst ook gemakkelijk controleren.” Herschreven: “Ik vergelijk het JSON-label met de verwachte labelkolom.”
- Week 3: “Zo test ik niet alleen makkelijke schoolmails.” Herschreven: “T08 is Engels en T09 is een korte Canva-welkomstmail.”
- Week 3: “Dit is een goed teken, maar nog geen bewijs.” Herschreven: “T01 was 1 op 1 juist; de volledige set was nog niet opnieuw getest.”
- Week 4: “Daarom is dit een transparante schatting, geen factuurbedrag.” Herschreven: “De CLI noemde `gpt-5.6-luna`; ik gebruikte de cursusprijs als aanname.”
- Week 4: “De beslissing hangt dus meer af van de tijd die controle kost en van gemiste belangrijke mails dan van de kleine tokenkost.” Herschreven: “De 55 seconden handwerk en de controle veranderen de waarde sterker dan €0,96 toolkost.”

## Meting met 20 inputs

De 20 menselijke keuzes zijn vooraf vastgelegd in `build/week-05-answers.md`. Daarna zijn dezelfde inputs één voor één door classifier v3 gestuurd. De classifier kwam in **11 van de 20 gevallen overeen (55%)**. De volledige vergelijking staat in `build/week-05-measurement.md`.

De afwijkingen tonen vooral grensgevallen: context die voor Lennert bepaalt of een bericht actie vraagt of irrelevant is, staat niet altijd volledig in de geanonimiseerde input. Daarom blijven de menselijke keuzes de referentie voor deze meting.

