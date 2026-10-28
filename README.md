# 李老师工作台（静态站）

单文件应用：`index.html` 即工作台本体（3.2MB，全内联，无外部依赖）。

- `index.html` —— 主页面
- `tb.html` —— 与 index.html 相同，供旧书签 `/tb.html` 继续可用
- `404.html` —— 未知路径跳回首页
- `.nojekyll` —— 关闭 Jekyll 处理（必须有）

## 自动部署
GitHub Pages 已开启「Deploy from a branch → main → / (root)」，**推送即自动部署**，无需任何手动操作。

改版：
```bash
cp -f 新源码.html index.html && cp -f 新源码.html tb.html
git add -A && git commit -m "说明改动" && git push origin main
```

## ⚠️ 首次在新域名打开后
Gitee 云同步配置存在浏览器 localStorage（按域名隔离），换域名后需在「同步设置」重新粘贴一次设置码，否则读不到云端数据。

## 安全
本仓库**公开**，但只含程序代码，**不含任何学生数据**。所有数据在 Gitee 私有仓库 `work`。
禁止向本仓库提交任何含学生姓名的文件。
