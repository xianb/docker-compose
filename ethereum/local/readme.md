// 查看当前用户，返回值为一个数组
eth.accounts 

// 创建一个新的用户
personal.newAccount('密码123456') 

// 把数组的第一个值赋予user1
user1 = eth.accounts[0]

// 查询这个账户的余额
eth.getBalance(user1) 

personal.unlockAccount(user1,'密码123456') // 解锁用户1

// user1 向 user2 转3个币
eth.sendTransaction({from: user1, to: user2, value:web3.toWei(3,'ether')}) 

// 此时在查询，就会发现user2中有3个币
eth.getBalance(user2)

miner.start() // 开始挖矿
miner.stop() // 停止挖矿