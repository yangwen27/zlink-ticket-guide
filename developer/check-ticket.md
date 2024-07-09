# 通过依赖注入方式来实现不同检票规则的组合

> 系统现在是将所有的检票校验规则都放在同一个方法里做判断，这样做的优点是代码集中开发起来也比较快，但是随着校验规则越来越多，弊端也凸显出来检票的方法越来越长，Debug也越来越困难。
有没有优化的办法？
有！就是今天要介绍的主角，《依赖注入》




[!COMMENT]
An alert of type 'comment' using style 'callout' with default settings.

#### 1 定义检票接口
{% code %}

``` c#
 public interface ICheckTicketService
  {
      Result Chceck(TicketOrder ticketOrder);
  }
```

 {% endcode%}

