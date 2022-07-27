# Dockcode_Solution
Solution to the dockcode test question

m, n = int(input()),int(input())
a = [[0]*n for _ in range(m)]
t=1
for i in range(1,(n*m)+1):
    st=max(0,i-m)
    count=min(i,(n-st),m)

    for j in range(0,count):
            a[min(m,i)-j-1][st+j]=t
            t+=1        
for x in a:
    for i in x:
        print(i,end=" ")
    print()    
