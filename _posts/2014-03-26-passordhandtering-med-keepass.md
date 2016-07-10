---
title: Passordhåndtering med KeePass
layout: post
excerpt: De fleste nettbrukere har nok fått med seg at man bør lage et komplisert passord på nett-tjenester man benytter, selv om det også jevnlig kommer artikler som forteller oss at vi kanskje ikke er så flinke til akkurat det.
categories:
  - Programvare
tags:
  - hacking
  - keepass
  - Linux
  - Mac OS X
  - passord
  - sikkerhet
  - tips
  - Windows
image:
  feature:
  teaser: keepass/keepass_teaser.png
  thumb:
---
De fleste nettbrukere har nok fått med seg at man bør lage et komplisert passord på nett-tjenester man benytter, selv om det også jevnlig kommer [artikler][1] som forteller oss at vi kanskje ikke er så flinke til akkurat det.  

Det som ofte kan være et problem er at enkelte passord vi mennesker synes er kompliserte, faktisk ikke tar lang tid å knekke for en datamaskin med de rette verktøyene. Og &laquo;kompliserte&raquo; passord er også ofte veldig vanskelige å huske, noe som igjen øker sjansen for at vi mennesker tar mindre smarte snarveier for å gjøre det enklere for oss, for eksempel ved å bruke det samme passordet på alle nettsteder man har bruker. Og fra tid til annen rulles det opp &laquo;skandaler&raquo;, der et eller annet kjent selskap har fått sine databaser med brukerdata kompromitert.

>   * [&laquo;To millioner passord på avveie&raquo; -NRK][2] 
>   * [&laquo;Over 90.000 Foto.no passord kan være på avveie&raquo; &#8211; VG][3]
>   * [&laquo;Millioner av LinkedIn -passord på avveie&raquo; &#8211; E24][4]
>   * [&laquo;Hackere stjal 150 millioner passord fra Adobe&#8230;&raquo; &#8211; Dagbladet][5]

Men hva kan man gjøre? Dette er hvordan jeg forsøker å håndtere utfordringen.

#### Finnes det en mirakelkur?

Dersom man er uhyre disiplinert, og har god hukommelse, kan man selvsagt bruke tips man finner på nettet for å lage gode passord.

>   * [&laquo;Slikt lager du et sikkert passord&raquo; &#8211; TV2][6] 
>   * [&laquo;Slik lager du gode passord&raquo; &#8211; NRK][7]

Jeg innså derimot raskt mine egne begrensinger, og søkte derfor etter en teknisk løsning i form av et såkalt passord-velv. Kort fortalt er det snakk om et program eller en tjeneste som genererer og lagrer gode passord som er vanskelige å knekke selv for datamaskiner. Jeg har tidligere brukt både nett-tjenesten [Lastpass][8][Multi-platform] og [1Password][9][Mac,Win,iOS], men landet til slutt på en løsning som heter [KeePass][10]. Dette er en åpen-kildekodeløsning som gir mange muligheter gjennom støtte for mange plattformer, og til en pris det er vanskelig å konkurrere med. Det skal nevnes at Lastpass også er gratis i den grunnleggende utgaven, men når jeg først skal ta litt ekstra vare på sikkerheten liker jeg uansett at kontrollen ligger fullt og helt hos meg selv.

#### Så hva er greia med KeePass?

{% include image.html img="/images/keepass/keepass1.png" title="http://keepass.info/" caption="Foto: http://keepass.info/" url="http://keepass.info" %}

  * Har kryptert database. Det vil si at passordene er uleselige for uvedkomne.
  * Støtter både master-passord og nøkkelfil, eller begge brukt sammen, for økt sikkerhet ved kryptering og dekryptering.
  * Kan brukes som en portabel Windowsapplikasjon, det vil si at den kan kjøres fra en usb-stick dersom man ønsker det.
  * Multiplattform. Støtter både Windows, Mac, Linux, iOS, Android, og mange fler[<http://keepass.info/download.html>].
  * Kan fylle ut tekstfelt og dialogbokser automatisk.
  * Genererer meget sterke passord for deg når du trenger det.
  * Støtte for plugins, som ytterligere utvider funksjonaliteten.

#### Ok, hva gjør jeg?

{% include image.html img="/images/keepass/getrand_big1.png" title="Nøkkelfil-generator - Foto: http://keepass.info/" caption="Nøkkelfil-generator - Foto: http://keepass.info/" url="http://keepass.info/" %}

Den korte versjonen er som følger:

1. Last ned KeePass fra nettsidene deres [<http://keepass.info/download.html>]. Du er ute etter den som kalles Professional Edition (versjonsnummer 2.25 eller høyere), og kan velge mellom &laquo;Installer&raquo; (installert på datamaskinen) og &laquo;Portable&raquo; (ha programmet på en flyttbar usb-stick). Jeg tar utgangspunkt i versjonen for windows, installert på datamaskinen.
2. Finn den nedlastede filen (KeePass-X.XX-Setup.exe, der X.XX er versjonsnummeret), og dobbeltklikk for å installere. Følg instruksjonene gjennom hele prosessen.
3. Start KeePass. Du skal nå lage en ny database, ved å trykke på ikonet av en hvit firkant med en stjerne i nedre høyre hjørne. Gi databasen et filnavn, og lagre den der du ønsker.For ekstra sikkerhet kan dette for eksempel gjøres på en separat usb-stick.
4. Det neste vinduet som møter oss er der grunnlaget for sikker lagring legges. Her skal du fylle inn ett sikkert master-passord, som er det eneste passordet du MÅ huske. Dersom du glemmer det, er dine passord for alle praktiske formål tapt. Du får en indikator på passordets kvalitet under tekstfeltet, og her er det bare å bruke alle triksene i boken.For å øke sikkerheten ytterligere kan du opprette en nøkkelfil ved huke av &laquo;Key file / provider&raquo;, og trykke på &laquo;Create&raquo;. Du må da gi nøkkelfilen et navn, og lagre den på et valgfritt sted (som du selvsagt må huske). For ekstra sikkerhet kan du lagre denne på en separat usb-stick, adskilt fra databasen.
5. Følg instruksjonene om å bevege muspekeren over bildet av støy, samt fyll inn tilfeldige tegn i tekstfeltet. Under bildet kan du se hvor mye data den har fått til nøkkelen. Denne nøkkelfilen vil, sammen med passordet ditt, gjøre databasen din praktisk talt uknekkbar (merk at den i teorien selvsagt fremdeles kan knekkes). [<a href="https://www.youtube.com/watch?v=JB1ePElPDjk" data-rel="lightbox-video-0">Brute force hacking attempts on KeePass files &#8211; Youtube</a>]
6. I det neste vinduet kan du gi databasen et navn, skrive en kort beskrivelse, samt skrive inn et standard brukernavn den skal bruke når den oppretter nye oppføringer.
7. Når den nye databasen åpnes for første gang, er den fylt opp med noen standardoppføringer. Disse kan du slette dersom du ønsker.
8. VIKTIG! Gå i menyvalget &laquo;Tools&raquo; og &laquo;Options&raquo;. Velg fanen &laquo;Advanced&raquo;, og huk av boksen for &laquo;Automatically save when closing/locking the database&raquo;. Det er ekstremt viktig at oppføringene du lager faktisk lagres i databasen, slik at du finner tilbake til de senere. Gjør det også gjerne til en vane at du lagrer hver gang du gjør en endring i en oppføring.
9. Trykk på ikonet av en nøkkel med grønn pil for å lage en ny oppføring. Gi oppføringen en tittel, et brukernavn, og en URL. Passordet genereres automatisk. Trykk ok og lagre databasen.

{% include image.html img="/images/keepass/addentry_big1.png" title="Legg til oppføring - Foto: http://keepass.info/" caption="Legg til oppføring - Foto: http://keepass.info/" url="http://keepass.info/" %}

#### Var dette alt?

Nei, selvsagt er det mange muligheter ved KeePass som ikke ble dekket her. Jeg vil følge opp med et senere innlegg der jeg tar for meg noen av muligheten som finnes.  

Dette ble det supervanskelige andre-innlegget, men det kom ut til slutt selv om det ble i overkant mange revisjoner først. Jeg setter veldig pris på tilbakemeldinger som kan hjelpe meg videre, være seg format, språk, eller annet ved innlegget som kunne vært bedre, og håper du vil ta deg tid til å si ifra dersom du ser noe.

 [1]: http://www.dagbladet.no/2014/01/23/tema/aller/teknologi/dinside/data/31434450/
 [2]: http://www.nrk.no/verden/to-millioner-passord-pa-avveie-1.11396869
 [3]: http://www.vg.no/nyheter/innenriks/foto-og-video/over-90-000-foto-no-passord-kan-vaere-paa-avveie/a/10055315/
 [4]: http://e24.no/digital/millioner-av-linkedin-passord-paa-avveie/20238830
 [5]: http://www.dagbladet.no/2013/11/09/nyheter/adobe/kunde/millioner/it/30062028/
 [6]: http://www.tv2.no/nyheter/innenriks/norsk-passordekspert-slik-lager-du-et-sikkert-passord-3976189.html
 [7]: http://www.nrk.no/programmer/radio/nitimen/1.1206641
 [8]: https://lastpass.com/
 [9]: https://agilebits.com/onepassword
 [10]: http://keepass.info/
