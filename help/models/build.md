---
title: Skapa modeller
description: Lär dig skapa modeller i Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: b08a24856e28a1377728bc2c511f6ea483cbd0fd
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Skapa modeller

Gränssnittet ger ett stegvis guidat modellkonfigurationsflöde när du vill skapa anpassade AI-baserade modeller.

I gränssnittet ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i Mix Modeler väljer du **[!UICONTROL Open model canvas]**.

## Inställningar

Du definierar namn och beskrivning i steget **[!UICONTROL Setup]**:

1. Ange modellen **[!UICONTROL Name]**, till exempel `Demo model`. Ange en **[!UICONTROL Description]**, till exempel `Demo model to explore AI featues of Mix Modeler`.

   ![Modellnamn och beskrivning](/help/assets/model-name-description.png)

1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.

## Konfigurera

Du konfigurerar modellen i steget **[!UICONTROL Configure]**. Konfiguration innefattar definition av konverteringsmål, kontaktytor för marknadsföring, den stödberättigade datapopulationen, externa och interna faktorer, med mera.

1. I avsnittet **[!UICONTROL Conversion goal]**:

   ![Modell - konverteringssteg](/help/assets/model-conversion-step.png)

   1. Välj en konvertering i listrutan **[!UICONTROL Conversion]**. De tillgängliga konverteringarna är konverteringen som du definierade som en del av [Konverteringar](../harmonize-data/conversions.md) i [!UICONTROL Harmonized datasets]. Exempel: **[!UICONTROL Online Conversion]**.

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

   * Om du vill ta bort en giltig dataifyllningsbehållare i behållaren väljer du ![Mer](/help/assets/icons/More.svg) och sedan **[!UICONTROL Remove marketing touchpoint]** på snabbmenyn.

   * Välj **And** och **Or** mellan behållare om du vill skapa mer komplexa definitioner för den giltiga datapifyllningen.


1. Om du vill lägga till datauppsättningar som innehåller externa faktorer i modellen använder du en eller flera behållare i avsnittet **[!UICONTROL External factors dataset]**. Ett exempel på externa faktorer är S&amp;P-index.

   ![Modell - datamängd för externa faktorer](/help/assets/model-external-factors-dataset-step.png)

   * För varje behållare:

      1. Ange en **[!UICONTROL External factor name]**, till exempel `External Factors`.

      1. Välj en datauppsättning i listrutan **[!UICONTROL Dataset]**. Du kan välja ![Data](/help/assets/icons/Data.svg) för att hantera datamängder. Mer information finns i [Datauppsättningar](../ingest-data/datasets.md).

      1. Välj ett alternativ i listrutan **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** eller **[!UICONTROL Negative]**. Standardalternativet är **[!UICONTROL Auto select]**, vilket gör att modellen kan avgöra påverkan. Du kan åsidosätta standardinställningen.

   * Om du vill lägga till ytterligare en datauppsättningsbehållare för externa faktorer väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

   * Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort en datauppsättningsbehållare för externa faktorer.




1. Om du vill lägga till datauppsättningar som innehåller interna faktorer i modellen använder du en eller flera behållare i avsnittet **[!UICONTROL Internal factors dataset]**. Ett exempel på interna faktorer är marknadsföringsdata för e-post.

   ![Modell - datauppsättning för interna faktorer](/help/assets/model-internal-factors-dataset-step.png)

   * För varje behållare:

      1. Ange en **[!UICONTROL Internal factor name]**, till exempel `Email Marketing Data`.

      1. Välj en datauppsättning från **[!UICONTROL _Välj en datauppsättning_]**. Du kan välja ![Data](/help/assets/icons/Data.svg) för att hantera datamängder. Mer information finns i [Datauppsättningar](../ingest-data/datasets.md).

      1. Välj ett alternativ i listrutan **[!UICONTROL Impact on conversion]**: **[!UICONTROL Auto select]**, **[!UICONTROL Positive]** eller **[!UICONTROL Negative]**.

   * Om du vill lägga till ytterligare en datauppsättningsbehållare för interna faktorer väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

   * Välj ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) om du vill ta bort en datauppsättningsbehållare för interna faktorer.



1. Ange ett värde mellan `1` och `52` i **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]** om du vill definiera uppslagsfönstret för modellen.

1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs. <br/>Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg. <br/>Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.


## Avancerat

Du kan ange avancerade inställningar i steget **[!UICONTROL Advanced]**. I det här steget kan du aktivera din modell för multitouch-attribuering (MTA).

1. I avsnittet **[!UICONTROL Spend share]**:

   * Aktivera **[!UICONTROL Allow spend share]** om du vill använda tidigare investeringsförhållanden för marknadsföring för att informera modellen när marknadsföringsdata är begränsade. Den här inställningen rekommenderas, särskilt i följande scenarier:
      * En kanal har inte tillräckligt många observationer (t.ex. låg frekvens av utgifter, visningar eller klick).
      * Du modellerar spiky men regular och potentiellt högspenderade media (som TV för vissa varumärken), där data kan vara glesa.

     >[!NOTE]
     >
     >För engångsinvesteringar (t.ex. en Super Bowl-annons) bör du överväga att lägga in dessa data som en faktor i stället för att förlita dig på kostnadsandelen.
     >


1. I avsnittet **[!UICONTROL MTA enabled]**:

   * Aktivera **[!UICONTROL MTA enabled]** om du vill aktivera MTA-funktioner för modellen. Om du har aktiverat MTA finns multitouch-attribueringsinsikter tillgängliga efter att du har utbildat och betygsatt modellen. Se fliken [Attribution](insights.md#attribution) i [Model insights](insights.md).

1. I avsnittet **[!UICONTROL Prior knowledge]**:

   ![Modell - tidigare kunskap](/help/assets/model-prior-knowledge-step.png)

   1. Välj **[!UICONTROL Rule type]**, som är standard **[!UICONTROL Absolute values]**.

   1. Ange procentsatser för bidrag för någon av kanalerna som listas under **[!UICONTROL Name]**, med kolumnen **[!UICONTROL Contribution proportion]**.

   1. Om det är lämpligt kan du lägga till **[!UICONTROL Level of confidence]** procent för varje kanal.

   1. Använd **[!UICONTROL Clear all]** vid behov för att rensa alla indatavärden för kolumnerna **[!UICONTROL Contribution proportion]** och **[!UICONTROL Level of confidence]**.


## Schema

Du kan schemalägga utbildning och inspelning för din modell i steget **[!UICONTROL Schedule]**.

1. I avsnittet **[!UICONTROL Schedule]** kan du schemalägga modellutbildning och poängsättning.

   ![Schemamodell](../assets/model-schedule.png)

   Så här schemalägger du betygsättning och utbildning:

   1. Aktivera **[!UICONTROL Enable scheduled model scoring and training]**.
   1. Välj en **[!UICONTROL Scoring frequency]**:

      * **[!UICONTROL Daily]**: Ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Weekly]**: Välj en veckodag och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
      * **[!UICONTROL Monthly]**: Välj en dag i månaden i listrutan Kör på varje och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).

   1. Välj en **[!UICONTROL Training frequency]** i listrutan: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** eller **[!UICONTROL None]**.

1. I avsnittet **[!UICONTROL Define training window]** väljer du mellan:

   ![Modell - Definiera utbildningsfönster](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** och

   * **[!UICONTROL Manually input a training window]**. Ange antalet år i **[!UICONTROL Include events the following years prior to a conversion]** när du väljer det här alternativet.


1. Välj **[!UICONTROL Finish]** för att slutföra modellkonfigurationen.

   * I dialogrutan **[!UICONTROL Create instance?]** väljer du **[!UICONTROL Ok]** för att utlösa den första uppsättningen kurser och poäng direkt. Din modell visas med statusen ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**.

     Välj **[!UICONTROL Cancel]** om du vill avbryta.

   * Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs.

   Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg.

   Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.
