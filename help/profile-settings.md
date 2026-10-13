---
title: 設定輪廓設定
description: 瞭解如何在Adobe Marketo Qualifier設定檔設定中設定您的電子郵件連線、簽名和行事曆可用性。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/YsrBduYA7jKhgxttexqMBBpgDIq23s6wUb4Wp6y6h3g'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Sales Qualifier
feature_v2:
  - id: 1e0ea71a-a210-5748-9b0f-c02c2ef6a746
    internal-label: Workflows
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 3b50b4d3000696cb25ef747fefd579cfd3b3ba0f
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 3%
---

# 輪廓設定

在左側導覽列中，展開&#x200B;**[!UICONTROL 設定]**&#x200B;並選取&#x200B;**[!UICONTROL 設定檔設定]**。 使用這些設定來管理您的個人詳細資料、電子郵件連線、行事曆和聊天可用性。

![設定檔設定](assets/profile-email-config.png)

## 電子郵件設定

在&#x200B;**[!UICONTROL 電子郵件設定]**&#x200B;索引標籤中，設定您的電子郵件連線。

* **[!UICONTROL 電子郵件連線]** — 選取Microsoft Outlook或Google並依照登入程式進行。 如需您核准的存取許可權和系統管理員核准路徑，請參閱[連線Outlook](integrations.md#connect-outlook) （如果需要）。
* **[!UICONTROL 電子郵件簽章]** — 新增或更新產生之電子郵件中所使用的簽章。 加入您的[會議預訂](outbound-workflows.md#meeting-booking)連結，讓潛在客戶可以排程與您共度的時間。
* **[!UICONTROL 會議預約連結]** — 在您的電子郵件中傳送會議邀請。 取得會議URL。

### 電子郵件草擬內容

![電子郵件內容](assets/profile-email-instructions.png)

使用&#x200B;**[!UICONTROL 電子郵件起草內容]**&#x200B;來設定電子郵件語調、結構和樣式，讓電子郵件保持一致。

在&#x200B;**[!UICONTROL 電子郵件起草內容]**區域以純文字標籤撰寫內容。
使用它來定義：

* 音調和聲音
* 結構和長度
* Personalization與問候語規則
* 主旨列樣式
* 如何使用參與訊號
* 量度、證據和客戶故事的框架方式

依預設，草稿使用自訂前後關聯，因此您現有的草稿在加入您自己的前後關聯之前不會變更。

## 行事曆設定

在&#x200B;**[!UICONTROL 行事曆組態]**&#x200B;索引標籤上，設定您的時區與可用性。

* **[!UICONTROL 行事曆連線]** — 選取&#x200B;**[!UICONTROL 連線]**&#x200B;並遵循Microsoft登入程式。
* **[!UICONTROL 會議確認電子郵件]** — 定義潛在客戶在預約會議後所收到之確認電子郵件的主旨與內文。
* **[!UICONTROL 偏好設定]** — 設定預設會議長度和會議之間的緩衝區。

如果您中斷行事曆的連線：

* 使用中的預訂連結停止運作。
* 預訂頁面會顯示暫時無法使用訊息。
* 當您重新連線時，您的設定會保留。

## 日曆可用性

您在Adobe Marketo Qualifier中的行事曆可用性是根據兩個輸入：

* 您連線的工作行事曆，例如Outlook或Gmail
* **[!UICONTROL 行事曆組態]**&#x200B;中的可用性與時距規則

Marketo Qualifier會從連線的行事曆讀取空閒/忙碌狀態，而非事件詳細資訊。 系統會將此狀態與您的規則結合，決定潛在客戶可以預約的時段。

您可以設定：

* 按星期幾的工作時數
* 每天多個區塊，例如，上午9:00至中午1:00至下午5:00。
* 您的時區
* 會議持續時間
* 在會議之前和之後緩衝
* 最低通知
* 預訂視窗

>[!MORELIKETHIS]
>
>* [傳出工作流程](outbound-workflows.md)
>* [整合](integrations.md)
>* [任務](tasks.md)
