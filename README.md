import random 
def agents():
    n=int(input("Enter no. of agents: "))
    final=[]
    is_avaliable=[]
    nm=[]
    role=[]
    mode=[]
    time_avaliable=[]
    for i in range(n):
        is_avaliable=[]
        nm=[]
        role=[]
        mode=[]
        time_avaliable=[]
        nm.append(input("Enter name of agent: "))
        bol=int(input("1.For avaliable 0. For not avaliable: "))
        is_avaliable.append(bol)
        if bol==1:
            time_avaliable.append(input("Time since the agent is avaliable: "))
        else:
            time_avaliable.append(0)
    mode=input("Enter selection mode:  ").lower()
    if mode=="all avaliable":
        return nm
    else:
        if mode=="least busy":
            j=time_avaliable.index(max(time_avaliable))
        else:
            if mode=="random":
                j=random.randrange(len(nm))
            else:
                print("Invalid Selection mode")
                exit(0)
    final=nm[j]
    return final
ans=agents()
print(ans)

