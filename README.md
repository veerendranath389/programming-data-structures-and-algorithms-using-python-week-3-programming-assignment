# programming-data-structures-and-algorithms-using-python-week-3-programming-assignment
def expanding(l1):
    list1=[]
    (p,q,m)=(0,1,len(l1)-1)
    while m>0:
        diff=l1[q]-l1[p]
        list1.append(abs(diff))
        (p,q,m)=(p+1,q+1,m-1)
    return increment(list1)
def increment(list1):
    for i in range(0,len(list1)-1):
        if list1[i]>=list1[i+1]:
            return False
    return True
def sumsquares(l):
    list1=[]
    even=0
    odd=0
    for number in l:
        if number%2==0:
            even=even+number*number
        else:
            odd=odd+number*number
    return [odd,even]
def transpose(m):
    list1=[]
    list2=[]
    p=0
    q=len(m)
    for j in range(0,len(m[0])):
        for k in range(0,len(m)):
            list1.append(m[k][j])
    for i in range(0,len(m[0])):
        list2.append(list1[p:q])
        p=p+len(m)
        q=q+len(m)
    return list2
