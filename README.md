import time
import math

start_time = time.time()
#kol-vo tochek pri tochnosti
N=99999
e=0.00001
#x, y, yl, xl, i
a=0
b=1
print('Passivnyi optimalnyi algorytm')
print('Kol-vo tochek = ', N, 'dlya tochnosti 0,00001')

#def f(x):
z=[]
for i in range(1, N+2):
    print('i=', i)
    x = float(a + (i) * (b - a) / (N + 1))
    print('x=', x)
    y=float((x**3) - x + math.exp(-x))
    z.append(y)
    print('y=', y)
#    m=[y]
#z=m+m
#print('m=', m)
print('z=', z)
print('Максимальное значение = ',max(z), '\n', 'Минимальное значение = ', min(z))



#    if y[i]<y[i+1]:
#        ymin=y[i]
#    elif y[i]>y[i+1]:
#        ymax=y[i]
#    else:
#        continue

#    if y[i]<y[i+1]:
#        ymin = y[i]

#        print(y(i))
#print(y[50])
#miny=float(min(y))()
print("--- %s seconds ---" % (time.time() - start_time))