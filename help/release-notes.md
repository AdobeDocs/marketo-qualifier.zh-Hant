---
title: '[!DNL Adobe Marketo Qualifier] 發行說明'
description: 瞭解[!DNL Adobe Marketo Qualifier]的新增功能。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
source-git-commit: 3b50b4d3000696cb25ef747fefd579cfd3b3ba0f
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 12%
---
# [!DNL Adobe Marketo Qualifier] 發行說明

## 10-08-2026

此版本包括：

* 重複使用傳出工作流程，或變更執行中工作流程的接觸點，複製並編輯副本。 複製會以無潛在客戶的私人草稿開始，而原始工作流程則保持不變。 [了解更多](outbound-workflows.md#duplicate-an-outbound-workflow)。
* 以精簡版面配置輸出工作流程，並在目標、目標定位、接觸點和設定之間導覽。 [了解更多](outbound-workflows.md#create-an-outbound-workflow)。
* 系統會自動辨識電子郵件回覆中的清除選擇退出請求。 潛在客戶會標籤為選擇退出，並且不會傳送進一步的接觸點。 [了解更多](outbound-workflows.md#opt-out-requests-in-replies)。
* 以結合網頁研究和產品特定客戶案例研究的單一簡報，根據相關性和識別出的來源來排名談話要點，為會議做好準備。 [了解更多](prospects.md#generate-meeting-prep)。
* 產生的電子郵件會根據品質准則進行檢查，並在您檢閱前視需要重新寫入。 您仍然會在傳送每封電子郵件之前稽核、編輯和核准。 [了解更多](outbound-workflows.md#review-and-refine-generated-emails)。

## 09-22-2026

此版本包括：

* 在內嵌CRM外掛程式中檢視[!DNL Marketo Sales Insights]和代理程式資料，並將潛在客戶新增至[!DNL Marketo Qualifier]。 [了解更多](admin-settings.md#crm-mcp-and-the-embedded-plugin)。
* 使用Best Bets、我的觀察清單、網路活動、電子郵件參與和網路研討會活動來排定CRM銷售機會的優先順序。 [了解更多](admin-settings.md#prioritize-leads-in-the-crm-plugin)。
* 當潛在客戶的上線[!DNL Marketo]活動符合工作流程條件時，自動將潛在客戶註冊到外站工作流程。 [了解更多](home.md#automatically-enroll-prospects-from-marketing-highlights)。
* 檢閱潛在客戶內容並匯出潛在客戶清單，以及在[!DNL Marketo Optimizer]個Prime和Ultimate執行個體上檢視AI人員摘要。 [了解更多](prospects.md#review-prospect-context-and-export-the-list)。
* 審查並核准從工作佇列產生的潛在客戶電子郵件，並在傳出工作流程期間以代理程式建議回覆。 [了解更多](tasks.md)。

## 09-08-2026

此版本包括：

* 在「設定檔」設定中設定一次您自己的電子郵件草擬樣式，每個產生的電子郵件都會依循該樣式。 [了解更多](profile-settings.md#email-drafting-context)。
* 在新的「會議研究」標籤中，從潛在客戶頁面產生目標型或自訂會議準備。 [了解更多](prospects.md#generate-meeting-prep)。
* 管理員可以將「輸出工作流程」指派給隊友，並將工作流程設定重設為預設值。 [了解更多](outbound-workflows.md#create-an-outbound-workflow)。
* 從CSV匯入潛在客戶時，請對應自訂欄位，並在產生的電子郵件中使用這些值。 [了解更多](prospects.md#build-your-prospect-list)。
* 產生的電子郵件會使用您匯入的任何其他潛在客戶資料，並且可以用潛在客戶的語言以原生方式撰寫。 [了解更多](outbound-workflows.md#step-5-add-prospects-and-start-email-generation)。
* 「出站績效」預設會顯示開啟率和點按率，在組織層次切換原始計數和潛在客戶總計。 [了解更多](performance.md)。
* 當潛在客戶在輸出工作流程中移動時，CRM同步規則會自動更新CRM狀態。 [了解更多](admin-settings.md#configure-crm-sync-rules)。
* 在您的[!DNL Marketo Qualifier]、CRM、[!DNL Marketo]和[!DNL Marketo Optimizer]資料中詢問AI Chat問題。 [了解更多](ai-assistant.md#ask-ai-chat-across-your-connected-data)。

## 08-17-2026

[!DNL Marketo Qualifier]現在可作為獨立應用程式使用。 它支援[!DNL Marketo Engage]和[!DNL Marketo Optimizer]。

此版本包括：

* 透過AI產生的活動摘要和訊號型評分，實現潛在客戶和帳戶優先順序。 [進一步瞭解](prospects.md#review-prospect-details)潛在客戶或[帳戶](accounts.md#account-insights)。
* 具有AI建議的步調和草擬電子郵件的目標導向傳出工作流程。 [了解更多](outbound-workflows.md)。
* 電話、LinkedIn InMails和電子郵件稽核的統一工作佇列。 [了解更多](tasks.md)。
* 透過行事曆整合自動預約會議。 [了解更多](outbound-workflows.md#meeting-booking)。
* 一個知識中心，可在您自己的行動手冊資料中將AI外聯活動納入基礎。 [了解更多](admin-settings.md#knowledge-center)。
* AI Chat會根據您的CRM、參與和知識中心資料提供自然語言問題。 [了解更多](ai-assistant.md)。
* 電子郵件和會議預約效能報表。 [了解更多](performance.md)。
* 在CRM或Outlook中存取的瀏覽器和電子郵件外掛程式。 [了解更多](admin-settings.md#crm-mcp-and-the-embedded-plugin)。
* 支援Salesforce和Microsoft Dynamics 365整合。 [了解更多](integrations.md)。
