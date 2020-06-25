# C-study
### 一、宏定义的使用

1. 调试程序时使用。

- **自定义调试数据**：在与其他人合作项目时，经常会先各自写自己的接口，为了验证自己的接口是否正确，于是便会模拟添加测试数据。而往往这些数据会根据实时情况更改，宏定义在这就能起到很好的作用了。只需要在一个地方更改，而不用满篇去search。避免因为遗忘部分数据，而导致程序调试现象异常。节约时间成本，且逻辑清晰明了。

- **Debug打印**：编写程序初期，在找问题时经常会做很多打印，待程序完成时又要将多余的打印去掉。此时使用宏定义"#define DEBUG_APP"（名字自己看着取），如下：

`
#ifdef DEBUG_APP 
printf("This is printf information. \n"); 
#endif 
`
当我们不需要这些打印时，只需注释掉上面的宏定义，便可。
- **代码中多次使用到同一常量**：比如在编写代码时，需求中要求有一最大数值1000000，定义宏定义：
`#define MAX_COUNT 1000000`
这样在需求变更中只需更改宏定义的值便可，方便又快捷。

