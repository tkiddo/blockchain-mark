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
