# bilibili-upload-organizer

用于在 Codex 中查询或管理 B 站创作中心的视频稿件和合集，也可根据自己的系列风格拟写标题、简介和标签。技能需要能操作网页的 Codex 环境。实际操作后台时，请先在受支持的浏览器中登录自己的 B 站账号。拟写文案可离线完成。

## 安装

将此仓库下载或克隆到个人 Codex 技能目录，使 `bilibili-upload-organizer/SKILL.md` 与 `references/` 一起保留。Windows PowerShell 示例：

```powershell
$skills = if ($env:CODEX_HOME) {
    Join-Path $env:CODEX_HOME 'skills'
} else {
    Join-Path $env:USERPROFILE '.codex\skills'
}
git clone https://github.com/li-zhaojun-george/bilibili-upload-organizer.git (Join-Path $skills 'bilibili-upload-organizer')
```

已有同名目录时，请先核实来源并保留自己的改动。安装后用 `$bilibili-upload-organizer` 调用。

## 最小示例

> 使用 $bilibili-upload-organizer 查看「我的示例合集」的前 3 集和当前顺序，只查询。

预期结果是找到目标合集、列出前三集，然后退出编辑界面。没有登录或有多个同名合集时，先确认账号和目标。要求调整顺序或定时时间时，技能会在提交后重新打开目标复核。

已实测已有定时稿的时间修改和普通合集排序。首次上传、草稿保存和完整发布流程以当时的页面提示为准。技能文件不包含脚本或遥测功能。上传素材和提交修改由用户授权后通过创作中心执行，相关权限和费用由平台决定。

卸载时移除本技能目录即可。B 站上的稿件及已保存变更仍由创作中心管理。反馈问题时请隐藏账号凭据、未公开稿件、素材和个人路径。
