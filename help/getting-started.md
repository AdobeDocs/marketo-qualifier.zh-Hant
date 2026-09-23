---
title: 開始使用Adobe Marketo辨識符號
description: 瞭解在您的團隊開始使用應用程式之前，如何完成Adobe Marketo限定元的一次性管理員設定，包括使用者群組和CRM連線。
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/-nfmFwZyZFUZhm-uQUjSyTvrORuqJgKSKnENWYtvubs'
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 0%
---

# 開始使用Adobe Marketo辨識符號

Adobe為您的組織布建Marketo限定詞後，[!DNL Marketo]系統管理員必須建立所需的使用者群組，並連線Salesforce或Microsoft Dynamics 365。

![Marketo辨識符號首頁](assets/homepage.png){width="800" zoomable="yes"}

## 設定使用者群組

Adobe Admin Console中的使用者群組可用來控制對Marketo限定詞的存取權。 必須先建立兩個群組，使用者才能登入。

如需設定群組的相關資訊，請參閱[Adobe Admin Console檔案](https://helpx.adobe.com/business/enterprise/users/users-and-groups/user-groups.html)。

>[!PREREQUISITES]
>
>建立群組的管理員必須同時符合下列兩項需求：
>
>* 成為組織管理員，並有權從Adobe應用程式切換器存取&#x200B;**[!UICONTROL Admin Console]**。
>* 已被指派Adobe Experience Platform產品或成為系統管理員。 否則，Adobe Experience Platform不會出現在產品清單中。

### Marketo限定詞使用者

使用者必須屬於`Marketo Qualifier`使用者群組才能存取應用程式。

這些步驟是在Adobe Admin Console中完成。

1. 從應用程式切換器中，選取&#x200B;**[!UICONTROL Admin Console]**。
1. 選取&#x200B;**[!UICONTROL 使用者]** > **[!UICONTROL 使用者群組]** > **[!UICONTROL 新增使用者群組]**。
1. 輸入`Marketo Qualifier`作為群組名稱，並選取&#x200B;**[!UICONTROL 儲存]**。
1. 開啟&#x200B;**[!UICONTROL 指派的產品設定檔]**&#x200B;並選取&#x200B;**[!UICONTROL 指派設定檔]**。
1. 選取&#x200B;**[!UICONTROL Adobe Experience Platform]**。
1. 選取&#x200B;**[!UICONTROL 預設的生產所有存取]**&#x200B;產品設定檔，選取&#x200B;**[!UICONTROL 套用]**，然後選取&#x200B;**[!UICONTROL 儲存]**。
1. 若要新增需要存取Marketo Qualifier的所有使用者，請開啟&#x200B;**[!UICONTROL 使用者]**&#x200B;並選取&#x200B;**[!UICONTROL 新增使用者]**。

### Marketo Qualifier管理員

設定CRM連線、[知識中心](admin-settings.md#knowledge-center)以及全域電子郵件選擇退出設定的管理員也必須屬於`Marketo Qualifier Admins`使用者群組。

1. 在Adobe Admin Console中，選取&#x200B;**[!UICONTROL 使用者]** > **[!UICONTROL 使用者群組]** > **[!UICONTROL 新增使用者群組]**。
1. 輸入`Marketo Qualifier Admins`作為群組名稱，並選取&#x200B;**[!UICONTROL 儲存]**。
1. 開啟&#x200B;**[!UICONTROL 使用者]**，選取&#x200B;**[!UICONTROL 新增使用者]**，然後新增系統管理員。
1. 確認每位管理員也是`Marketo Qualifier`群組的成員。

兩個群組的成員資格可讓左側導覽中的&#x200B;**[!UICONTROL 管理]**&#x200B;下顯示&#x200B;**[!UICONTROL 管理設定]**。 標準使用者可處理管理員設定的欄位、篩選器和教戰手冊。 設定的選擇退出頁尾會自動套用至其傳出電子郵件。 標準使用者無法變更這些設定。

使用者群組名稱必須完全符合上述步驟。

您也可以建立選用的`Marketo Qualifier BDR managers`群組。 此群組的成員可以存取電子郵件效能報表。

## 連線您的CRM

Marketo Qualifier會連線至Salesforce或Microsoft Dynamics 365，為BDR提供使用者、潛在客戶、聯絡人、帳戶、機會、擁有者對應和相關活動的統一檢視。 初始連線需要此CRM資料的唯讀存取權。 若要在連線Marketo Qualifier之前準備認證，請洽詢您的CRM管理員。 如需整合詳細資訊，請參閱[整合](integrations.md)。

>[!PREREQUISITES]
>
>若要存取CRM管理介面，您必須屬於`Marketo Qualifier Admins` Adobe Admin Console群組和`Marketo Qualifier`群組。

>[!BEGINTABS]

>[!TAB Salesforce]

Salesforce系統管理員會建立外部使用者端應用程式（也稱為連線應用程式），並設定其執行身分使用者。

>[!PREREQUISITES]
>
>確認Salesforce管理員具備下列許可權：
>
>* 自訂應用程式
>* 檢視設定
>* 修改所有資料
>* 管理連線應用程式
>
>系統管理員需要&#x200B;_管理連線的應用程式_&#x200B;才能檢視使用者端ID和使用者端密碼。

1. 在Salesforce中，移至&#x200B;**[!UICONTROL 設定]** > **[!UICONTROL 應用程式管理員]**&#x200B;並選取&#x200B;**[!UICONTROL 新連線應用程式]**&#x200B;或&#x200B;**[!UICONTROL 新外部使用者端應用程式]**。
1. 輸入應用程式名稱和管理連絡人電子郵件。
1. 啟用OAuth並輸入回呼URL。

   如果連線未使用重新導向，請輸入任何有效的URL。

1. 新增下列OAuth範圍：

   * 存取身分URL服務(`id`， `profile`， `email`， `address`， `phone`)
   * 透過API (`api`)管理使用者資料
   * 存取不重複的使用者識別碼(`openid`)

1. 啟用使用者端認證流程並選取&#x200B;**[!UICONTROL 執行身分]**&#x200B;使用者。
1. 確認執行身分使用者擁有`Leads`、`Accounts`、`Contacts`、`Tasks`、`Events`、`Opportunity`、`OpportunityContactRoles`和`OpportunityLineItems`的&#x200B;**讀取**&#x200B;存取權。 同時確認已啟用&#x200B;**存取活動**。
1. 儲存應用程式。
1. 從&#x200B;**[!UICONTROL 應用程式管理員]**，開啟應用程式並選取&#x200B;**[!UICONTROL 檢視]** > **[!UICONTROL 消費者詳細資料]**。
1. 為Marketo限定詞連線複製下列值：

   * 消費者金鑰（使用者端ID）
   * 使用者密碼（使用者端密碼）
   * 回呼 URL
   * Salesforce執行個體URL

步驟與此處說明的稍有不同。 如需詳細資訊，請參閱[Salesforce檔案](https://help.salesforce.com/s/?language=en_US)。

### 尋找您的Salesforce執行個體URL

1. 從瀏覽器位址列（`{{mydomain}}`值）登入並記下您的組織&#x200B;_我的網域_&#x200B;子網域。
1. 對Marketo限定詞使用標準格式： `https://{{mydomain}}.my.salesforce.com`。

請勿使用`lightning.force.com` URL作為執行個體URL。

>[!TIP]
>
>如果CRM連線介面報告缺少範圍，請檢查&#x200B;**[!UICONTROL 標準物件許可權]**&#x200B;下的執行身分使用者設定檔，以取得潛在客戶、連絡人、帳戶和商機的&#x200B;**讀取**&#x200B;存取權。 同時檢查每個指派許可權集中的&#x200B;**[!UICONTROL 物件設定]**。

>[!TAB Microsoft Dynamics 365]

Microsoft Dynamics 365或Azure管理員會註冊應用程式，並將其新增至Dynamics環境。

1. 在Microsoft Entra ID中，選取&#x200B;**[!UICONTROL 應用程式註冊]**&#x200B;並註冊應用程式。
1. 複製使用者端ID和租使用者ID，並建立使用者端密碼。
1. 在&#x200B;**[!UICONTROL Power Platform系統管理中心]**&#x200B;中，選取&#x200B;**[!UICONTROL 環境]**&#x200B;並開啟Dynamics環境。
1. 移至&#x200B;**[!UICONTROL 設定]** > **[!UICONTROL 使用者+許可權]** > **[!UICONTROL 應用程式使用者]**，然後選取&#x200B;**[!UICONTROL 新應用程式使用者]**。
1. 選取已註冊的Microsoft Entra應用程式。
1. 指定安全性角色，以授予潛在客戶、聯絡人、帳戶、商機及活動的讀取存取權。

   需要安全性角色。 應用程式必須有安全性角色才能存取Dynamics資料。

1. 收集使用者端ID、使用者端密碼、租使用者ID以及Dynamics執行個體URL。 使用標準URL表單`https://{{mydomain}}.crm.dynamics.com`。

>[!ENDTABS]

### 輸入您的連線

1. 請登入Marketo辨識符號群組，並確認已選取正確的沙箱或環境，以確認您是必要的Marketo辨識符號群組的成員。
1. 在左側導覽列中，展開&#x200B;**[!UICONTROL 管理]**&#x200B;並選取&#x200B;**[!UICONTROL 管理設定]**。
1. 選取&#x200B;**[!UICONTROL 整合]**&#x200B;下的&#x200B;**[!UICONTROL CRM連線]**。

   頁面會顯示Salesforce和Microsoft Dynamics的卡片。 非使用中的連線顯示&#x200B;**[!UICONTROL 連線]**。 已設定的連線顯示&#x200B;**[!UICONTROL 已連線]**&#x200B;和&#x200B;**[!UICONTROL 管理]**。

   ![Salesforce認證](assets/crm-salesforce-config.png){width="800" zoomable="yes"}

1. 為您使用的CRM選取&#x200B;**[!UICONTROL 連線]**。
1. 輸入您CRM管理員提供的認證和執行個體URL。
1. 成功連線後，請確認卡片顯示&#x200B;**[!UICONTROL 已連線]**。

### 匯入CRM欄位

連線CRM後，請設定輸入對應，以決定哪些CRM欄位會出現在Marketo限定詞中。 若要開啟&#x200B;**[!UICONTROL 輸入對應]**，請在連線的CRM卡片上選取&#x200B;**[!UICONTROL 管理]**，然後為您要匯入其欄位的每個實體型別新增區段。

如需完整的步驟，包括如何讓匯入的欄位成為可用的篩選器，請參閱[對應CRM欄位（輸入對應）](integrations.md#map-crm-fields-inbound-mapping)。

## 後續步驟

>[!MORELIKETHIS]
>
>* [潛在客戶](prospects.md)
>* [傳出工作流程](outbound-workflows.md)
