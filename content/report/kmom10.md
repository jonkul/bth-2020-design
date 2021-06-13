---
Title: Kmom10
Description: Part 7/10
Template: kmom
kmom: 10
---

Kursmoment 10
==================

1. **Implementerade uppdrag**

    1. Webbplats

        Jag utgick ifrån min portfolio och försökte skala bort det mesta överflöd av css, sidor och bilder. Eftersom jag gör det här projektet i efterhand och inte riktigt har alla kursmoments innehåll och instruktioner helt färska i minnet så kändes det som att jag skulle undvika flest missar och dubbelarbete på det sättet.

        Valet föll på exempel nummer 2, en artist (fotograf). För mig förs då de designmässiga tankarna direkt till minimalism vad gäller allt utom bilder, för att framhäva dessa, och för att skapa den känsla av lugn och eftertänksamhet som jag förknippar med fotografering. 
        
        Vad gäller logotyp så ville jag hålla det enkelt och i ren textform, vilket känns mest rimligt för de flesta artister ärligt talat (utom rockband antar jag). Favicon är implementerad i form av Ethereums monokroma logotyp. Det enda färgelement jag använt mig av är footerns övre border, som är baserad på en av Polaroids gamla logotyper. Footern är annars också ganska minimal, med en länkar till sociala medier och mail. Navigationen fungerar både på desktop och ett gäng simulerade mobiler (för mig i alla fall). Jag tycker själv att jag har fyllt sidan med lagom mycket (kopierat) innehåll, men beroende på om man är en artistisk eller komersiell fotograf så vill man förmodligen ha antingen ännu mindre eller betydligt mer. Cimage är använt för samtliga bilder.
        
        När jag valde flash/hero-bilden så märkte jag direkt att jag ville integrera den hårdare i själva designen än bara som ett fyrkantigt avgränsat objekt längst upp, så jag modifierade den en smula så att den börjar i ~vitt och slutar i ~svart. Resten av sidans tema är sedan uppbyggt kring denna tanke, där den inledande och avslutande bilden fungerar som intro/outro samt färgmässig inramning och brygga mellan ljust och mörkt. Färgtemat är på sätt och vis därmed hämtat från bilden, samtidigt som det utgjort grunden för modifikationer av bilderna. För förstasidan är både logotyp och hero-bild extra stora, medan de är mindre på undersidorna där man förmodligen är mer intresserad av själva innehållet.

    2. Tema

        Jag utgick från portfolio-temat, men skrotade det mesta. Det hela är ganska väl dokumenterat på about-sidans tema-länk, så jag upprepar mig säkert, men jag har som sagt försökt fokusera på minimalism. Dels genom val av enkelt monokromt färgtema samt diskreta typsnitt, och dels genom att försöka undvika plottrighet och en massa småelement, utan istället mest jobbat med stora bilder som är integrerade i designen snarare än avgränsade i avskilda rutor.

        Temat använder sig av SASS (.scss), uppdelat på tre olika filer för de tre olika sidorna. De innehåller dock gradvis allt mindre kod, utan det mesta är gemensamt och koncentrerat i en fil, som dock är avdelad i utmärkta stycken. Temat använder sig av variabler för färger, vilket är en av mina favoritsaker med SASS. Den andra favoritsaken är att stacka css för klasser i varandra, vilket gör det enkelt att modifiera en H1 på ett unikt sätt för ett element, exempelvis. Jag har försökt använda mig av ett antal designprinciper, men om jag hade gjort om sidan från början så hade jag nog fokuserat ännu hårdare på white/negative space, och att verkligen ge elementen luft.

    3. Responsivitet och tillgänglighet

        Jag har använt mig av flexbox på en hel del ställen på den här sidan, då jag tycker att det är smidigast att använda. De flesta element är procentbaserade (fluid), och likaså bilderna som skalas, men autocropar för att dölja overflow. Ovanpå det så har jag helt enkelt använt mig av webbläsarens inspect för att kolla så att allt ser ok ut i olika storlekar, och tweakat här och där.
        
        Jag har två olika genomgående breakpoints, en på 1400 där sidan börjar bli för bred, och en på ~7-800 där den börjar bli för smal. Den hade eventuellt haft glädje av ytterligare en mindre breakpoint för mobila enheter, men jag tyckte att det fungerade rätt ok såhär.

        100 accessibility är uppnått på alla sidor vad jag vet, och färgblindhet är inget problem eftersom allt är monokromt, och dessutom kontrasttestat.

2. **Genomförande**

    Jag tycker att det gick ganska bra att genomföra detta projekt, speciellt med tanke på att jag gjort det nu några månader efter kursens slut. Det mesta kom tillbaka ganska snabbt, även om jag så klart känner mig betydligt säkrare nu efter att jag gjort projektet än jag kände mig precis när jag började med det.

    Några stora problem uteblev faktiskt, vare sig med pico, cimage eller SASS. Däremot är jag rätt säker på att jag ska plöja ett antal böcker/kurser/videoserier om CSS ifall jag någonsin ska jobba mycket med det. Grunderna vad gäller margins/paddings och vilket element det är bäst att utföra ändringarna på kan man nog inte nöta in för hårt. Samma sak med responsivitet och flexbox.

    Det var ett någorlunda lätt och rimligt projekt, tidsåtgången styrs dock kanske främst av brist på kreativitet och fallenhet för design, samt viss brist på rutin.

3. **Kursen**

    Jag tycker att detta varit en bra kurs, med bra material och handledning. Om jag skulle föreslå någon ändring så vore det kanske i så fall ett tillägg av en viss mängd kraftigt avgränsat nötande, som labbarna i de andra kurserna. Typ 50 små CSS-problem som behöver lösas, med stegrande svårighetsgrad. Kan tänka mig att det blir lite svårt att implementera rättning av det, men kanske något att fundera på åtminstone. Jag är nöjd och ger kursen 10 av 10, samt kan definitivt tänka mig att rekommendera den till vänner/kollegor.
    
