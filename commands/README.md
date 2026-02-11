# SuperCaseCompany Commands

快速存取 CEO 和各維度總監的指令集。

## 可用指令

| 指令 | 角色 | 維度 | 團隊規模 |
|------|------|------|----------|
| `/scc-ceo` | CEO (Chief Executive Officer) | 總調度 | 7 維度, 50+ 專家 |
| `/scc-req` | Requirements Director | 需求探索與市場情報 | 6 specialists |
| `/scc-sales` | Sales Director | 業務與供應鏈 | 3 specialists |
| `/scc-design` | Design Director | Mock 系統設計與開發 | 10 specialists |
| `/scc-tech` | Tech Director | 系統開發與雲端基礎設施 | 5 specialists |
| `/scc-ops` | Operations Director | 營運管理與支援 | 8 specialists |
| `/scc-innovation` | Innovation Director | 學習、發展與創新 | 3 specialists |
| `/scc-industry` | Industry Consulting Director | 產業專家與採購 | 7 specialists |

---

## 使用方式

### 安裝 Commands

#### 方法 1: Symlink（推薦）

```bash
# 建立 symlink 到 ~/.claude/commands/
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-* ~/.claude/commands/

# 或逐個建立
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-ceo ~/.claude/commands/scc-ceo
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-req ~/.claude/commands/scc-req
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-sales ~/.claude/commands/scc-sales
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-design ~/.claude/commands/scc-design
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-tech ~/.claude/commands/scc-tech
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-ops ~/.claude/commands/scc-ops
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-innovation ~/.claude/commands/scc-innovation
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-industry ~/.claude/commands/scc-industry
```

#### 方法 2: 複製

```bash
# 複製所有 commands
cp ~/DEV/claude-teams/SuperCaseCompany/commands/scc-* ~/.claude/commands/
```

### 驗證安裝

```bash
# 列出所有 SuperCaseCompany commands
ls -la ~/.claude/commands/scc-*
```

---

## 使用場景

### 場景 1: 啟動專案 - 找 CEO

```bash
# 在任何專案目錄中
/scc-ceo
```

然後說：
```
我需要為一家連鎖餐廳開發排班系統，支援多店管理、勞基法合規、技能配對。
```

CEO 會：
1. 分析需求（產銷人發財框架）
2. 組建虛擬團隊（Requirements Director, Restaurant Expert, Tech Director, Legal Expert）
3. 指派虛擬團隊 lead
4. 設定專案目標與時程

---

### 場景 2: 需求探索階段 - 找 Requirements Director

```bash
/scc-req
```

適用於：
- 釐清客戶需求
- 進行市場研究
- SEO 策略規劃
- 建立需求可追溯性

---

### 場景 3: 技術開發 - 找 Tech Director

```bash
/scc-tech
```

適用於：
- 技術架構設計
- Claude API 整合（參考 Anthropic 官方 repos）
- 雲端部署規劃
- 程式碼審查與品質把關

範例對話：
```
我需要整合 Claude API 實作客服聊天機器人，支援串流回應和工具呼叫。
```

Tech Director 會：
1. 參考 `/anthropic-sdk-reference` skill
2. 推薦使用 anthropic-sdk-typescript (前端) + anthropic-sdk-python (後端)
3. 提供 streaming 和 tool use 實作模式
4. 協調 Software Engineer 和 QA Expert

---

### 場景 4: 產業專業諮詢 - 找 Industry Consulting Director

```bash
/scc-industry
```

適用於：
- 餐飲業排班系統
- 咖啡店原料採購
- 冷鏈物流監控
- 連鎖店管理系統

範例對話：
```
客戶是咖啡店，需要協助採購哥倫比亞單品豆，並設計生豆庫存管理系統。
```

Industry Consulting Director 會：
1. 指派 Coffee Shop Expert（咖啡專業）
2. 指派 Procurement Expert（供應商搜尋、成本分析）
3. 提供產業最佳實踐
4. 確保符合食品安全法規

---

### 場景 5: 設計審核 - 找 Design Director

```bash
/scc-design
```

適用於：
- UI/UX 設計
- Mock 系統開發
- 設計系統建立
- 技術架構（前後端）

---

### 場景 6: 營運支援 - 找 Operations Director

```bash
/scc-ops
```

適用於：
- 財務規劃與預算
- 法律合規（台灣法規）
- 人力資源管理
- 客戶服務策略

---

### 場景 7: 培訓與創新 - 找 Innovation Director

```bash
/scc-innovation
```

適用於：
- 團隊 Claude API 培訓
- 技術能力提升
- 創新專案 POC
- AI 整合諮詢

---

### 場景 8: 業務開發 - 找 Sales Director

```bash
/scc-sales
```

適用於：
- 銷售提案
- 客戶關係管理
- 供應鏈規劃
- 倉儲與庫存

---

## 指令執行流程

### Step 1: 呼叫指令
```bash
/scc-ceo
```

### Step 2: 載入角色 Context
系統會載入該角色的：
- 核心職責
- 團隊組成
- 可用技能
- 協作協定

### Step 3: 開始互動
直接描述你的需求：
```
我需要...
```

### Step 4: 角色回應
角色會根據職責：
- 分析需求
- 推薦方案
- 組建團隊（如 CEO）
- 提供專業建議

---

## 整合工作流程

### 完整專案流程

```
1. /scc-ceo
   └─ 分析專案，組建虛擬團隊

2. /scc-req
   └─ 需求探索與市場研究

3. /scc-design
   └─ UI/UX 設計與 Mock 開發

4. /scc-tech
   └─ 系統開發與部署

5. /scc-ops
   └─ 營運支援與合規

6. /scc-ceo
   └─ 最終交付與專案總結
```

### 特定領域流程

**餐飲業系統開發**：
```
/scc-industry (餐飲專家)
  → 確認產業需求與法規

/scc-req (需求分析)
  → 建立需求規格

/scc-design (設計)
  → UI/UX 符合餐飲業操作流程

/scc-tech (開發)
  → 系統實作與整合 POS

/scc-ops (法務)
  → 確保勞基法合規
```

---

## 快速參考

| 需求類型 | 推薦指令 | 說明 |
|---------|---------|------|
| 專案啟動 | `/scc-ceo` | 組建虛擬團隊 |
| 需求釐清 | `/scc-req` | 需求探索與分析 |
| 市場研究 | `/scc-req` | 競品分析、SEO |
| 系統設計 | `/scc-design` | UI/UX、架構 |
| API 整合 | `/scc-tech` | Claude API、後端開發 |
| 雲端部署 | `/scc-tech` | GCP, Azure, AWS |
| 產業諮詢 | `/scc-industry` | 餐飲、零售、物流 |
| 採購管理 | `/scc-industry` | 供應商、進口、成本 |
| 法律合規 | `/scc-ops` | 台灣法規、合約 |
| 財務規劃 | `/scc-ops` | 預算、投資 |
| AI 培訓 | `/scc-innovation` | Claude API 教學 |
| 業務提案 | `/scc-sales` | 銷售、客戶關係 |

---

## 進階技巧

### Technique 1: 組合使用

```bash
# 先找產業專家確認需求
/scc-industry
「咖啡店需要排班系統」

# 再找技術團隊開發
/scc-tech
「根據咖啡店專家的需求，設計排班系統架構」
```

### Technique 2: 持續對話

同一個 command 可以持續對話：
```bash
/scc-ceo

You: 我需要電商網站
CEO: [分析需求，組建團隊]

You: 預算有限，優先 MVP
CEO: [調整方案，建議階段性開發]

You: 第一階段需要哪些功能？
CEO: [列出 MVP 功能清單]
```

### Technique 3: 跨維度協作

```bash
# 先找設計
/scc-design
「設計電商網站 UI」

# 再找技術
/scc-tech
「實作剛才的設計」

# 最後找營運
/scc-ops
「設定金流與法律合規」
```

---

## 疑難排解

### Q: Command 找不到？
```bash
# 檢查 symlink
ls -la ~/.claude/commands/scc-*

# 重新建立 symlink
ln -s ~/DEV/claude-teams/SuperCaseCompany/commands/scc-* ~/.claude/commands/
```

### Q: 不確定找哪個維度？
**永遠先找 CEO (`/scc-ceo`)**，CEO 會幫你組建正確的虛擬團隊。

### Q: 需要多個維度協作？
找 CEO 說明需求，CEO 會組建跨維度虛擬團隊。

---

## 更多資訊

- **團隊完整說明**：查看 `~/DEV/claude-teams/SuperCaseCompany/README.md`
- **CLAUDE.md**：查看 `~/DEV/claude-teams/SuperCaseCompany/CLAUDE.md`
- **GitHub**：https://github.com/pin0513/SuperCaseCompany

---

**SuperCaseCompany Commands - 快速存取你的專業顧問團隊** 🚀
