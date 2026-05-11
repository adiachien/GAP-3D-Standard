# GAP 3D 作業知識庫

## 部署步驟

### Step 1 — Supabase 建表
1. 登入 Supabase → 進入你的 project
2. 左側選 **SQL Editor**
3. 把 `supabase_schema.sql` 的內容全部貼上 → 點 **Run**
4. 確認左側 Table Editor 出現 `sections`、`entries`、`checklist_items` 三張表

### Step 2 — 建立 Supabase 帳號（用來登入後台）
1. Supabase → Authentication → Users
2. 點 **Invite user** → 輸入你的 email
3. 去 email 收確認信，設定密碼
4. 之後用這組帳密登入 `admin.html`

### Step 3 — GitHub 建 Repo
1. GitHub 新建一個 repo（例如 `gap-3d-wiki`）
2. 把這個資料夾的所有檔案 push 上去

```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/你的帳號/gap-3d-wiki.git
git push -u origin main
```

### Step 4 — Vercel 部署
1. 登入 Vercel → **Add New Project**
2. Import 你剛建的 GitHub repo
3. Framework Preset 選 **Other**
4. 直接點 **Deploy**
5. 完成後會給你一個網址，例如 `https://gap-3d-wiki.vercel.app`

---

## 使用方式

### 同事看
直接開網址，左側選分類，右上角可以搜尋

### 你編輯
1. 進入 `網址/admin.html`
2. 用 Supabase 帳號登入
3. 選分類 → 新增/編輯條目
4. 儲存後主頁面馬上更新

### 每季更新
只需要進後台新增或修改有變動的條目，其他的維持不動

---

## 檔案說明
| 檔案 | 說明 |
|------|------|
| `index.html` | 主介面（同事瀏覽用） |
| `admin.html` | 編輯後台（你填表用） |
| `vercel.json` | Vercel 部署設定 |
| `supabase_schema.sql` | 資料庫建表 SQL |
