---
title: Datauppsättningsregler
description: Lär dig hur du definierar datauppsättningsregler som ska användas som en del av att harmonisera data i Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 9987c845414fa5a3abda201d55f7b1ed6e211780
workflow-type: tm+mt
source-wordcount: '2102'
ht-degree: 0%

---

# Datauppsättningsregler

Datauppsättningsreglerna hjälper dig att mappa dina harmoniserade fält till fält från data som du har inhämtat i Mix Modeler.

* För sammanställda data som du har kapslat i Adobe Experience Platform mappar du ett eller flera av de tillgängliga datamängdsfälten till lämpliga harmoniserade fält.
* För händelsedata kan du mappa ett eller flera harmoniserade fält till fält från datauppsättningen, direkt eller med villkor.


## Hantera datauppsättningsregler

Om du vill visa en tabell med tillgängliga datauppsättningsregler i Mix Modeler-gränssnittet:

1. Välj ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** i den vänstra listen.

1. Välj **[!UICONTROL Dataset rules]** i det övre fältet. Du ser en tabell med datauppsättningsreglerna.

Du kan snabbt söka efter en datauppsättning med ![Sök](/help/assets/icons/Search.svg) **[!UICONTROL _Ange ett datauppsättningsnamn_]**.

Tabellkolumnerna anger information om datauppsättningsreglerna:

| Kolumnnamn | Information |
| ---------------------- | ----------|
| **[!UICONTROL Dataset]** | Datauppsättningens namn.  Använd ![Mer](/help/assets/icons/More.svg) för att välja åtgärder för en datauppsättning. Du kan:<ul><li>![Förhandsgranska](/help/assets/icons/Preview.svg) **[!UICONTROL View]** om du vill visa datauppsättningsregelkonfigurationen. Alla fält är inaktiverade.</li><li>![Redigera](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** om du vill redigera regelkonfigurationen för datauppsättningen.</li><li>![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** om du vill ta bort konfigurationen för datauppsättningsreglerna. Du uppmanas att bekräfta borttagningen i dialogrutan Ta bort datauppsättning. Välj **[!UICONTROL Delete]** om du vill ta bort datauppsättningsregelkonfigurationen permanent.</li><ul> |
| **[!UICONTROL Source]** | Källan till datauppsättningen: Adobe Analytics, Experience Events, Summary (sammanställd) eller Consumer Experience Events. |
| **[!UICONTROL Schema]** | Schemat som datauppsättningen följer. Du kan snabbt välja schemanamnet för att öppna schemat på en ny flik i schemaredigeraren i ![Schema](/help/assets/icons/Schemas.svg) [Scheman](../ingest-data/schemas.md). |
| **[!UICONTROL Granularity]** | Detaljrikedomen för data i datauppsättningen. Möjliga värden är Daily, Weekly, Monthly eller Yearly. |
| **[!UICONTROL Start of the week]** | Anger vilken veckodag som betraktas som början av en ny vecka för den specifika datauppsättningen. |
| **[!UICONTROL Status]** | Fältets status: ![StatusGray](/help/assets/icons/StatusGray.svg) Draft eller ![StatusGreen](/help/assets/icons/StatusGreen.svg) Active |
| **[!UICONTROL Last modified]** | Data och tid för den senaste ändringen av datauppsättningsregeln. |

{style="table-layout:auto"}

### Skapa en datauppsättningsregel

Om du vill skapa en datauppsättningsregel väljer du ![ i guiden ](/help/assets/icons/DataCheck.svg) i **[!UICONTROL Harmonized data]** **[!UICONTROL Dataset rules]** > **[!UICONTROL Create a dataset rule]** i Mix Modeler-gränssnittet **[!UICONTROL Dataset rules configuration]** DataSearch .

På skärmen **[!UICONTROL Create]**

1. I **[!UICONTROL Dataset details]** väljer du en datauppsättning från **[!UICONTROL Select dataset]** för att starta konfigurationen. I listan kategoriseras datauppsättningar i **[!UICONTROL Summary]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]**, **[!UICONTROL Factors]** och **[!UICONTROL Consumer Experience Events]**.

1. Välj en dag för **[!UICONTROL Start of the week]**.

1. Välj **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** eller **[!UICONTROL Yearly]** för **[!UICONTROL Granularity]**.

1. När du har valt en datauppsättning i kategorin **[!UICONTROL Summary]** eller **[!UICONTROL Factors]** väljer du **[!UICONTROL Aggregation]** eller **[!UICONTROL Replacement]** för **[!UICONTROL Data restatement is by]**.

   Att rapportera data från utgivare är mycket viktigt för marknadsföringsanalytiker, eftersom det ofta innebär betydande utgifter, och förändringar i rapporteringsdata kan leda till mycket olika insikter och investeringsplaner. Dessutom behöver marknadsföringsanalytiker korrekta data för att få fram rätt insikter och lägga fram övertygande förslag för att få intressenternas förtroende. Men dessa utgivare, som Google och Facebook, skriver ofta om eller tar bort rapporteringsdata när de sammanställer deras data. Tidsperioden för de flesta ändringar är inom 7 dagar från den rapporterade medieprestandan. Ytterligare förändringar i data är möjliga inom 30 dagar. Efter 30 dagar betraktas böcker som stängda och data fullständiga.

   Mix Modeler har stöd för omräkning av data. För att säkerställa att de data som används för rapportering, modellering och planering är korrekta. Och att data kan stödja varumärkes- och marknadsföringsanalytikernas förväntningar och behov.

   Du kan skicka omräknade rader med sammanfattningsdata som inkrementella rader i en Experience Platform-datamängd och harmoniseringstjänsten uppdaterar den harmoniserade datamängden med dessa omräknade data. På samma sätt kan du även ta bort rader med sammanfattningsdata som måste återspeglas i harmoniseringstjänsten.

1. I avsnittet **[!UICONTROL Map to harmonized fields]** väljer du ett harmoniserat fält från **[!UICONTROL Standard harmonized field]**. Om du snabbt vill [skapa ett nytt harmoniserat fält](/help/harmonize-data/fields.md#add-a-harmonized-field) väljer du **[!UICONTROL Create new]**.

   * När det valda harmoniserade fältet är av typen mätvärde:

      1. Välj **[!UICONTROL Count]** eller **[!UICONTROL Sum]** från **[!UICONTROL Mapping type]**.

      1. Välj ett **[!UICONTROL *AEP-datamängdsfält *]**som du vill att det harmoniserade fältet ska mappas till som standard.

   * När det markerade fältet är av typen dimension:

      1. Välj **[!UICONTROL Map Into]** eller **[!UICONTROL Case]** från **[!UICONTROL Mapping type]**.

      1. När du har valt **[!UICONTROL Map Into]** väljer du **[!UICONTROL Field]** och **[!UICONTROL *AEP-datamängdsfält *]**eller **[!UICONTROL Value]**och ett standardvärde som mappar det harmoniserade fältet som standard till datamängdsfältet eller det angivna värdet.

      1. När du väljer **[!UICONTROL Case]** väljer du **[!UICONTROL Field]** och **[!UICONTROL *AEP-datamängdsfält *]**eller **[!UICONTROL Value]**och ett standardvärde för att mappa det harmoniserade fältet som standard till datamängdsfältet eller det angivna värdet.

         1. Om du vill ange värden explicit definierar du ett eller flera fall som består av ett eller flera villkor. Varje villkor kan kontrollera om det finns ett specifikt **[!UICONTROL *AEP-datamängdsfält *]**, om det är **[!UICONTROL Exists]**eller **[!UICONTROL Not Exists]**eller om det är **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**eller **[!UICONTROL Ends With]**ett värde som anges vid**[!UICONTROL * Ange indatavärde *]**.

         1. Om du vill lägga till ytterligare ett ärende väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]** och väljer ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Om du vill ta bort ett ärende eller villkor väljer du ![Stäng](/help/assets/icons/Close.svg) i motsvarande behållare.

         1. Välj **[!UICONTROL Any of]** eller **[!UICONTROL All of]** om du vill välja om något eller alla villkor ska gälla för ett ärende.

         1. Om du vill ange resultatvärdet för ett ärende anger du värdet på **[!UICONTROL Then]**.

     Exemplet nedan:

      * använder en **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** för att mappa det **[!UICONTROL Channel Type At Source]** harmoniserade fältet till fältet **[!UICONTROL channel_type]** från datamängden **[!DNL Luma Transactions]**.

      * använder **[!UICONTROL Case]** **[!UICONTROL Mapping type]** för att mappa värdet för fältet **[!UICONTROL marketing.campaignName]** i datamängden **[!DNL Luma Transactions]** villkorligt till det **[!UICONTROL Campaign]** harmoniserade fältet. Det harmoniserade fältet Campaign är inställt på:

         * `Black Friday` när **[!UICONTROL marketing.campaignName]** är `_black_friday` eller `BlackFriday`.
         * till värdet för **[!UICONTROL marketing.campaignName]** i alla andra fall.

        ![Datauppsättningsregelhändelse](/help/assets/dataset-create-event.png)

1. Välj ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** om du vill definiera ytterligare fält.

När du är klar väljer du **[!UICONTROL Save as draft]** om du vill spara ett utkast av regeln eller **[!UICONTROL Save]** om du vill spara och aktivera regeln. Välj **[!UICONTROL Cancel]** om du vill avbryta regelkonfigurationen.

>[!NOTE]
>
>Den dedikerade **[!UICONTROL Map to harmonized fields]**-upplevelsen för regler för sammanfattningsdatauppsättningar är föråldrad. Alla datauppsättningsregler använder nu liknande **[!UICONTROL Map to harmonized fields]**-upplevelse, oavsett datamängdstyp. För sammanfattningsdatauppsättningar för vilka du har definierat regler med hjälp av den föråldrade **[!UICONTROL Map to harmonized fields]**-upplevelsen kanske du vill verifiera dessa regler mot den generiska **[!UICONTROL Map to harmonized field]**-upplevelsen.
>

#### Sammanfattningsdatamängder

När du mappar ett standardiserat, harmoniserat fält från en sammanfattningsdatauppsättning försöker Mix Modeler att ta fram motsvarande Experience Platform-datamängdsfält. När det lyckades:

* Om fältet är av typen dimension markeras **[!UICONTROL Map into]** som **[!UICONTROL Mapping type]**.
* Om fältet är av måtttyp markeras **[!UICONTROL Sum]** som **[!UICONTROL Mapping type]**.
* **[!UICONTROL Field]** har valts som mappningstyp för **[!UICONTROL Default]**.
* Motsvarande Experience Platform-datamängdsfält infogas automatiskt för *AEP-datamängdsfält*.

Du kan ändra vilket som helst av de föreslagna värdena om de är felaktiga eller inte stöder ditt specifika användningssätt.


#### Faktordatamängder

Du mappar harmoniserade fält till fält i en faktordatauppsättning, så att du kan [lägga till faktorer som en del av modellkonfigurationen](/help/models/build.md).

När du mappar harmoniserade fält till fält i en faktordatauppsättning gäller följande:

##### Faktornamn

När du mappar ett standardfält för harmoniserad faktor från en faktordatamängd och fakturor innehåller en enda faktor, använder du **[!UICONTROL Map into]** som **[!UICONTROL Mapping type]** och anger ett standardvärde för det **[!UICONTROL Factor Name]** harmoniserade fältet.

![Datauppsättningsregel - mappa datauppsättning med en faktor](../assets/dataset-create-rule-factor-single.png)

Om faktordatauppsättningen innehåller flera faktorer använder du **[!UICONTROL Case As]** som **[!UICONTROL Mapping Type]** för att definiera en mappning mellan det harmoniserade fältet Faktornamn och varje distinkt faktornamn.

![Datauppsättningsregel - mappa datauppsättning med en faktor](../assets/dataset-create-rule-factor-multiple.png)


##### Typ av faktor

Det här fältet är valfritt i faktordatauppsättningen och schemat. Om **[!UICONTROL Factor type]** definieras i faktordatauppsättningen och schemat och anger antingen **[!UICONTROL Internal]** eller **[!UICONTROL External]** används det angivna värdet. Om inget värde anges används standardvärdet **[!UICONTROL Internal]**.

##### Värdetyp

Det här fältet är valfritt i faktordatauppsättningen och schemat. Om **[!UICONTROL Value type]** definieras i faktordatauppsättningen och schemat och anger antingen **[!UICONTROL Actual]** eller **[!UICONTROL Forecasted]** används det angivna värdet. Om inget värde anges används standardvärdet **[!UICONTROL Actual]**.


##### Kornighet

Du kan definiera en datauppsättningsregel för granulariteten för en faktordatauppsättning när alla faktorer i faktordatauppsättningen har samma källgranularitet.

Så snart faktablad har harmoniserats överensstämmer alla datauppsättningar med den högsta detaljnivån i den harmoniserade datauppsättningen.


##### Faktorvärde

För det **[!UICONTROL Factor value]** harmoniserade fältet använder du en av aggregeringsoperatorerna som **[!UICONTROL Mapping Type]**. När flera faktorer definieras i en faktordatauppsättning tillämpas den aggregerade operatorn på alla faktorer.


##### Exempel

* Du har en faktordatauppsättning med följande exempeldata:

  | Tidsstämpel | Faktornamn | Faktorvärde |
  |---|---|---:|
  | 13 mars 2025 | _defindesp500 | 10 |
  | 13 mars 2025 | cpi | 20 |
  | 14 mars 2025 | _defindesp500 | 30 |
  | 14 mars 2025 | cpi | 40 |
  | 15 mars 2025 | _defindesp500 | 50 |
  | 15 mars 2025 | cpi | 60 |


* Och du definierar följande datauppsättningsregler för **[!UICONTROL Factor Name]**, **[!UICONTROL Factor Value]** och **[!UICONTROL Granularity]**:

  ![Datauppsättningsregler - exempel på faktorer](../assets/dataset-create-rule-factor-example.png)

* Då resulterar detta i följande harmoniserade data:

  | Faktornamn | Faktorvärde | Typ av faktor | Värdetyp |
  |---|---:|---|---|
  | CPI | 20 | Intern | Faktisk |
  | S&amp;P 500 | 10 | Intern | Faktisk |

  Eftersom inga datauppsättningsregler har definierats för **[!UICONTROL Factor Type]** och **[!UICONTROL Value Type]** används standardvärdena.

### Redigera en datauppsättningsregel

Om du vill redigera en datauppsättningsregel går du till ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** i Mix Modeler:

1. Välj ![Mer](/help/assets/icons/More.svg) i kolumnen **[!UICONTROL Dataset]** för datauppsättningsregeln som du vill redigera.
1. Välj ![Redigera](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]** på snabbmenyn för att börja redigera datauppsättningsregeln. Mer information finns i [Skapa en datauppsättningsregel](#create-a-dataset-rule).


### Ta bort en datauppsättningsregel

Om du vill ta bort en datauppsättningsregel går du till ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** i Mix Modeler:

1. Välj ![Mer](/help/assets/icons/More.svg) i kolumnen **[!UICONTROL Dataset]** för den datauppsättningsregel som du vill ta bort.
1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** på snabbmenyn om du vill ta bort datauppsättningsregeln. Du uppmanas att bekräfta åtgärden. Välj **[!UICONTROL Delete]** om du vill ta bort den markerade datauppsättningsregeln permanent.



## Synkronisera data

Så här synkroniserar du data mellan harmoniserade data och sammanfattningar och/eller händelsedatamängder när du använder logiken i datauppsättningsreglerna:

1. Välj **[!UICONTROL Sync data]**.

1. I dialogrutan **[!UICONTROL Sync data for dataset rules]** väljer du antingen
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]** eller
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. Välj **[!UICONTROL Sync]** om du vill starta synkroniseringen baserat på definierade datauppsättningsregler mellan harmoniserade data och data i datauppsättningar. Om du vill avbryta synkroniseringen väljer du **[!UICONTROL Cancel]**.

   ![Synkronisera data](/help/assets/sync-data.png)


## Inställningar för datasammanfogning {#data-merge-preferences}


>[!CONTEXTUALHELP]
>id="harmonizeddata_datasetrules_datamergepreferences"
>title="Standardmåttinställning"
>abstract="Standardinställningen används när flera datakällor försöker uppdatera ett mätfält för en viss kanal under harmoniseringen. Den här inställningen används på sandlådenivå såvida den inte åsidosätts för vissa mätinställningar om de definieras nedan."


>[!NOTE]
>
>[!BADGE beta]{type=Informative} Inställningarna för datasammanfogning är en betafunktion och funktionen kan komma att ändras.

För att få korrekta modellprognoser kan du definiera inställningar för datasammanfogning. Med den här funktionen kan användare lösa eventuella konflikter efter sammanfogning av data på sammanfattningsnivå och händelsenivå.

Du kan konfigurera en standardmåttinställning som ska användas om det uppstår konflikter mellan uppdateringar. Det här standardmåttet kan vara ett av tre alternativ:

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

När flera datakällor försöker uppdatera ett mätfält för en viss kanal under en harmonisering, används den standardinställning som har konfigurerats av användaren. Den här inställningen används på sandlådenivå såvida den inte åsidosätts för vissa metriska inställningar som har konfigurerats ytterligare.

Under **[!UICONTROL Metric based preferences]** kan användaren konfigurera den specifika källan (**[!UICONTROL Summary]** eller **[!UICONTROL Event]**) för ett givet mätresultat och motsvarande konverteringstyp för det mätvärdet.

Vanliga användningsområden är:

* samma reklammått mäts och rapporteras i flera datauppsättningar, eller
* Måtten kan vara ofullständiga i vissa datauppsättningar, medan en annan datauppsättning kan vara en övermängd av ett visst mått, vilket resulterar i dubbelräkning.

### Konfigurera

Så här konfigurerar du inställningar för datasammanfogning:


1. Välj ![Inställningar för datasammanfogning](/help/assets/icons/Merge.svg) [!BADGE beta].

1. I dialogrutan **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}:

   ![Inställningar för datasammanfogning](/help/assets/data-merge-preferences.png)

   * Välj en **[!UICONTROL Default metric preference]**. Den valda standardinställningen för mätvärden används när flera datakällor uppdaterar ett mätfält för en viss kanal under harmonisering. Inställningen används på sandlådenivå, såvida den inte åsidosätts för specifika måttbaserade inställningar. Du kan välja mellan **[!UICONTROL Summary data]**, **[!UICONTROL Event data]** och **[!UICONTROL Sum of summary and event data]**.

   * Så här lägger du till specifika måttbaserade inställningar:

      1. Välj ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**.
         1. Välj ett mått i listan **[!UICONTROL *Måttval *]**.
         1. Välj **[!UICONTROL CHANNELS]** eller **[!UICONTROL CONVERSION TYPES]**. Välj **[!UICONTROL All]** eller en viss kanal eller konverteringstyp i listan.
         1. Välj **[!UICONTROL Summary]** eller **[!UICONTROL Event]** om du vill ange om sammanfattningsdata eller händelsedata ska prioriteras för måttet (och alla eller valda kanaler) när data sammanfogas.

         Så här lägger du till en eller flera ytterligare kanal- eller konverteringstyper:

         1. Välj ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** eller ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]**.
         1. Välj **[!UICONTROL Summary]** eller **[!UICONTROL Event]**.

         Om du vill ta bort en kanal eller konverteringstyp väljer du ![Korsa](/help/assets/icons/Close.svg).

      1. Om du vill lägga till mer specifika måttbaserade inställningar upprepar du föregående steg.

   * Om du vill ta bort en befintlig specifik måttbaserad inställning väljer du ![Ta bort](/help/assets/icons/Delete.svg).

1. Välj **[!UICONTROL Save]** om du vill spara inställningarna för datasammanfogning. En omsynkronisering av data initieras. <br/>Välj **[!UICONTROL Cancel]** om du vill avbryta.

## Ta bort en källdatauppsättning

När du tar bort en källdatauppsättning som används i dina harmoniserade data, tas de underliggande posterna i den källdatauppsättningen bort från [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md). Datauppsättningsregeln med den borttagna källdatauppsättningen finns dock kvar i konfigurationslistan för datauppsättningsregler med ikonen ![DataRemove](/help/assets/icons/DataRemove.svg) som anger att källdatauppsättningen har tagits bort. Mer information:

* Välj ![Mer](/help/assets/icons/More.svg) och ![Förhandsgranska](/help/assets/icons/Preview.svg) **[!UICONTROL View]** på snabbmenyn.
Dialogrutan **[!UICONTROL Dataset rule mapping - Fields]** visar information om den borttagna källdatauppsättningen och fälten som används i konfigurationen av datauppsättningsregeln.

När du återgår till din **[!UICONTROL Dataset rules]**-konfiguration visas en dialogruta som förklarar att en eller flera av källdatauppsättningarna har tagits bort. De harmoniserade uppgifterna påverkas av nästa ad hoc- eller schemalagda synkronisering. Granska konfigurationen av datauppsättningsregeln.

De harmoniserade data uppdateras utan borttagna källdata vid nästa ad hoc-synkronisering eller schemalagda synkronisering. Du kommer dock även fortsättningsvis att se varningsdialogrutor som uppmanar dig att ta bort datauppsättningsregeln baserat på den borttagna källdatauppsättningen. Med den här varningen kan användare visa och utvärdera de påverkade fälten i den borttagna datauppsättningen. Och för att avgöra vilken påverkan marknadsföringskontaktytor eller konverteringar kan ha på alla modeller. När du har granskat och mildrat den här effekten bör du ta bort datauppsättningsregeln från konfigurationslistan för datauppsättningsregler.
