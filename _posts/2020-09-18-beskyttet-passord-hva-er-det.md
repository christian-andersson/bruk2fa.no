---
title: "Beskyttet passord, hva er det?"
slug: beskyttet-passord-hva-er-det
original_url: https://bruk2fa.no/blogg/beskyttet-passord-hva-er-det/
date: 2020-09-18T23:25:30
modified: 2020-10-04T10:10:01
layout: post
permalink: /blogg/beskyttet-passord-hva-er-det/
---

Jeg skriver på hovedsiden om «Beskyttet passord» hva mener jeg egentlig med det? Jo, det betyr helt enkelt at de gjør om passordet ditt på en sånn måte at det ikke er mulig å lese ut hva passordet ditt er.

Hvis man spør de som står bak en nettside så bruker de oftest si at passordet ditt er kryptert, men sanningen er at det mest sannsynlig er hashet. Årsaken til dette er at de som skriver disse svarene ikke tror at vi som spør skjønner hva hashing betyder og sier da at det er kryptert i stedet. Men hva er da forskjellen mellom kryptering og hashing? Svaret er enklere en hva man tror, og det er at når man krypterer noe så er det tenkt at man og kan dekryptere noe, dvs man skal kunne få tilbake originalen, mens når man hasher så er det en enveis funksjon, når du har en hash skal det være nært umulig å finne ut hva originalen er for noe. En nærmere forklaring på hva kryptering og hashing er finner du nedenfor,

## Hva er kryptering?

Å kryptere noe betyr at man skjuler informasjonen for å senere kunne lese det, en veldig enkel kryptering er [Cæsarchiffer](https://no.wikipedia.org/wiki/C%C3%A6sarchiffer), denne krypteringen går enkelt ut på at hver bokstav i alfabetet er byttet ut mot en annan, for eksempel at du skriver bokstaven Z i stedet for bokstaven A.

For eksempel La oss si at 2 personer vill skrive til hverandre uten at noen annen skal skjønne hva som skrives, så bestemmer de at de skal skifte alle A til D, alle B til E, etc dvs de bytter ut en bokstav med den 3:e etter den boksaven, og lar det gå rundt, dvs Å blir da C. Når disse 2 personer da kommet overens hvilka bokstever de skal bytte med andre så er det bare å begynne.

Hvis de da vil sende teksten «La det svinge, La det rock’n’ Roll» til hverandre så begynner man med L og erstatter det med O ettersom O er den 3:e bokstaven etter L, og sånn fortsetter de igjennom hele teksten. Resultatet blir da «Od ghw vzlqjh od ghw urfn q uroo» og for en person fra utsiden så klarer de ikke av å lese dette. Mottakeren tar da dette og bare gjør «motsatt» dvs tar O og tar den 3:e bokstaven foran i alfabetet og får L, og så videre.

Nå er Cæsarchiffer en ekstremt enkel kryptering, og i dag så er det omtrent ingen som blir lurt av dette, men prinsippet er det samme, dvs du har en text som krypteres av deg, så sender du dette til mottakeren og de kan da dekryptere teksten å lese det du skrev. Dagens løsninger for kryptering er derimot mye mer avanserte, for eksempel ta cæsarchiffer ovenfor, den bygger på at du har samme nøkkel på begge sider, det vil si hvilken bokstav som byttes ut mot en annen. Ulempen med dette er at hvis noen får tag i nøkkelen så kan de ikke bare lese det som sendes, de kan og sende egne meldinger.

Idag så har man ofte to nøkler, en for å kryptere (offentlig), og en for å dekryptere (privat), Hvis du da vil at en person skal kunne skrive noe til deg så gir du han din offentlige nøkkel, med den så kan han krypterer teksten, men han kan aldri med denne nøkkel dekryptere teksten igjen. Når så meldingen kommer til deg så bruker du din private nøkkel som du aldri skal gi til noen for å dekryptere teksten for å lese det avsenderen skrev til deg. Fordelen med dette er at du kan trygt gi din offentlige nøkkel til hvem som helst, det gjør heller ikke noe om en uærlig person får tag på din nøkkel, for det eneste han kan gjøre med den er kryptere en melding å sende den til deg, han kan ikke lese meldinger som andre sender til deg.

## Hva er da hashing?

Mens kryptering er til for å kunne sende en melding kryptert for å så kunne dekrypteres sånn at mottaker skal kunne lese, så brukes hashing når man ikke vill at noen skal kunne få ut originalen på nytt. Dette kan da brukes for å verifisere at den meldingen du har fått faktisk er korrekt, men denne funksjonen er og perfekt å bruke når man skal beskytte passord, får da kan ingen bruke hash verdien for å få ut originalen.

La oss se på en ekstremt enkel måte å utføre en hash på. Dette eksempel er på ingen måte en hash som skal brukes da den er totalt ubrukelig, men den skal derimot ses på som et eksempel på at man ikke kan finne ut originalen igjen. Det første man må gjøre er å bytte ut alle tegn man skriver med tall, i dette eksemplet så setter vi at mellomrom=0, a=1, b=2, etc. La oss da se på hvordan «La det svinge» ser ut. 12 1 0 4 5 20 0 19 22 9 14 7 5. Hvis man da tar og legger ihop alle disse tall så får man 118. Og her ser man da ganske enkelt at det er umulig å gå fra 118 tilbake igjen til «La det svinge». Årsaken til at jeg sier at metoden ovenfor for å hashe teksten er totalt ubrukelig er fordi at det er alt for enkelt å finne en annen tekst som får svaret 118. For eksempel «WWWWWC» gir 118, og det gikk veldig raskt å finne ut av dette. Det å finne en annen tekst som gir samme hash kalles at man har funnet en kollisjon

Dagens metoder for å beregne frem en hash er derimot mye mer avanserte matematiske funksjoner enn ovenfor som gjør at det kreves ekstremt avanserte maskiner som må utføre ekstremt mye arbeid for å kunne finne frem til en kombinasjon av tegn som gir en kollisjon, og dette kan ta så lang tid at det er ikke ens er verdt å prøve.

## Hvorfor hasher man passord og ikke krypterer?

Som beskrevet ovenfor så bruker man kryptering når man vill kunne hente ut originalen, mens når man bruker hashing så er ikke dette mulig, og når det gjelder passord, så er det ikke ønskelig for å kunne hente ut originalen. La oss ta ett eksempel, du har en konto på Facebook, Twitter, Snapchat eller Tiktok, hva hadde skjedd om noen klarer av å stjele din brukerinformasjon fra nettsiden?

Hvis passordet er kryptert og tyvene og hadde fått tak i nøkkelen for å dekryptere (nettsiden må ha denne nøkkelen selve), da hadde tyvene brukt denne nøkkel for å dekryptere ditt passord sånn at de kan lese det. Tyvene kommer da å prøve ut om du bruker samme passord på andre tjenester.

Hvis passordet er hashet så hadde tyvene fått tak i din hash, da hadde tyvene prøvd å se om din hash finnes i en liste over allerede eksisterende hasher, hvis de ikke finner den der, så hadde de gått videre til neste hashede passord til en annen bruker, fordi det tar alt for lang tid å prøve å finne en kollisjon. ditt passord er dermed mye mer beskyttet.

Som dere ser er da hashing mye smartere for en nettside å bruke, så neste gang en nettside sier at passord er kryptert, spør dem da om de ikke mener at passordet er hashet.
