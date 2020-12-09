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

__Avanza__

_Skärmdump_

![Skärmdump av Avanza](../assets/img/avanza.png "Skärmdump av Avanza") {.image2}

_Google PageSpeed_
+ Desktop: 72
+ Mobile: 32

Pagespeed (mobile) klagar främst på Speed Index, Largest Contentful Paint, Time to Interactive, samt Total Blocking Time. 

Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Minimize main-thread work, 5.7 s
+ Serve static assets with an efficient cache policy, 22 resources found
+ Reduce JavaScript execution time, 4.3 s

Förslag på åtgärder är:
+ Serve images in next-gen formats, 2.7 s
+ Remove unused JavaScript, 1.21 s
+ Avoid multiple page redirects, 1.11 s
+ Properly size images 0.45 s

För desktop rör motsvarande klagomål bara Largest Contentful Paint.

Diagnostics:
+ Does not use passive listeners to improve scrolling performance
+ Serve static assets with an efficient cache policy, 26 resources found

Förslag på åtgärder är:
+ Serve images in next-gen formats, 0.48 s
+ Avoid multiple page redirects, 0.34 s
+ Remove unused JavaScript, 0.24 s

_Google DevTools_
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

__Nordnet__

_Skärmdump_

![Skärmdump av Nordnet](../assets/img/nordnet.png "Skärmdump av Nordnet") {.image2}

_Färgpalett_

Nordnet använder sig av ett minimalt monokront färgschema, nästan helt baserat på fullt svart och vitt, med en ljusare grå som bakgrundsfärg på vissa element, och en mörkare grå på ett enstaka element som avbrott i slutet av sidan. 

De använder bara två accentfärger, nämligen en blå och en rosa ton, båda med stark färgmättnad.

Nordnet använder sitt eget typsnitt Nordnet Sans Mono på allt textinnehåll på sidan, såväl rubriker som brödtext och knappar eller länkar. Som namnet antyder är det ett typsnitt utan serifer.

Jag tycker att Nordnets färgval och typografi motsvarar den profil jag tror att de vill ha. Helhetsintrycket är piggt och modernt webbigt, men samtidigt med en kraftig kontrast och skarpa accentfärger som signalerar lite mer energisk business.

* * *

__Swedbank__

_Skärmdump_

![Skärmdump av Swedbank](../assets/img/swedbank.png "Skärmdump av Swebank") {.image2}

_Färgpalett_

Swedbank använder sig precis som de flesta andra av ett färgschema som till större delen är baserat på nästan svart och nästan vitt, samt en hel del full vit. Vad gäller accentfärger så arbetar mycket med de gula och orange toner (samt gradienter mellan dessa) som ingår i logotyp och varumärke sedan länge. Dessutom använder de en bred uppsättning av andra matta och varma färger i diverse kulörer.

Man använder en bred uppsättning typsnigg. SwedbankHeadlineBlack (h1, h2), SwedbankHeadlineBold (h3), SwedbankSansMedium, SwedbankSansRegular, Helvetica Neue, Arial, Helvetica. Främst Arial på vanlig brödtext, och SwedbankSansRegular/Medium på lite mer profilerade textrutor. Inga serifer någonstans på sidan.

Jag tycker att Swedbanks färgval och typografi motsvarar den profil jag tror att de vill ha. Helhetsintrycket är precis som för de andra sidorna ganska modernt, men jämförelsevis mest uppmjukat och folkligt av de tre.

Analys
-----------------------

Jag tycker mig ha hittat tre stycken snygga och bra hemsidor att analysera. Bästa sättet att sammanfatta deras skillnader är förmodligen att titta på hur mysiga, mjuka och folkliga de försöker vara (professionella kontra amatörer). 

Nordnet har den hårdaste och mest professionella framtoningen av de tre, och Swedbank den varmaste och mysigaste. Mängden varma färger och bilder får en nästan att tänka på IKEA-katalogen, fast faktiskt ännu mysigare. Avanza ligger någonstans mitt emellan, med behagliga färger (inte så starka kontraster), men knappt några bilder.

Både Avanza och Nordnet jobbar med innehåll direkt på den vita/ljusa bakgrunden, utan några avgränsningar till vänster och höger. Även om allt material har en maxbredd så är vissa av styckenas bakgrund 100% av sidans bredd, och i Avanzas fall använder man dessutom lite grafik istället för enfärgade fält.
 Swedbanks hemsida är för tillfället inramad av en julig bild, även om innehållet i mitten också till stor del ligger direkt på bakgrunden.

Vad gäller negative space så ser man stora skillnader. Avanza är extremt luftig, Nordnet ganska luftig, och Swedbank väldigt kompakt. 

Typsnitten skiljer sig inte speciellt drastiskt mellan sidorna. Avanza är den enda som använder serifer på sina rubriker, och Nordnet sticker ut lite med sitt täta teckenavstånd, kompakta teckenhöjd samt tunga vikt på rubriker.

Om jag ska välja en favorit bland sidornas design så får det bli Nordnet, som bäst kommunicerar den professionella image jag tänker mig att en bank eller värdepappershandlare bör ha. Med det sagt så använder jag mest Avanza, så...

Övrigt
-----------------------

Denna analys är skriven av Jon Kullberg.
