---
title: Översikt över modeller
description: Lär dig hur du bygger och använder modeller i Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 8b0dfbe136986bc97c6793538518679b64d7801c
workflow-type: tm+mt
source-wordcount: '1208'
ht-degree: 0%

---

# Översikt över modeller

Med modellfunktionerna i Mix Modeler kan du konfigurera, utbilda och poängsätta modeller som är specifika för dina affärsmål. Utbildningen och poängsättningen stöder AI-drivet överföringslärande mellan multitouch-attribuering och modellering av marknadsföringsmixar.

Modellerna bygger på de harmoniserade data som du skapar som en del av Mix Modeler arbetsflöde.

En modell i Mix Modeler är en maskininlärningsmodell som används för att mäta och förutsäga ett specifikt resultat baserat på en marknadsförares investeringar. Marknadsföringskontaktytor och data på sammanfattningsnivå kan användas som indata. Med Mix Modeler kan ni skapa olika typer av modeller baserade på olika uppsättningar av variabler, dimensioner och resultat, som intäkter, sålda enheter, leads.

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

När en modell skapas för första gången kommer man omedelbart igång med utbildningen och poängprocessen. När den inledande kursen och poängsättningen är klara finns modellinsikter att granska. En modell kan därefter omskolas. Dessutom kan data läggas till i modellen, vilket kräver att du anger om modellen manuellt. Omutbildning och ompoängtering är en repetitiv process i takt med att nya resultat och ny information kommer fram och justeringar behövs för att skapa en modell som passar era affärsmål bäst.


## Skapa modeller

Om du vill skapa en modell använder du Mix Modeler steg-för-steg-guidade modellkonfigurationsflöde som är tillgängligt när du väljer **[!UICONTROL Open model canvas]**. Mer information finns i [Skapa modeller](build.md).

## Hantera modeller

Om du vill visa en tabell över de aktuella modellerna i Mix Modeler-gränssnittet:

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
   | Status | Modellens status. |

   {style="table-layout:auto"}

   Modellens rapporterade status beror på var modellen befinner sig under sin livscykel. Till exempel om en modell skapas, (omutbildas) har lyckats eller inte, eller om (ompoängteras) har lyckats eller inte.

   I tabellen nedan:

   * ![Markering](/help/assets/icons/Checkmark.svg) - indikerar att ett steg i modelllivscykeln har körts.
   * ![Klocka](/help/assets/icons/Clock.svg) - indikerar en pågående körning av ett steg i modellens livscykel.
   * ![Close](/help/assets/icons/Close.svg) - indikerar att ett steg i modelllivscykeln inte kunde köras.

   | Status | Skapa | Tåg | Poäng | Retrain | Rescore |
   |---|:---:|:---:|:---:|:---:|:---:|
   | Pågår | ![Markering](/help/assets/icons/Checkmark.svg) | | | | |
   | Pågår | ![Markering](/help/assets/icons/Checkmark.svg) | ![Klocka](/help/assets/icons/Clock.svg) | | | |
   | Pågår | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Klocka](/help/assets/icons/Clock.svg) | | |
   | Pågår | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Klocka](/help/assets/icons/Clock.svg) | |
   | Pågår | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Klocka](/help/assets/icons/Clock.svg) |
   | Utbildningen misslyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Stäng](/help/assets/icons/Close.svg) | | | |
   | Utbildningen misslyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Stäng](/help/assets/icons/Close.svg) | |
   | Utbildning lyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | | | |
   | Utbildning lyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | |
   | Bedömningen misslyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Stäng](/help/assets/icons/Close.svg) | | |
   | Bedömningen misslyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Stäng](/help/assets/icons/Close.svg) |
   | Bedömningen lyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | | |
   | Bedömningen lyckades | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) | ![Markering](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

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

Du omdirigeras till stegen för att skapa en ny modell, med ett föreslaget namn bestående av den ursprungliga modellens namn som bifogas med **[!UICONTROL (Copy)](_n_)**.

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



### Retrain

Behåll en modell finns bara för framgångsrika modeller.

Överväg att träna om en modell när du vill:

* Inkludera nya inkrementella marknadsförings- och faktordata. Under det senaste kvartalet har till exempel marknadsdynamiken ändrats eller så har er distribution av marknadsföringsdata ändrats avsevärt.

Så här omskolar du en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Train]** på snabbmenyn. Du kan också välja ![Datauppdatering](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** i det blå åtgärdsfältet.

   I dialogrutan **[!UICONTROL Train model]** väljer du alternativet att:

   * **[!UICONTROL Train model with last 2 years of marketing data]** eller
   * **[!UICONTROL Train model using specific date range of data]**.
Ange datumintervall. Du kan använda ![kalendern](/help/assets/icons/Calendar.svg) för att välja ett datumintervall. Du måste välja ett dataintervall med minst ett år.

   ![Behåll en modell](../assets/retrain-model.png)

1. Välj **[!UICONTROL Train]** om du vill träna om modellen.


### Poäng eller bakgrundsmusik


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



### Ta bort modeller

Ta bort en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.
1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Delete]** på snabbmenyn. Du kan också välja ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** i det blå åtgärdsfältet.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan **[!UICONTROL Delete model]** om du vill ta bort modellen. Välj **[!UICONTROL Cancel]** om du vill avbryta.

Så här tar du bort flera modeller:

1. Markera flera modeller.
1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** från det blå åtgärdsfältet för att ta bort modellerna.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan för **[!UICONTROL Delete *x *modeller]**om du vill ta bort modellerna. Välj **[!UICONTROL Cancel]**om du vill avbryta.

