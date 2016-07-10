---
title: 'Passord og internett &#8211; KeePass og nettlesere'
layout: post
excerpt: I løpet av en dag er de fleste av oss innom flere tjenester på internett som krever en form for innlogging. Når vi samtidig vet at et passord bør være unikt, og ikke minst vanskelig å knekke, kan dette fort bli til en tungvinn affære. Må det være sånn? Dette er jo ofte grunnen til at vi velger snarveier og enkle løsninger, som kanskje ikke gir den nødvendige sikkerheten vi bør ønske oss. Det er her KeePass kan hjelpe oss.
categories:
  - Programvare
tags:
  - Chrome
  - Firefox
  - Google
  - keepass
  - Linux
  - Mac OS X
  - Mozilla
  - passord
  - tips
  - Windows
image:
  feature:
  teaser: keepass/keepass_teaser.png
  thumb:
---
I løpet av en dag er de fleste av oss innom flere tjenester på internett som krever en form for innlogging. Når vi samtidig vet at et passord bør være unikt, og ikke minst vanskelig å knekke, kan dette fort bli til en tungvinn affære. Må det være sånn? Dette er jo ofte grunnen til at vi velger snarveier og enkle løsninger, som kanskje ikke gir den nødvendige sikkerheten vi bør ønske oss. Det er her KeePass kan hjelpe oss. For hjelp til å begynne å bruke KeePass, er det bare å lese det <a title="Passordhåndtering med KeePass" href="http://www.hybel.net/passordhandtering-med-keepass/" target="_blank">forrige innlegget</a> mitt.

#### Så, hvordan kan KeePass hjelpe meg?

{% include image.html img="/images/keepass/keepass1.png" title="Foto: http://keepass.info/" caption="Foto: http://keepass.info/" url="http://keepass.info/" %}

Når du har åpnet databasen i KeePass, har du tilgang til alle dine lagrede brukernavn og passord. Ved å høyreklikke på en oppføring, får du opp en meny der de øverste valgene lar deg kopiere henholdsvis brukernavn eller passord slik at du kan lime de inn dit de skal.

En enda raskere metode er å velge det første tekstfeltet du skal fylle ut før du høyreklikker i KeePass, og velger &laquo;Perform Auto-Type&raquo;. Da vil KeePass fylle ut begge feltene for deg, med brukernavn og passord fra oppføringen du har valgt.

#### Integrering i nettleseren

Dersom du bruker Mozilla Firefox eller Google Chrome finnes det også en enda enklere metode for å få brukernavn og passord til og fra KeePass. Med tillegget KeePassHttp skapes en integrert kobling mellom KeePass og nettleseren din, som også hjelper deg med å generere sterke passord når du skal lage den en ny bruker et eller annet sted.

{% include image.html img="/images/keepass/keepasshttp_options.png" title="KeePassHttp Options" caption="KeePassHttp Options" %}

For å bruke det må du laste ned KeePassHttp[<a href="https://raw.github.com/pfn/keepasshttp/master/KeePassHttp.plgx" target="_blank">direktelenke</a>] fra utviklerens nettside. Her finner du også en detaljert guide for oppsett og innstillinger. Når KeePassHttp er lastet ned, trenger du bare å legge filen i mappen der KeePass ble installert, og starte KeePass på nytt. Du vil da få et nytt valg i &laquo;Tools&raquo;-menyen som heter &laquo;KeePassHttp Options&raquo;. Jeg anbefaler at du leser avsnittet &laquo;Settings in KeePassHttp Options&raquo; hos utvikleren når du setter det opp.

I tillegg til KeePassHttp må du også installere enten <a href="https://chrome.google.com/webstore/detail/chromeipass/ompiailgknfdndiefoaoiligalphfdae" target="_blank">chromeIPass</a> til Google Chrome eller <a href="https://passifox.appspot.com/passifox.xpi" target="_blank">PassIFox</a> for Mozilla Firefox. Du kan lese mer om de på utviklerens <a href="https://github.com/pfn/passifox/" target="_blank">nettside</a>.

#### Installert, hva nå?

Dersom alt har gått etter planen har du nå ikke lenger noen unnskyldning for å opprette brukere med svake passord, fordi du nå raskt kan få tak i dine lagrede passord i KeePass. Men det er selvsagt flere muligheter med KeePass, og neste gang skal jeg ta for meg hvordan jeg håndterer det at jeg har behov for passordene mine på flere enheter.

Jeg setter veldig pris på tilbakemeldinger som kan hjelpe meg videre, og håper du vil ta deg tid til å si ifra dersom du har noe som kan gjøre innleggene mine bedre.
