# Kostenmeting — 19 oktober 2026

De cursus vraagt de context en het verschil tussen de context en de volledige run. Voor Codex heb ik een nieuwe CLI-sessie gebruikt; die rapporteerde input- en outputtokens.

| Model | Context (`/context`) | Totaal (`/cost`) | Jouw deel | Kost per run | Per maand (100 runs) | 10× | 1.000× |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Codex / GPT-5.6 Luna | n.v.t. voor Codex | 14.794 tokens | 14.784 input + 10 output | €0,00080 | €0,08 | €0,80 | €79,59 |

## Meting

Codex rapporteerde 14.784 inputtokens, waarvan 6.656 cached, en 10 outputtokens.
Ik gebruikte de cursusprijs als aanname: $0,10 per miljoen gewone inputtokens,
$0,01 per miljoen cached inputtokens en $0,50 per miljoen outputtokens, met $1 =
€0,90. Dat geeft ongeveer €0,00080 per run. De gerapporteerde modelnaam was
`gpt-5.6-luna`; die komt niet letterlijk overeen met de modelnaam in de cursus-
tabel, dus dit blijft een transparante prijsaanname.

## Schaalformule

`maandkost = kost per run × aantal runs per maand`. Bij 100 berichten per maand
geeft €0,00080 per run ongeveer €0,08 per maand, €0,80 bij 10× en €79,59 bij 1.000×.

De volledige tweede testpass staat in `build/test-set.md`.
