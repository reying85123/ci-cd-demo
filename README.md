# Github Action 部署到 Google Cloud Platform Compute Engine

1. 產生SSH金鑰,儲存於當前路徑,不設定金要密碼
```bash
ssh-keygen -t rsa -b 4096 -C "ci-cd-deploy-key" -f ./gce_ci_cd_key
```

2. 將公鑰複製到gcp vm,使用者帳號authorized_keys,路徑 /home/USER/.ssh/authorized_keys

3. Github Action專案內 setting Actions secrets and variables, 設置以下參數
<br />
GCE_HOST=主機的公網IP
<br />
GCE_USERNAME=主機的使用者名稱
<br />
GCE_SSH_PRIVATE_KEY=私鑰內容

4. 建立.github/workflows/deploy.yml部署流程, 範例參考專案內github-action-example/deploy.yml

5. 將更新推送至production分支,Github Action觸發自動部署到伺服器




