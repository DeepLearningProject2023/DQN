# 修改小结

## 重构代码

* 共享部分
  * 删除无用变量，无用函数，无用import等dead code
  * 删除弃用掉的（被注释掉的）代码
  * 统一注释风格
  * 删除测试用代码，如test.py，test_model.py
* model.py
  * 封装不同网络结构代码以方便调用
    * resnet18与resnet34
    * 全连接层数量调整，1->3
    * 恢复resnet模块的batch normalization
* DQN.py
  * MoveModel与ActionModel分块成不同class
  * 只调用一两次的函数删去，代码直接使用
* train.py
  * 暂无
* Agent.py
  * 修改无意义数字为宏定义
  * 简单的if语句修改为运算
* 可参考commit记录的修改！！

## 网络结构更改

目前计划如下

* 修改resnet结构，如resnet18，34，50，56等等
* 增加输出层的全连接层数量，如1，3，5等等
* 绘制出不同网络结构的表格数据

|          |  1   | 3    | 5    |
| -------- | :--: | ---- | ---- |
| resnet18 |      |      |      |
| resnet34 |      |      |      |
| resnet50 |      |      |      |
| resnet56 |      |      |      |

