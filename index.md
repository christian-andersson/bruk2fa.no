---
title: "Hva er 2FA?"
slug: hva-er-2fa
original_url: https://bruk2fa.no/
date: 2020-08-28T21:37:26
modified: 2022-08-10T13:30:49
layout: page
permalink: /
---

2FA (tofaktorautentisering) er kjent ved mange navn, men i korthet betyr det at man bruker 2 faktorer ved innlogging, dvs man legger på en ekstra sikkerhet foruten bare passordet. Det mest kjente 2FA systemet i Norge er BankID (og BankID på mobil).

Litt lenger forklart så er 2FA en del av Multi Factor Authentication (MFA), dvs at man bruker mer enn 1 faktor for å komme inn i et system, 2FA er bare at man bruker 2, men det finnes systemer som krever at man bruker fler enn 2 faktorer. Når det gjelder faktorer så brukes de deles inn i ulike grupper, se og [Ulike former av 2FA](#ulikeformerav2fa)\
Noe du vet, dvs passord, pin kode og lignende.\
Noe du har, for eksempel en mobil, en app installert på mobilen og lignende.\
Noe du er, her inkluderer man for eksempel fingeravtrykk, ansikt eller lignende.\
Det kan og være andre faktorer som for eksempel hvor du er.

BankID på mobil, som nevnt ovenfor, benytter seg av 2 faktorer; Noe du har, dvs mobiltelefonen – uten mobiltelefon så kan du ikke bruke bankid på mobil. Noe du vet, dvs passordet til BankID, foruten om dette så kan du ikke logge inn.

Mange nettsider støtter en eller annen form av 2 faktor. For eksempel Norsk Tipping støtter 2FA: Når du logger inn så får du en kode på SMS (Igjen så er det noe du har, dvs mobiltelefon) som du må skrive inn på nettsiden.

**Hvorfor bruke 2FA**

Gjennom å bruke 2FA så legger du inn ekstra sikkerhet til kontoen din du prøver å bruke. Nesten hver dag er det en tjeneste på nettet som blir hacket og informasjon om de som bruker denne tjenesten blir stjålet. Det kan da være at ditt brukernavn (ofte din e-post adresse) og en beskyttet variant av ditt passord da kommer på avveie. Hvis du er virkelig uheldig så er til og med passordet ubeskyttet, eller såpass svakt, at de som stjeler informasjonen vet både brukernavnet og passordet ditt. De kan da begynne og teste ut andre tjenester med brukernavnet og passordet som de fant. Plutselig så har de kommet inn på din konto andre steder. Det er dessverre veldig vanlig at folk bruker samme passord på flere steder, eller små variasjoner på passordet. Hvis du hadde brukt 2FA på de andre tjenestene så hadde de ikke kunnet komme inn, fordi de ikke hadde hatt tilgang til din andre faktor. De andre tjenestene hadde da vært beskyttet til tross for at de visst både brukernavnet og passordet ditt.

Nå synes du kanskje at det å taste inn en ekstra kode fra en app, eller vente på en SMS, blir for mye arbeid, men ta det med ro: De fleste tjenester på nett husker maskinen eller nettleseren din, sånn at den bruker dette som andre faktor. Derfor trenger du ikke nødvendigvis å skrive inn en kode hver gang du skal inn på tjenesten. Andre nettsider derimot, som for eksempel nettbanker, tvinger deg alltid til å bruke 2FA. Dette er for å kunne bekrefte at du er du, og at du har lov til å bruke tjenesten.

2FA Bidrar dermed til å gi deg ekstra beskyttelse på nettet.\

**Hvordan aktivere 2FA**

Dette er ulikt fra tjeneste til tjeneste, og hvilken form av 2FA tjenesten tilbyr. De fleste nettsider bruker ha aktivering av 2FA på samme side der man bytter passord, om det er profilsiden din, eller en side for sikkerhetsinnstillinger.

**Hvor kan jeg bruke 2FA**

Det finnes ikke en komplett liste over hvilke nettsteder eller tjenester som støtter 2FA, men på dette nettstedet så kan man finne ut hvem av de største nettstedene støtter 2FA [https://2fa.directory/](https://2fa.directory/)

<a id="ulikeformerav2fa"></a>
**Ulike former av 2FA**

Som beskrevet i Hva er 2FA så finnes det flere typer av Faktorer man kan bruke for å autentisere seg. Her går vi i mer detalj på de ulike faktorene. Brukernavn, som er noe du vet, er ikke en del av dette.

Noe du vet.

**Passord**: De fleste er kjent med at man benytter seg av passord for å logge inn – dette er den mest vanlige varianten av innlogging. Man kan skrive veldig mye om bra måter å velge passord, men det viktigste er at man velger lange og komplekse passord som ikke er lett å gjette. Ulike nettsteder har forskjellige krav til hvordan passord skal se ut, men på de fleste steder må man blande små og store bokstaver med tall og spesialtegn.

**Pin kode**: Dette er mest vanlig når 2FA, eller MFA er involvert. Det brukes som oftest ikke som eneste faktoren. Eksempelvis bankkortet ditt; når du går til minibanken og skal hente ut penger, da bruker du 2FA (en ting du vet – pin koden, og en ting du har – bankkortet). Når det gjelder for eksempel ulike mobilbank apper, så er det igjen 2FA. Dette er noe du har: mobiltelefonen, og noe du vet: pin koden. Prøver du på en annen telefon, må du inn med BankID første gang innen du setter opp en pin kode.

Noe du har.

**Mobiltelefon**: Nesten alle har nå for tiden en mobiltelefon. Den vanligste måten å bruke 2FA på, som involverer mobiltelefon, er å sende en SMS med en kode som du må skrive inn på nettstedet etter du har oppgitt brukernavn og passord. For en app som allerede er installert på telefonen så kan de, etter første innlogging, tillate at du logger inn med for eksempel en pin kode i stedet. Da blir pin koden den første faktoren og mobiltelefonen den andre.

**App**: I mange tilfeller blir man tilbudt å bruke en app for å få en kode man skal skrive inn. Den meste kjente appen her er Google Authenticator. Denne appen fungere etter “Timed One time Password”-prinsippet, også kjent som TOTP. Kort fortalt betyr det at appen gir deg en kode som du kan bruke på nettstedet, og denne koden byttes ut etter kort tid (normalt etter 30 sekunder).\
Noen av de appene som finnes er:\
Google Authenticator, Authy, Microsoft Authenticator og Lastpass

**BankId**: Denne kjenner mange til, det er en liten kodebrikke med en knapp på. Når man trykker på knappen så får man opp en kode som man skal skrive inn på nettstedet. Denne fungerer likt som appen med at det er en kode som kun er gyldig innenfor en gitt tid, etter det må man trykke på knappen igjen for å få en ny kode.

**BankId på mobil**: Denne er knyttet til sim kortet ditt. Det som skjer når du bruker dette er at du ikke lenger trenger å bruker passord for å komme inn på nettsiden, men du må bruke et passord for å autentisere deg for BankID. På nettsiden bes du skrive inn fødselsdato og mobilnummer, det sendes da ut en melding til sim kortet som aktiverer bankId funksjonaliteten. Denne meldingen er ofte 2 ord som både vises på nettstedet og i appen, man skal da skrive inn passordet til BankId og den sender da tilbake informasjon til nettstedet at alt er ok. Det er meget viktig her at de 2 ordene som vises på nettstedet er likt de 2 ordene som vises på telefon. Hvis det er ulikt så skal man avslutte med en gang.

**USB Nøkkel**: Denne fungerer som så at når nettsiden ber om den andre faktoren så er det usb nøkkelen som gir den tilbake. Dette er en standard som heter “FIDO U2F”. Det innebær at du slipper å trykke inn en kode, USB nøkkelen gjør det for deg. Eneste du må gjøre er å trykke på en knapp på nøkkelen eller berøre den. Dette er den mest avanserte og sikreste måten for å gi den andre faktoren.\
Noen merker av USB nøkler: [Yubiko Yubikey](https://www.yubico.com/), [Google Titan security key](https://cloud.google.com/titan-security-key)

Noe du er

**Fingeravtrykk**: Mange telefoner og datamaskiner har fingeravtrykk-avlesere bygget inn. Disse kan brukes sammen med passord, pin kode eller visse mobiltelefoner for å angi den andre faktoren.

**Øye**: Noen steder anser ikke fingeravtrykk som sikkert nok, ettersom du etterlater dem overalt (på glass, dører, rekkverk, etc). Der kan de skanne øyet ditt, da blodårene bak i øyet er like unikt som et fingeravtrykk. Dette er mest brukt i fysiske installasjoner og ikke på nettsteder.

**Øye**: Noen Nyere mobiltelefoner kan og bruke øyet ditt som en andre faktor, men i stedet for å skanne blodårene så ser de på hvordan din iris ser ut, dvs det fargede området rundt pupillen, dette er og like unikt som et fingeravtrykk

**Ansikt**: Det aller siste i teknologi er ansiktsgjenkjenning, dvs at datamaskinen eller mobilen kjenner igjen ansiktet ditt.

**Stemme**: Det finnes og stemmegjenkjenning systemer som kan identifisere deg gjennom at du sier noen ord.

Hvor du er

**Posisjonene din**: Det kan være at når du er hjemme, så kanskje du ikke trenger å låse opp telefonen med pin kode.

**Nærhet til andre enheter**: For eksempel når telefonen kobler seg opp til til dataen med bluetooth så trenger man ikke logge inn på dataen, man blir automatisk logget inn.

**Et par ord om passord**

Når man står med valget av hvilket passord man skal bruke så er det noe man trenger å tenke over.\
**Aldri gjenbruk et passord**: Hvis du har gjenbrukt et passord og noen finner ut av det, så er det enklere å hacke dine andre kontoer\
**Bruk et komplekst passord**: Hackere liker å teste enkle passord først, så hvis man har et komplekst passord så er det stor sjanse for at hackerne aldri finner ut av det.\
**Bruk et langt passord**: Hvis hackere har fått tak på et beskyttet passord, så kan de bruke samme teknikk som nettstedet de har fått tak på det beskyttede passordet på for å test passord. De kan for eksempel begynne med “a” og beskytte det, for å se om det matcher, deretter går de til b, osv. Hvis du har et langt passord så kommer det til å ta ekstremt lang tid for dem å finne ut hva passordet ditt er, og det er da stor sjanse at de aldri klarer av finne ut av det.

Når alt dette er sagt, hvordan skal du klare å huske alle passord som du kommer til å få? Vel det kan du ikke… Skriv dem ned i en bok, ja du leste rett, og det høres galt ut, vi har tross alt blitt fortalt at man ikke skal skrive ned passord, MEN det er mye bedre å skrive ned ett passord enn å bruke samme passord på flere steder, dessuten så trenger den hackeren tilgang til din fysiske bok for å få tilgang til passordet. Altså, personen må være fysisk tilstede.

Kan man ikke gjøre noe bedre enn å skrive ned passordene? Jo det kan man, gjennom å bruke et passordhåndteringsprogram. Med et slikt verktøy kan du skrive ned passordene på en sikker måte, den kan også hjelpe deg med å lage et nytt, langt og komplekst passord. Det eneste man da trenger å huske er passordet til passordhåndtereren.\
Noen passordhåndterer:\
[Lastpass](https://www.lastpass.com/)\
[1Password](https://1password.com/)\
[Bitwarden](https://bitwarden.com/)\
[KeePass](https://keepass.info/)\
[Dashlane](https://www.dashlane.com/)

**haveibeenpwnd.com**

Hva er da neste steg i å sikre seg bra passord? Det man kan gjøre er å sjekke om dine eksisterende passord har blitt funnet av hackere, for eksempel gjennom [https://haveibeenpwned.com/Passwords](https://haveibeenpwned.com/Passwords). Denne nettsiden har informasjon om over 500 millioner passord, og den er helt trygg i forhold til å sjekke ditt passord. Den fungerer slik at nettleseren din beskytter passordet, for så å sende kun en del av det beskyttede passordet til haveibeenpwnd. Hvis haveibeenpwnd finner den delen så sender den tilbake alle en liste over alle passord som matcher den delen og med hvor ofte den har blitt funnet. Nettleseren tester da om ditt beskyttede passord er i den listen og hvis den er del av listen så sier den ifra hvor ofte den har funnet dette passord. Derfor kommer aldri haveibeenpwnd til å få hele ditt passord, kun en del av det beskyttete, og fra den delen kan de ikke gjenskape ditt passord.

Eksempel: hvis vi tester passordet “password” så får vi beskjed om at dette passord har blitt sett over 3,7 millioner ganger. Hvis vi tester passordet “dvrtyw%V$” så har det blitt funnet 0 ganger og da er det passordet mye sikrere enn “password”. Det er også mye vanskeligere å gjette. Noen passordhåndterer er også integrert med haveibeenpwnd og sjekker passordene dine for å se om de blitt lekket.

En annen sak man kan gjøre med haveibeenpwnd.com er å sjekke om din e-postadresse har blitt funnet i lekkasjer. Det gjør man på første siden [https://haveibeenpwned.com/](https://haveibeenpwned.com/) her er det bare å fylle in e-postadressen din så forteller den om hvorvidt din e-postadresse har blitt funnet i en lekkasje. Den vil også informere deg om fra hvilken lekkasje det er. Det kan da være en idé å bytte passord på disse tjenestene. Ved å registrere sin e-postadresse med haveibeenpwnd så kommer de til å sende en mail til deg hvis e-postadressen din er funnet i en ny lekkasje.
