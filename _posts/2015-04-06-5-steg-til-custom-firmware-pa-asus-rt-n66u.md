---
title: 5 steg til custom firmware på Asus RT-N66U
layout: post
excerpt: ASUS RT-N66U er kjent for å være både god og stabil, og regnes som en av de beste routere på forbrukermarkedet. Men dersom du synes programvaren blir litt begrenset, kan du enkelt installere en tredjeparts-firmware og gjøre den enda bedre. Og om du gjør alt rett, er du oppe og kjører innen 30 minutter.
categories:
  - Prosjekter
tags:
  - custom firmware
  - diy
  - router
  - rt-n66u
  - TomatoUSB
---
*ASUS RT-N66U* er kjent for å være både god og stabil, og regnes som en av de beste routere på forbrukermarkedet. Men dersom du synes programvaren blir litt begrenset, kan du enkelt installere en tredjeparts-firmware og gjøre den enda bedre. Og om du gjør alt rett, er du oppe og kjører innen 30 minutter.

{% include image.html img="/images/tomatoUSB/asus-forfra_63031e_0.jpg" title="ASUS Ruter forfra" caption="" %}

> **ADVARSEL**: Denne posten er kun til informasjon, og ment for personer som vet hva de driver med. Dersom terminologien på noe som helst tidspunkt virker skremmende og fremmed vil jeg anbefale å finne en mer utfyllende guide, eventuelt la routeren beholde original firmware. Dersom noe uforutsett skjer underveis, eller det oppstår en brukerfeil, vil det kunne gjøre at routeren ikke kan brukes uten å legge inn original firmware på nytt. Det kan også i ytterste konsekvens gjøre at routeren din blir ubrukelig. Les nøye gjennom stegene før du bestemmer deg om du vil gjøre det, og dersom du velger å følge stegene, skjer det på eget ansvar.

### 5 steg til TomatoUSB

  1. Last ned siste versjon av Shibbys TomatoUSB (pr idag build5x-128-EN). &laquo;Asus RT-N66u 64k&raquo; er den som virker på RT-N66U, og last ned filen med AIO (All in one) i navnet. [[http://tomato.groov.pl/download/K26RT-N/]][1]

  2. Tøm **NVRAM** på routeren &#8211; hold nede **WPS** knapp og restart routeren. Hold WPS i **10 sekunder** for å tømme NVRAM.

  3. Boot router i recovery mode &#8211; hold nede **RESET** og restart routeren. Hold RESET i **10 sekunder**.  

  4. Kontroller at din PC har en IP i 192.168.1.X serien. Gå til 192.168.1.1 i nettleseren. Du kommer da til det webbaserte verktøyet på routeren.

  5. Velg filen du lastet ned fra Shibby, og last opp. Du kan følge statusen nederst i nettleseren din. Når den er lastet opp får du melding i nettleseren, og du vil se at det begynner å blinke på routeren.**VIKTIG**: NÅ MÅ DU VENTE I CA 15-20 MINUTTER, OG LA ROUTEREN JOBBE FERDIG PÅ EGENHÅND. Routeren bruker lang tid på å installere firmwaren, og det er ingen måte å se fremgangen på bortsett fra at routeren restarter når den er ferdig. Da kan du gå til 192.168.1.1 igjen,og begynne oppsettet av din nye router. Brukernavn er root. Passord er admin. Dette bør du skifte med en gang du begynner oppsettet,for å sikre routeren din.

{% include image.html img="/images/tomatoUSB/TomatoUSB_Status.png" title="Status Overview" caption="Status Overview" %}

> #### Kilder:
>
>   * <http://www.shadowandy.net/2012/03/asus-rt-n66u-tomatousb-firmware-flashing-guide.htm>
>   * <https://gist.github.com/joshenders/3941269>
>   * <http://www.dd-wrt.com/wiki/index.php/Asus_RT-N66U>

 [1]: http://tomato.groov.pl/download/K26RT-N/
