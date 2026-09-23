---
title: 管理整合
description: 瞭解如何連線Outlook、管理CRM連線、對應輸入欄位、同步活動，以及在Adobe Marketo限定詞中設定全域電子郵件選擇退出。
feature: Agentic AI, Sales Insights, Account Journeys
role: User, Admin
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '1383'
ht-degree: 1%
---

# 整合

連線Outlook以傳送電子郵件、辨識潛在客戶回覆，以及排程會議。 若要讓銷售機會、聯絡人、客戶、商機、活動和擁有者可用於Account Qualification Agent (AQA)和對外工作流程，您也可以將Adobe Marketo Qualifier連線至Salesforce或Microsoft Dynamics 365。 Marketo限定詞可讀取CRM資料、將外聯活動和選擇退出狀態寫入回CRM，並可將外聯活動同步到Marketo。 它不會以其他方式修改CRM記錄。

本文說明如何連線Outlook、管理CRM連線、對應欄位、同步活動以及設定電子郵件選擇退出。 若要第一次連線CRM，請參閱[開始使用](getting-started.md#connect-your-crm)。

>[!IMPORTANT]
>
>Outlook連線是依代表而定。 本文稍後說明的CRM和合規性設定適用於整個組織。 若要存取這些全組織的設定，您必須屬於`Marketo Qualifier`和`Marketo Qualifier Admins`使用者群組。 標準使用者可使用已設定的CRM資料和篩選器，但無法變更設定。

## 連線Outlook

每個代表都會連線自己的Outlook帳戶：

1. 選取&#x200B;**[!UICONTROL 連線Outlook]**。
1. 使用您的Microsoft帳戶登入。
1. 檢閱並核准要求的存取權。

此連線可讓Marketo Qualifier從您的信箱傳送、識別潛在客戶回覆的時間，以及排程您行事曆上的會議。

連線時，您可以核准允許Marketo限定詞的存取權：

* 識別潛在客戶的回覆。
* 代表您建立並傳送電子郵件。
* 使用您的行事曆排程會議。
* 讀取您的信箱時區與排程工作時間。
* 保持自動登入，讓這些功能繼續運作，而不需要您再次登入。

### Outlook核准（如果需要）

依預設，不需要系統管理員採取任何動作。 每位代表都會在連線Outlook時核准自己的存取權。

如果您的組織已在Microsoft 365或Microsoft Entra中關閉協力廠商應用程式的使用者同意，Microsoft 365或Entra管理員必須針對整個組織核准一次Marketo限定詞。 管理員會在代表連線其Outlook帳戶之前完成此核准。 在整個組織核心准後，每個代表都可以連線其帳戶。

### Marketo限定詞如何處理您的信箱資料

Marketo限定詞只會讀取其所傳送之電子郵件的回覆，而不會讀取收件匣的其他部分。 不會將傳入附件或電子郵件儲存在作用中參與以外的位置。 已加密儲存的登入認證。

## 開啟CRM設定

在左側導覽列中，展開&#x200B;**[!UICONTROL 管理]**&#x200B;並選取&#x200B;**[!UICONTROL 管理設定]**。 設定會分為兩個群組：

| 群組 | 專案 |
| --- | --- |
| **[!UICONTROL 整合]** | **[!UICONTROL CRM連線]**，**[!UICONTROL 知識中心]** |
| **[!UICONTROL 合規性]** | **[!UICONTROL 電子郵件設定]** |

若為知識中心，請參閱[建立知識中心行動手冊](admin-settings.md#knowledge-center)。

## 管理CRM連線

選取&#x200B;**[!UICONTROL CRM連線]**。 此頁面包含&#x200B;**[!UICONTROL Salesforce]**&#x200B;和&#x200B;**[!UICONTROL Microsoft]** (Microsoft Dynamics 365)的卡片。 每張卡片都會顯示以下其中一種狀態：

| 狀態 | 含義 |
| --- | --- |
| **[!UICONTROL 已連線]** | 連線處於作用中狀態並經過驗證。 |
| **[!UICONTROL 非使用中]** | 沒有為此CRM設定連線。 |
| **[!UICONTROL 需要的許可權]** | 連線已驗證，但缺少必要的範圍。 卡片會列出缺少的範圍。 |

>[!NOTE]
>
>一次只能有一個CRM為作用中。 當一個CRM連線時，另一個卡片會停用。 請先中斷使用中CRM的連線，然後再連線其他的CRM。

未設定的卡片顯示&#x200B;**[!UICONTROL 連線]**。 已設定的卡片顯示&#x200B;**[!UICONTROL 管理]**&#x200B;和具有&#x200B;**[!UICONTROL 編輯設定]**&#x200B;和&#x200B;**[!UICONTROL 中斷連線]**&#x200B;的&#x200B;**[!UICONTROL 更多]**&#x200B;功能表。

### 連線或編輯連線

1. 若要建立連線，請在CRM卡片上選取&#x200B;**[!UICONTROL 連線]**。 若要更新現有的連線，請選取&#x200B;**[!UICONTROL 更多]** > **[!UICONTROL 編輯組態]**。
1. 輸入您CRM管理員的認證。

   >[!BEGINTABS]

   >[!TAB Salesforce]

   輸入&#x200B;**[!UICONTROL 使用者端識別碼（使用者金鑰）]**、**[!UICONTROL 執行個體URL]**&#x200B;和&#x200B;**[!UICONTROL 使用者端密碼]**。 使用標準執行個體URL表單`https://{{mydomain}}.my.salesforce.com`。

   ![Salesforce認證](assets/crm-salesforce-config.png){width="800" zoomable="yes"}

   >[!TAB Microsoft Dynamics]

   輸入&#x200B;**[!UICONTROL 使用者端識別碼（消費者金鑰）]**、**[!UICONTROL 租使用者識別碼]**、**[!UICONTROL Microsoft Dynamics執行個體URL]**&#x200B;以及&#x200B;**[!UICONTROL 使用者端密碼]**。 使用標準執行個體URL表單`https://{{mydomain}}.crm.dynamics.com`。

   >[!ENDTABS]

1. 選取&#x200B;**[!UICONTROL 連線]** （編輯時選取&#x200B;**[!UICONTROL 儲存]**）。

如果Marketo限定詞拒絕認證，則會識別原因，例如認證無效或過期、缺少許可權或無法辨識的Dynamics租使用者。 請更正值，然後再試一次。

>[!IMPORTANT]
>
>請勿透過電子郵件傳送使用者端密碼。 使用您組織核准的安全管道，與在Marketo辨識符號中輸入認證的人共用認證。

### 中斷連線

1. 在連線的CRM卡片上，選取&#x200B;**[!UICONTROL 更多]** > **[!UICONTROL 中斷連線]**。
1. 檢閱警告。 若要確認，請選取&#x200B;**[!UICONTROL 中斷連線]**。

>[!WARNING]
>
>當您中斷CRM連線時，組織中的所有潛在客戶都會暫停傳出工作流程，在您重新連線之前，不會有任何新的潛在客戶從您的CRM同步。

## 對應CRM欄位（傳入對應） {#map-crm-fields-inbound-mapping}

傳入對應可控制Marketo限定詞匯入的CRM欄位及其顯示位置。 欄位會分組為多個區段，每個區段都屬於一個實體型別。

![傳入對應](assets/crm-conn-salesforce.png){width="800" zoomable="yes"}

1. 在連線的CRM卡上，選取&#x200B;**[!UICONTROL 管理]**。
1. 在&#x200B;**[!UICONTROL 入站對應]**&#x200B;索引標籤上，選取&#x200B;**[!UICONTROL 新增區段]**。

   ![新增節](assets/crm-add-section.png){width="800" zoomable="yes"}

1. 在&#x200B;**選取區段**&#x200B;步驟中，選擇實體型別，然後選取&#x200B;**[!UICONTROL 下一步]**：

   | 實體 | 其欄位出現的位置 |
   | --- | --- |
   | **[!UICONTROL 潛在客戶]** | 潛在客戶的&#x200B;**[!UICONTROL 人員]**&#x200B;標籤。 |
   | **[!UICONTROL 聯絡人]** | 連絡人記錄。 |
   | **[!UICONTROL 帳戶]** | **[!UICONTROL 帳戶]**&#x200B;標籤。 檢視[帳戶](accounts.md)。 |
   | **[!UICONTROL 機會]** | 帳戶的機會詳細資料。 |

1. 輸入&#x200B;**[!UICONTROL 區段名稱]**&#x200B;和選用的&#x200B;**[!UICONTROL 描述]**。 然後，選取&#x200B;**[!UICONTROL 下一步]**。
1. 在&#x200B;**[!UICONTROL 新增欄位]**&#x200B;步驟中，若要匯入CRM欄位，請搜尋並選取它們。 然後，若要繼續，請選取&#x200B;**[!UICONTROL 下一步]**。 每個欄位會顯示其&#x200B;**[!UICONTROL 顯示名稱]**、**[!UICONTROL 欄位名稱]**&#x200B;和&#x200B;**[!UICONTROL 資料型別]**。
1. 針對&#x200B;**[!UICONTROL 潛在客戶]**、**[!UICONTROL 連絡人]**&#x200B;及&#x200B;**[!UICONTROL 商機]**&#x200B;區段，針對[潛在客戶](prospects.md)清單上代表所需的每個欄位，開啟&#x200B;**[!UICONTROL 可篩選]**。

   如果欄位的資料型別不支援篩選，或欄位已用於其他區段中，則無法將其設為可篩選。

   在&#x200B;**[!UICONTROL 我的機會聯絡人]**&#x200B;中，可篩選的機會欄位會顯示為單獨的欄，並帶有&#x200B;**[!UICONTROL 階段（機會）]**&#x200B;等標籤。 尾碼可區分相關連絡人欄位中的機會屬性。

1. 在&#x200B;**[!UICONTROL 預覽]**&#x200B;步驟中，確認您的選取專案並選取&#x200B;**[!UICONTROL 新增]**。

若要稍後變更節，請選取節卡上的&#x200B;**[!UICONTROL 編輯]**。 若要移除節，請選取節卡上的&#x200B;**[!UICONTROL 移除]**。 若要移除個別欄位，請在欄位列中選取刪除動作。 確認每次移除。

## 設定活動同步（傳出對應） {#configure-activity-sync-outbound-mapping}

Activity Sync會將Marketo Qualifier外聯活動寫入您的CRM和Marketo。 已傳送、已開啟、已點按和已回覆的電子郵件活動包含傳出工作流程名稱。 代表可以在CRM中看到活動，而行銷團隊可以在潛在客戶評分和參與時間表中使用Marketo活動。

1. 在連線的CRM卡上，選取&#x200B;**[!UICONTROL 管理]**。
1. 開啟&#x200B;**[!UICONTROL 傳出對應]**&#x200B;索引標籤。
1. 開啟&#x200B;**[!UICONTROL 活動同步]**。 設定會立即儲存。

當活動同步關閉時，Marketo Qualifier會繼續使用傳入CRM資料，但不會將外聯活動同步至CRM或Marketo。

>[!NOTE]
>
>活動同步作業需要您CRM中的寫入許可權。 如果缺少必要的許可權，則會停用切換器，且Marketo限定詞會提示您連絡管理員。 若要授與活動寫入許可權，請與您的CRM管理員合作。

## 設定行銷重點專案 {#turn-on-marketo-engagement-filtering}

行銷重點可讓代表透過其即時[!DNL Marketo]參與（例如電子郵件開啟和點按），尋找潛在客戶並安排其優先順序。 請參閱[依行銷重點篩選](prospects.md#filter-by-marketing-highlights)。

管理員完成一次性設定，將[!DNL Marketo]連線到相關組織和沙箱的Marketo限定詞。 此設定涵蓋在Adobe Developer Console中建立API認證、在[!DNL Marketo]中設定webhook，以及將該webhook新增至觸發程式Smart Campaign。 如需完整步驟，請參閱[設定行銷重點專案](marketing-highlights-setup.md)。

行銷重點適用於所有生產區域：北美、歐洲、中東和非洲及澳洲。

## 設定全域電子郵件選擇退出 {#configure-global-email-opt-out}

選擇退出設定會在每封傳出電子郵件後附加取消訂閱頁尾。 標準使用者無法針對個別電子郵件將其關閉。

1. 在左側導覽列中，展開&#x200B;**[!UICONTROL 管理]**&#x200B;並選取&#x200B;**[!UICONTROL 管理設定]**。
1. 選取&#x200B;**[!UICONTROL 合規性]**&#x200B;下的&#x200B;**[!UICONTROL 電子郵件設定]**。
1. 開啟每封電子郵件的&#x200B;**[!UICONTROL 包含選擇退出連結]**。
1. 在&#x200B;**[!UICONTROL 選擇退出訊息範本]**&#x200B;中輸入頁尾文字。 納入應該顯示可點按取消訂閱連結的`{opt_out_link}`權杖。

   例如︰`If you'd prefer not to receive these emails, you can {opt_out_link}.`

設定和範本會自動儲存。

當潛在客戶選取連結時，Marketo Qualifier會停止向該潛在客戶傳送電子郵件，並將選擇退出狀態同步到連線的CRM。

## CRM存取範圍

Marketo Qualifier會讀取所需的CRM實體，並只回寫已定義的資料集：

* **讀取** — 使用者、連絡人、擁有者對應、潛在客戶、帳戶、商機及活動。
* **寫入** — 記錄外展活動（當[活動同步](#configure-activity-sync-outbound-mapping)開啟時）和選擇退出狀態。

您的CRM管理員已在Salesforce或Dynamics中準備API存取。 Marketo Qualifier管理員接著會連線CRM、對應傳入欄位，並選擇是否同步活動。 初始連線需要唯讀存取權。 活動同步和選擇退出回寫需要對應的寫入許可權。

>[!MORELIKETHIS]
>
>* [開始使用](getting-started.md)
>* [帳戶](accounts.md)
