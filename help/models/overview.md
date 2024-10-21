---
title: Models
description: Lär dig hur du konfigurerar och använder modeller i Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 3801d6637fee491aa295ef586c2017a503466ffc
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Models

Med modellfunktionerna i Mix Modeler kan du konfigurera, utbilda och poängsätta modeller som är specifika för dina affärsmål. Utbildningen och poängsättningen stöder AI-drivet överföringslärande mellan multitouch-attribuering och modellering av marknadsföringsmixar.

Modellerna bygger på de harmoniserade data som du skapar som en del av arbetsflödet i programmet Mix Modeler.

En modell i Mix Modeler är en maskininlärningsmodell som används för att mäta och förutsäga ett specifikt resultat baserat på en marknadsförares investeringar. Marknadsföringskontaktytor och data på sammanfattningsnivå kan användas som indata. Med Mix Modeler kan ni skapa olika modeller baserade på olika uppsättningar av variabler, dimensioner och utfall, till exempel intäkter, sålda enheter, leads.

En modell kräver:

* En konvertering.
* En eller flera kontaktytor (kanaler) för marknadsföring består av data på sammanfattningsnivå, marknadsföringsdata (händelsedata) eller båda.
* Ett konfigurerbart uppslagsfönster.
* Ett konfigurerbart utbildningsfönster.

En modell kan även innehålla:

* Externa faktorer.
* Interna faktorer.
* Tidigare kunskap om marknadsbidrag från andra källor, som tidigare erfarenheter från intressenter, stegvis testning och andra modeller.
* Utgiftsandel, som använder relativ utgiftsresurs som proxy när marknadsföringsdata är glesare.


## Skapa en modell

Om du vill skapa en modell använder du det guidade modellkonfigurationsflöde för Mix Modeler steg som är tillgängligt när du väljer **[!UICONTROL Open model canvas]**. Mer information finns i [Skapa en modell](create.md).

## Hantera modeller

Om du vill visa en tabell över dina aktuella modeller i gränssnittet Mix Modeler:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. En tabell över de aktuella modellerna visas.

   Tabellkolumnerna anger information om modellen.

   | Kolumnnamn | Information |
   |---|---|
   | Namn | Modellens namn |
   | Beskrivning | Beskrivning av modellen |
   | Konverteringshändelse | Den konvertering du har valt för modellen. |
   | Körningsfrekvens | Körfrekvensen för utbildningen av modellen. |
   | Senaste körning | Datum och tid för modellens senaste utbildning. |
   | Status | Status för den senaste kursen av modellen. <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) Success<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) Training issue<br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) Väntar på utbildning <br/>![StatusRed](/help/assets/icons/StatusRed.svg) Misslyckades <br/>![StatusGreen](/help/assets/icons/StatusGray.svg) _ (när en senaste körning pågår) |

   {style="table-layout:auto"}

1. Om du vill ändra vilka kolumner som visas för listan väljer du ![Kolumninställningar](/help/assets/icons/ColumnSetting.svg) och aktiverar ![Kontrollera](/help/assets/icons/Checkmark.svg) eller inte.

Du kan utföra följande åtgärder på en viss modell.

### Modellinsikter

Funktionen för modellinsikter är bara tillgänglig på framgångsrika, utbildade och poängsatta modeller.

Så här visar du insikter om en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Markera modellnamnet.

Du omdirigeras till [Modellinsikter](insights.md).


### Visa detaljer

Så här visar du mer information om en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Info](/help/assets/icons/Info.svg) för en modell om du vill visa ett popup-fönster med information.


### Duplicera

Du kan snabbt duplicera en modell.

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Duplicate]** på snabbmenyn.


### Redigera

Du kan redigera namn, beskrivning och planering av utbildning och poängsättning för en modell.

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Edit]** på snabbmenyn.

   I dialogrutan **[!UICONTROL Edit model]**:

   * Ange en ny **[!UICONTROL Name]** och **[!UICONTROL Description]**.

   * Aktivera **[!UICONTROL Status]** om du vill aktivera schemaläggning. Du kan bara aktivera schemaläggning för modeller som är tränade och poängsatta.

      1. Välj en **[!UICONTROL Scoring frequency]**:

         * **[!UICONTROL Daily]**: Ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Weekly]**: Välj en veckodag och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).
         * **[!UICONTROL Monthly]**: Välj en dag i månaden i listrutan Kör på varje och ange en giltig tid (till exempel `05:22 pm`) eller använd ![Klocka](/help/assets/icons/Clock.svg).

      1. Välj en **[!UICONTROL Training frequency]** i listrutan: **[!UICONTROL Monthly]**, **[!UICONTROL Quarterly]**, **[!UICONTROL Yearly]** eller **[!UICONTROL None]**.

     ![Redigera en modell](../assets/model-edit.png)

1. Välj **[!UICONTROL Save]**.



### Återtåg


Omskolning av en modell är endast tillgängligt för modeller som utbildats med framgång.

Överväg att utbilda om en modell när du vill:

* Inkludera nya inkrementella marknadsförings- och faktordata. Under det senaste kvartalet har till exempel marknadsdynamiken ändrats eller så har er distribution av marknadsföringsdata ändrats avsevärt.

Så här omskolar du en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Train]** på snabbmenyn. Du kan också välja ![Datauppdatering](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** i det blå åtgärdsfältet.

   I dialogrutan **[!UICONTROL Train model]** väljer du alternativet att:

   * **[!UICONTROL Train model with last 2 years of marketing data]** eller
   * **[!UICONTROL Train model using specific date range of data]**.
Ange datumintervall. Du kan använda ![kalendern](/help/assets/icons/Calendar.svg) för att välja ett datumintervall. Du måste välja ett dataintervall med minst ett år.

   ![Utbilda om en modell](../assets/re-train-model.png)

1. Välj **[!UICONTROL Train]** om du vill träna om modellen.


### Poäng eller bakgrundsmusik


Ni kan stegvis poängsätta en modell baserat på nya marknadsföringsdata eller poängsätta en modell för ett visst datumintervall.

Tänk på att göra om poängen för en modell när du vill:

* Korrigera felaktiga marknadsföringsdata. De senaste betalda sökdata som du tog med i utbildningen och poängsättningen för modellen missade t.ex. en veckas data.
* Använd nya inkrementella marknadsföringsdata som har blivit tillgängliga via uppdateringar i de datauppsättningar som du har konfigurerat som en del av dina harmoniserade data.

Så här gör du för att poängsätta eller poängsätta om en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Score]** på snabbmenyn. Du kan också välja ![Datauppdatering](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** i det blå åtgärdsfältet.

   I dialogrutan **[!UICONTROL Score marketing data]** väljer du alternativet att:

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**om du vill poängsätta modellen stegvis med nya marknadsföringsdata, eller
   * **[!UICONTROL Score specific date range of marketing data]** om du vill göra om poängen för ett visst datumintervall.
Ange datumintervall. Du kan använda ![kalendern](/help/assets/icons/Calendar.svg) för att välja ett datumintervall.

   ![Utbilda om en modell](../assets/re-score-model.png)

1. Välj **[!UICONTROL Score]**. När du ändrar skala på en modell med ett visst dataområde visas en **[!UICONTROL Existing model is replaced]**-dialogruta där du uppmanas att bekräfta att du vill ersätta modellen med nya poäng för det valda datumintervallet. Bekräfta genom att välja **[!UICONTROL Replace model]**.


### Ta bort en modell

Ta bort en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Delete]** på snabbmenyn. Du kan också välja ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** i det blå åtgärdsfältet.

Så här tar du bort flera modeller:

1. Markera flera modeller.

1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** från det blå åtgärdsfältet för att ta bort modellerna.

   >[!WARNING]
   >
   >Modellen tas bort omedelbart.


