
解决vi/vim中粘贴会在行首多很多缩进和空格的问题

当你的服务器上的vim设置为autoindent的话，在i模式下，那么它会将拷贝的文本进行一下缩进。
若你拷贝的文本中已经有表示缩进的空格或者制表符的话，它们也会被当成字符串，而被缩进。

解决办法：
1. 在拷贝前输入:set paste (此时，vim就不会启动自动缩进，而只是纯拷贝粘贴）
2. 拷贝完成之后，输入:set nopaste (关闭paste)
