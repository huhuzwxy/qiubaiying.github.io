# lambda函数
    排序时
    a = [(3, 1), (2, 4), (8, 0)]
    a.sort(key=lambda x: x[1])

# map函数
    对sequence中的item依次执行function(item),
    python3中需要转为list再输出
    print(list(map(lambda x: x**2, [1, 5, 2])))
    output: [1, 25, 4]

# filter函数
    对sequence中的item依次执行function(item)，返回执行结果为True的item
    python3中需要转为list再输出
    def div(x):
        return x % 2 == 1
    print(list(filter(div, [1, 5, 2])))
    output:[1, 5]

# reduce函数
    对sequence中的item顺序迭代调用function
    python3中reduce在functools模块中
    from functools import reduce
    print(reduce(lambda x, y: x + y, [1, 5, 2]))
    output:8

# zip函数
    将sequence中的item打包成元组
    python3中转为list再输出
    p = [1, 4, 6]
    q = [2, 5, 8]
    print(list(zip(p, q)))
    output:[(1, 2), (4, 5), (6, 8)]