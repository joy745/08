# 08
T 组数据，每组两行，第一行 N，B 代表有 N 个待售房屋，你拥有的钱是 B。第二行是 N 个整数，代表每个房屋的价格。
求能购买的最多房屋数量。
代码：
T = int(input())
for t in range(T):
    N, B = map(int, input().split())
    a = list(map(int, input().split()))
    a.sort()
    cnt = 0
    for x in a:
        if B < x:
            break
        cnt += 1
        B -= x
    print('Case #%d: %d' % (t+1, cnt))    cnt:能买的房屋的数量
##map函数的用法
>>def square(x) :            # 计算平方数
...     return x ** 2
... 
>>> map(square, [1,2,3,4,5])   # 计算列表各个元素的平方
[1, 4, 9, 16, 25]
>>> map(lambda x: x ** 2, [1, 2, 3, 4, 5])  # 使用 lambda 匿名函数
[1, 4, 9, 16, 25]
 
# 提供了两个列表，对相同位置的列表数据进行相加
>>> map(lambda x, y: x + y, [1, 3, 5, 7, 9], [2, 4, 6, 8, 10])
[3, 7, 11, 15, 19]
