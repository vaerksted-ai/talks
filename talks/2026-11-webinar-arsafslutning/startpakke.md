# Startpakke: AI-agent til årsafslutningen

Pakken hører til webinaret om din AI-bogholder den 25. nov. kl. 15. Den giver dig det, en AI-agent skal bruge for at gøre forarbejdet til årsafslutningen: en skill (faste instruktioner) og otte prompts, én pr. opgave.

Agenten gør forarbejdet. Du eller din bogholder gennemgår og godkender. Pakken erstatter ikke din bogholder eller revisor og giver ikke juridisk eller skattemæssig rådgivning.

Pakken dækker ikke årsrapporten, indberetninger eller lagertælling. Den indeholder heller ingen satser, grænser eller frister. Dem skal din bogholder give dig for det aktuelle år.

## Før du går i gang

1. Du skal bruge en AI-assistent, hvor du kan lægge faste instruktioner ind og uploade filer, fx ChatGPT eller Claude. Har du ingen endnu, så opret en gratis konto hos en af dem. Kan din assistent ikke gemme faste instruktioner, så indsæt skill'en nedenfor som første besked i en ny samtale.
2. Giv kun læseadgang, helst eksportfiler i stedet for login. Det kan være eksport fra dit regnskabsprogram (fx Dinero, e-conomic, Billy), bankudtog og din bilagsmappe. Agenten foreslår kun. Du eller din bogholder beslutter.
3. Tjek, hvor din AI-assistent gemmer data, før du uploader. Send ikke lønsedler eller CPR-numre, og fjern dem fra bankudtog og bilag, hvis de står der.
4. Fortæl agenten fem ting først: virksomhedsform (fx enkeltmandsvirksomhed, I/S, ApS), regnskabsår, balancedato, momsperiode (måned, kvartal eller halvår) og regnskabsprogram. Uden dem gætter agenten.
5. Kør én prompt ad gangen. Læs resultatet, før du går videre.
6. Tjek tre tal mod bilaget, før du stoler på resultatet.

## Skill: årsafslutning, forarbejde

Navn: aarsafslutning-forarbejde

Beskrivelse: Brug når en ejer eller bogholder vil forberede årsafslutningen i en dansk virksomhed.

Instruktioner til agenten:

- Du forbereder årsafslutningen. Du bogfører ikke, indberetter ikke og ændrer ikke i regnskabsprogrammet. Du foreslår kun.
- Spørg først efter virksomhedsform, regnskabsår, balancedato, momsperiode og regnskabsprogram, hvis de ikke er oplyst.
- Hvert forslag skal pege på kilden: bilag, bankpost eller konto. Kan du ikke pege på en kilde, så skriv "ukendt, spørg" i stedet for at gætte.
- Gæt aldrig beløb, datoer eller kontonumre. Foreslå konto i ord (fx "software"), aldrig som kontonummer.
- Skriv tvivl som tvivl ("ser ud til"), ikke som fakta.
- Del altid svaret i tre: det der ser rigtigt ud, det der afviger, og det der mangler.
- Ved tvivl om regler, moms, skat eller afskrivninger: skriv spørgsmålet ned til bogholderen. Giv ikke selv et svar.
- Ser du lønsedler eller CPR-numre i materialet, så stop og bed om, at de fjernes.
- Skriv på dansk, i korte sætninger, uden fagudtryk du ikke forklarer.
- Slut hver opgave med en liste: "Det skal du eller din bogholder beslutte".

## Prompt 1: Bilag, bank og fejl

"Her er bankudtog og bogføringseksport for [regnskabsår]. 1) Match hver bankpost med et bilag: samme beløb, dato inden for 7 dage, modtager passer, ét bilag til én post. Passer to bilag, så vis begge og vælg ikke. 2) Vis bankposter uden bilag i en tabel (dato, beløb, tekst), og hold løn, gebyrer, renter, skat, moms og egne overførsler i en separat liste. 3) Vis bilag uden bankpost. 4) Find det, der ser ud til at være dobbeltbetaling, privat udgift eller et beløb, der er langt fra det sædvanlige for modtageren. Skriv 'ser ud til', ikke at det er sikkert. Sorter efter beløb, største først. Hvis noget skal afgøres af min bogholder, så skriv det som et spørgsmål til bogholderen. Gæt ikke."

## Prompt 2: Stemmer banken?

"Sammenlign saldoen på hver bankkonto i regnskabet med bankudtoget pr. [balancedato]. Tag alle konti med: opsparing, kreditkort, valutakonto, MobilePay og udbetalinger fra webshop eller betalingstjenester. Vis forskellen pr. konto og de poster, der kan forklare den, med dato. Skil poster med forskellig dato fra poster, der slet ikke kan forklares. Skriv, hvad der er uforklaret. Gæt ikke."

## Prompt 3: Kunder der ikke har betalt

"Lav en liste over åbne fakturaer pr. [balancedato], sorteret efter alder. Tjek først mod banken, så jeg ikke rykker for noget, der er betalt. Foreslå en kort, høflig rykkertekst til hver faktura over 30 dage. Skriv ikke gebyr eller rente i teksten, det beslutter jeg eller min bogholder. Vis meget gamle eller bestridte fakturaer, kreditnotaer og forudbetalinger i en egen liste til min bogholder, og afgør ikke selv, om noget er tabt. Send intet. Jeg godkender teksterne først."

## Prompt 4: Leverandører og periodisering

"Lav tre lister pr. [balancedato]: 1) ubetalte leverandørfakturaer, 2) udgifter betalt i år, som ser ud til at høre til næste år (fx forsikring og abonnementer), 3) udgifter, der ser ud til at høre til i år, men endnu ikke er faktureret. Brug regnskabsåret, ikke nødvendigvis kalenderåret. Regn ikke på periodiseringen selv. Skriv spørgsmålene til min bogholder."

## Prompt 5: Moms

"Her er momsangivelserne, som jeg selv har hentet, og momskontiene fra regnskabet for [regnskabsår]. Du har ikke adgang til Skat. Sammenlign periode for periode og vis afvigelser. Den sidste periode er måske ikke indberettet endnu: skriv i så fald, hvad der mangler, i stedet for at sammenligne. Afgør ikke selv poster, hvor moms ofte er særlig: løn, bankgebyrer, forsikring, køb fra udlandet, restaurant og repræsentation, privat brug. Skriv dem som spørgsmål til min bogholder. Forklar kun det, du kan se i tallene."

## Prompt 6: Anlægskøb

"Find køb i [regnskabsår] over [beløb fra min bogholder]. Vis dato, modtager, beløb og tekst. Afgør ikke selv, om noget skal afskrives. Skriv det som spørgsmål til min bogholder."

## Prompt 7: Privat forbrug og hævninger

"Find bankposter, der ser ud til at være private, og hævninger eller overførsler til mig som ejer. Vis dem i en liste med beløb. Vurder ikke, hvordan de skal bogføres. Skriv spørgsmålene til min bogholder."

## Prompt 8: Spørgsmål til bogholderen

"Her er resultaterne fra opgave 1 til 7: [indsæt]. Saml dem i ét dokument til min bogholder, højst én side, på dansk: hvad ser rigtigt ud, hvad afviger, hvad mangler. Til sidst højst fem spørgsmål, hver i én sætning, sorteret efter kroner, største beløb først. Gæt ikke."

## Det her skal din bogholder selv tage stilling til

Løn, feriepenge, skyldig A-skat og AM-bidrag, lagertælling og selve årsrapporten ligger uden for pakken. Tag dem med til din bogholder.

