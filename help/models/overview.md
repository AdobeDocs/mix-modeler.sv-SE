---
title: Models
description: Lär dig hur du konfigurerar och använder modeller i Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Models

Med modellfunktionerna i Mix Modeler kan ni konfigurera, utbilda och poängsätta AI/ML-modeller som är specifika för era affärsmål och som stöds av AI-drivet överföringslärande mellan multitouch-attribuering och marknadsmixmodellering.

Modellerna bygger på de harmoniserade data som du skapar som en del av arbetsflödet i programmet Mix Modeler.

En modell i Mix Modeler är en maskininlärningsmodell som används för att mäta och/eller förutsäga ett visst resultat baserat på en marknadsförares investeringar. Marknadsföringskontaktytor och data på sammanfattningsnivå kan användas som indata. Med Mix Modeler kan ni skapa olika modeller baserade på olika uppsättningar av variabler, dimensioner och utfall, till exempel intäkter, sålda enheter, leads.

En modell kräver:

* en konvertering,
* en eller flera kontaktytor för marknadsföring (kanaler) som består av data på sammanfattningsnivå, data om kontaktytor för marknadsföring (händelsedata) eller båda,
* ett konfigurerbart uppslagsfönster för
* ett konfigurerbart utbildningsfönster.

En modell kan även innehålla:

* yttre faktorer,
* interna faktorer,
* s.k.&quot;priors&quot; (sannolikhetsfördelning som representerar kunskap eller osäkerhet om data före eller innan dessa data observeras), som indexerar tidigare konverteringar per kanal,
* utgiftsresurs, som använder relativ utgiftsresurs som proxy när marknadsföringsdata är glesare.


## Skapa en modell

Om du vill skapa en modell använder du det guidade modellkonfigurationsflöde för Mix Modeler steg som är tillgängligt när du väljer **[!UICONTROL Open model canvas]**. Mer information finns i [Skapa en modell](create.md).

## Hantera modeller

Om du vill visa en tabell över dina aktuella modeller i gränssnittet Mix Modeler:

1. Välj ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. En tabell över de aktuella modellerna visas.

   Tabellkolumnerna anger information om modellen.

   | Kolumnnamn | Information |
   |---|---|
   | Namn | Modellens namn |
   | Beskrivning | Beskrivning av modellen |
   | Konverteringshändelse | Den konvertering du har valt för modellen. |
   | Körningsfrekvens | Körfrekvensen för utbildningen av modellen. |
   | Senaste körning | Datum och tid för modellens senaste utbildning. |
   | Status | Status för den senaste kursen av modellen. <br/><span style="color:green"> ●</span> Slutfört <br/><span style="color:orange"> ●</span> Utbildningsproblem <br/> <span style="color:orange"> ●</span> Väntar på utbildning <br/><span style="color:red"> ●</span> Misslyckades <br/><span style="color:gray"> ●</span> _ (när en senaste körning pågår) |

   {style="table-layout:auto"}

1. Om du vill ändra vilka kolumner som visas för listan väljer du ![Kolumninställningar](/help/assets//icons/ColumnSetting.svg) och aktiverar ![Kontrollera](/help/assets//icons/Checkmark.svg) eller inte.


### Visa information om en modell

Så här visar du mer information om en modell:

1. Välj ![Info](/help/assets//icons/Info.svg) för en modell om du vill visa ett popup-fönster med information.



### Modellinsikter

Så här visar du insikter om en modell i Mix Modeler-gränssnittet:

1. Välj ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj namnet på en modell med **[!UICONTROL Last run status]** av <span style="color:green"> ●</span> **[!UICONTROL Success]** från tabellen **[!UICONTROL Models]**. Modellinsikter är bara tillgängliga för framgångsrika modeller.

1. Välj **[!UICONTROL Model Insights]** på snabbmenyn. Du omdirigeras till [Modellinsikter](insights.md).


### Poäng igen


Så här gör du om en modell i gränssnittet för Mix Modeler:

1. Välj ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj namnet på en modell med **[!UICONTROL Last run status]** av <span style="color:green"> ●</span> **[!UICONTROL Success]** från tabellen **[!UICONTROL Models]**. Ompoängen är endast tillgängliga för korrekt utbildade modeller.

1. Välj **[!UICONTROL Re-score]** på snabbmenyn. Det kan ta några minuter att visa en uppdaterad status för modellen.


### Ta bort en modell

Ta bort en modell:

1. Markera namnet på modellen som du vill ta bort.

1. Välj **[!UICONTROL Delete]** på snabbmenyn för att ta bort modellen.

   >[!WARNING]
   >
   >Modellen tas bort omedelbart.


