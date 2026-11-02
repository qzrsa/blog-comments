# blog-comments

这个仓库不存放任何代码，它只是 [quzhongrensan.cn](https://quzhongrensan.cn) 的评论区存储。

站点使用 [giscus](https://giscus.app) 作为评论系统，每条评论就是这里 Discussions 里的一条发言。
之所以单独建一个公开仓库，是因为：

- giscus 要求仓库**必须公开**，否则访客读不到 discussion；
- 站点源码仓库需要保持私有。

把两者分开后，源码私有不影响评论，评论数据也不会随着换部署平台或换博客框架而丢失。

## 说明

- 分类固定为 **Announcements**：只有仓库维护者能手动发帖，giscus bot 仍可在访客首次评论时自动创建 discussion，天然防垃圾。
- 想删评论或管理讨论，直接在 Discussions 里操作即可，站点会实时同步。
- 页面与 discussion 的映射方式是 `pathname`，即以文章路径匹配。
- 站点配置位置：`_config.fomalhaut.yml` 的 `giscus:` 段（repo / repo_id / category_id）。
