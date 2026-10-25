# Modeltest — 21 oktober 2026

## Mijn gok vooraf

Mijn verwachting was dat lage effort voldoende zou zijn. Deze taak heeft vier
vaste labels en korte input; meer reasoning lijkt waarschijnlijk weinig extra
waarde te geven.

## Resultaat

Ik gebruikte dezelfde tien cases en dezelfde v3-regels. De verwachte labels
staan vooraf in `build/test-set.md`. De zichtbare CLI-output bevatte geen
betrouwbaar afzonderlijk output-tokenveld; daarom noteer ik de kost als een
transparante benadering op basis van de week-4-run, niet als exacte factuur.

| Setup | Model | Effort | Score (n = 10, 1 run) | Binnen foutmarge 7–9? | Outputtokens | Kost/run (benadering) | Per jaar (1.200 runs) |
| --- | --- | --- | ---: | --- | ---: | ---: | ---: |
| A standaard | `gpt-5.6-luna` | medium | 8/10 | ja | niet apart beschikbaar | ± €0,00080 | ± €0,96 |
| B omlaag | `gpt-5.6-luna` | low | 9/10 | ja | niet apart beschikbaar | ± €0,00080 | ± €0,96 |
| C omhoog | `gpt-5.6-luna` | high | 8/10 | ja | niet apart beschikbaar | ± €0,00080 | ± €0,96 |

Alle drie scores vallen binnen de foutmarge. Op basis van deze meting is low
effort de logischste keuze: dezelfde taakscore als medium/high, met de laagste
verwachte rekentijd. Ik heb geen kleiner of groter Codex-model kunnen testen;
de omgeving bood alleen `gpt-5.6-luna` aan.

De kostbenadering gebruikt de week-4-meting van 14.784 inputtokens, waarvan
6.656 cached, en 10 zichtbare outputtokens. De verborgen reasoning-tokens zijn
niet apart betrouwbaar uit de CLI-output af te leiden, dus ik doe daar geen
preciese claim over.
