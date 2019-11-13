# qs - quick start
快速开始行动, 不必担心环境.

- 立刻创建所需目录结构, 自动安装相关依赖, 并且启动项目甚至打开编辑器.
- 跨平台使用常用工具, 例: ssh, scp.
- 任务存储及管理.

## 选项

- [x] `qs -v --vers` -- 显示版本号
- [x] `qs -h --help` -- 显示帮助信息
- [x] `qs -r --cmdRaw` -- 以字符串形式运行, 避免存储记录时变量、通配符被解析
  - 例: `qs -a -r "ls ./*"` linux 上列出当前目录所有文件, 并保存命令到任务列表中
- [x] `qs --explicit` -- 查找任务时使用精确匹配
- [x] `qs --regexp` -- 查找任务时使用正则匹配(默认)
- [x] `qs --task [kv...]` -- 显示或查找、修改任务
- [x] `qs -a --task-add` -- 添加到任务记录
  - 例: `qs -a echo 123` 保存 `echo 123` 这条记录(及运行目录), 以方便再次运行
- [x] `qs -n --task-name <name>` -- 添加任务时创建任务名称, 包含 -a
- [x] `qs -d --task-des <info>` -- 添加任务记录并创建任务描述, 包含 -a
- [x] `qs -s --task-start <id|name>` -- 启动任务
- [x] `qs -k --task-kill <id|name>` -- 停止任务
- [x] `qs --task-remove <id|name>` -- 删除任务
- [x] `qs --config [k[=v]]` -- 查看、修改配置
- [x] `qs --config-reset` -- 重置配置
- [ ] `qs --node-modules-remove` -- 删除 qs 中的 node_modules
- [ ] `qs --init` -- 初始化 qs, 不包含命令
- [ ] `qs --init-extend` -- 安装 extend 目录中的相关依赖
- [ ] `qs --init-outside` -- 安装 outside 目录中的相关依赖, 可以独立运行的第三方程序, 如 ssh, scp, shx
- [ ] `qs --add <执行器|系统> <name1, name2...>` -- 添加一个功能, 默认为 node 执行器或当前系统, 执行器存在时忽略系统
  -  例: `qs --add python httpie` 则表示 `pip install httpie` 到 qs 的 python 执行器下, 执行器可在配置中添加.
  -  例: `qs --add win32 ssh` 则表示 下载适用于 win32 的 ssh 工具.

提示: 
  - kv: `k` 是显示 `v` 的值, `k=v` 是修改, `k==v` 是查找, `name==xw age=23` 是把 name 为 xw 的数据的 age 修改为 23.
