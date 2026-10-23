# LemonTea

## 版本

适用于 Minecraft Java Edition 1.21.1。

| 内容 | 目录 | pack_format |
| --- | --- | --- |
| LemonTea v0.17 数据包 | LemonTea | 48 |
| LemonYellow v0.1 资源包 | LemonYellow | 34 |

LemonTea 包含 88 个配方、14 个进度、14 个函数和 11 个战利品表，提供附魔书合成、五行元素压缩与分解、气元素合成与切石机转换。

## 安装

1. 把 LemonTea-v0.17-MC1.21.1.zip 放进存档的 datapacks 文件夹，保留 ZIP 格式。
2. 进入世界后执行 /reload；已有世界也可以退出后重新进入。
3. 执行 /datapack list enabled，确认列表包含 LemonTea。
4. 把 LemonYellow-v0.1-MC1.21.1.zip 放进游戏的 resourcepacks 文件夹，在选项的资源包界面启用，以显示自定义物品的名称、说明和贴图。

macOS 官方启动器默认游戏目录为 ~/Library/Application Support/minecraft。其他启动器使用其对应实例的游戏目录。

新建世界时，也可以在数据包选择界面直接拖入数据包 ZIP。

## 合成示例

- 工作台中放置九个熔炉，得到一个土元素；把土元素放入合成栏并取出结果，得到九个熔炉。
- 工作台中放置金、木、水、火、土元素各一个，得到一个气元素。
- 在切石机中放入气元素，选择对应元素并取出结果，得到五个对应元素。
- 工作台中放置一本书和五颗钻石，得到锋利 V 附魔书。

元素转换使用合成进度发放真实产物，并清理配方产生的指示物。

## 1.21.1 适配

- 数据目录使用 advancement、function、loot_table、recipe。
- 进度中的物品类型使用 items 字段。
- 自定义元素标识使用 predicates 下的 minecraft:custom_data 进行部分匹配，允许物品携带额外自定义数据。
- 更新数据包与资源包版本声明。

## 验证

使用 Mojang 官方 1.21.1 服务端加载并执行 /reload，确认全部配方、进度、函数和战利品表可加载。

通过客户端真实取出合成与切石机结果，再读取服务端背包数据验证：五种元素分解、重复分解、气元素还原、五种元素合成气元素、五种切石机转换、指示物清理、普通附魔书不会误发元素、附魔书合成。

ZIP 根目录直接包含 pack.mcmeta，数据包包含 data，资源包包含 assets。
