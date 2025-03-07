#note 1 哩扣第1題
a = input()
b = int(input())
a = a.split(",")
for i in range(len(a)):
    a[i] = int(a[i])
    for j in range(i+1,len(a)) :
        a[j] = int(a[j])
        if a[i] == a[j]:
                continue
        else:
             if a[i] + a[j] == b:
                  c = [i,j]
                  print(c)
#note 2 哩扣第441題
a = int(input())
print("星星可以排列成以下幾行")
for i in range(1,a+1):
    if a - i >= 0 :
        c = i*"*"
        print(c)
        a = a - i
    else:
        d = a*"*"
        print(d)
        break
print(f"因為第{i}行不完整，所以返回第{i-1}行")
