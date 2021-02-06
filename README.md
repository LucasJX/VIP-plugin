# API
- <kbd>forward void</kbd> VIP_OnKeyExchange
    - 说明：当玩家兑换VIP卡密成功时调用
    - <kbd>client</kbd> client index.
    - <kbd>key</kbd> vip key.
    - <kbd>days</kbd> key days.
- <kbd>forward void</kbd> VIP_OnClientPutInServer
    - 说明：当玩家进入服务器，且读取完用户VIP数据时调用
    - <kbd>client</kbd> client index.
    - <kbd>State</kbd> client vip state.
- <kbd>forward void</kbd> VIP_OnClientStateChanged
    - 说明：当玩家的VIP状态改变时调用
    - <kbd>client</kbd> client index.
    - <kbd>State</kbd> client vip state.
- <kbd>native void</kbd> VIP_Message
    - 说明：向指定玩家发送信息，会自动带上VIP前缀
    - <kbd>client</kbd> client index.
    - <kbd>text</kbd> Format message.
- <kbd>native void</kbd> VIP_MessageToAll
    - 说明：向所有玩家发送信息，会自动带上VIP前缀
    - <kbd>text</kbd> Format message.
- <kbd>native bool</kbd> VIP_IsVIP
    - 说明：判断玩家是否为VIP，是则返回true，不是则返回false
    - <kbd>client</kbd> client index.
- <kbd>native int</kbd> VIP_GetClientDays
    - 说明：返回玩家的VIP剩余天数，若玩家不是VIP或不是一个有效的玩家则返回-1
    - <kbd>client</kbd> client index.
- <kbd>native bool</kbd> VIP_SetClientDays
    - 说明：设置玩家的VIP剩余天数，若用户未拥有VIP则自动注册用户信息
    - <kbd>client</kbd> client index.
    - <kbd>days</kbd> vip days.
- <kbd>native bool</kbd> VIP_SetClientState
    - 说明：设置玩家的VIP状态
    - <kbd>client</kbd> client index.
    - <kbd>state</kbd> vip state.
- <kbd>native VIPState</kbd> VIP_GetClientState
    - 说明：获取玩家的VIP状态
    - <kbd>client</kbd> client index.
# 更新日志
- 2021-2-6 22:30
    - 新增vip_flag插件，会自动令管理员拥有年VIP
    - 新增API
    - 新增年VIP判断
    - 修改了数据库中vipUsers的结构
    - 修复了BUG
- 2021-1-30 21:52
    - 修改自动更新地址
- 2021-1-30 20:34
    - 修改了VIP时长限制，可自定义限制时长，踢出信息
    - 新增仅VIP可进入的插件
    - 修复自动更新bug
- 2021-1-23 13:20
    - 修复了颜色代码不生效的bug
- 2021-1-22 21:00
    - 版本变更为1.6.1
    - 新增自动更新（测试），需要安装updater插件
- 2021-1-22 17:00
    - 跳过1.5版本，来到1.6版本
    - VIP功能模块化
    - 优化了VIP系统
    - 新增VIP时长限制（目前锁定200小时，后续会出自定义，可自己更改源码编译，需要system2扩展）
    - 修复了一些bug
    - 新增api
- 2020-12-13 0:35
    - 修复了聊天前缀以及聊天中所有颜色不保存的bug
    - 修复了数据库不保存聊天中所有颜色的bug *原显示乱码*
- 2020-12-11 23:10
    - 更新了断开连接时的提示
    - 更新了自定义前缀
    - 更新了伤害提示
    - 新增api
    - 修复了玩家不是vip但仍然会显示进服提示的bug
# 即将完成
- VIP专属等级图标自定义
- VIP时长限制更改
- 计划移除chat-processor插件
