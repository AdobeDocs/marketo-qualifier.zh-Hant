---
title: 設定行銷重點專案
description: 瞭解如何將Marketo連結至Adobe Marketo Qualifier，讓代表可以透過「行銷焦點」中的即時Marketo活動檢視和篩選潛在客戶。
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
subfeature_v2:
  - id: 7b0925d9-0dc0-5c75-a54d-2bcc31c6ebe4
    internal-label: Marketing highlights
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: fcdc5d36cbb1500cf984e1439291aa8dbf17b72b
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%
---

# 設定行銷重點專案

行銷重點顯示每個潛在客戶的即時[!DNL Marketo]活動，例如電子郵件開啟與點按、網站造訪及表單填寫。 本文說明如何連線您的[!DNL Marketo]執行個體，讓活動能夠順利進行。

>[!IMPORTANT]
>
>完成此設定需要在[!DNL Marketo]中存取Adobe Developer Console和&#x200B;**[!UICONTROL 管理員]**。 請與您的Adobe連絡人及[!DNL Marketo]管理員合作，完成下列四個部分。

設定包含四個部分：

* A部分：在Adobe Developer Console中建立API認證。
* B部分：收集您的Adobe Marketo Qualifier端點和識別碼。
* C部分：在[!DNL Marketo Engage]中設定webhook。
* D部分：將webhook新增至觸發器Smart Campaign。

安裝完成後，使用者可以在&#x200B;**[!UICONTROL 潛在客戶]** > **[!UICONTROL 行銷焦點]**&#x200B;上看見並篩選此活動。

## A部分：建立API認證 {#part-a-create-api-credentials}

這些認證可讓[!DNL Marketo]安全地向Marketo Qualifier進行驗證。

若要建立證明資料：

1. 移至[Adobe Developer Console](https://developer.adobe.com/console/)並使用您的Adobe ID登入。
1. 選取&#x200B;**[!UICONTROL 建立新專案]**，或開啟現有的專案。
1. 若要重新命名專案，請選取&#x200B;**[!UICONTROL 編輯專案]**，輸入可識別的名稱，例如`Marketo Qualifier Marketing Highlights`，然後選取&#x200B;**[!UICONTROL 儲存]**。
1. 選取「**[!UICONTROL 新增API]**」、選取「**[!UICONTROL Experience Platform API]**」，然後選取「**[!UICONTROL 下一步]**」。
1. 選擇&#x200B;**[!UICONTROL OAuth伺服器對伺服器]**&#x200B;做為驗證型別，然後選取&#x200B;**[!UICONTROL 下一步]**。

   **[!UICONTROL OAuth伺服器對伺服器]**&#x200B;可讓[!DNL Marketo]直接從伺服器呼叫Marketo Qualifier API，而不需要人員登入。

1. 輸入45個字元或更少的認證名稱，例如`Marketo Qualifier Marketing Highlights Creds`。
1. 若要關聯產品設定檔，請選取該設定檔，然後選取[儲存]設定的API ]**。**[!UICONTROL 
1. 在&#x200B;**[!UICONTROL 連線的認證]**&#x200B;底下，開啟&#x200B;**[!UICONTROL OAuth伺服器對伺服器]**&#x200B;認證。 選取&#x200B;**[!UICONTROL 擷取使用者端密碼]**，然後複製&#x200B;**[!UICONTROL 使用者端識別碼]**&#x200B;和&#x200B;**[!UICONTROL 使用者端密碼]**。 您在[Part C](#part-c-configure-the-marketo-webhook)中使用這些值。

>[!WARNING]
>
>將使用者端密碼設為私人。 將其視為密碼，請勿透過電子郵件傳送。 使用您組織核准的安全頻道，與設定webhook的人共用它。

## B部分：收集您的端點與識別碼 {#part-b-gather-your-endpoint-and-identifiers}

您需要[Part C](#part-c-configure-the-marketo-webhook)的三個值：

* **端點URL** — 您地區的Marketo Qualifier webhook位址。
* **imsOrg ID** — 貴組織在Adobe Identity Management System (IMS)中的識別碼，格式為`{ORG_ID}@AdobeOrg`。
* **沙箱名稱** — 您的AEP沙箱名稱與Marketo Qualifier URL中顯示的名稱完全相同（`sname`值），不是UI中顯示的顯示名稱。 使用小寫URL值，例如`prod`，而不是`Prod`。

| 區域 | Webhook端點URL |
| --- | --- |
| 北美 | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| 歐洲、中東和非洲地區 | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC /澳洲 | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

如果您不確定自己的地區、imsOrg ID或沙箱名稱，您的Adobe聯絡人可以確認。

## C部分：設定Marketo webhook {#part-c-configure-the-marketo-webhook}

若要建立webhook：

1. 在[!DNL Marketo]中，選取&#x200B;**[!UICONTROL 管理員]** > **[!UICONTROL Webhooks]**。
1. 選取&#x200B;**[!UICONTROL 新Webhook]**。
1. 將&#x200B;**[!UICONTROL URL]**&#x200B;設定為[B](#part-b-gather-your-endpoint-and-identifiers)部分之您地區的端點URL。
1. 將&#x200B;**[!UICONTROL 要求型別]**&#x200B;設定為`POST`。
1. 將&#x200B;**[!UICONTROL 要求權杖編碼]**&#x200B;設定為`JSON`。 此為必要設定。
1. 將以下的裝載範本貼到&#x200B;**[!UICONTROL 範本]**&#x200B;中。 使用[!DNL Marketo]的&#x200B;**[!UICONTROL 插入Token]**&#x200B;來比對您執行個體中的欄位名稱。

   >[!NOTE]
   >
   >使用JSON編碼時，請勿將字串權杖括在引號中。 [!DNL Marketo]會自動新增它們。

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. 選取&#x200B;**[!UICONTROL Webhook動作]** > **[!UICONTROL 設定自訂標頭]**，然後使用[部分A](#part-a-create-api-credentials)和[部分B](#part-b-gather-your-endpoint-and-identifiers)的值新增下列標頭：

   | 標頭 | 值 |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | 您的使用者端ID |
   | `x-client-secret` | 您的使用者端密碼 |
   | `x-gw-ims-org-id` | 您的imsOrg ID |
   | `x-sandbox-name` | 您的沙箱名稱 |

   {style="table-layout:auto"}

1. 選取「**[!UICONTROL 儲存]**」。

## D部分：將webhook新增至觸發器Smart Campaign {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

將&#x200B;**[!UICONTROL 呼叫Webhook]**&#x200B;流程步驟新增至觸發智慧行銷活動（現有行銷活動或新行銷活動）。 智慧清單會在該行銷活動中觸發，以決定要將哪些活動傳送至Marketo Qualifier。

若要新增webhook：

1. 開啟現有的觸發器Smart Campaign，或建立新的觸發器（**[!UICONTROL 行銷活動]** > **[!UICONTROL 新增]** > **[!UICONTROL Smart Campaign]**）。
1. 在&#x200B;**[!UICONTROL 智慧列示]**&#x200B;索引標籤上，為您要傳送的活動新增觸發程式，例如&#x200B;**[!UICONTROL 在電子郵件中點按連結]**、**[!UICONTROL 填寫表單]**&#x200B;或&#x200B;**[!UICONTROL 瀏覽網頁]**。
1. 在&#x200B;**[!UICONTROL 流程]**&#x200B;索引標籤上，新增&#x200B;**[!UICONTROL 呼叫Webhook]**&#x200B;步驟，並選取您在[C](#part-c-configure-the-marketo-webhook)部分中建立的webhook。
1. 啟動Smart Campaign。

該Smart Campaign的活動現在流入Marketo Qualifier。 代表可以在&#x200B;**[!UICONTROL 潛在客戶]** > **[!UICONTROL 行銷重點專案]**&#x200B;上檢視並篩選此活動。

>[!MORELIKETHIS]
>
>* [管理整合](integrations.md)
>* [潛在客戶](prospects.md)
>* [開始使用](getting-started.md)
