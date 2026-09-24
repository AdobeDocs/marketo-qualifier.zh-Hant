---
title: '[!DNL Adobe Marketo Qualifier]中的潛在客戶'
description: 瞭解如何在[!DNL Adobe Marketo Qualifier]中從CRM、匯入和手動新增來源、篩選潛在客戶以及檢閱潛在客戶詳細資訊，建立您的潛在客戶清單。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
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
source-git-commit: 2124387555f5fb08ea19eaf121fc87aa66d66de2
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%
---

# 潛在客戶

若要檢視您可以存取的潛在客戶與聯絡人，請在左側導覽中選取&#x200B;**[!UICONTROL 潛在客戶]**。 使用清單來檢閱每個潛在客戶的狀態和最新活動。

![潛在客戶表格顯示潛在客戶管理的潛在客戶狀態和最後一個活動](./assets/prospects.png){width="800" zoomable="yes"}

* 在連線的CRM中指派給您的&#x200B;**[!UICONTROL 銷售機會]**&#x200B;銷售機會。
* 在連線的CRM中指派給您的&#x200B;**[!UICONTROL 連絡人]**&#x200B;連絡人。
* **[!UICONTROL 行銷重點]**&#x200B;具有即時Marketo活動（例如電子郵件開啟或點按）的潛在客戶。
* **[!UICONTROL 人員清單]**&#x200B;您手動匯入或新增的潛在客戶。

## 檢閱潛在客戶內容並匯出清單

潛在客戶清單會總結是否有其他內容可用於個人化外聯。 清單上方的摘要會顯示每個狀態的潛在客戶數量，而內容欄會顯示每個潛在客戶的狀態：

* **[!UICONTROL 已套用]**&#x200B;可用的內容已套用至潛在客戶。
* **[!UICONTROL 部分]**&#x200B;僅套用部分可用的內容。
* **[!UICONTROL 遺失]**&#x200B;沒有其他可用的內容。

若要將目前的潛在客戶清單下載為CSV檔案，請選取&#x200B;**[!UICONTROL 匯出CSV]**。

## 建立您的潛在客戶清單

潛在客戶清單結合來自多個來源的人員：

* **CRM潛在客戶**—[!DNL Adobe Marketo Qualifier]會自動匯入指派給連線使用者的潛在客戶與連絡人。 請參閱[整合](integrations.md)。
* **匯入的潛在客戶** — 從CSV檔案匯入的潛在客戶。
* **手動新增潛在客戶** — 在Marketo限定詞中新增個別潛在客戶。

若要新增非來自您CRM的潛在客戶：

1. 在&#x200B;**[!UICONTROL 潛在客戶]**&#x200B;頁面上，選取&#x200B;**[!UICONTROL 人員清單]**。

   ![人員清單](assets/prospects-people-list.png){width="800" zoomable="yes"}

1. 選取&#x200B;**[!UICONTROL +新增人員]**，然後選取&#x200B;**[!UICONTROL 匯入CSV]**&#x200B;或&#x200B;**[!UICONTROL 新增人員]**。

   * 若要匯入CSV，請上傳`firstname,email`格式的CSV。
     名字和電子郵件為必填。 姓氏為選用。 CSV範本不包含CRM銷售機會ID欄，但您可以在匯入之前將該欄及其值新增到檔案中。 如果匯入失敗，請檢閱錯誤訊息以尋找要更正的欄位或值，然後再次上傳檔案。
     對應任何自訂或其他CSV欄位，而不僅僅是標準欄位。 Marketo Qualifier會將這些值儲存給每個潛在客戶，並於稍後提供這些值，包括產生[電子郵件](outbound-workflows.md#step-5-add-prospects-and-start-email-generation)。
   * 若要手動新增人員，請在表單中輸入其詳細資料。

1. 選取「**[!UICONTROL 儲存]**」。

## 篩選和尋找潛在客戶

若要縮小清單範圍，請選取&#x200B;**[!UICONTROL 篩選器]**。 您可以依下列條件篩選：

* 傳出工作流程狀態
* 建立者
* 職稱
* 帳戶
* 來源
* 上次更新時間

管理員也可以將對應的CRM欄位設為篩選條件。 在&#x200B;**[!UICONTROL 管理設定]**&#x200B;中，針對使用者用來尋找潛在客戶的每個欄位開啟&#x200B;**[!UICONTROL 可篩選]**。 檢視[對應CRM欄位](integrations.md#map-crm-fields-inbound-mapping)。

在&#x200B;**[!UICONTROL 我的商機聯絡人]**&#x200B;中，您也可以依相關商機的欄位來篩選聯絡人，例如階段、型別和結束日期。 商機欄位有標籤，例如&#x200B;**[!UICONTROL 階段（商機）]**，這會將商機欄位與聯絡人欄位區分開來。 您的管理員可控制哪些機會欄位可做為篩選器。

### 依行銷重點篩選

透過潛在客戶的即時[!DNL Marketo]參與（例如電子郵件活動、網站造訪和表單填寫）來檢閱並排定其優先順序。 參與幾乎會即時出現。

若要依行銷重點篩選潛在客戶：

1. 選取&#x200B;**[!UICONTROL 篩選器]**。
1. 新增行銷重點篩選並設定活動型別、行銷活動或其他屬性，以聚焦於重要的參與。

每個潛在客戶都會顯示其最新的[!DNL Marketo]活動以及最近的歷史記錄。

行銷重點適用於所有生產區域。 管理員完成一次性設定，將[!DNL Marketo]連線至Marketo辨識符號。 請參閱[設定行銷重點專案](integrations.md#turn-on-marketo-engagement-filtering)。

## 檢閱潛在客戶詳細資訊

若要開啟潛在客戶設定檔，請選取潛在客戶。 在聯絡之前，請先檢閱重要的訊號：

* **AI人員摘要** — 潛在客戶或連絡人及其最近參與的AI寫入快照。 在檢閱個別活動之前，使用摘要快速瞭解人員。 執行[!DNL Marketo Optimizer] Prime或Ultimate的執行個體上有AI人員摘要。
* **活動清單** — 按時間順序排列的活動和最近行為清單。
* **時間表檢視** — 跨管道互動的視覺時間表。
* **已檢視內容** — 潛在客戶已檢視的網頁和資產。 若要開啟專案，請選取該專案。

### 產生會議準備

除了長期的AI人員摘要之外，您還可以從&#x200B;**[!UICONTROL 帳戶研究]**&#x200B;旁的&#x200B;**[!UICONTROL 會議研究]**&#x200B;索引標籤，產生針對特定近期通話量身打造的會議準備。

* **目標型** — 如果潛在客戶已註冊執行中的輸出工作流程，請選取它。 準備作業會符合該傳出工作流程的目標，例如預約會議或重新與潛在客戶互動。
* **自訂提示** — 輸入您要準備的內容，例如`Focus on renewal risk`或`Prepare for a technical deep dive with their IT lead`。 準備符合您的提示。 只要潛在客戶不在執行中的傳出工作流程中，就可以使用自訂提示選項。

>[!MORELIKETHIS]
>
>* [帳戶](accounts.md)
>* [傳出工作流程](outbound-workflows.md)
>* [AI聊天](ai-assistant.md)
