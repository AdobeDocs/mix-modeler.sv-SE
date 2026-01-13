---
title: Översikt över modeller
description: Lär dig hur du bygger och använder modeller i Mix Modeler.
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 8f4b07782d74341afd23e8c3d15f7f2d30a7ccbd
workflow-type: tm+mt
source-wordcount: '963'
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

1. Välj ![FileData](/help/assets/icons2/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.

1. En tabell över de aktuella modellerna visas.

   Tabellkolumnerna anger information om modellen.

   | Kolumnnamn | Information |
   |---|---|
   | **[!UICONTROL Name]** | Modellens namn |
   | **[!UICONTROL Description]** | Beskrivning av modellen |
   | **[!UICONTROL Conversion event]** | Den konvertering du har valt för modellen. |
   | **[!UICONTROL Run]** frekvens | Körfrekvensen för utbildningen av modellen. |
   | **[!UICONTROL Last run]** | Datum och tid för modellens senaste utbildning. |
   | **[!UICONTROL Status]** | Modellens status. |

   Om du vill sortera tabellen i en kolumn i stigande ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg)- eller fallande ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg)ordning, markerar du kolumnens rubrik.

   Om du vill sortera eller ändra storlek på kolumnen **[!UICONTROL Name]** väljer du **[!UICONTROL Name]** ![KranNed](/help/assets/icons/ChevronDown.svg). Välj **[!UICONTROL Sort ascending]**, **[!UICONTROL Sort descending]** eller **[!UICONTROL Resize column]** på snabbmenyn. Du kan också hovra över kolumnavgränsaren för att ändra storlek på kolumnen **[!UICONTROL Name]**.

   Modellens rapporterade status beror på var modellen befinner sig under sin livscykel. Till exempel om en modell skapas, (omutbildas) har lyckats eller inte, eller om (ompoängteras) har lyckats eller inte.

   I tabellen nedan:

   * ![Markering](/help/assets/icons/Checkmark.svg) - indikerar att ett steg i modelllivscykeln har körts.
   * ![Klocka](/help/assets/icons/Clock.svg) - indikerar en pågående körning av ett steg i modellens livscykel.
   * ![Close](/help/assets/icons/Close.svg) - indikerar att ett steg i modelllivscykeln inte kunde köras.

   | Status | [Bygg](/help/models/build.md) | [Tåg](/help/models/train-score.md#train) | [Poäng](/help/models/train-score.md#score) | [Retrain](/help/models/train-score.md#train) | [Rescore](/help/models/train-score.md#score) |
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



### Tåg

Överväg att träna om en modell när ni vill inkludera nya inkrementella marknadsförings- och faktordata. Mer information finns i [Utbildning och poängmodeller](train-score.md#train).


### Poäng

Ni kan stegvis poängsätta en modell baserat på nya marknadsföringsdata eller poängsätta en modell för ett visst datumintervall. Mer information finns i [Utbildning och poängmodeller](train-score.md#score).


### Ta bort modeller

Ta bort en modell:

1. Välj ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** i den vänstra listen.
1. Välj ![Mer](/help/assets/icons/More.svg) för en modell och välj **[!UICONTROL Delete]** på snabbmenyn. Du kan också välja ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** i det blå åtgärdsfältet.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan **[!UICONTROL Delete model]** om du vill ta bort modellen. Välj **[!UICONTROL Cancel]** om du vill avbryta.

Så här tar du bort flera modeller:

1. Markera flera modeller.
1. Välj ![Ta bort](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]** från det blå åtgärdsfältet för att ta bort modellerna.
1. Välj **[!UICONTROL Delete]** i bekräftelsedialogrutan för **[!UICONTROL Delete *x *modeller]**om du vill ta bort modellerna. Välj **[!UICONTROL Cancel]**om du vill avbryta.

