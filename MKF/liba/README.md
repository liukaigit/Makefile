**1、简介**
- 该框架用来生成静态库和头文件，规范化编写Makefile，可以扩展添加第三方依赖库和头文件，并包含测试用例。

**2、测试**
- 测试对外输出动态库和头文件分别为：libaprint.a和aprint.h，测试用例目录为：example，测试情况如下步骤所示：
    - \# cd xxx/liba
    - \# make
        - 先编译当前目录生成动态库，然后自动进入example目录编译测试用例
    - \# export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$PWD
        - 添加临时动态库环境变量
    - \# ./example/test
        - 运行测试用例，输出结果如下
        - Output: The is libaprint.a test.

**3、应用**
- 根据业务需求，编辑对应c和h文件，修改Makefile目标和依赖对象名称，再对应调整example测试用例c和Makefile，参考第二步测试过程进行验证。
