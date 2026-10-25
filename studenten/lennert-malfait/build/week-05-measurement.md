# Week 5 — meting met 20 menselijke inputs

De menselijke labels en redenen zijn vooraf ingevuld in [week-05-answers.md](week-05-answers.md). Daarna zijn dezelfde 20 geanonimiseerde inputs één voor één door classifier v3 gestuurd. De menselijke keuze blijft de referentie; de classifier wordt achteraf niet gebruikt om die keuze te wijzigen.

Modelrun: `gpt-5.6-luna`, `reasoning_effort=low`, één input per run.

| ID | Mens | Classifier v3 | Match |
| --- | --- | --- | --- |
| W5-01 | doen | doen | ja |
| W5-02 | lezen | doen | nee |
| W5-03 | herhaling | herhaling | ja |
| W5-04 | doen | lezen | nee |
| W5-05 | lezen | lezen | ja |
| W5-06 | lezen | lezen | ja |
| W5-07 | doen | lezen | nee |
| W5-08 | negeren | lezen | nee |
| W5-09 | lezen | lezen | ja |
| W5-10 | doen | doen | ja |
| W5-11 | lezen | lezen | ja |
| W5-12 | doen | lezen | nee |
| W5-13 | negeren | lezen | nee |
| W5-14 | lezen | lezen | ja |
| W5-15 | lezen | lezen | ja |
| W5-16 | negeren | lezen | nee |
| W5-17 | negeren | negeren | ja |
| W5-18 | lezen | negeren | nee |
| W5-19 | negeren | lezen | nee |
| W5-20 | negeren | negeren | ja |

**Resultaat: 11/20 = 55%.**

De grootste afwijkingen zitten bij grensgevallen: de classifier kiest daar vaak `lezen`, terwijl Lennert op basis van zijn eigen context `doen` of `negeren` koos. Dat is precies de reden om menselijke input als meetreferentie te bewaren.
