---
title: Tåg- och poängmodeller
description: Lär dig att utbilda och poängsätta modeller.
feature: Models
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Tåg- och poängmodeller

När du har [skapat](/help/models/build.md) en modell får modellen automatiskt en utbildning och poäng. Du kan manuellt omskola en modell eller göra om den.

## Tåg

Överväg att träna om en modell när ni vill inkludera nya inkrementella marknadsförings- och faktordata. Under det senaste kvartalet har till exempel marknadsdynamiken ändrats eller så har er distribution av marknadsföringsdata ändrats avsevärt.

Så här omskolar du en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Train]** på snabbmenyn. Du kan också välja ![Datauppdatering](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** i det blå åtgärdsfältet.

   I dialogrutan **[!UICONTROL Train model]** väljer du alternativet att:

   * **[!UICONTROL Train model with last 2 years of marketing data]** eller
   * **[!UICONTROL Train model using specific date range of data]**.
Ange datumintervall. Du kan använda ![kalendern](/help/assets/icons/Calendar.svg) för att välja ett datumintervall. Du måste välja ett dataintervall med minst ett år.

   ![Behåll en modell](../assets/retrain-model.png)

1. Välj **[!UICONTROL Train]** om du vill träna om modellen.


Du kan bara omutbilda en modell när modellen har tränats.


## Poäng


Ni kan stegvis poängsätta en modell baserat på nya marknadsföringsdata eller poängsätta en modell för ett visst datumintervall.

Överväg att göra om en modell när du vill:

* Korrigera felaktiga marknadsföringsdata. De senaste betalda sökdata som du tog med i utbildningen och poängsättningen för modellen missade t.ex. en veckas data.
* Använd nya inkrementella marknadsföringsdata som har blivit tillgängliga via uppdateringar i de datauppsättningar som du har konfigurerat som en del av dina harmoniserade data.

Så här poängterar du en modell eller anger om den:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Score]** på snabbmenyn. Du kan också välja ![Datauppdatering](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** i det blå åtgärdsfältet.

   I dialogrutan **[!UICONTROL Score marketing data]** väljer du alternativet att:

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**om du vill poängsätta modellen stegvis med nya marknadsföringsdata, eller
   * **[!UICONTROL Score specific date range of marketing data]** om du vill upprepa för ett visst datumintervall.
Ange datumintervall. Du kan använda ![kalendern](/help/assets/icons/Calendar.svg) för att välja ett datumintervall.

   ![Posta om en modell](../assets/rescore-model.png)

1. Välj **[!UICONTROL Score]**. När du ändrar skala på en modell med ett visst dataområde visas en **[!UICONTROL Existing model is replaced]**-dialogruta där du uppmanas att bekräfta att du vill ersätta modellen med nya poäng för det valda datumintervallet. Bekräfta genom att välja **[!UICONTROL Replace model]**.

>[!IMPORTANT]
>
>Omkodning av en modell ändrar inte planer som redan har skapats baserat på den omfärgade modellen. Om du vill använda den nya omgjorda modellen i en plan måste du skapa en ny plan.

