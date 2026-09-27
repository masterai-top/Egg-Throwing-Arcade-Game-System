[简体中文](README.md) | [繁體中文](README.zh-TW.md) | [English](README.en.md)

# 摜蛋遊戲原始碼：C++ / Cocos2d-x 客戶端與連線大廳模組

本專案聚焦 **摜蛋原始碼、摜蛋遊戲原始碼、摜蛋牌類客戶端、Guandan game source code**。公開檔案包含客戶端生命週期、斷線重連、使用者與頭像道具、兌換資料、視覺效果及部分通訊結構；真實畫面展示大廳、四人牌桌與結算流程。

> 本倉庫是可核驗的客戶端程式片段與產品資料，不代表開箱即用的完整伺服器、規則引擎或營運後台。

## 產品功能與玩法

- 大廳提供不同房間入口、快速開始與幫助功能。
- 四名玩家分成兩隊，對家為隊友，使用兩副牌進行合作競技。
- 常見牌型包含單張、對子、三張、三帶二、順子、連對、鋼板與炸彈。
- 標準流程為：大廳、房間、入座、發牌、輪流出牌、結算與升級。
- 公開程式可核驗斷線恢復、帳號切換、頭像選擇、震動/漣漪效果與資料工具。

## 真實產品畫面

| 大廳 | 四人牌桌 |
|---|---|
| ![摜蛋遊戲大廳](docs/assets/images/guandan-lobby.png) | ![摜蛋四人牌桌](docs/assets/images/guandan-table.png) |
| ![摜蛋品牌畫面](docs/assets/images/guandan-brand.png) | ![摜蛋結算畫面](docs/assets/images/guandan-result.png) |

## 技術內容

`AppDelegate.*` 負責 Cocos2d-x 應用啟動與前後台生命週期；`BreakLineReconnectionHint.*` 處理重新連線提示；`ClientData.*` 和 `ClientServerMsg.h` 保存客戶端狀態與訊息結構；其餘模組涵蓋頭像、帳號、兌換資料、Base64/MD5 和視覺效果。

完整建置仍需補齊倉庫外的引擎、UI、場景、網路、伺服器和美術資源，並完成測試、素材授權與法規審查。

## 線上文件

- [繁體中文](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/zh-tw/)
- [简体中文](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/zh-cn/)
- [English](https://masterai-top.github.io/Egg-Throwing-Arcade-Game-System/en/)

