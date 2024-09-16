---
title: Skapa en modell
description: Lär dig hur du skapar en modell i Mix Modeler.
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Skapa en modell

Om du vill skapa en modell väljer du **[!UICONTROL Open model canvas]** i gränssnittet ![Models](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i Mix Modeler.

Gränssnittet ger ett stegvis guidat modellkonfigurationsflöde när du vill skapa anpassade AI-baserade modeller.

1. I steget **[!UICONTROL Setup]**:

   1. Ange modellen **[!UICONTROL Name]**, till exempel `Demo model`. Ange en **[!UICONTROL Description]**, till exempel `Demo model to explore AI featues of Mix Modeler`.

      ![Modellnamn och beskrivning](/help/assets/model-name-description.png)

   1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.

1. I steget **[!UICONTROL Configure]**:

   1. I avsnittet **[!UICONTROL Conversion goal]** i behållaren:

      1. Ange **[!UICONTROL Conversion name]** för konverteringen, till exempel `Conversion`

      1. Välj en konvertering från **[!UICONTROL *Välj harmoniserat fält *]**som innehåller de tillgängliga konverteringar du definierat som en del av [Konverteringar](../harmonize-data/conversions.md) i [!UICONTROL Harmonized datasets]. Exempel:**[!UICONTROL Online Conversion]**.

      1. Du kan välja ![Svara](/help/assets/icons/Reply.svg) **[!UICONTROL Create new conversion]** om du vill skapa en konvertering direkt från modellkonfigurationen.

         ![Modell - konverteringssteg](/help/assets/model-conversion-step.png)

   1. I avsnittet **[!UICONTROL Marketing touchpoints]** ser du ett antal kontaktpunktsbehållare för marknadsföring, som motsvarar de kontaktpunkter för marknadsföring som du har definierat som en del av [Marknadsföringskontaktytor](../harmonize-data/marketing-touchpoints.md) i [!UICONTROL Harmonized datasets].

      * För varje behållare:

         1. Du kan ändra **[!UICONTROL Marketing touchpoint name]**.

         1. Välj en kontaktyta för marknadsföring från **[!UICONTROL _Välj kontaktyta för marknadsföring_]**.

         1. Du kan välja ![Svara](/help/assets/icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** om du vill skapa en kontaktyta för marknadsföring direkt från modellkonfigurationen.

      * Om du vill lägga till en kontaktpunktsbehållare för marknadsföring väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * Om du vill ta bort en kontaktpunktsbehållare för marknadsföring, markerar du ![Mer](/help/assets/icons/More.svg) i behållaren och väljer **[!UICONTROL Remove container]** på snabbmenyn.

        ![Modell - marknadsföring touchpoints-step](/help/assets/model-marketing-touchpoint-step.png)

   1. Som standard genereras en poäng för alla data i din harmoniserade vy. Om du bara vill poängsätta en delmängd av populationen definierar du ett eller flera filter med hjälp av behållare i avsnittet **[!UICONTROL Eligible data population]**.

      * Definiera en eller flera händelser för varje behållare.

         1. För varje händelse:

            1. Välj ett mått eller en dimension från **[!UICONTROL _Välj harmoniserat fält_]**.

            1. Välj lämplig operator: **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]** eller **[!UICONTROL is not in]**.

            1. Ange eller välj ett värde vid **[!UICONTROL _Ange eller välj värdet_]**.

         1. Om du vill lägga till ytterligare en händelse i behållaren väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. Om du vill ta bort en händelse från behållaren väljer du ![Stäng](/help/assets/icons/Close.svg).

         1. Om du vill filtrera med hjälp av alla eller några av flera händelser som definieras i behållaren väljer du **[!UICONTROL Any of]** eller **[!UICONTROL All of]**. Etiketten ändras på motsvarande sätt från **[!UICONTROL Include ... Or ...]** till **[!UICONTROL Include ... And ...]**.

      * Välj ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]** om du vill lägga till en giltig dataifyllningsbehållare.

      * Om du vill ta bort en giltig dataifyllningsbehållare i behållaren väljer du ![Mer](/help/assets/icons/More.svg) och sedan **[!UICONTROL Remove marketing touchpoint]** på snabbmenyn.

        ![Modell - kvalificerade datapifieringar](/help/assets/model-eligible-data-population-step.png)

   1. Om du vill lägga till datauppsättningar som innehåller externa faktorer i modellen använder du en eller flera behållare i avsnittet **[!UICONTROL External factors dataset]**.

      * För varje behållare:

         1. Ange **[!UICONTROL Factor name]** vid **[!UICONTROL _Ange faktor_]**.

         1. Välj en datauppsättning från **[!UICONTROL _Välj en datauppsättning_]**. Du kan välja ![Data](/help/assets/icons/Data.svg) för att hantera datamängder. Mer information finns i [Datauppsättningar](../ingest-data/datasets.md).

      * Om du vill lägga till ytterligare en datauppsättningsbehållare för externa faktorer väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * Om du vill ta bort en datauppsättningsbehållare för externa faktorer i behållaren väljer du ![Mer](/help/assets/icons/More.svg) och sedan **[!UICONTROL Remove external factor]** på snabbmenyn.

        ![Modell - datamängd för externa faktorer](/help/assets/model-external-factors-dataset-step.png)


   1. Om du vill lägga till datauppsättningar som innehåller interna faktorer i modellen använder du en eller flera behållare i avsnittet **[!UICONTROL Internal factors dataset]**.

      * För varje behållare:

         1. Ange **[!UICONTROL Factor name]** vid **[!UICONTROL _Ange faktor_]**.

         1. Välj en datauppsättning från **[!UICONTROL _Välj en datauppsättning_]**. Du kan välja ![Data](/help/assets/icons/Data.svg) för att hantera datamängder. Mer information finns i [Datauppsättningar](../ingest-data/datasets.md).

      * Om du vill lägga till ytterligare en datauppsättningsbehållare för interna faktorer väljer du ![Lägg till](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * Om du vill ta bort ytterligare en datauppsättningsbehållare för interna faktorer i behållaren väljer du ![Mer](/help/assets/icons/More.svg) och **[!UICONTROL Remove internal factor]** på snabbmenyn.

        ![Modell - datauppsättning för interna faktorer](/help/assets/model-internal-factors-dataset-step.png)

   1. Ange ett värde mellan `1` och `52` i **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]** om du vill definiera uppslagsfönstret för modellen.

   1. Välj **[!UICONTROL Next]** om du vill fortsätta till nästa steg. Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs. <br/>Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg. <br/>Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.

1. I steget **[!UICONTROL Advanced]**:

   1. I avsnittet **[!UICONTROL Define training window]** väljer du

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** och

      * **[!UICONTROL Manually input a training window]**. Ange antalet år i **[!UICONTROL Include events the following years prior to a conversion]** när du väljer det här alternativet.

        ![Modell - Definiera utbildningsfönster](/help/assets/model-define-training-window.png)

   1. I avsnittet **[!UICONTROL Spend share]**:

      * Aktivera **[!UICONTROL Allow spend share]** om du vill använda tidigare investeringsförhållanden för marknadsföring för att informera modellen när marknadsföringsdata är begränsade.

   1. I avsnittet **[!UICONTROL Prior knowledge]**:

      1. Välj **[!UICONTROL Rule type]**.

      1. Ange procentsatser för bidrag för någon av kanalerna som listas under **[!UICONTROL Name]**, med kolumnen **[!UICONTROL Contribution proportion]**.

      1. Om det är lämpligt kan du lägga till **[!UICONTROL Level of confidence]** procent för varje kanal.

      1. Använd **[!UICONTROL Clear all]** vid behov för att rensa alla indatavärden för kolumnerna **[!UICONTROL Contribution proportion]** och **[!UICONTROL Level of confidence]**.

         ![Modell - tidigare kunskap](/help/assets/model-prior-knowledge-step.png)

1. Välj **[!UICONTROL Finish]** om du vill avsluta din modellkonfiguration.

   * I dialogrutan **[!UICONTROL Create instance?]** väljer du **[!UICONTROL Ok]** för att utlösa den första uppsättningen kurser och poäng direkt. Din modell är listad med statusen <span style="color:orange"> ●</span> **[!UICONTROL Awaiting training]**.

     Välj **[!UICONTROL Cancel]** om du vill avbryta.

   * Om mer konfiguration behövs, förklarar en röd kontur och text vilken ytterligare konfiguration som krävs.

   Välj **[!UICONTROL Back]** om du vill gå tillbaka till föregående steg.

   Välj **[!UICONTROL Cancel]** om du vill avbryta modellkonfigurationen.
