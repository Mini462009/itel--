# iTEL 投诉系统

一个静态投诉系统示例，支持：

- 手机号码注册 / 登录
- 自动生成用户名（`user000001`），`6000000` 特殊账号显示 `iTEL Customer Service（客服）`
- 留言提交与本地保存（`localStorage`）
- 嵌套回复功能
- 中英语言显示支持
- 本地演示服务器启动脚本 `demo.py`

> 注意：所有留言和回复都保存在浏览器本地存储中，不会存到服务器。登录状态使用 `sessionStorage` 保存，浏览器会话结束后可能失效。

## 文件说明

- `rp/index.html`：登录 / 注册页面
- `rp/home.html`：投诉留言页面
- `rp/demo.py`：本地静态服务器，用于测试

## 本地运行

双击运行 `rp\start_server.bat`，或命令行执行：

```bash
cd e:\html\rp
python demo.py
```

然后在浏览器中打开：

- 本机访问： `http://127.0.0.1:8000/index.html`
- 局域网访问：`http://192.168.1.45:8000/index.html`

如果你想让同一局域网里的其它设备访问，就用上面的局域网地址。

## GitHub 上传建议

1. 初始化仓库：
   ```bash
git init
```
2. 添加文件：
   ```bash
git add README.md index.html home.html demo.py
```
3. 提交：
   ```bash
git commit -m "Add iTEL complaint system demo"
```
4. 添加远程仓库并推送：
   ```bash
git remote add origin <your-github-repo-url>
git push -u origin main
```

## 部署到 GitHub Pages

如果你想把这个项目直接托管在 GitHub Pages：

1. 在仓库设置里启用 GitHub Pages，选择 `main` 分支或 `gh-pages` 分支，根目录即可。
2. 上传 `index.html`, `home.html`, `logo.jpg`, `demo.py`（可选）以及 `README.md`。
3. 访问生成的网址，例如 `https://<your-user>.github.io/<repo-name>/rp/index.html`。

> 由于这是纯静态页面，数据只会保存在访问者本地浏览器中，不会跨浏览器或跨设备同步。
