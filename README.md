# Slow-Start
# cook your dish here
t=int(input())
for i in range(t):
    attack,hp=map(int,input().split())
    counter=0
    index=0
    c=5
    for i in range(1,6):
        counter=1
        if attack//2 * i >=hp:
            index=i
            break
    new= (attack//2 * 5)
    while new<hp:
        new+=attack
        c+=1
        if new>=hp:
            counter=2
            break
    if counter==1:
        print(index)
    elif counter==2:
        print(c)
    else:
        print(hp)
        
    
