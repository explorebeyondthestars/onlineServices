## 开发日志写于beta0.8

借鉴我在我的另外一个项目当中收获的经验，我优化了这个项目的配置Caddy的流程，现在，可以说这种配置方式更稳健也更简单了，当然，也就更不容易出错了. 大体的流程图可以参看documentations目录下的configureCaddy.pdf这个文件. 其实只要把过程想明白了，实现起来还是非常简单的，如此，也就可以不再认为Caddy难配置了，并且，更好的是，这种配置方式是通用的，只需改动很少的代码，甚至都不用改动代码而是把变化的部分放到配置文件里边去. 可以比较我的这个项目和我的另外一个项目links. 并且，同样是参照links这个项目，我还把这个项目中对webRoot的配置去掉了，默认就是在frontend目录，以及，把一些配置项写到了配置文件当中，这样，实际上更好理解一些，也就是说更加简单一些. 依赖于这样一种新的配置方式，新的服务模块可以能够很轻松地被集成到现有的服务集合当中，并且不会产生什么不一致性，这就是意义所在. 伟大之事物皆始于渺小.

接下来，我可以考虑将Telegram的通知功能集成进来，实现通过TelegramBot查看统计信息. 以及像在links那个项目中所做的那样，同样地在frontend目录下造出一个具有基本功能和使用价值的前端出来，或许会参照同样的主题方案.

另外，毋庸置疑，虽然说这个项目看起来似乎是复杂了一点，毕竟，有这么多个class，这么多个文件和这么多个文件夹，但是，不论怎么样，这些class的分布仅仅是逻辑在物理上的体现，我们只需从逻辑上思考这个项目应该被通过何种方式开发以何种方式演化即可，而无需关系具体地表现，再多的class也都是尽职的class，这么多的文件当中，是没有多余的.