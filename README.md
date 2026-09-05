# framework-zh_CN

framework 的简体中文本地化组件。通过 `LocalizedMessage` / `LocalizedEntityField` 覆盖 framework 文案与枚举，不改 framework 源码。

## 约定

- locale 统一为 `zh_CN`（与 Java `Locale.toString()` 一致）。
- 不要覆盖 `EmailTemplate`、`ScreenTheme` 等英文种子记录本身，只用 LocalizedEntityField。
- Uom、货币、中国省/市/县随默认 `./gradlew load`（seed / seed-initial）载入。
- 中国地级、县级区划来自民政部《2024年中华人民共和国县以上行政区划代码》（https://www.mca.gov.cn/mzsj/xzqh/2025/202401xzqh.html）。`./gradlew load` 会新增/更新记录；已废止代码（如原密云县 `CHN_110228`）不会自动删除，需清库后重载或手工清理。
