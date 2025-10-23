# 12
code
f = open('exprecion.txt')
n = int(f.readline())
a = []
d,k,p = 0,0,0
for i in f:
    s = i.split()
    s = list(map(int,s))
    s.sort(reverse=True)
    d = min((s[0] - s[1]),(s[0] - s[2]))
    a.append(d)
    k += s[1] + s[2]
    p += s[0]
a.sort()
g = 0
while k % 2 == 0:
    if (k + a[g]) % 2 == 1:
        p -= a[g]
        break
    else:
        g += 1
print(p)
