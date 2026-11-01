# Humanizer NL

Herschrijf Nederlandstalige AI-tekst in natuurlijk Nederlands, met behoud van feiten en de stem van de schrijver. Gericht op taalgebruik in Nederland. De skill geeft standaard alleen de eindtekst terug.

**Voor:**
> Laten we dieper ingaan op onze baanbrekende update. Het is niet zomaar een functie, het is een revolutie. Vanaf maandag kunnen twee mensen tegelijk hetzelfde document bewerken. Laat dat even bezinken.

**Na:**
> Vanaf maandag kunnen twee mensen tegelijk hetzelfde document bewerken.

## Installatie

Installeer met de Skills CLI voor een ondersteunde agent, bijvoorbeeld:

```bash
npx skills add pinkroosterai/humanizernl --global --agent codex
npx skills add pinkroosterai/humanizernl --global --agent claude-code
```

Gebruik `--agent '*'` voor alle ondersteunde agents. Laat `--global` weg voor installatie in het huidige project. Je kunt ook de hoofdmap met `SKILL.md` naar de skillmap van je agent kopiëren. Voor omgevingen die skills als ZIP laden, upload je deze repository als ZIP.

Voor Claude Code als plugin:

```text
/plugin marketplace add pinkroosterai/humanizernl
/plugin install humanizer-nl@humanizer-nl
```

De plugin gebruikt `/humanizer-nl:humanizer-nl`. Andere installaties gebruiken doorgaans `/humanizer-nl`; de precieze aanroep hangt van de agent af. De Nederlandse versie kan naast het origineel bestaan.

## Gebruik

```text
/humanizer-nl

Herschrijf deze tekst:
[plak je tekst]
```

Of vraag: “Maak deze tekst natuurlijker met humanizer-nl.” Geef voor stembehoud twee of drie alinea’s van jezelf mee als schrijfvoorbeeld. De skill volgt je woordkeus, ritme en interpunctie en behoudt de aanspreekvorm. Hij legt geen vast taalniveau op.

Voor een bestand: “Herschrijf de lopende tekst in docs/artikel.md met humanizer-nl.” Code, gegevens, metadata en linkdoelen blijven intact. Na bestandsbewerking volgt een korte samenvatting. Vraag expliciet om toelichting als je de redactie wilt bespreken.

## Werkwijze

De skill leest de tekst, beoordeelt patronen, herschrijft en vergelijkt de uitkomst met de bron. Die controle blijft intern. Feiten, onzekerheid en betekenis blijven behouden. Een natuurlijke tekst hoeft niet te veranderen. De skill vertaalt geen anderstalige tekst zonder opdracht en is niet bedoeld om AI-detectoren te omzeilen.

## De 26 patronen

De eerste vijf patronen krijgen als eerste aandacht. De redactie blijft afhankelijk van context. Een zwak signaal, zoals een gedachtestreepje of lijdende vorm, is op zichzelf geen reden om tekst te veranderen. De volledige voorwaarden staan in [SKILL.md](SKILL.md).

### A. Nadruk zonder inhoud

| # | Patroon | Voor | Na |
|---|---|---|---|

| 1 | **Niet X maar Y** | Het is niet zomaar een update, het is een revolutie. De update maakt samen bewerken mogelijk. | Met de update kun je samen bewerken. |

| 2 | **Dramatische slotzinnen en losse flarden** | De opslag is verdubbeld. Laat dat even bezinken. | De opslag is verdubbeld. |

| 3 | **Schijnbaar diepzinnige uitspraken** | In de kern is vertrouwen de brandstof van samenwerking. | Samenwerken vraagt om vertrouwen. |

| 4 | **Een aanloop voor het punt** | Laten we eens kijken naar de kosten. Het abonnement kost 12 euro per maand. | Het abonnement kost 12 euro per maand. |

| 5 | **Reageren op een ongenoemd bezwaar** | Begrijp me niet verkeerd, ik zeg niet dat overleg zinloos is. We moeten vandaag beslissen. | We moeten vandaag beslissen. |

### B. Ritme volgens een vast recept

| # | Patroon | Voor | Na |
|---|---|---|---|

| 6 | **Geforceerde drietallen** | Een inspirerende, vernieuwende en baanbrekende bijeenkomst over de nieuwe wet. | Een bijeenkomst over de nieuwe wet. |

| 7 | **Herhaalde zinsopeningen** | Ze zag de deur. Ze zag het slot. Ze onthield beide. | Ze zag de deur en het slot en onthield beide. |

| 8 | **Gedachtestreepjes als standaardverbinding** | Het besluit — gisteren genomen — geldt — vanaf maandag — voor iedereen. | Het gisteren genomen besluit geldt vanaf maandag voor iedereen. |

| 9 | **Opgestapelde voorbehouden** | Het zou mogelijk wellicht kunnen helpen. | Het zou kunnen helpen. |

| 10 | **Losse samenstellingen en onnodige koppeltekens** | Het klanten service team schrijft een project-plan. | Het klantenserviceteam schrijft een projectplan. |

| 11 | **Lijdende vorm en verborgen handelende persoon** | De controle wordt door de beheerder uitgevoerd. | De beheerder voert de controle uit. |

### C. Opgeblazen taal en geleend gezag

| # | Patroon | Voor | Na |
|---|---|---|---|

| 12 | **Versleten woorden en vertaald Engels** | We maken een verschil door deze uitdaging te adresseren en onze workflow te optimaliseren. | We pakken dit probleem aan en verbeteren onze werkwijze. |

| 13 | **Overdreven betekenis** | De opening in 2024 markeerde een cruciaal keerpunt naar een stralende toekomst. | De opening was in 2024. |

| 14 | **Vage verbanden** | Zij is verbonden aan het koor, dat zij heeft opgericht en dirigeert. | Zij heeft het koor opgericht en dirigeert het. |

| 15 | **Aangeplakte betekenis in bijzinnen** | De winkel opent maandag, wat getuigt van een ongekende inzet voor de gemeenschap. | De winkel opent maandag. |

| 16 | **Reclametaal** | Ontdek dit adembenemende pareltje: een ongeëvenaard hotel met 20 kamers in Delft. | Het hotel in Delft heeft 20 kamers. |

| 17 | **Geleend gezag** | Volgens experts is dit een baanbrekende ontwikkeling. De proef start dinsdag. | De proef start dinsdag. |

| 18 | **Omslachtige werkwoorden en naamwoordstijl** | Er vindt een beoordeling van de aanvraag plaats door de commissie. | De commissie beoordeelt de aanvraag. |

### D. Opmaak volgens een vast recept

| # | Patroon | Voor | Na |
|---|---|---|---|

| 19 | **Vet als versiering** | **Kosten:** De kosten bedragen 12 euro. | De kosten bedragen 12 euro. |

| 20 | **Versierde koppen** | ## 🚀 Onze Nieuwe Strategische Samenwerking | ## Onze nieuwe strategische samenwerking |

| 21 | **Inconsistente aanhalingstekens** | Hij zei “morgen”. Zij zei "vandaag". | Hij zei “morgen”. Zij zei “vandaag”. |

### E. Resten van het gesprek en het concept

| # | Patroon | Voor | Na |
|---|---|---|---|

| 22 | **Chatbotformuleringen** | Goede vraag! De winkel sluit om 18.00 uur. Ik hoop dat dit helpt! | De winkel sluit om 18.00 uur. |

| 23 | **Modelbeperkingen en gokwerk** | Volgens mijn laatste trainingsupdate is het bedrijf vermoedelijk in 1990 opgericht. | De oprichtingsdatum is onzeker. |

| 24 | **De kop herhalen in de eerste zin** | ## Openingstijden  Hier volgen de openingstijden. Op maandag zijn we gesloten. | ## Openingstijden  Op maandag zijn we gesloten. |

| 25 | **Over de tekst schrijven in plaats van het onderwerp** | De onderstaande tabel toont de prijzen. Het abonnement kost 12 euro per maand. | Het abonnement kost 12 euro per maand. |

### F. Schrijven voor de verkeerde lezer

| # | Patroon | Voor | Na |
|---|---|---|---|

| 26 | **Herhalen wat de lezer al weet** | Zoals je zelf al schreef, is vrijdag te laat. Daarom stel ik donderdag voor. | Ik stel donderdag voor. |

## Ontwikkeling

Er is geen bouwstap. Controleer het pakket met:

```bash
python3 scripts/validate-package.py
npx skills add . --list
claude plugin validate .
```

## Herkomst en licentie

Nederlandse bewerking van [Humanizer van blader](https://github.com/blader/humanizer), onder de [MIT-licentie](LICENSE). De oorspronkelijke patronen zijn mede gebaseerd op Wikipedia’s “Signs of AI writing”; de Nederlandse bewerking is geen onderzoek naar de betrouwbaarheid van die signalen.

Zie [CHANGELOG.md](CHANGELOG.md) voor de versiegeschiedenis.
