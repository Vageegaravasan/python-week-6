1.
l=[]
temp=l
a=int(input())
for i in range(a):
    s=int(input())
    l.append(s)
l1=sorted(l)
k=l1[0]
for i in l:
    if(i-1!=k):
        l.remove(i)
        l1.remove(i)
        break
    else:
        k=i
print(l==l1 or l==l1[::-1])

2.
a=int(input())
dic={}
for i in range(a):
    k=int(input())
    if k not in dic:
        dic[k]=1
    else:
        dic[k]+=1
for i in dic:
    print(f"{i} occurs {dic[i]} times")

3.
t=int(input())
n=int(input())
l1=list()
for i in range(n):
    a=int(input())
    l1.append(a)
m=int(input())
l2=list()
for i in range(m):
    b=int(input())
    l2.append(b)

for i in l1:
    if i in l2:
        print(i,end=' ')
    else:
        continue

4.
a=int(input())
for _ in range(a):
    l=[]
    s=0
    n = int(input())
    for _ in range(n):
        l.append(int(input()))
    k=int(input())
    for i in range(n):
        for j in range(i+1,n):
            if l[j]-l[i]==k and i!=j:
                s=1
                break
        if(s):
            break
    print(s)

5.
l=[]
for i in range(10):
    l.append(int(input()))
c=int(input())
l.append(c)
l=sorted(l)
print(f"ITEM to be inserted:{c}\nAfter insertion array is:")
for i in l:
    print(i)

6.
def print_distinct_elements(arr):
    # Convert the array to a set to remove duplicates
    distinct_elements = set(arr)
    
    # Print the distinct elements separated by space
    print(*distinct_elements)


# Read input length
n = int(input())

# Read array elements
arr = []
for _ in range(n):
    arr.append(int(input()))

# Call the function to print distinct elements
print_distinct_elements(arr)

7.
n = int(input().strip())
p = int(input().strip())
factors = []
for i in range(1, int(n**0.5) + 1):
    if n % i == 0:
        factors.append(i)
        if i != n // i:
            factors.append(n // i)

factors.sort()
if p <= len(factors):
    print(factors[p - 1])
else:
    print(0)

8.
a=int(input())
l=[]
for i in range(a):
    l.append(int(input()))
c=sum(l)//2
q=0
for j in l:
    q+=j
    if q >=c:
        q=j
        break;
print(l.index(q))

9.
a=input()
b=input()
c=input()
l1=b.split(' ')
l2=c.split(' ')
for i in l1:
    print(l2.index(i),end=' ')

10.
l1=set()
l2=set()
a=int(input())
for i in range(a):
    l1.add(int(input()))
b=int(input())
for i in range(b):
    l2.add(int(input()))
l1.update(l2)
m=sorted(list(l1))
for i in m:
    print(i,end=' ')
