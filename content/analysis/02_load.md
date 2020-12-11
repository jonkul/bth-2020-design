Webbplatser laddningstid
=======================

Uppgiften går ut på att välja ut ett antal olika webbplatser och testa dem för att mäta hur snabbt de laddas och om de innehåller några saker som kan förbättras med tanke på laddningstid och användbarhet.

Urval
-----------------------

Jag har valt att återigen undersöka de tre olika finansiella hemsidor jag använde i förra uppgiften, då även laddningstid och optimering är en intressant sak att titta på hos dessa ganska lyckade hemsidor. Det är alltså först och främst de digitala uppstickarna för aktie- och fondhandel, Avanza och Nordnet, samt som jämförelse Sveriges största gammelbank, Swedbank.

Metod
-----------------------

Jag använder helt enkelt Network-fliken i Googles DevTools (inspect) för att mäta lite olika data om sidorna, samlar den i Excel, och analyserar sidorna i Google Pagespeed. Alla extensions var inaktiverade för dessa tester.

Resultat
-----------------------

## Avanza
#### Skärmdump

![Skärmdump av Avanza](../assets/img/avanza.png "Skärmdump av Avanza") {.image2}

### Google PageSpeed
#### avanza.se

+ Desktop: 72
+ Mobile: 32

Pagespeed _(mobile)_ klagar främst på Speed Index, Largest Contentful Paint, Time to Interactive, samt Total Blocking Time. 

#### Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Minimize main-thread work, 5.7 s
+ Serve static assets with an efficient cache policy, 22 resources found
+ Reduce JavaScript execution time, 4.3 s

#### Förslag på åtgärder är:
+ Serve images in next-gen formats, 2.7 s
+ Remove unused JavaScript, 1.21 s
+ Avoid multiple page redirects, 1.11 s
+ Properly size images 0.45 s

För _desktop_ rör motsvarande klagomål bara Largest Contentful Paint.

#### Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Serve static assets with an efficient cache policy, 26 resources found

#### Förslag på åtgärder är:
+ Serve images in next-gen formats, 0.48 s
+ Avoid multiple page redirects, 0.34 s
+ Remove unused JavaScript, 0.24 s

### Google DevTools

Desktop (2560 x 1440px):

+ Requests:	60
+ kB transfered:	468
+ MB resources:	4
+ s finish:	1,2
+ ms load:	240,7

Mobile (genomsnitt av iPad Pro, iPad och iPhone 5/SE):
+ Requests:	57
+ kB transfered:	467,6
+ MB resources:	4
+ s finish:	1,1
+ ms load:	202,9

* * *

### Google PageSpeed
#### avanza.se/kundservice.html/

+ Desktop: 85
+ Mobile: 43

Pagespeed _(mobile)_ klagar främst på Largest Contentful Paint, Time to Interactive, samt Total Blocking Time.

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Avoid an excessive DOM size, 2,053 elements
+ Serve static assets with an efficient cache policy, 34 resources found
+ Minimize main-thread work, 4.7 s
+ Reduce JavaScript execution time, 2.6 s

#### Förslag på åtgärder är:
+ Remove unused JavaScript, 1.35 s
+ Preload key requests, 0.78 s
+ Eliminate render-blocking resources, 0.66 s
+ Remove unused CSS, 0.3 s
+ Minify JavaScript, 0.15 s
+ Avoid serving legacy JavaScript to modern browsers, 0.15 s

För _desktop_ rör motsvarande klagomål bara Largest Contentful Paint och Time to Interactive, men varningarna är orange, inte röda.

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Avoid an excessive DOM size, 2,053 elements
+ Serve static assets with an efficient cache policy, 39 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 0.45 s
+ Remove unused JavaScript, 0.24 s
+ Preload key requests, 0.18 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests: 57
+ kB transfered: 789
+ MB resources:	3
+ s finish: 0,9
+ ms load: 563,7

Mobile (iPad 768x1024px):
+ Requests:	56
+ kB transfered: 763,7
+ MB resources:	2,9
+ s finish:	0,9
+ ms load: 498,3

* * *

### Google PageSpeed
#### avanza.se/placera/forstasidan.html

+ Desktop: 69
+ Mobile: 20

Pagespeed _(mobile)_ klagar på Speed Index, Largest Contentful Paint, Time to Interactive, samt Total Blocking Time, med en orange varning för Cumulative Layout Shift.

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Reduce the impact of third-party code, third-party code blocked the main thread for 1,850 ms
+ Does not use passive listeners to improve scrolling performance
+ Avoid document.write()
+ Avoid enormous network payloads, total size was 7,389 KiB
+ Serve static assets with an efficient cache policy, 75 resources found
+ Minimize main-thread work, 10.2 s
+ Reduce JavaScript execution time, 7.0 s
+ Avoid an excessive DOM size, 1,817 elements

#### Förslag på åtgärder är:
+ Serve images in next-gen formats, 30 s
+ Defer offscreen images, 24.6 s
+ Remove unused JavaScript, 2.28 s
+ Preload key requests, 1.83 s
+ Properly size images, 1.35 s
+ Efficiently encode images, 0.9 s
+ Eliminate render-blocking resources, 0.71 s
+ Remove unused CSS, 0.3 s

För _desktop_ rör motsvarande klagomål bara Speed Index, samt orange varning på Largest Contentful Paint, Time to Interactive och Cumulative Layout Shift.

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Does not use passive listeners to improve scrolling performance
+ Avoid document.write()
+ Avoid enormous network payloads, total size was 7,859 KiB
+ Serve static assets with an efficient cache policy, 82 resources found
+ Avoid an excessive DOM size, 1,820 elements
+ Minimize main-thread work, 3.3 s
+ Reduce JavaScript execution time, 1.9 s

#### Förslag på åtgärder är:
+ Serve images in next-gen formats, 5.12 s
+ Properly size images, 1.68 s
+ Eliminate render-blocking resources, 0.45 s
+ Remove unused JavaScript, 0.32 s
+ Preload key requests, 0.27 s
+ Efficiently encode images, 0.16 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests: 283
+ kB transfered: 8433
+ MB resources:	14
+ s finish: 4,7
+ ms load: 753

Mobile (iPad 768x1024px):
+ Requests:	172
+ kB transfered: 7566
+ MB resources:	11
+ s finish:	2,9
+ ms load: 672

* * *

## Nordnet

#### Skärmdump

![Skärmdump av Nordnet](../assets/img/nordnet.png "Skärmdump av Nordnet") {.image2}

### Google PageSpeed
#### nordnet.se

+ Desktop: 45
+ Mobile: 21

Pagespeed _(mobile)_ klagar på Speed Index, Largest Contentful Paint, Time to Interactive, samt Total Blocking Time. 

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Minimize main-thread work, 7.5 s
+ Reduce JavaScript execution time, 5.2 s
+ Avoid an excessive DOM size, 1,094 elements

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 2.57 s
+ Remove unused JavaScript, 2.4 s
+ Avoid multiple page redirects, 1.11 s
+ Serve images in next-gen formats, 0.15 s

För _desktop_ rör motsvarande klagomål Largest Contentful Paint, Time to Interactive, samt Total Blocking Time. 

#### Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Serve static assets with an efficient cache policy, 26 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 0.95 s
+ Remove unused JavaScript, 0.4 s
+ Serve images in next-gen formats, 0.4 s
+ Efficiently encode images, 0.36 s
+ Avoid multiple page redirects, 0.34 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests:	71
+ kB transfered: 2600
+ MB resources:	8
+ s finish:	1,1
+ ms load: 1100

Mobile (genomsnitt av iPad Pro, iPad och iPhone 5/SE):
+ Requests:	64,5
+ kB transfered: 2311
+ MB resources:	7,8
+ s finish:	1,2
+ ms load: 1160

* * *

### Google PageSpeed
#### nordnet.se/faq

+ Desktop: 60
+ Mobile: 24

Pagespeed _(mobile)_ klagar på Speed Index, Largest Contentful Paint, Time to Interactive, samt Total Blocking Time. Orange varningar på First Contentful Paint och Cumulative Layout Shift.

#### Diagnostics:
+ Ensure text remains visible during webfont load
+ Minimize main-thread work, 7.0 s
+ Reduce JavaScript execution time, 5.2 s
+ Serve static assets with an efficient cache policy, 4 resources found
+ Avoid an excessive DOM size, 1,081 elements

#### Förslag på åtgärder är:
+ Remove unused JavaScript, 2.85 s
+ Eliminate render-blocking resources, 0.36 s

För _desktop_ rör motsvarande klagomål bara Total Blocking Time. Orange varningar på Speed Index, Largest Contentful Paint samt Time to Interactive.

#### Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Serve static assets with an efficient cache policy, 26 resources found

#### Förslag på åtgärder är:
+ Remove unused JavaScript, 0.56 s
+ Serve images in next-gen formats, 0.52 s
+ Efficiently encode images, 0.4 s
+ Eliminate render-blocking resources, 0.14 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests:	44
+ kB transfered: 2300
+ MB resources:	10
+ s finish:	3,2
+ ms load: 1200

Mobile (iPad 768x1024px):
+ Requests:	43
+ kB transfered: 1900
+ MB resources:	9,5
+ s finish:	3,1
+ ms load: 1087

* * *

### Google PageSpeed
#### nordnet.se/marknaden/nyheter

+ Desktop: 65
+ Mobile: 46

Pagespeed _(mobile)_ klagar på Cumulative Layout Shift och Total Blocking Time, med orange varningar på Speed Index, samt Time to Interactive.

#### Diagnostics:
+ Reduce JavaScript execution time, 1.9 s
+ Avoid an excessive DOM size, 1,007 elements
+ Minimize main-thread work, 2.5 s

#### Förslag på åtgärder är:
+ Reduce initial server response time, 0.57 s
+ Remove unused JavaScript, 0.48 s

För _desktop_ rör motsvarande klagomål Total Blocking Time och Cumulative Layout Shift, med orange varningar på Time to Interactive samt Total Blocking Time. 

#### Diagnostics:
+ Minimize main-thread work, 8.2 s
+ Reduce JavaScript execution time, 6.7 s
+ Avoid an excessive DOM size, 1,038 elements

#### Förslag på åtgärder är:
+ Remove unused JavaScript, 2.55 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests:	42
+ kB transfered: 1500
+ MB resources:	8
+ s finish:	2,9
+ ms load: 966

Mobile (iPad 768x1024px):
+ Requests:	42
+ kB transfered: 1500
+ MB resources:	8,4
+ s finish:	3
+ ms load: 970

* * *

## Swedbank
#### Skärmdump

![Skärmdump av Swedbank](../assets/img/swedbank.png "Skärmdump av Swebank") {.image2}

### Google PageSpeed
#### swedbank.se

+ Desktop: 58
+ Mobile: 36

Pagespeed _(mobile)_ klagar på First Contentful Paint, Speed Index, Largest Contentful Paint, Time to Interactive, samt orange varning på Cumulative Layout Shift. 

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 47 resources found
+ Minimize main-thread work, 2.4 s

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 5.18 s
+ Remove unused CSS, 2.1 s
+ Properly size images, 0.75 s
+ Serve images in next-gen formats, 0.3 s

För _desktop_ rör motsvarande klagomål First Contentful Paint, Speed Index samt Largest Contentful Paint.

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 46 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 1.59 s
+ Remove unused CSS, 0.4 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests:	75
+ kB transfered: 2000
+ MB resources:	2,9
+ s finish:	0,4
+ ms load: 410

Mobile (genomsnitt av iPad Pro, iPad och iPhone 5/SE):
+ Requests:	74
+ kB transfered: 1989
+ MB resources:	2,9
+ s finish:	0,3
+ ms load: 316

* * *

### Google PageSpeed
#### swedbank.se/om-oss

+ Desktop: 53
+ Mobile: 34

Pagespeed _(mobile)_ klagar på allt, även om Total Blocking Time bara är en orange varning. 

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 48 resources found
+ Minimize main-thread work, 2.8 s

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 5.2 s
+ Remove unused CSS, 2.1 s
+ Remove unused JavaScript, 0.45 s
+ Properly size images, 0.15 s
+ Serve images in next-gen formats, 0.15 s
+ Avoid serving legacy JavaScript to modern browsers, 0.15 s

För _desktop_ rör motsvarande klagomål First Contentful Paint, Speed Index, Largest Contentful Paint samt orange varning för Time to Interactive.

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 46 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 1.86 s
+ Remove unused CSS, 0.4 s

### Google DevTools

Desktop (2560 x 1440px):
+ Requests:	84
+ kB transfered: 2500
+ MB resources:	3,9
+ s finish:	0,5
+ ms load: 516

Mobile (iPad 768x1024px):
+ Requests:	84
+ kB transfered: 2500
+ MB resources:	3,9
+ s finish:	0,5
+ ms load: 485

* * *

### Google PageSpeed
#### swedbank.se/privat.html

+ Desktop: 67
+ Mobile: 37

Pagespeed _(mobile)_ klagar på First Contentful Paint, Speed Index, Largest Contentful Paint, Time to Interactive, samt orange varning på Cumulative Layout Shift. 

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 51 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 5.83 s
+ Remove unused CSS, 2.1 s
+ Properly size images, 0.15 s
+ Serve images in next-gen formats, 0.15 s

För _desktop_ rör motsvarande klagomål First Contentful Paint, Speed Index samt Largest Contentful Paint.

#### Diagnostics:
+ Replace unnecessarily large JavaScript libraries, 1 large library found
+ Serve static assets with an efficient cache policy, 50 resources found

#### Förslag på åtgärder är:
+ Eliminate render-blocking resources, 1.61 s
+ Remove unused CSS, 0.4 s

### Google DevTools

Desktop (2560 x 1440px):

+ Requests:	86
+ kB transfered: 1700
+ MB resources:	2,7
+ s finish:	0,4
+ ms load: 415

Mobile (iPad 768x1024px):
+ Requests:	86
+ kB transfered: 1700
+ MB resources:	2,7
+ s finish:	0,4
+ ms load: 389

* * *

Analys
-----------------------

Det första man slås av är nog att alla tre hemsidorna, samt deras utvalda undersidor, får ganska dåliga betyg i Google PageSpeed, och då i synnerhet i mobilvarianterna. 

De vanligaste föreslagna förbättringsåtgärderna för de tre bankernas startsidor är:
använd bilder i nästa generations format (2), undvik multipla omdirigeringar (2), ta bort oanvänd JS (2), undvik renderingsblockerande resurser (2), komprimera bilder effektivare, samt ta bort oanvänd CSS.

Rangordning
-----------------------

De tre sidorna bör främst jämföras mellan respektive startsida, då undersidorna inte är exakt jämförbara, även om jag har valt undersidor som liknar varandra. 

Avanza.se vinner PageSpeed-testerna ganska stort i den stationära varianten, Swedbank kommer tvåa, och Nordnet trea. 

Swedbanks mobila variant är snäppet snabbare än Avanzas, men skillnaden är inte lika stor som den mellan de stationära (till Avanzas fördel). Nordnets mobilsida är klart sämst.

Upplevd hastighet
-----------------------

Vad gäller den upplevda hastigheten ser resultaten dock lite annorlunda ut, vilket man till viss del kan se på DevTools-mätningarna. Alla tre sidor är helt klart godkända.

Swedbank laddar omedelbart, så snabbt att hela sidan bara blinkar till, utan fördröjning eller inladdning av något innehåll.

Avanza har en sekunds fördröjning innan sidan visas, men sen ploppar den fram i ett enda svep.

Nordnet har ibland en inledande fördröjning, men framförallt laddas deras stora bild in så pass långsamt att man ser den renderas ut på sidan. 


Övrigt
-----------------------

Denna analys är skriven av Jon Kullberg. Rådata från testerna i denna [ods-fil](../assets/misc/speed.ods "Rådata").
