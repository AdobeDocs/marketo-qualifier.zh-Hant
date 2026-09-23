---
title: Adobe Marketo Qualifier中的帳戶
description: 瞭解如何在Adobe Marketo Qualifier中檢閱客戶情報（包括AI研究、最近的新聞、機會和最熱門的參與連絡人），以排定外聯的優先順序。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%
---

# 帳戶

帳戶檢視結合了AI產生的研究、最近的新聞、開放的商機、管道值和參與的聯絡人。 在聯絡之前，請先透過這些資訊瞭解帳戶並排定優先順序。

## 開立帳戶

從與其相關聯之潛在客戶的設定檔中開啟帳戶。

1. 在左側導覽中選取&#x200B;**[!UICONTROL 潛在客戶]**&#x200B;並開啟潛在客戶。 檢視[潛在客戶](prospects.md)。
1. 在潛在客戶詳細資訊頁面上，選取&#x200B;**[!UICONTROL 帳戶]**&#x200B;標籤。

![具有「人員」和「帳戶」索引標籤的「潛在客戶」詳細資料頁面](./assets/account-home.png){width="800" zoomable="yes"}

Adobe Marketo Qualifier會從潛在客戶的CRM記錄中識別帳戶。 與該帳戶相關聯的每個潛在客戶都可以使用相同的帳戶檢視。 如果Marketo Qualifier無法比對帳戶，索引標籤會顯示&#x200B;_找不到帳戶_。

>[!NOTE]
>
>可用的區段和量度取決於您的CRM、您組織的設定和帳戶資料。 如果此處說明的區段未出現，則表示未設定必要的資料或功能。

帳戶檢視有兩個標籤： **[!UICONTROL 詳細資料]**&#x200B;和&#x200B;**[!UICONTROL 帳戶研究]**。

## 檢閱帳戶詳細資料

**[!UICONTROL 詳細資料]**&#x200B;索引標籤會提供您帳戶及其管道的快照。

### 帳戶總覽

標籤頂端的概觀卡片會識別帳戶並彙總其值：

* 帳戶名稱和區域
* **年度週期性收入(ARR)** — 所有使用中訂閱的年度週期性收入。 若要在&#x200B;**[!UICONTROL 年度循環收入]**&#x200B;對話方塊中依產品檢視ARR，請選取&#x200B;**[!UICONTROL 檢視全部]**。
* 帳戶統計資料，包括未結機會和聯絡人計數以及管道值

### 帳戶總覽摘要

**[!UICONTROL 帳戶總覽]**&#x200B;面板會根據CRM資料和Account Qualification Agent研究摘要該帳戶。 如果研究正在進行中，面板會顯示載入狀態。 如果無法調研，面板會顯示訊息。

### 帳戶分析

使用總覽下方的按鈕，在帳戶檢視之間切換。 可用的檢視視視您的CRM和設定而定：

| 檢視 | 它顯示的內容 |
| --- | --- |
| **[!UICONTROL 機會]** | 開啟連結至帳戶的機會，每個機會都有關鍵欄位。 若要在表格中檢視完整清單，請選取&#x200B;**[!UICONTROL 全部檢視]**。 當管理員讓這些欄位可篩選時，機會詳細資訊（例如，階段、型別和關閉日期）也可用來篩選&#x200B;**[!UICONTROL 我的機會聯絡人]**&#x200B;中的帳戶聯絡人。 |
| **[!UICONTROL 最上層成員]** | 帳戶參與次數最多的聯絡人（依參與度排名）。 每個聯絡人都會顯示其職稱、電子郵件地址、參與分數和緊急程度指標。 |
| **[!UICONTROL 意圖資料]** | 為帳戶購買意向訊號，例如帳戶正在研究的產品和主題。 |
| **[!UICONTROL 帳戶團隊成員]** | 指派至帳戶的人員，包括其電子郵件、職稱、區域和產品群組。 |
| **[!UICONTROL CRM欄位]** | 從您的CRM匯入的帳戶欄位，如傳入對應中所設定。 請參閱[整合](integrations.md#map-crm-fields-inbound-mapping)。 |

從&#x200B;**[!UICONTROL 最上層成員]**&#x200B;檢視，為連絡人執行下列任一動作：

* **[!UICONTROL 新增至傳出工作流程]** — 在[傳出工作流程](outbound-workflows.md)中註冊連絡人。
* **[!UICONTROL 新增至Marketo行銷活動]** — 觸發連絡人的[!DNL Marketo]行銷活動。

## 研究帳戶

**[!UICONTROL 帳戶研究]**&#x200B;索引標籤包含三個區域：

* **[!UICONTROL 研究類別]** — 研究主題。 若要在中心窗格中檢視類別的研究，請選取類別。
* **研究內容**—AI產生的研究卡片，依類別分組。 卡片可包含來源網域，以及首次和上次偵測訊號的日期。
* **[!UICONTROL 最近新聞]** — 帳戶的最新新聞，包括日期、標籤和來源連結。

![帳戶研究標籤](./assets/account-detail.png){width="800" zoomable="yes"}

如果無法載入研究或新聞，每個區域都會提供&#x200B;**[!UICONTROL 重新載入]**&#x200B;動作以重試。

## 在外聯中使用客戶情報

帳戶智慧在決定您傳送的內容時最有價值：

* 參考最近的新聞專案或研究訊號，讓您的開放變得相關，而不是使用一般的推介。
* 勾選未結商機與管道值，以決定是否要優先處理科目。
* 使用&#x200B;**[!UICONTROL 最上層成員]**&#x200B;來識別要聯絡的人，然後將其註冊到外站工作流程。
* 在通話前詢問[AI聊天](ai-assistant.md)以開發帳戶的定位。

>[!MORELIKETHIS]
>
>* [潛在客戶](prospects.md)
>* [傳出工作流程](outbound-workflows.md)
>* [AI聊天](ai-assistant.md)
