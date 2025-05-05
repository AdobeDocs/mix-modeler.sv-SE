---
title: Datauppsättningsregler
description: Lär dig hur du definierar datauppsättningsregler som ska användas som en del av att harmonisera data i Mix Modeler.
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a8590d604f79268bc8d1f012f2c19271a3b38668
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 0%

---

# Datauppsättningsregler

Datauppsättningsreglerna hjälper dig att mappa dina harmoniserade fält till fält från data som du matat in i Mix Modeler.

* För sammanställda data som du har kapslat i Adobe Experience Platform mappar du ett eller flera av de tillgängliga datamängdsfälten till lämpliga harmoniserade fält.
* För händelsedata kan du mappa ett eller flera harmoniserade fält till fält från datauppsättningen, direkt eller med villkor.


## Hantera datauppsättningsregler

Om du vill visa en tabell med tillgängliga datauppsättningsregler i gränssnittet Mix Modeler:

1. Välj ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** i den vänstra listen.

1. Välj **[!UICONTROL Dataset rules]** i det övre fältet. Du ser en tabell med datauppsättningsreglerna.

Tabellkolumnerna anger information om datauppsättningsreglerna:

| Kolumnnamn | Information |
| ---------------------- | ----------|
| Datauppsättning | Datauppsättningens namn. |
| Source | Källan till datauppsättningen: Adobe Analytics, Experience Events, Summary (sammanställd) eller Consumer Experience Events. |
| Schema | Schemat som datauppsättningen följer. Du kan snabbt välja schemanamnet för att öppna schemat på en ny flik i schemaredigeraren i ![Schema](/help/assets/icons/Schemas.svg) [Scheman](../ingest-data/schemas.md). |
| Kornighet | Detaljrikedomen för data i datauppsättningen. Möjliga värden är Daily, Weekly, Monthly eller Yearly. |
| Veckostart | Anger vilken veckodag som betraktas som början av en ny vecka för den specifika datauppsättningen. |
| Status | Fältets status: <p><span style="color:gray"> ●</span> utkast eller <p><span style="color:green"> ●</span> aktiv |
| Senast ändrad | Data och tid för den senaste ändringen av datauppsättningsregeln. |

{style="table-layout:auto"}

### Skapa en datauppsättningsregel

Om du vill skapa en datauppsättningsregel väljer du **[!UICONTROL Create a dataset rule]** i guiden **[!UICONTROL Dataset rules configuration]** i ![&#128279;](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** i Mix Modeler. DataSearch  > .

På skärmen **[!UICONTROL Create]**

1. I **[!UICONTROL Dataset details]** väljer du en datauppsättning från **[!UICONTROL Select dataset]** för att starta konfigurationen. I listan kategoriseras datauppsättningar i **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** och **[!UICONTROL Summary]**.

1. Välj en dag för **[!UICONTROL Start of the week]**.

1. Välj **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** eller **[!UICONTROL Yearly]** för **[!UICONTROL Granularity]**.

1. När du har valt en datauppsättning i kategorin **[!UICONTROL Summary]**:

   1. Om du vill definiera om data för datauppsättningen ska aggregeras eller ersätta befintliga data väljer du **[!UICONTROL Aggregation]** eller **[!UICONTROL Replacement]** för **[!UICONTROL Data restatement is by]**.

   1. Avbilda var och en av **[!UICONTROL Available dataset fields]** till motsvarande **[!UICONTROL Standard harmonized fields]** i **[!UICONTROL Map to harmonized fields]**. Om du inte vill mappa ett datamängdsfält till ett harmoniserat fält väljer du **[!UICONTROL -- None --]** uttryckligen.

   1. Om du behöver ett nytt harmoniserat fält, som inte är tillgängligt från listan, väljer du **[!UICONTROL Create New]** för att skapa ett nytt harmoniserat fält. Dialogrutan visas enligt beskrivningen i [Lägg till ett nytt harmoniserat fält](fields.md#add-a-harmonized-field).

   1. När mappningen är klar för alla fält för regeln väljer du **[!UICONTROL Save as draft]** om du vill spara ett utkast av regeln eller **[!UICONTROL Save]** om du vill spara och aktivera regeln. Välj **[!UICONTROL Cancel]** om du vill avbryta regelkonfigurationen.

      ![Skapa datauppsättningsregler](/help/assets/dataset-create-summary.png)

1. När du har valt en händelsekategoridatauppsättning (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**), i rutan under **[!UICONTROL Map to harmonized fields]**:

   1. Välj ett harmoniserat fält från **[!UICONTROL Standard harmonized field]**.

   1. När det valda harmoniserade fältet är av typen mätvärde:

      1. Välj **[!UICONTROL Count]** eller **[!UICONTROL Sum]** från **[!UICONTROL Mapping type]**.

      1. Välj ett **[!UICONTROL *AEP-datamängdsfält *]**&#x200B;som du vill att det harmoniserade fältet ska mappas till som standard.

   1. När det markerade fältet är av typen dimension:

      1. Välj **[!UICONTROL Map Into]** eller **[!UICONTROL Case]** från **[!UICONTROL Mapping type]**.

      1. När du har valt **[!UICONTROL Map Into]** väljer du **[!UICONTROL Field]** och **[!UICONTROL *AEP-datamängdsfält *]**&#x200B;eller **[!UICONTROL Value]**&#x200B;och ett standardvärde som mappar det harmoniserade fältet som standard till datamängdsfältet eller det angivna värdet.

      1. När du väljer **[!UICONTROL Case]** väljer du **[!UICONTROL Field]** och **[!UICONTROL *AEP-datamängdsfält *]**&#x200B;eller **[!UICONTROL Value]**&#x200B;och ett standardvärde som mappar det harmoniserade fältet som standard till datamängdsfältet eller det angivna värdet.

         1. Om du vill ange värden explicit definierar du ett eller flera fall som består av ett eller flera villkor. Varje villkor kan söka efter ett specifikt **[!UICONTROL *AEP-datamängdsfält *]**&#x200B;vare sig det är **[!UICONTROL Exists]**&#x200B;eller **[!UICONTROL Not Exists]**&#x200B;eller om det är **[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**&#x200B;eller **[!UICONTROL Ends With]**&#x200B;ett värde som anges vid&#x200B;**[!UICONTROL * Ange indatavärde *]**.

         1. Om du vill lägga till ytterligare ett ärende väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add case]** och väljer ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. Om du vill ta bort ett ärende eller villkor väljer du ![Stäng](/help/assets/icons/Close.svg) i motsvarande behållare.

         1. Välj **[!UICONTROL Any of]** eller **[!UICONTROL All of]** om du vill välja om något eller alla villkor ska gälla för ett ärende.

         1. Om du vill ange resultatvärdet för ett ärende anger du värdet på **[!UICONTROL Then]**.

      Exemplet nedan

      * använder en **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** för att mappa det **[!UICONTROL Channel Type At Source]** harmoniserade fältet till fältet **[!UICONTROL channel_type]** från datamängden **[!DNL Luma Transactions]**.

      * använder **[!UICONTROL Case]** **[!UICONTROL Mapping type]** för att mappa värdet för fältet **[!UICONTROL marketing.campaignName]** i datamängden **[!DNL Luma Transactions]** villkorligt till det **[!UICONTROL Campaign]** harmoniserade fältet. Det harmoniserade fältet Campaign är inställt på:

         * `Black Friday` när **[!UICONTROL marketing.campaignName]** är `_black_friday` eller `BlackFriday`.
         * till värdet för **[!UICONTROL marketing.campaignName]** i alla andra fall.

        ![Datauppsättningsregelhändelse](/help/assets/dataset-create-event.png)

1. Välj ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]** om du vill definiera ytterligare fält.

När du är klar väljer du **[!UICONTROL Save as draft]** om du vill spara ett utkast av regeln eller **[!UICONTROL Save]** om du vill spara och aktivera regeln. Välj **[!UICONTROL Cancel]** om du vill avbryta regelkonfigurationen.


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


## Inställningar för datasammanfogning

>[!NOTE]
>
>[!BADGE beta]{type=Informative}

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

1. I **[!UICONTROL Data merge preferences]** [!BADGE beta]{type=Informative}

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
