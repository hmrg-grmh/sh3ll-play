# meta-shells

一些基于 `eval` 而成的 SHell 「框架」

- `childs-fun` ：
  
  这个能用来比较方便地编写「子命令」。
  
  默认的命名不适合 POSIX 标准，想在简单 SHell 里使用的话请更改命名，之后我也会写一个逻辑能直接获取到 POSIX 的命名。
  
- `dialec-cmdline` ：
  
  这个里面有能够用统一方式编写用户交互逻辑的框架。
  
  你只需要在 `ask_user` 命令后面写好该有的四个参数（**其中包括问话逻辑**），就能让它生效，不带参数会有个有趣的默认效果，**关键就在于你可以把你的逻辑代码以字符串的形式传递进去**（这就得益于在里面使用的 `eval` 了）。
  
- `history_machines`
  
  这并不是库，不同于前两个。
  
  这是个工具，也是个尝试。
  
  （而能够作为库的东西在它里面……但那些里面并没有用到 `eval` ……）

--------

*这些东西本来也就是我写着玩儿的。*

*……特别是子命令那个，可能并不能像成熟的语言里的子命令那样严谨。*

*——但也不失为一种组织代码的手段：借用 \*nix SHell 自有的函数定义规则，并借助 \*nix SHell 的「一切皆字符串」的特性——来完成对各个代码部分之间的组织关系的尽可能简洁的表达……*
