# Employee_seating.py
input1=input('seat:')
input2=input().split()#[1A 2B - 3C 4D]
x=input2.index(input1) #STORE 3C OR INPUT 1 VALUE
d=float('inf')
for i in range(x+1,len(input2)): #for first half before the input value e
    if input2[i]=='-':   #example if we give input 1A it will split[2B - 3C 4D] AND ENCOUNTER -        
        d=min(abs(i-x)-1,d)
for i in range(x):   #for second half before the input value
    if input2[i]=='-':  #example if we give input 4D it will split[1A 2B - 3C] AND ENCOUNTER - 
        d=min(abs(i-x)-1,d)
print(d)
