# Lotteritrekning

Et enkelt verktøy for å trekke vinnere i lotteri, laget for Skautrollet 4H. Alt ligger i én HTML-fil (`Lotteritrekning.html`). Du trenger ikke installere noe, og det trengs ingen server eller internettforbindelse.

**Bruk det direkte i nettleseren: https://estromsnes.github.io/Lotteritrekning/Lotteritrekning.html**

## Skjermbilder

**Hovedvisning**: oppsett av loddbøker, trekning og vinnerliste.

![Hovedvisning](docs/hovedvisning.png)

**Projektorvisning**: vises på storskjerm under trekningen.

![Projektorvisning](docs/projektorvisning.png)

## Funksjoner

- Legg til loddbøker med bokstav og nummerserie, for eksempel `K 1–63`. Bokstaven er valgfri, så lodd med bare tall (`1–200`) fungerer også.
- Lagre og last inn sikkerhetskopi av oppsett og trekninger som fil.
- Trekning med rulleanimasjon, konfetti og valgfri lyd.
- Egen projektorvisning for storskjerm, som kan åpnes i et nytt vindu eller i fullskjerm.
- Premie kan oppgis for hver trekning.
- «Ikke til stede – trekk på nytt» markerer loddet som ugyldig og trekker et nytt.
- Angre siste trekning.
- Vinnerliste som kan skrives ut.
- Dataene lagres automatisk i nettleseren (`localStorage`), så de overlever en omlasting av siden.

## Kom i gang

1. Åpne [lenken til verktøyet](https://estromsnes.github.io/Lotteritrekning/Lotteritrekning.html) i en moderne nettleser (Chrome, Edge, Firefox eller Safari). Vil du bruke det uten internett, kan du i stedet laste ned `Lotteritrekning.html` (på GitHub: åpne filen, velg «Download raw file») og åpne den fra maskinen.
3. Skriv inn navn på lotteriet øverst.
4. Under **1. Legg til loddbøker** fyller du inn bokstav (valgfri), «Fra nr.» og «Til nr.», og trykker **Legg til** eller Enter. «Til nr.» er siste solgte lodd. Tallene kan endres senere.
5. Skriv eventuelt inn en premie under **2. Trekning**, og trykk **Trekk lodd**.

Tips: prøv gjerne en testtrekning først, og bruk **Nullstill alt** før den ekte trekningen.

## Sjekkliste på lotteridagen

1. Åpne siden og skriv inn navn på lotteriet.
2. Legg inn alle solgte loddbøker.
3. Lagre en sikkerhetskopi (**Lagre sikkerhetskopi**).
4. Koble til projektor og åpne projektorvisningen. Trykk `F` for fullskjerm.
5. Skriv inn premie, trekk, og noter vinnerens navn og telefonnummer på den utskrevne vinnerlisten.

## Projektorvisning

- **Åpne projektorvisning i nytt vindu**: dra vinduet over til projektoren og trykk `F` for fullskjerm. Du styrer fra det opprinnelige vinduet, eller fra projektorvinduet. De to vinduene holdes synkronisert.
- **Fullskjerm i dette vinduet**: viser trekningen i samme vindu.

Taster i visningen:

| Tast | Funksjon |
|------|----------|
| Mellomrom / Enter | Trekk lodd |
| `N` | Ikke til stede, trekk på nytt |
| `F` | Fullskjerm av/på |
| `M` | Lyd av/på |
| `Esc` | Lukk visningen |

## Om trekningen

Trekningen bruker `crypto.getRandomValues` uten modulo-skjevhet, så alle gjenværende lodd har like stor sjanse. Et lodd kan bare trekkes én gang, og samme loddnummer telles bare én gang selv om bøkene overlapper.

## Lisens

MIT-lisens. Se [LICENSE](LICENSE).

## Merknader

- Data lagres lokalt i nettleseren på den maskinen som brukes. Bruker du en annen nettleser eller maskin, starter du med et tomt oppsett, med mindre du flytter oppsettet med **Lagre/Last inn sikkerhetskopi**. Å tømme nettleserdata sletter også oppsettet.
- **Nullstill alt** sletter både loddbøker og trekninger.
- Navn og telefonnummer til vinnere må noteres for hånd i den utskrevne vinnerlisten.
