# 🚀 Automate your Airtable → GitHub → Trello workflow in one click!
# Documents Dispatch and Receipt Log


## Airtable → GitHub → Trello Automation Flow
📌Project Introduction:
This project demonstrates how to integrate Airtable’s “Documents Dispatch & Receipt Log” with GitHub Issues and Trello.  

🪄Whenever a record in Airtable is checked:
1. A new GitHub Issue is created automatically.
2. GitHub Actions detect the new Issue and call the Trello API.
3. A new card is created in the “To Do List” column of Trello.
   
🔧Using Tools:
* Airtable Automations
* Github Issue + Github Actions
* Trello API

🚀Demonstration screenshots:

1. Airtable checked records
![Airtable checked record example](images/airtable-demo.png)
2. Trello automatically creates a new card in the TO DO List Column
![Trello new card automatically create example](images/trello-demo.png)
3. Watch Demo Video
[![Watch the video](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)

## Workflow Diagram
The following flow illustrates the automation pipeline across Airtable, GitHub, and Trello.
```mermaid
graph LR
  A[Airtable checked]:::airtable --> B[GitHub creates Issue]:::github
  B --> C[GitHub Actions detect]:::github
  C --> D[Trello creates a new card]:::trello

  classDef airtable fill:#E6F7FF,storke:#1890FF,stoke-width:2px;
  classDef github fill:#FFF3E0,strok:#FB8C00,strok-width:2px;
  classDef trello fill:#E8F5E9,strok:#43a047,strok-width:2px;
``` 
## Features:
1. Secure management of API Keys/Tokens through GitHub Secrets
2. Fully automated process
3. Extensible to other project workflows

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/iodocumentsreceiving-airtable-trello-bridge.git
2. Configure API Keys:
   * Add your Trello API Key and Token in GitHub Secrets.
   * Add your Airtable API Key if needed.
3. Run the automation:
   * Mark a record in Airtable.
   * A GitHub Issue will be created automatically.
   * A new Trello card will appear in the "To Do List" column.

## Future Improvements / TODO
- [ ] **Integrate Slack notification**  
  Enable real-time notifications in Slack channels whenever a new Trello card is created.  
  *Value:* Improves team transparency and communication, making the workflow useful not only for individuals but also for collaborative environments.  
- [ ] **Support Airtable → Notion sync**  
  Extend the integration by sending Airtable records into Notion databases for archiving or further project management.  
  *Value:* Bridges multiple tools often used in modern workspaces, making the workflow more versatile.  
- [ ] **Add unit tests for API calls**  
  Implement automated tests (e.g., with Jest + mocked Trello API) to validate API requests and responses.  
  *Value:* Ensures the reliability and maintainability of the automation, and demonstrates professional software engineering practices.

## Repository Structure
```
├── .github/
│ └── workflows/ # GitHub Actions workflows 
│
├── images/ # Airtable, Trello demo screenshots
│ ├── airtable-demo.png
│ └── trello-demo.png
│
├── README.md 
└── LICENSE (optional) 
```

 ## 中文補充
📌 自動化管理公文紀錄，從 Airtable 到 GitHub，再同步到 Trello！

這個專案示範如何把 Airtable 的【公文收發紀錄表】與 GitHub Issue、Trello 串接，勾選紀錄後系統會自動建立 GitHub Issue，並同步在 Trello 的 To Do List 建立卡片。
未來規劃:
* 未來可讓系統在建立 Trello 卡片時，同步把訊息推送到 Slack 平台，方便團隊即時掌握工作進度。
* 把 Airtable 紀錄同步到 Notion 資料庫，適合需要跨平台管理專案或做長期歸檔。
* 未來可以加上單元測試，讓系統自動檢查 API 呼叫是否正確，提升專案穩定性與專業度。
## 資料庫結構
```
├── .github/
│ └──GitHub 自動化流程設定
│
├── images/ Airtable, Trello 專案截圖
│ ├── airtable-demo.png
│ └── trello-demo.png
│
├── README.md 專案說明文件
└── 授權檔案
```
