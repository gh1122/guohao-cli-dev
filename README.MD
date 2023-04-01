# lerna 基于 git 和 npm 的多 packjson 的项目管理工具

# 初始化流程

1. 初始化 npm 项目 npm init -y
2. 安装 lerna yarn add lerna -D
3. 初始化 lerna 项目 lerna init
   -- 会初始化一个没有关联线上地址的 git 仓库
   -- 增加一个 lerna.json
4. 增加包项目 lerna create XXX
5. 安装依赖 lerna add XXX
   -- 指定目录安装依赖 lerna add XXX packages/core/
6. 清理依赖包 lerna clean
7. 重新安装依赖 lerna bootstrap
8. lerna link
   -- 可以给 package 下面相互依赖的包，进行软连接

# 开发和测试

1. lerna exec 执行一些脚本
2. lerna run 执行每个 packages 下面的 npm 脚本
   -- lerna run --scope 包名(@guohao-dev-cli/utils) build

# 发布流程

1. lerna version 增加版本号
2. lerna changed 查看上版本以来所有的变更
3. lerna diff 针对 git commit 之间的比较
4. lerna publish
