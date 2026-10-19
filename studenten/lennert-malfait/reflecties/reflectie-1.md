# Reflectie 1

## Wat kan mijn tool nu?

Mijn tool kan een geanonimiseerde Outlook-mail in precies één van vier labels plaatsen: `doen`, `lezen`, `negeren` of `herhaling`. De huidige v3-prompt bevat ook een regel voor een aanbeveling met een expliciet alternatief.

## Wat kan hij niet?

De tool weet niet vanzelf welke informatie voor mij persoonlijk belangrijk is. Hij kan een dubbelzinnige mail verkeerd inschatten en controleert niet of een deadline werkelijk in mijn agenda staat. Menselijke controle blijft dus nodig, zeker voor `doen` en `negeren`.

## Welk cijfer bewijst dat?

In de eerste v2-run waren 9 van 10 labels juist (n = 10, 1 run). T01 was een F1-fout. Na de gerichte wijziging gaf v3 voor T01 `lezen`: 1 op 1 juist (n = 1, 1 run). In een tweede volledige v3-run waren 10 van 10 labels juist (n = 10, 1 run). Dat is een verbetering in deze testset, maar nog geen bewijs van algemene betrouwbaarheid.
