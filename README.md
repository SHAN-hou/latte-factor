# 拿铁因子 · Latte Factor

最小又最强的致富习惯——基于大卫·巴哈《拿铁因子》一书做的互动式 Web App + Android 原生 App。

## 功能（严格按书中 5 步逻辑）
1. **找出你的拿铁因子** — 勾选每日小额支出
2. **看复利** — 30 年定投资产推演图
3. **先付钱给自己** — 收入比例计算 30 年终值
4. **让它自动化** — 三账户资金流可视化
5. **梦想账户** — 把梦想换算成"每天多少钱"

## 在线访问（PWA）
打开网页 → 浏览器菜单"添加到主屏幕" → 像 App 一样使用，支持离线。

## 安卓 APK 下载
每次推送到 `main` 后，GitHub Actions 自动编译：
- **Releases 页**下载最新 `latte-factor-debug.apk`
- 或在 Actions → 最近一次运行 → Artifacts 下载

## 本地开发
```bash
# 跑网页
npx serve www

# 打包 Android（需 Android Studio + JDK 21）
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
```

## 技术栈
- 静态 HTML + TailwindCSS + Chart.js（无构建）
- Capacitor 6 包装为原生 Android
- GitHub Actions 自动 CI 构建 APK

## 致谢
内容基于：David Bach & John David Mann《The Latte Factor》（《拿铁因子：最小又最強的致富習慣》）
