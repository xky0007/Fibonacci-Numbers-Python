# Fibonacci-Numbers-Python

Generally, we can use iterative and recursive ways to get the Fibonacci numbers.

1. Iterative

        def fibonacci1(num):
            result=[0,1]
            if num==1:
                return [0]
            elif num==2:
                return [0,1]
            for i in range (2,num):
                result.append(result[i-1]+result[i-2])
            return result
        
If we call as fibonacci1(20)

It will display [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181]

2. Recursive

We need to get the nth Fibonacci number in recursive way first.

    def fibonacci(num):
        if num==1 or num==0:
            return num
        else:
            return fibonacci(num-1)+fibonacci(num-2)
            

If we run fibonacci(20) and it will show the 21th fibonacci number - 6765

Second, we can write a loop to add them to the list.

    def fibonacci2(num):
        res=[]
        for i in range(0,num):
            res.append(fibonacci(i))
            num-=1
        return res
        
If we call fibonacci2(20), it will display the same result as fibonacci1(20).        
