# code-of-the-day-codechef
CODE OF THE DAY WITH PYTHON 
for _ in range(int(input())):
    q = int(input())
    initial = set()
    initial.add(0)
    E, O = 0, 0

    for i in range(q):
        j = int(input())
        if j in initial:
            print(E, O)
        else:
            a = []
            for i in initial:
                e = i ^ j 
                if Counter(bin(e)[2:])['1'] % 2 == 1:
                    O += 1
                else:
                    E += 1
                a.append(e)
            
            for k in a:
                initial.add(k)
            print(E, O)
