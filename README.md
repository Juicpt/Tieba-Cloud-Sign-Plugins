# Tieba-Cloud-Sign-Plugins

## 插件列表
### 云封禁
吧务专用，可循环封禁指定账号

**1.1版不支持直接覆盖文件更新，需要卸载重装后重新导入封禁列表，卸载会清空列表，请谨慎执行**

### 云知道抽奖
自动完成知道抽奖，每日

### 云回贴
强大的自定义回帖功能

### 名人堂
自动刷名人堂

更新1.1版后请执行，其中 `tc_` 是默认表名前缀，如有过修改请自行修改表名前缀

```sql
ALTER TABLE `tc_ver4_ban_list` CONVERT TO CHARACTER SET `utf8mb4` COLLATE `utf8mb4_general_ci`;
ALTER TABLE `tc_ver4_rank_list`
CHANGE `nid` `nid` varchar(15) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `fid`,
CHANGE `name` `name` varchar(255) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `nid`,
CHANGE `tieba` `tieba` varchar(255) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `name`;
ALTER TABLE `tc_ver4_ban_userset` CONVERT TO CHARACTER SET `utf8mb4` COLLATE `utf8mb4_general_ci`;
ALTER TABLE `tc_ver4_rank_list`
CHANGE `nid` `nid` varchar(15) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `fid`,
CHANGE `name` `name` varchar(255) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `nid`,
CHANGE `tieba` `tieba` varchar(255) COLLATE 'utf8mb4_general_ci' NOT NULL AFTER `name`;
```

### 自动刷新贴吧列表
完全自动每日刷新贴吧列表

### 贴吧云审查
吧务专用，审查贴吧内不符合规范的帖子

### 云签AmazeUI
云签的一款UI产品

### 知道文库签到
自动签到百度知道，文库已废
