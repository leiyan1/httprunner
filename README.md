# httprunner
从 2.0.0 版本开始，HttpRunner 不再支持在测试用例文件中进行参数化配置；参数化的功能需要在 testsuite 中实现。变更的目的是让测试用例（testcase）的概念更纯粹，关于测试用例和测试用例集的概念定义，详见《测试用例组织》。

参数化机制需要在测试用例集（testsuite）中实现。如需实现数据驱动机制，需要创建一个 testsuite，在 testsuite 中引用测试用例，并定义参数化配置。

第一：这里记录了三种参数化的基本操作，分别是list,debugtalk,csv，第三种可能用的最多，希望今后能在JC一样的工作中，大量反复使用接口测试时能够用到。
第二：之前我就是在testcase或者是在teststep里反复折腾还是不对，后来发现2.0后suite和case要分开写，现在用这里来记录历程并且备忘,顺带httprunner也能结合locusts进行性能测试，我的电脑稍微加一百个用户几十个线程cpu就预警了。
