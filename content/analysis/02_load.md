---
Title: Load
Description: Rapportsida
---

Load
=======================


Uppgiften går ut på att analysera tre wepplatser och mäta ett antal värden som har med hur lång tid det tar att ladda innehållet på hemsidorna. 

Urval
-----------------------

Jag har valt att analysera följande webbplatser:

<ul>
    <li>
<a href="https://www.youtube.com/watch?v=b1kbLwvqugk">YouTube</a></li>
</ul>

![Youtube](%base_url%/image/youtube.png?h=550&w=650) {.loadImg}

<ul>
    <li> 
<a href="https://www.asos.com/se/kvinna/ctas/host-visa-alla/cat/?cid=51129">Asos</a></li>
</ul>

![Asos](%base_url%/image/asos.png?h=550&w=650) {.loadImg}

<ul>
    <li> 
<a href="https://en.wikipedia.org/wiki/Antarctica">Wikipedia</a></li>
</ul>

![Wikipedia](%base_url%/image/wikipedia.png?h=550&w=650&border=) {.loadImg}



Jag valde dessa tre då jag ville ha helt olika typer av hemsidor för att se om det finns stora skillnader beroende på vilket innehåll de har. Youtube är som bekant en sida med videor, Asos är en onlineshop och Wikipedia är ett uppslagsverk. Youtube har som sagt mest videor på sin sida, medan Asos har till största del bilder och Wikpedia har till största del text. 

Metod
-----------------------

Jag utförde analysen genom att analysera webbplatserna på https://pagespeed.web.dev/analysis genom att mäta deras respektive hastighet och lade sedan in datan i ett kalkylark. 

Resultat
-----------------------
<div class="kalkylark">
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRuVU3Q1DPt7T1gfA5KQPxcGUIzRUn47fcTnj3AjtZH88dVshzFNY5D3C2MGS8Sa_AdnYkqStuBICd5/pubhtml?widget=true&amp;headers=false"></iframe>
</div>

Ovan har jag i Google Kalkylark rangordnat webbplatserna från långsammast till snabbast enligt devtools nätverk. Som går att utläsa så var YouTube den webbplats som tog mest tid att ladda in allt innehåll, men det var också den som hade det störst storlek och antal resurser att ladda in. Asos var den som tog näst mest tid att ladda in allt innehåll, samt var den som hade näst störst storlek och antal resurser att ladda in. Wikipedia hade minst antal resurser och minst totala storlek att ladda in och tog även kortast tid.   

PageSpeed hade också ett antal mätvärden som finns att utläsa i tabellen, exempelvis LCP (Largest Contentful Paint) och innebär tiden som det tar att ladda den största bild- eller textområdet från det att man klickar sig in på hemsidan. FID (First Input Delay) är ett annat mätvärde och mäter tider som det tar för en hemsida att ladda från det att man har interagerat med den genom att exempelvis klicka på en länk. CLS (Cumulative Layout Shift) mäter de så kallade största "layout-skiften" som sker oväntad på en sida. 

Som man kan se i tabellen så skiljer sig hastigheten exempelvis gällande LCP och hastigheten som mättes från devtools. Till exempel skilde sig Wikipedia och Youtube gällande deras LCP hastighet till deras laddningstid enligt devtools - där var deras LCP hastighet långsammare än vad laddningstiden på devtools visade. 

Man kan också se att det skiljer sig i hastigheterna beroende på om det är en mobil eller en dator som laddar in hemsidan. På Youtube och Wikipedia gick det snabbare på de mobila enheterna medan det på Asos gick aningen långsammare. Enligt PageSpeed så blev heller inte Youtube på dator godkänd enligt deras mått. 

Analys
-----------------------

Som man kunde se i tabellerna så beror laddningstid till största del på hur många resurser och den totala storleken som fanns på respektive hemsida. Det känns logiskt att den hemsida som har störst innehåll att ladda också tar längre tid på sig att göra det. Wikipedia som har mest textinnehåll gick att ladda på kortast tid. Asos hade till största del bilder och tog näst längst tid medan YouTube laddade in en video och var den som tog längst tid - mer än dubbelt så lång tid som Wikipedia-sidan. 

Pagespeed gav ett antal rekommendationer för att förbättra YouTube (dator) sidan vlket exempelvis var att "reducera JavaScript som inte används" och "reducera CSS som inte används". Enligt PageSpeed kan det ge en tisbesparing på upp till 1.08s respektive 0.20s. 

Asos hade också bland annat rekommendationerna att "reducera JavaScript som inte används" och "reducera CSS som inte används". Den uppskattade tidsbesparingen var här 0.29s repsektive 0.27s enligt PageSpeed. Wikipedia-artikelsidan var den enda som inte hade dessa rekommendationer utan hade istället "skicka bilder i modernare bildformat" och "använd bilder med rätt storlek". Uppskattade tidsbesparingar var här 0.20s och 0.18s. Varför rekommendationerna skiljer sig åt misstänker jag kan ha att göra med att Wikipedia inte i samma utsträckning använder sig av JavaScript som de andra två webbplatserna, utan där fanns till största del text och lite bilder. 

Jag tycker generellt att alla hemsidor gick att ladda väldigt snabbt och hade inga problem med tiden det tog att hämta innehållet. I och med att jag redan innan visste om vilka hemsidor det var så misstänkte jag att en sida som exempelvis Wikipedia ska gå snabbare att ladda än till exempel YouTube då jag på förhand vet att videor tar längre tid att ladda än text. Men om man inte vet vad det är för typ av hemsida i förväg skulle jag nog säga att 10 sekunder är väldigt långsamt. Alla hemsidor jag har med i den här rapporten är långt under det. 



Referenser
-----------------------
Kursmaterialet på Canvas


Övrigt
-----------------------
<i>Skriven av: Madeleine Andersson</i> 
