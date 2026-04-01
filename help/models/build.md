---
title: Bygg modeller i Mix Modeler
description: Lär dig hur du bygger modeller i Mix Modeler, inklusive hur du konfigurerar, konfigurerar och anger avancerade alternativ för modellen. som konverteringsmål, kontaktytor, adstock och schemaläggning.
feature: Models
solution: Mix Modeler
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 7836e378a0f9068fc868dcede0ab8b3e2803776a
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 0%

---

# Skapa modeller

Gränssnittet ger ett stegvis guidat modellkonfigurationsflöde när du vill skapa anpassade AI-baserade modeller.

Välj **[!UICONTROL Open model canvas]** i gränssnittet ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i [!DNL Mix Modeler].

## Inställningar

Du definierar ett namn och en beskrivning i **[!UICONTROL Setup]**-steget:

1. Ange modellen **[!UICONTROL Name]**, till exempel `Demo model`. Ange en **[!UICONTROL Description]**, till exempel `Demo model to explore AI features of Mix Modeler`.

   ![Modellnamn och beskrivning](/help/assets/model-name-description.png)

1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.

## Konfigurera {#configure}

>[!CONTEXTUALHELP]
>id="model_marketingtouchpoints_select"
>title="Marknadsföringskontaktytor"
>abstract="Marknadsföringskontaktytorna är marknadshändelser på mottagarnivå, individ- och cookienivå som används för att utvärdera effekten av marknadsinvesteringar på numeriska eller intäktsbaserade konverteringar.<br/><br/>Du kan inte konfigurera modellen med kontaktytor som har överlappande data och det måste finnas minst en kontaktyta med utgift."


Du konfigurerar modellen i steget **[!UICONTROL Configure]**. Konfiguration innefattar definition av konverteringsmål, kontaktytor för marknadsföring, den stödberättigade datapopulationen, externa och interna faktorer, med mera.

1. I avsnittet **[!UICONTROL Conversion goal]**:

   ![Modell - konverteringssteg](/help/assets/model-conversion-step.png)

   1. Välj en konvertering i listrutan **[!UICONTROL Conversion]**. De tillgängliga konverteringarna är de konverteringar som du har definierat som en del av [Konverteringar](../harmonize-data/conversions.md) i [!UICONTROL Harmonized datasets]. Exempel: **[!UICONTROL Online Conversion]**.

   1. Du kan välja ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]** om du vill skapa en konvertering direkt från modellkonfigurationen.



1. I avsnittet **[!UICONTROL Marketing touchpoints]** kan du välja en eller flera kontaktytor för marknadsföring, som motsvarar de kontaktytor för marknadsföring som du har definierat som en del av [Marknadsföringskontaktytor](../harmonize-data/marketing-touchpoints.md) i [!UICONTROL Harmonized datasets].


   ![Modell - steg för kontaktyta vid marknadsföring](/help/assets/model-marketing-touchpoint-step.png)

   1. Välj en eller flera kontaktytor för marknadsföring i listrutan **[!UICONTROL Touchpoint include]**.

      * Du kan använda ![CrossSize75](/help/assets/icons/CrossSize75.svg) för att ta bort en kontaktyta.
      * Du kan använda **[!UICONTROL Clear all]** för att ta bort alla kontaktytor.

   1. Du kan välja ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]** om du vill skapa en marknadsföringskontaktyta direkt från modellkonfigurationen.

   >[!NOTE]
   >
   >Du kan inte ställa in modellen med kontaktytor som har överlappande data och det måste finnas minst en kontaktyta med utgifter.

1. Som standard genereras en poäng för alla data i din harmoniserade vy. Om du bara vill poängsätta en delmängd av populationen definierar du ett eller flera filter med hjälp av behållare i avsnittet **[!UICONTROL Eligible data population]**.

   ![Modell - kvalificerade datapifieringar](/help/assets/model-eligible-data-population-step.png)

   * Definiera en eller flera händelser för varje behållare.

      1. För varje händelse:

         1. Välj ett mått eller en dimension från **[!UICONTROL _Välj harmoniserat fält_]**.

         1. Välj lämplig operator: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** eller **[!UICONTROL is not in]**.

         1. Ange eller välj ett värde vid **[!UICONTROL _Ange eller välj värdet_]**.

      1. Om du vill lägga till ytterligare en händelse i behållaren väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

      1. Om du vill ta bort en händelse från behållaren väljer du ![Stäng](/help/assets/icons/CrossSize75.svg).

      1. Om du vill filtrera med hjälp av alla eller några av flera händelser som definieras i behållaren väljer du **[!UICONTROL Any of]** eller **[!UICONTROL All of]**. Etiketten ändras på motsvarande sätt från **[!UICONTROL Include ... Or ...]** till **[!UICONTROL Include ... And ...]**.

   * Välj ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]** om du vill lägga till en giltig dataifyllningsbehållare.

   * Om du vill ta bort en giltig dataifyllningsbehållare i behållaren väljer du ![Mer](/help/assets/icons/More.svg) och sedan **[!UICONTROL Remove container]** på snabbmenyn.

   * Välj **And** och **Or** mellan behållare om du vill skapa mer komplexa definitioner för den giltiga datapifyllningen.

1. Du kan hantera datauppsättningar som innehåller interna eller externa faktorer i avsnittet **[!UICONTROL Factor dataset]**.

   ![Modell - Faktordatamängdssteg](../assets/model-factors-dataset-step.png)

   * Om du vill lägga till en faktordatauppsättning väljer du **[!UICONTROL Add Factor]**. Du kan lägga till högst 30 faktorer i en modell.

      1. Välj en **[!UICONTROL Factor dataset]** i listrutan. De tillgängliga faktorerna är de faktorer som du har definierat ett harmoniserat fält för i [datauppsättningsreglerna](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule).
Baserat på den valda datauppsättningen är **[!UICONTROL Factor type]** antingen **[!UICONTROL Internal]** eller **[!UICONTROL External]**.

      1. Välj **[!UICONTROL Impact on conversion]** i listrutan. Tillgängliga alternativ är: **[!UICONTROL Auto]**, **[!UICONTROL Positive]** eller **[!UICONTROL Negative]**. Standardalternativet är **[!UICONTROL Auto]**, vilket gör att modellen kan avgöra faktordatauppsättningens påverkan.

   * Om du vill ta bort en faktordatauppsättning väljer du ![CrossSize200](/help/assets/icons/CrossSize400.svg).


1. Ange ett värde mellan `1` och `52` i **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]** i avsnittet **[!UICONTROL Define lookback window]** om du vill definiera uppslagsfönstret för modellen.

1. Om du vill definiera utbildningsfönstret för en modell väljer du på **[!UICONTROL Define training window]** var du vill starta poängkonverteringar.

   ![Modell - Definiera utbildningsfönster](/help/assets/model-define-training-window.png)

   Du kan välja mellan:

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** och

   * **[!UICONTROL Manually input a training window]**. Ange antalet år i **[!UICONTROL Include events the following years prior to a conversion]** när du väljer det här alternativet.

   Den här inmatningen krävs för en modell. Antalet år avgör hur mycket av kanalens adstock som du kan konfigurera i steget **[!UICONTROL Advanced]** begränsas.

1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs. <br/>Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg. <br/>Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.


## Avancerat {#advanced}

>[!CONTEXTUALHELP]
>id="model_advanced_channeladstock"
>title="Kanaladstock"
>abstract="Lägg in domänexpertis, experimentella resultat eller tidigare kanalanalyser direkt i modellkonfigurationen. Adstock-konfigurationen hjälper modellen att anpassa sig efter verkliga förväntningar och förbättrar tolkningsförmågan och förtroendet för resultatet. Det totala antalet uppslagsveckor plus fördröjningsveckor per kanal begränsas till en åttondel av det konfigurerade utbildningsfönstret. Den här begränsningen tillåter tillräckligt med data för att modellen ska kunna lära sig adstock-effekterna."

Du kan ange avancerade inställningar i steget **[!UICONTROL Advanced]**. I det här steget kan du definiera [utgiftsresurs](#spend-share), aktivera modellen för [multi-touch-attribution (MTA)](#mta), definiera [tidigare kunskap](#prior-knowledge) och definiera [kanaladstock](#channel-adstock).

### Utgiftsresurs

I avsnittet **[!UICONTROL Spend share]**:

* Aktivera **[!UICONTROL Allow spend share]** om du vill använda tidigare investeringsförhållanden för marknadsföring för att informera modellen när marknadsföringsdata är begränsade. Den här inställningen rekommenderas, särskilt i följande scenarier:
   * En kanal har inte tillräckligt många observationer (t.ex. låg frekvens av utgifter, visningar eller klick).
   * Du modellerar spiky men regular och potentiellt högspenderade media (som TV för vissa varumärken), där data kan vara glesa.

  >[!NOTE]
  >
  >För engångsinvesteringar (t.ex. en Super Bowl-annons) kan ni lägga in dessa data som en faktor i stället för att förlita er på utgiftsdelen.
  >

### MTA

I avsnittet **[!UICONTROL MTA enabled]**:

* Aktivera **[!UICONTROL MTA enabled]** om du vill aktivera MTA-funktioner för modellen. Om du har aktiverat MTA finns multitouch-attribueringsinsikter tillgängliga efter att du har utbildat och betygsatt modellen. Se fliken [Attribution](insights.md#attribution) i [Model insights](insights.md).


### Tidigare kunskap

I avsnittet **[!UICONTROL Prior knowledge]**:

![Modell - tidigare kunskap](/help/assets/model-prior-knowledge-step.png)

1. Välj **[!UICONTROL Rule type]**, som är standard **[!UICONTROL Absolute values]**.

1. Ange procentsatser för bidrag för någon av kanalerna som listas under **[!UICONTROL Name]**, med kolumnen **[!UICONTROL Contribution proportion]**.

1. Om det är lämpligt kan du lägga till **[!UICONTROL Level of confidence]** procent för varje kanal.

1. Använd **[!UICONTROL Clear all]** vid behov för att rensa alla indatavärden för kolumnerna **[!UICONTROL Contribution proportion]** och **[!UICONTROL Level of confidence]**.


### Kanaladstock

I avsnittet **[!UICONTROL Channel adstock]** kan du definiera enskilda adstock-lookback (överföringar eller dekorationseffekter) och fördröjning (fördröjd svarstid) för varje kanal (marknadsföringskanal) som du har definierat i modellen.

Den här kanalens adstock-konfiguration ger detaljerad kontroll över hur olika marknadsföringskanaler påverkar affärsresultatet över tid. Du kan också använda systemstandardvärden och en konfiguration som passar alla.

Kanalkonfigurationen hjälper dig att fånga kanalspecifika nyanser. Exempel: den långvariga effekten av tv-kampanjer, den kortvariga effekten av betalsökningar eller fördröjningen mellan påverkarutgifter och observerbara konverteringar. Experimentera med parametrar för snabb sökning och fördröjning för att skapa mer korrekta, skräddarsydda och pålitliga insikter. I slutändan kan en kanalkonfiguration leda till exaktare budgetallokeringar och bättre affärsbeslut.

![Kanaldata](/help/assets/channel-ad-stock.png)

Så här konfigurerar du kanaldata:

* Definiera ett **[!UICONTROL Lag (weeks)]**-, **[!UICONTROL Min Lookback (weeks)]**- och **[!UICONTROL Max Lookback (weeks)]**-värde för varje kanal (**[!UICONTROL Name]**). För varje värde:

   * Använd ![Lägg till](/help/assets/icons/Add.svg) om du vill öka ett värde, ![Subtrahera](/help/assets/icons/Subtract.svg) om du vill minska ett värde eller ange ett värde manuellt.

  Det totala antalet fördröjningsveckor plus maximala uppslagsveckor per kanal begränsas till en åttondel av det konfigurerade utbildningsfönstret. Den här begränsningen tillåter tillräckligt med data för att modellen ska kunna lära sig adstock-effekterna. För ett tvåårigt utbildningsfönster är det maximala antalet **[!UICONTROL Lag (weeks)]** och **[!UICONTROL Lookback (weeks)]** för en kanal till exempel 13 veckor. Den här ändpunkten används när du definierar värdena.


## Ange alternativ

Du kan [schemalägga utbildning och poängsättning](#schedule) och ange [detaljerade insikter, rapportfält](#granular-insights-reporting-fields) för modellen i steget **[!UICONTROL Set options]**.


### Schema

I avsnittet **[!UICONTROL Schedule]** kan du schemalägga modellutbildning och poängsättning.

![Schemamodell](../assets/model-schedule.png)

Så här schemalägger du poäng och utbildning för modeller:

1. Aktivera **[!UICONTROL Enable scheduled model scoring and training]**.
1. Välj en **[!UICONTROL Scoring frequency]**:

   * **[!UICONTROL Daily]**: Ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg) för att definiera tiden.
   * **[!UICONTROL Weekly]**: Välj en veckodag och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg) för att definiera tiden.
   * **[!UICONTROL Monthly]**: Välj en dag i månaden i listrutan Kör på varje och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg) för att definiera tiden.

1. Välj en **[!UICONTROL Training frequency]** i listrutan: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** eller **[!UICONTROL None]**.


### Rapporteringsfält för detaljerade insikter

Avsnittet **[!UICONTROL Granular insights reporting fields]** använder rapportfunktionen för detaljerad inkrementalitet. Med den här funktionen kan du välja harmoniserade fält för att bryta ned poängen för konvertering och kontaktpunktsökning.

![Definiera detaljerade insikter, rapportfält](/help/assets/granular-insights-reporting-fields.png)

Du definierar dessa harmoniserade fält så att du kan gå nedåt i modellrapporteringen med hjälp av detaljerade rapportkolumner i stället för att behöva skapa separata modeller.

Du kan till exempel skapa en modell som fokuserar på intäkter, men du är också intresserad av kampanjernas, medietyperna, regionerna och trafikkällornas prestanda. Utan den detaljerade inkrementalitetsrapporteringen skulle du behöva skapa fyra separata modeller. Med den detaljerade funktionen för inkrementalitetsrapportering kan ni dela upp intäktsmodellen för kampanjer, medietyper, regioner och trafikkällor.

1. Välj ett eller flera harmoniserade fält från **[!UICONTROL _Välj harmoniserade fält_]** under **[!UICONTROL Includes]**. De valda harmoniserade fälten läggs till på panelen.
1. Välj **[!UICONTROL *Harmoniserat fält *]**![CrossSize100](/help/assets/icons/CrossSize100.svg) om du vill ta bort ett harmoniserat fält från behållaren med de valda harmoniserade fälten.
1. Välj **[!UICONTROL Clear all]** om du vill ta bort alla markerade harmoniserade fält.

De valda harmoniserade fälten för detaljerad tillväxtrapportering är tillgängliga som en del av Experience Platform [schema](/help/ingest-data/schemas.md) och [datamängd](/help/ingest-data/datasets.md) som är ett resultat av att modellen bedömts. Rapporteringsfälten för detaljerade insikter finns i objekten **[!UICONTROL conversionPassthrough]** och **[!UICONTROL touchpointPassthrough]**.

![Skärmbild av objekten conversionPassthrough och touchPointPassthrough i ett schema för en modell som har aktiverats för detaljerad rapportering om inkrementalitet](/help/assets/schema-granular-insights-reporting.png)


## Slutför

* Välj **[!UICONTROL Finish]** för att slutföra modellkonfigurationen.

   * I dialogrutan **[!UICONTROL Create instance?]** väljer du **[!UICONTROL Ok]** för att utlösa den första uppsättningen kurser och poäng direkt. Din modell visas med statusen ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Välj **[!UICONTROL Cancel]** om du vill avbryta.

   * Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs.

* Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg.

* Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.

