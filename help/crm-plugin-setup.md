---
title: CRM連線
description: 瞭解如何在Salesforce或Microsoft Dynamics 365中安裝Marketo Qualifier，以及如何為傳出工作流程和Marketo行銷活動設定Salesforce動作。
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
subfeature_v2:
  - id: d2fe5f36-5653-5902-937c-9d3026104284
    internal-label: CRM integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 633ca975d4fe58bdcc84caf633049ae1190b0f56
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%
---

# CRM連線

安裝[!DNL Adobe Marketo Qualifier] CRM外掛程式，讓代表可以在潛在客戶、連絡人和帳戶記錄頁面上使用[!DNL Marketo Sales Insights]和AI產生的深入分析，而不需要離開Salesforce或Microsoft Dynamics 365。 外掛程式也會提供主檢視，讓您[優先處理CRM](admin-settings.md#prioritize-leads-in-the-crm-plugin)中的潛在客戶。

在Salesforce中，代表還可以從潛在客戶和聯絡人清單檢視及個別記錄頁面，將潛在客戶新增到對外工作流程或Marketo行銷活動。

## 開始之前

請確定安裝及使用外掛程式的人員具備必要的存取權：

* **Salesforce系統管理員**：安裝套件和編輯頁面配置的許可權。
* **Microsoft Dynamics 365系統管理員**：在Power Apps中將解決方案匯入目標環境的許可權。
* **代表**：存取Marketo Qualifier和相關CRM記錄。

安裝外掛程式與[將您的CRM連線至Marketo Qualifier](getting-started.md#connect-your-crm)是分開的。

## 在Salesforce中安裝

安裝套件，然後將其元件新增到代表使用的記錄頁面。

1. 開啟[Salesforce安裝頁面](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce)，並以管理員身分登入Salesforce。
1. 在套件安裝頁面上，選取[為所有使用者安裝]&#x200B;**&#x200B;**，然後選取[安裝]&#x200B;**&#x200B;**。

   您仍然可以透過Salesforce許可權控制個別使用者的存取權。

1. 當提示核准協力廠商存取時，請選取核准核取方塊並選取&#x200B;**[!UICONTROL 繼續]**。
1. 安裝完成時，請選取&#x200B;**[!UICONTROL 完成]**。

   安裝需要幾分鐘的時間。 確認封裝出現在&#x200B;**[!UICONTROL 已安裝的封裝]**&#x200B;頁面上。

1. 在Lightning App Builder中，編輯Lead、Contact和Account記錄頁面，並新增Marketo Qualifier元件。

### 新增動作至清單檢視

針對潛在客戶與連絡人清單檢視，分別設定&#x200B;**[!UICONTROL 新增至傳出工作流程]**&#x200B;和&#x200B;**[!UICONTROL 新增至Marketo行銷活動]**。 使用套件中包含的按鈕來避免重複專案。

1. 移至&#x200B;**[!UICONTROL 安裝程式]** > **[!UICONTROL 物件管理員]**&#x200B;並選取&#x200B;**[!UICONTROL 銷售機會]**&#x200B;或&#x200B;**[!UICONTROL 連絡人]**。
1. 開啟&#x200B;**[!UICONTROL 按鈕、連結和動作]**，然後找到清單按鈕&#x200B;**[!UICONTROL AMQ Add to Outbound Workflow]**&#x200B;和&#x200B;**[!UICONTROL AMQ Add to Marketo Campaign]**。
1. 開啟物件的&#x200B;**[!UICONTROL 清單檢視按鈕配置]**&#x200B;並選取&#x200B;**[!UICONTROL 編輯]**。

   根據您的Salesforce設定，清單檢視配置可能會位於&#x200B;**[!UICONTROL 搜尋配置]** > **[!UICONTROL 清單檢視]**&#x200B;下。

1. 將兩個清單按鈕移動到&#x200B;**[!UICONTROL 選取的按鈕]**&#x200B;並儲存。
1. 對其他物件重複此動作。

代表在清單檢視中選取一或多個記錄，然後選取動作。

### 新增動作以記錄頁面

記錄頁面動作必須與清單檢視按鈕分開設定。 將兩個動作新增至每個使用中的Lead和Contact頁面配置。

1. 移至&#x200B;**[!UICONTROL 安裝程式]** > **[!UICONTROL 物件管理員]**&#x200B;並選取&#x200B;**[!UICONTROL 銷售機會]**&#x200B;或&#x200B;**[!UICONTROL 連絡人]**。
1. 開啟&#x200B;**[!UICONTROL 按鈕、連結和動作]**，然後找到詳細資料按鈕&#x200B;**[!UICONTROL AMQ Add to Outbound Workflow]**&#x200B;和&#x200B;**[!UICONTROL AMQ Add to Marketo Campaign]**。
1. 開啟&#x200B;**[!UICONTROL 頁面配置]**&#x200B;並編輯指派給您的代表的配置。
1. 將兩個詳細資料按鈕新增至&#x200B;**[!UICONTROL Salesforce Mobile和Lightning Experience Actions]**&#x200B;並儲存。
1. 對每個適用的版面以及其他物件重複此步驟。

動作會出現在記錄的動作列或其功能表中，並套用至正在檢視的記錄。

>[!NOTE]
>
>這些動作適用於案頭Salesforce Lightning Experience，而非Salesforce行動應用程式。 名為&#x200B;**[!UICONTROL Salesforce Mobile和Lightning Experience Actions]**&#x200B;的版面配置區段也用於案頭動作。

### 取代缺少的按鈕

如果缺少封裝按鈕，請在物件的&#x200B;**[!UICONTROL 按鈕、連結和動作]**&#x200B;下建立取代專案。

1. 選取&#x200B;**[!UICONTROL 新按鈕或連結]**。
1. 輸入動作的標籤，例如`Add to Outbound Workflow`或`Add to Marketo Campaign`。
1. 選擇清單檢視的&#x200B;**[!UICONTROL 清單按鈕]**&#x200B;或記錄頁面的&#x200B;**[!UICONTROL 詳細資料頁面按鈕]**。
1. 將&#x200B;**[!UICONTROL 內容Source]**&#x200B;設定為&#x200B;**[!UICONTROL Visualforce頁面]**，然後選擇符合動作、物件和位置的封裝動作頁面。

   潛在客戶清單、潛在客戶詳細資訊、聯絡人清單和聯絡人詳細資訊版位使用不同的頁面。 確認選取的頁面符合您設定的版位。

1. 針對清單按鈕，請選取&#x200B;**[!UICONTROL 需要選取資料列]**。
1. 儲存按鈕並將其新增至適當的清單檢視按鈕版面配置或記錄頁面動作，如上所述。

### 檢查Salesforce動作

儲存版面配置後，請確認這兩個動作都會出現在「銷售機會」與「連絡人」清單檢視及記錄頁面上。 使用選取的記錄測試每個清單動作，並從個別記錄測試每個記錄頁面動作。

如果動作無法使用或未開啟，請使用以下檢查：

| 問題 | 檢查內容 |
| --- | --- |
| 清單檢視中缺少按鈕 | 確認清單按鈕位於正確物件的&#x200B;**[!UICONTROL 清單檢視按鈕配置]**&#x200B;上的&#x200B;**[!UICONTROL 選取的按鈕]**&#x200B;中，並儲存配置。 |
| 記錄頁面中缺少按鈕 | 確認詳細資訊按鈕位於指派給使用者的版面配置上的&#x200B;**[!UICONTROL Salesforce Mobile和Lightning Experience Actions]**&#x200B;中。 如果您的組織使用「動態動作」，請一併檢查記錄頁面的動作可見性。 |
| 建立按鈕時，預期頁面選項無法使用 | 檢查清單檢視的顯示型別是否為&#x200B;**[!UICONTROL 清單按鈕]**，或記錄頁面是否為&#x200B;**[!UICONTROL 詳細頁面按鈕]**。 |
| 動作未開啟或顯示存取錯誤 | 確認使用者有權存取Marketo Qualifier和選取的記錄。 |

## 在Microsoft Dynamics 365中安裝

將外掛程式套件匯入您的代表工作的環境。

1. 開啟[Microsoft Dynamics 365安裝頁面](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics)並下載套件ZIP檔。
1. 以系統管理員身分登入[Power Apps](https://make.powerapps.com/)並選取目標環境。
1. 開啟&#x200B;**[!UICONTROL 解決方案]**&#x200B;並選取&#x200B;**[!UICONTROL 匯入解決方案]**。
1. 選取&#x200B;**[!UICONTROL 瀏覽]**，選擇下載的ZIP檔案，然後選取&#x200B;**[!UICONTROL 下一步]**。
1. 檢閱封裝詳細資料，並選取&#x200B;**[!UICONTROL 下一步]**。
1. 保留預填的環境變數值，並選取&#x200B;**[!UICONTROL 匯入]**。
1. 在頁面頂端等候確認訊息，告知解決方案已成功匯入。

匯入需要幾分鐘的時間。

>[!MORELIKETHIS]
>
>* [優先處理CRM外掛程式中的潛在客戶](admin-settings.md#prioritize-leads-in-the-crm-plugin)
>* [整合](integrations.md)
>* [開始使用](getting-started.md)
