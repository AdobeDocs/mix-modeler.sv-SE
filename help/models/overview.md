---
title: Models
description: Lär dig hur du konfigurerar och använder modeller i Mix Modeler.
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Models

Med modellfunktionerna i Mix Modeler kan ni konfigurera, utbilda och poängsätta AI/ML-modeller som är specifika för era affärsmål och som stöds av AI-drivet överföringslärande mellan multitouch-attribuering och marknadsmixmodellering.

Modellerna bygger på de harmoniserade data som du skapar som en del av arbetsflödet i programmet Mix Modeler.

Om du vill skapa en modell använder du det guidade modellkonfigurationsflöde för blandningsmodell som finns tillgängligt när du väljer **[!UICONTROL Guide me]**. Se [Skapa en modell](create.md) för mer information.

## Hantera modeller

Om du vill visa en tabell över dina aktuella modeller i gränssnittet Mix Modeler:

1. Välj ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** från den vänstra listen.

1. En tabell över de aktuella modellerna visas.

   Tabellkolumnerna anger information om modellen.

   | Kolumnnamn | Information |
   |---|---|
   | Namn | Modellens namn |
   | Beskrivning | Beskrivning av modellen |
   | Konverteringshändelser | Den konvertering du har valt för modellen. |
   | Datauppsättning | Den datamängd som modellen använder för att träna och poängsätta. Detta är som standard den harmoniserade datauppsättningen. |
   | Körningsfrekvens | Körfrekvensen för utbildningen av modellen. |
   | Senaste körning | Datum och tid för modellens senaste utbildning. |
   | Senaste körningsstatus | Status för den senaste kursen av modellen. <br/><span style="color:green">●</span> Lyckades<br/><span style="color:orange">●</span> Utbildningsproblem<br/> <span style="color:orange">●</span> Väntar på utbildning <br/><span style="color:red">●</span> Misslyckades |

   {style="table-layout:auto"}

1. Om du vill ändra kolumnerna som visas för listan väljer du ![Kolumninställningar](../assets/icons/ColumnSetting.svg) och aktivera/inaktivera kolumner ![Kontrollera](../assets/icons/Checkmark.svg) eller inte.

### Ta bort en modell

Ta bort en modell:

1. Markera namnet på modellen som du vill ta bort.

1. Välj **[!UICONTROL Delete]** för att ta bort modellen.

### Visa information om en modell

Så här visar du mer information om en modell:

1. Markera namnet på modellen som du vill visa mer information om.

1. Välj **[!UICONTROL More]**. Information om den valda modellen visas i den högra rutan.



### Modellinsikter

>[!NOTE]
>
>Det här valet är endast tillgängligt för färdiga, utbildade modeller.
>

Så här visar du insikter om en modell i Mix Modeler-gränssnittet:

1. Välj ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** från den vänstra listen.

1. Markera namnet på en modell med en **[!UICONTROL Last run status]** av <span style="color:green">●</span> **[!UICONTROL Success]** från **[!UICONTROL Models]** tabell.

1. Välj **[!UICONTROL Model Insights]**. Du omdirigeras till [Modellinsikter](insights.md).


