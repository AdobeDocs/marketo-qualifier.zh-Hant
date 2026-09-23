---
title: '[!DNL Adobe Marketo Qualifier]中的任務'
description: 瞭解如何在[!DNL Adobe Marketo Qualifier]工作佇列中處理手動外展工作，並檢閱代理程式建議的潛在客戶。
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/MbTN1r-ARrW-XYtdIS-KZT7K1Lk-B3GihT8iXL60GrQ'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%
---

# 工作

使用&#x200B;**[!UICONTROL 任務]**&#x200B;完成輸出工作流程產生的動作。 選取工作、執行動作、將工作標示為完成，然後繼續下一個工作而不離開頁面。

在左側導覽列中，移至&#x200B;**[!UICONTROL 活動]** > **[!UICONTROL 任務]**。

![任務面板](assets/tasks.png)

## 任務檢視

此頁面有兩個索引標籤：

* **[!UICONTROL 手動工作]** — 已註冊傳出工作流程的潛在客戶的電話通話、LinkedIn InMails和電子郵件評論。
* **[!UICONTROL 代理程式建議]** — 符合輸出工作流程目標定位准則並建議註冊的潛在客戶。

每個標籤都有自己的篩選器、排序選項和雙面板配置。 工作清單會顯示在左側，而工作面板會顯示在右側。 選擇任務會在工作面板中載入其詳細資訊。 當您完成任務時，系統會自動選取下一個任務。

## 手動任務

### 任務型別

手動任務與出站工作流程步驟相關聯，並有三種型別：

* **[!UICONTROL 電話通話]** — 在節奏達到電話通話步驟時建立。 工作面板會顯示潛在客戶的電話號碼，並會在AI產生呼叫指令碼（可用時）。

* **[!UICONTROL LinkedIn InMail]** — 在順序達到LinkedIn InMail步驟時建立。 工作面板會顯示要從LinkedIn複製和傳送的內容。 展開&#x200B;**[!UICONTROL AI基本原則]**&#x200B;以檢閱基本原則。

* **[!UICONTROL 電子郵件評論]** — 建立於[!DNL Adobe Marketo Qualifier]產生潛在客戶個人化電子郵件之後。 若要在外聯開始前檢閱及核准草稿，請選取&#x200B;**[!UICONTROL 檢閱電子郵件]**。 請參閱[檢閱並調整產生的電子郵件](outbound-workflows.md#review-and-refine-generated-emails)。

![電子郵件評論](assets/tasks-review.png)

### 工作面板

對於&#x200B;**[!UICONTROL 電話]**&#x200B;或&#x200B;**[!UICONTROL LinkedIn InMail]**&#x200B;工作，工作面板包含：

* **[!UICONTROL 潛在客戶]** — 潛在客戶的名稱、電子郵件連結和電話號碼（如果適用）。
* **[!UICONTROL 傳出工作流程]** — 連結的傳出工作流程名稱、到期日和自動略過指標（如適用）。
* **任務內容** — 呼叫指令碼或InMail內容。
* **[!UICONTROL 附註]** — 當您選取其他任務時，附註會自動儲存。 在任務完成、略過或取消之後，您無法編輯附註。

### 產生呼叫指令碼

針對&#x200B;**[!UICONTROL 電話通話]**&#x200B;工作，選取&#x200B;**[!UICONTROL 產生通話指令碼]**。 當產生完成時，請選取&#x200B;**[!UICONTROL 檢視詳細的呼叫指令碼]**。 如果產生失敗，請從面板重試。

### 任務動作

工作面板標題中有兩個動作可供使用：

* **[!UICONTROL 標示完成]** — 在您進行通話、傳送InMail或檢閱電子郵件之後使用此動作。 佇列前進到下一個任務。
* **[!UICONTROL 跳過]** — 當您無法完成步驟，但想要將潛在客戶保留在輸出工作流程中時，請使用此動作。 潛在客戶前進到下一個步調步驟。

如果電話和LinkedInMail工作保持開啟狀態超過設定的臨界值，則可以自動略過這些工作。 自動略過會隨著節奏前進潛在客戶，不會影響排程的電子郵件接觸點。

### 篩選、搜尋和排序

清單上方的工具列可控制要顯示哪些工作以及工作順序。 您的篩選和排序選擇會儲存起來，並在您下次開啟頁面時重新套用。

* **[!UICONTROL 篩選器]** — 開啟篩選器面板：
  * **[!UICONTROL 狀態]**—**[!UICONTROL 目前]**，**[!UICONTROL 近期]**，**[!UICONTROL 過期]**，**[!UICONTROL 已完成]**，**[!UICONTROL 已取消]**，**[!UICONTROL 已略過]**。
  * **[!UICONTROL 工作型別]**—**[!UICONTROL 電子郵件檢閱]**，**[!UICONTROL LinkedIn InMail]**，**[!UICONTROL 電話]**。
  * **[!UICONTROL 到期日期]**。
  * **[!UICONTROL 傳出工作流程]** — 您傳出工作流程的可搜尋清單。
* **[!UICONTROL 排序]** — 依到期日或建立日期排序。 排序順序也會決定佇列前進的順序。
* **[!UICONTROL 搜尋任務]** — 依潛在客戶名稱、公司名稱或出站工作流程尋找任務。 搜尋會套用作用中的篩選器。

作用中的濾鏡在工具列下方會顯示為晶片。 若要重設，請選取&#x200B;**[!UICONTROL 全部清除]**。

### 任務狀態

每個任務會顯示其目前狀態：

| 狀態 | 說明 |
| --- | --- |
| **[!UICONTROL 目前]** | 現在到期，已準備好採取行動。 目前任務未顯示徽章。 |
| **[!UICONTROL 即將推出]** | 前述步驟已完成，但到期日期為未來日期。 如果時機正確，您可以及早採取行動。 |
| **[!UICONTROL 過期]** | 已超過到期日但尚未完成。 任務已標幟以引起注意。 |
| **[!UICONTROL 已完成]** | 您已完成動作並將工作標示為完成。 |
| **[!UICONTROL 已略過]** | 您已略過該步驟，或該步驟已自動略過。 潛在客戶在「出站工作流程」中前進。 |
| **[!UICONTROL 已取消]** | 由於外站工作流程變更，系統已取消工作。 |

已完成、已略過和已取消的任務為最終任務。 他們的動作不再可用，其附註為唯讀。

## 代理程式建議

**[!UICONTROL 代理程式建議]**&#x200B;索引標籤會列出符合輸出工作流程目標定位准則且建議註冊的潛在客戶。 若要開啟建議，請參閱[輸出工作流程](outbound-workflows.md)。

若要在工作面板中檢閱建議，請選取建議：

* 使用間隔徽章將每個建議標示為&#x200B;**[!UICONTROL 新的]**&#x200B;或&#x200B;**[!UICONTROL 先前的]**。
* **[!UICONTROL 建議的潛在客戶]**&#x200B;或&#x200B;**[!UICONTROL 建議的連絡人]**&#x200B;資料表列出建議的潛在客戶，其資料行包括&#x200B;**[!UICONTROL 名稱]**、**[!UICONTROL 標題]**、**[!UICONTROL 帳戶]**、**[!UICONTROL 狀態]**、**[!UICONTROL 電子郵件]**&#x200B;和&#x200B;**[!UICONTROL 上次更新時間]**。

有兩個動作可供使用：

* **[!UICONTROL 檢閱潛在客戶]** — 開啟[外站工作流程]以檢閱及註冊建議的潛在客戶。 檢視[新增潛在客戶並開始產生電子郵件](outbound-workflows.md#step-5-add-prospects-and-start-email-generation)。
* **[!UICONTROL 標示為完成]** — 在您檢閱建議後將其關閉。

**[!UICONTROL 代理程式建議]**&#x200B;索引標籤包含&#x200B;**[!UICONTROL 目前]**、**[!UICONTROL 已完成]**&#x200B;和&#x200B;**[!UICONTROL 已取消]**&#x200B;狀態篩選器、傳出工作流程篩選器，以及依建立日期排序。

### 使用代理商建議回覆潛在客戶

潛在客戶回覆電子郵件時，[!DNL Marketo Qualifier]可以草擬執行緒內回應，並將其新增為&#x200B;**[!UICONTROL 代理程式建議]**&#x200B;下的工作。 草稿使用來自下列專案的相關前後關聯：

* 完整的電子郵件執行緒，而不僅僅是最新的訊息。
* 您的知識中心附屬資料和產品研究。
* 帳戶訊號，例如最近的新聞、行銷參與和CRM活動。
* 您儲存的[電子郵件起草內容](profile-settings.md#email-drafting-context)。

助理會根據潛在客戶的意圖調整回應。 例如，它可以透過您的預約連結提供會議要求的時間、在潛在客戶感興趣時強化價值、從您的附屬資料中回答產品問題、共用相關資產、以一個差異化因素處理異議，或在潛在客戶想要延遲時使用低壓回應。

有關定價、法律或安全性要求、惡意回應以及不明確請求的訊息，仍會保留給代表以個人回應。

1. 開啟回復建議，並檢閱完整對話串和草擬的回覆。
1. 若要建立另一個草稿，請編輯回應，或選取&#x200B;**[!UICONTROL 使用AI產生]**。
1. 若要傳送回應並繼續潛在客戶的輸出工作流程，請選取&#x200B;**[!UICONTROL 核准並傳送]**。

## 從傳出工作流程完成任務

在輸出工作流程的&#x200B;**[!UICONTROL 參與的潛在客戶]**&#x200B;檢視上，手動接觸點提供相同的&#x200B;**[!UICONTROL 標籤為完成]**、**[!UICONTROL 跳過]**&#x200B;和附註選項。 在那裡完成一項任務也會更新其在&#x200B;**[!UICONTROL 任務]**&#x200B;頁面上的狀態。 請參閱[輸出工作流程](outbound-workflows.md)。

## 空白狀態

* 當您沒有任務可執行時，清單會顯示&#x200B;_您今天已全部完成_&#x200B;訊息。
* 當篩選器沒有符合任務時，清單會報告沒有符合您篩選器的任務。
* 未選取任何任務時，工作面板會提示您選取任務。 若要檢視其詳細資訊，請選取工作。

>[!MORELIKETHIS]
>
>* [傳出工作流程](outbound-workflows.md)
>* [傳出效能](performance.md)
>* [潛在客戶](prospects.md)
