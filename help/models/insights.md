---
title: Modellinsikter
description: Lär dig mer om din modell, som historisk översikt, modellinsikter och modellkvalitet i Mix Modeler.
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 0ee212a626986e4c721d0e58f2528d0ca1a9fdbf
workflow-type: tm+mt
source-wordcount: '1549'
ht-degree: 0%

---

# Modellinsikter

Så här visar du modellinsikter i gränssnittet ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i Mix Modeler:

1. I tabellen **[!UICONTROL Models]** väljer du namnet på en modell som har **[!UICONTROL Last run status]** av <span style="color:green"> ●</span> **[!UICONTROL Success]**.

1. Välj **[!UICONTROL Model Insights]** på snabbmenyn.

![Flikfältet Modellinsikter](/help/assets/model-insights-tabbar.png)

Du ser när den angivna modellen senast har uppdaterats och visualiseringar visas på fyra flikar: [Modellinsikter](#model-insights), [Attribution](#attribution), [Factors](#factors), [Diagnostics](#diagnostics) och [Historiköversikt](#historical-overview).

Du kan ändra den datumperiod som visualiseringarna på varje flik baseras på. Ange en datumperiod eller välj ![Kalender](/help/assets/icons/Calendar.svg) för att välja en datumperiod.

## [!UICONTROL Model insights]

På fliken Modellinsikter visas visualiseringar för [Bidrag per datum och basmedia](#contribution-by-date-and-base-media), [Bidrag per kanal](#contribution-by-channel), [Sammanfattning av marknadsföringsprestanda](#marketing-performance-summary) och [Marginalkurvor](#marginal-response-curves). Fliken innehåller även en [tabell för sammanställning av kontaktpunkter](#touchppint-breakdown).

![Modell - Modellinsikter](/help/assets/model-insights-insights.png)

* Du kan hovra över enskilda diagramelement i varje visualisering för att visa en pover med mer information.

* Om du vill hämta en CSV-fil som innehåller data för visualiseringen väljer du ![Hämta](/help/assets/icons/Download.svg).

* Om du vill hämta fullständiga modellinsiderdata i Microsoft® Excel-format väljer du ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Download data]**.


### Bidrag per datum och basmedia.

Det staplade diagrammet ordnas: Bas längst ned, Ej använda kanaler i mitten och Utläggskanaler överst.

### Bidrag per kanal

I donutvisualiseringen visas en fördelning av bidraget per kanal.

### Sammanfattning av marknadsföringsprestanda.

Ett vågrätt stolpdiagram som visar ROI-prestanda per kanal.

### Marginalkurvor.

Linjediagrammet visar och jämför de marginella vinster som genereras av investeringen i era marknadsföringskanaler.  Och identifierar den brytpunkt där den inkrementella avkastningen är mindre än de inkrementella utgifterna. Den här visualiseringen hjälper er därför att förstå när era marknadsföringsinvesteringar börjar bli mindre effektiva.

Kurvan, brytpunkten och motsvarande värden beräknas baserat på det markerade dataområdet och den kanal du har valt.

Så här ändrar du kanal:

* Välj en kanal i listrutan **[!UICONTROL Channel]** om du vill uppdatera visualiseringen för en viss kanal.


### Uppdelning efter kontaktpunkter

Kontaktpunktsuppdelningstabellen visar brytpunkter för alla eller valda kanaler varje vecka.

![Uppdelning efter kontaktpunkter](../assets/touchpoint-breakdown.png)

Följande kolumner är tillgängliga:

| Kolumn | Beskrivning |
|---|---|
| **[!UICONTROL Date range]** | Veckan att rapportera om. |
| **[!UICONTROL Touchpoint]** | Den specifika kontaktytskanalen. |
| **[!UICONTROL ROI]** | Procentandelen (**[!UICONTROL Revenue]** - **[!UICONTROL Spend]**) / **[!UICONTROL Spend]**. |
| **[!UICONTROL Revenue]** | Intäkterna för datumintervallet. |
| **[!UICONTROL CPA]** | **[!UICONTROL Spend]** / **[!UICONTROL Conversions]**. |
| **[!UICONTROL Conversions]** | Konverteringarna för datumintervallet. |
| **[!UICONTROL Spend]** | Utgifterna för dataområdet. |

Om du vill välja en viss kanal eller alla kanaler väljer du den i listrutan **[!UICONTROL View]**.

Välj ![Hämta](/help/assets/icons/Download.svg) **[!UICONTROL Download CSV]** om du vill hämta innehållet i Touchpoint-tabellen.

## **[!UICONTROL Factors]** [!BADGE beta]

Fliken Faktorer [!BADGE beta] visar externa faktorrelaterade insikter.

![Faktorer](/help/assets/factors.png)

Den här visualiseringen hjälper dig att förstå den inkrementella effekt som olika interna och externa faktorer har på konverteringens baslinje. Exempel: ekonomiska villkor eller marknadsföringsaktiviteter.

Använd listrutan **[!UICONTROL Factors]** för att välja vilka faktorer du vill visa.

<!-- need to update the image when we do have a proper example -->

Om du vill hämta en CSV-fil som innehåller data för tabellen väljer du ![Hämta](/help/assets/icons/Download.svg).

Om inga data är tillgängliga visas meddelandet ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]**.

## [!UICONTROL Attribution]

>[!NOTE]
>
Fliken Attribution är bara tillgänglig för MTA-aktiverade modeller.


På fliken [!UICONTROL Attribution] kan du förstå effekten av kontaktytor och marknadsföringskampanjer som har data på händelsenivå.  Se [Skapa modell](build.md).

Följande attribueringsmodeller stöds:

* Baserat på den valda modellen i Mix Modeler:
   * Algoritmisk - påverkad
   * Algoritmisk - inkrementell
* Regelbaserad:
   * Minskningsenheter
   * Första beröringen
   * Senaste beröring
   * Linjär
   * Ushape

Se [Multi-touch-attribuering](../get-started/about.md#multi-touch-attribution) för en introduktion om multitouch-attribueringsfunktionen i Mix Modeler.

Välj en eller flera attribueringsmodeller i listrutan **[!UICONTROL Attribution Model]**. De valda attribueringsmodellerna gäller för alla visualiseringar på fliken Attribution.

![Attribution](/help/assets/model-insights-attribution.png)

Mix Modeler Multi-Touch-attribuering i korthet anpassar sig efter Mix Modeler övergripande poäng och ROI. Dessa bakgrundsmusik är också tillgängliga som datauppsättningar i Experience Platform.

Fliken Attribution består av följande visualiseringar:

### [!UICONTROL Overview]

Visualiseringen av [!UICONTROL Overview] visar, för de valda attribueringsmodellerna, konverteringssummor och procentandelar. Om du väljer flera modeller läggs ytterligare cirklar till i visualiseringen, där var och en har en egen färg som motsvarar teckenförklaringen.

Om du vill visa ett popup-fönster med information om en attribueringsmodell håller du pekaren över någon av cirklarna i visualiseringen.

### [!UICONTROL Trends]

Visualiseringen [!UICONTROL Daily trends], [!UICONTROL Weekly trends] eller [!UICONTROL Monthly trends] visar konverteringstrender per dag, vecka eller månad för de valda attribueringsmodellerna.

Välj punkt genom att välja **[!UICONTROL Daily trends]**, **[!UICONTROL Weekly trends]** eller **[!UICONTROL Monthly trends]** från ![Mer](/help/assets/icons/More.svg).

Om du vill se information för du markören över dataraden för en viss attribueringsmodell och visar en portfölj som visar det totala antalet konverteringar för dessa data.

### [!UICONTROL Breakdown]

Visualiseringen [!UICONTROL Breakdown] är en uppdelning efter kanal eller kontaktyta av konverteringarna för var och en av de valda attribueringsmodellerna. Den här visualiseringen kan vara till hjälp när du ska fatta beslut om effektiviteten för varje kanal eller kontaktyta.

Välj uppdelningstyp select **[!UICONTROL Breakdown by channel]** eller **[!UICONTROL Breakdown by touchpoint]** från ![Mer](/help/assets/icons/More.svg).

Håll markören över något av diagramelementen om du vill se detaljer.

### [!UICONTROL Top campaigns]

I visualiseringen av de populäraste kampanjerna visas en tabell över de främsta kampanjerna med kolumner för Campaign-namn, Channel-typ och medietyp and Inkrementella konverteringar. Den här visualiseringen kan hjälpa ert team att informera om effektiviteten hos en viss kampanj för en viss kanal och ge er insikter om vilka kampanjer ni bör investera i ytterligare.

Sortera tabellen i stigande eller fallande ordning ↓ för kanal, medietyp or Stegvisa konverteringar, markera kolumnrubriken och växla sortering.

Om du vill expandera tabellen i en separat dialogruta väljer du **[!UICONTROL Expand]** från ![Mer](/help/assets/icons/More.svg).

I den utökade dialogrutan för de bästa kampanjerna visas samma tabell med extra kolumner för

* Inkrementella konverteringar
* Påverkade konverteringar
* Första beröringskonverteringen
* Senaste pekkonverteringar

Du kan markera de extra kolumnrubrikerna om du vill sortera tabellen i stigande eller fallande ordning.

Välj **[!UICONTROL Close]** om du vill stänga den utökade dialogrutan för de bästa kampanjerna.


### [!UICONTROL Breakdown by touchpoint position]

Visualiseringen av [!UICONTROL Breakdown by touchpoint position] är en uppdelning av konverteringar av attribut efter position för kontaktytan och kontaktytan över alla konverteringssökvägar. I det här diagrammet kan du jämföra om en kontaktyta bidrar bättre på en position än återstående positioner och andra kontaktytor på en position.

>[!NOTE]
>
Summan av procentandelen för en attribueringsmodell för alla kontaktytor och positioner ska vara lika med 100.


Positionerna [!UICONTROL Starter], [!UICONTROL Player] och [!UICONTROL Closer] definieras enligt följande:

| Position | Beskrivning |
|---|---|
| [!UICONTROL Starter] | Den här positionen anger om kontaktytan är den första beröringen i en konverteringsbana. |
| [!UICONTROL Player] | Den här positionen anger om kontaktytan inte är den första eller sista beröringsraden som leder till konvertering. |
| [!UICONTROL Closer] | Den här positionen anger om kontaktytan är den sista kontakten före konvertering. |


### [!UICONTROL Top conversion paths]

Visualiseringen [!UICONTROL Top conversion paths] visar de fem populäraste konverteringssökvägarna baserat på de valda attribueringsmodellerna.

För varje konverteringsbana ser du:

* antalet kanaler som påverkas,
* de totala tilldelade banorna,
* procentandelen av de tilldelade banorna för denna konverteringsbana jämfört med de totala tilldelade banorna,
* för varje kanal, bidragsprocenten för attribueringsmodellen, och
* summan av dessa procentsatser för kanalattribueringsmodellen.


## [!UICONTROL Diagnostics]

På fliken Diagnostik visas visualiseringar för:

* [!UICONTROL Model Assessment]-visualisering, som du kan bryta ned för konverteringar av faktisk kontra förväntad eller residual.

Om du vill bryta ned visualiseringen väljer du **[!UICONTROL Actual vs. Predicted]** eller **[!UICONTROL Residuals]** i listan **[!UICONTROL Breakdown]**.

* [!UICONTROL Model fitting metrics]-tabell, med följande kolumner för varje konverteringsmått:

   * Faktisk konvertering

   * Modellerad konvertering

   * Restkonvertering (skillnad mellan faktisk konvertering och modellkonvertering)

   * Värden för modellkvalitetsskala:

      * R2 (R-fyrkantig), som anger hur väl data passar in i regressionsmodellen (godheten i passform).

      * MAPE (medelvärde för absolut procentfel), som är en av de mest använda KPI:erna för att mäta prognosens exakthet och uttrycker prognosfelet som en procentandel av det faktiska värdet.

      * RMSE (Rot Mean Square Error): som visar det genomsnittliga felet, viktat enligt kvadraten på felet.

Om du vill hämta en CSV-fil som innehåller data för tabellen väljer du ![Hämta](/help/assets/icons/Download.svg).

* [!UICONTROL Touchpoint effectiveness]-tabellen, som representerar resultatet av AI-algoritmisk modell för attribuering. Data för det här registret genereras endast för specifika tidsperioder. Välj **[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg) om du vill ha mer information.

Visualiseringen visar, i fallande ordning [!UICONTROL Efficiency measure] ![Fallande ordning](/help/assets/icons/SortOrderDown.svg), för varje kontaktyta:

   * [!UICONTROL Paths touched]: visualiserar procentandelen sökvägar som uppnår konvertering och procentandelen sökvägar som inte uppnår konvertering. För en kontaktyta ser du fler konverteringar när attribueringskonverteringsgraden är hög. Proportionerna jämför procentandelen sökvägar som leder till konvertering med procentandelen sökvägar som *inte* leder till konvertering.
   * [!UICONTROL Efficiency measure]: genereras av den algoritmiska attribueringsmodellen och effektivitetsmåttet anger den relativa vikten av en kontaktyta mot konverteringen, oberoende av kontaktytpunktsvolym. Effektiviteten mäts på en skala från 1 till 5. Observera att högre kontaktytpunkter inte garanterar högre effektivitetsmått.
   * [!UICONTROL Total volume]: Det sammanlagda antalet gånger en användare vidrör en kontaktyta. Antalet är inklusive kontaktytor som visas på en bana som uppnår konvertering samt banor *som inte* resulterar i konvertering.

![Diagnostik](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

Fliken Historisk översikt visar visualiseringar för:

* Konvertering och utgifter per kv och produkt.

* Utgift per kanal.

* Utlägg för kontaktpunkt.

Du kan välja en alternativ utgiftsbaserad kanal att visa för den här visualiseringen. Välj en kanal från **[!UICONTROL Channels]**.

* Pekpunktsvolym.

Du kan välja en alternativ volymbaserad kanal att visa för den här visualiseringen. Välj en kanal från **[!UICONTROL Channels]**.

![Modell - historisk översikt](/help/assets/model-insights-historical-overview.png)

## **[!UICONTROL Edit]**

Du kan redigera namn, beskrivning och schemaläggning av utbildning och poängsättning för modellen.

1. Välj ![Redigera](/help/assets/icons/Edit.svg) Redigera

1. I dialogrutan **[!UICONTROL Edit model]**:

   * Ange en ny **[!UICONTROL Name]** och **[!UICONTROL Description]**.

   * Aktivera **[!UICONTROL Status]** om du vill aktivera schemaläggning. Du kan bara aktivera schemaläggning för modeller som är tränade och poängsatta.

      1. Välj en **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: Ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Välj en veckodag och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Välj en dag i månaden i listrutan Kör på varje och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).

      1. Välj en **[!UICONTROL Training frequency]** i listrutan: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** eller **[!UICONTROL None]**.

     ![Redigera en modell](../assets/model-edit.png)

1. Välj **[!UICONTROL Save]**.
