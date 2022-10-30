# blockchain-mark

区块链笔记

学习资源

1. B 站肖臻区块链教程
2. 《精通以太坊》
3. 《零基础学区块链》

## Day 1

密码学基础

- 哈希算法

哈希碰撞：对于两个不同的输入，进过哈希计算后得到同样的输出，则改哈希算法存在哈希碰撞。

- 加密方式：

1. 对称加密：加密和解密用同样的密钥

2. 非对称加密（公钥加密 Public-key cryptography）：加密和解密用不同密钥。

非对称加密举例： 小明在本地生成一对公私钥，把公钥发给小红，小红用公钥把信息加密后发给小明，小明收到信息后用自己的私钥解密。

签名：小明用自己的私钥给信息签名，发送给小红后，小红用私钥验证信息来自小明。

## Day 2

solidity 是以太坊虚拟机智能合约的编程语言
[solidity 文档](https://solidity-cn.readthedocs.io/zh/develop/introduction-to-smart-contracts.html)

solidity 开发 IDE 使用[remix](https://remix.ethereum.org/#optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.7+commit.e28d00a7.js)

solidity 语言注意：

1.  软件许可：第一行注释软件许可，不写会警告，但可以运行。

2.  版本：声明源文件使用的 solidit 版本，不同版本语法差别较大。

3.  语句分号结尾。

## Day 3

solidity 数值类型：布尔 bool，有符号整数 int，无符号整数 uint，256 位整数 uint256，字节数组 bytes（定长和不定长），地址类型 address，枚举值 enum

以太坊安全知识：

重入攻击：the DAO 被盗事件。

## Day 4

solidity 函数：

可见性：

`external`: 只能外部调用
`internal`: 只能内部调用，包括子合约
`public`: 内部外部均可见
`private`: 内部调用，不包括子合约

合约状态相关：

`view`: 可以查看合约状态，不能修改
`pure`: 对合约状态不能看也不能修改
`payable`:可支付

## Day 5

[崔棉大师 solidity 教程](https://space.bilibili.com/286084162/channel/collectiondetail?sid=296410)

变量默认值，循环语句（和 javascript 类似）

## Day 6

vscode remix 插件使用。

1. command+shift+P 唤起命令窗口，找到 remix compile with solidity extension 执行编译

2. 打开插件，点击 run and deploy，然后连接到 remix，需要点开浏览器并 connect to localhost

## Day 7

[remix 本地化部署](https://learnblockchain.cn/article/3426)

```
docker run -p 8080:80 remixproject/remix-ide:latest
remixd -s ./ --remix-ide http://localhost:8080
```
