#### 三种基于字典的value对字典排序的方法
```
# method1
d = {'lilee':25, 'wangyan':21, 'liqun':32, 'age':19}
c = sorted(d.items(), key=lambda item:item[1], reverse=True)


# method2
import operator
c = sorted(d.items(), key=operator.itemgetter(1), reverse=True)

# method3
f = zip(d.keys(), d.values())
c = sorted(f, key=lambda item:item[1], reverse=True)
```