### 🆕 New Features
  * none

### 🛠️ Bug Fixes
  * 修复天气预警 `id` 的 UUID 解码形态，确保解码后与业务侧期望（字符串）一致。

### 🔣 Dependencies
  * none

### ‼️ Breaking Changes
  * none

### 🔄 Other Changes
  * 统一 `news.placements.articles.alertIds` 的 UUID 表达形态：编码支持 `{ bytes: [...] }` 输入，解码统一输出字符串 UUID，减少上下游结构差异。
  * 增加 `placementType()` 的内部比较能力，用于更稳定地处理 news placements 的 `placement` 字段判定。
  * 调整响应处理顺序（`refactor(response)`），进一步收敛逻辑执行路径，降低后续维护复杂度。
  * 更新子模块引用到最新提交，确保主仓库与依赖子项目的版本关系保持一致。
  * 新增并完善 UUID 映射测试脚本，覆盖多组 `uuid <-> bytes` 双向转换及 FlatBuffer round-trip 校验。
