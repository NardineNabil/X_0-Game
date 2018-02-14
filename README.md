print("            \n\n")
print("WELCOME TO X_O ^_^ !!\n\n")
a=[0,1,2,3,4,5,6,7,8]
def showa():
    print("------------")
    print("|",a[0],"|",a[1],"|",a[2],"|")
    print("------------")
    print("|",a[3],"|",a[4],"|",a[5],"|")
    print("------------")
    print("|",a[6],"|",a[7],"|",a[8],"|")
    print("------------")
showa()
count1=0
while(count1<5):
  T=True
  while(T==True):
    try:  
        p=int(input("Player1,choose position from(0-8):\n\n"))
    except:
        print("It is not a number..please,TRY AGAIN!!\n\n")
        continue
    if p in range(0,9):
        T==False
    else:
        print("This number is not in board..please,TRY AGAIN!!!\n\n")
        continue
    if(a[p]!="X" and a[p]!="O" ):
        a[p]="X"
        showa()
        count1+=1
        T=False
      
    else:
        print("Sorry,this place has already taken!!!\n\n")
     
  if(a[0]==a[1]==a[2]=="X" or a[0]==a[4]==a[8]=="X" or a[0]==a[3]==a[6]=="X" or 
    a[2]==a[4]==a[6]=="X" or a[6]==a[7]==a[8]=="X" or a[2]==a[5]==a[8]=="X" or
    a[1]==a[4]==a[7]=="X" or a[3]==a[4]==a[5]=="X" ):
     
       print("Player1 has won!")
       break
  
  if(count1==5):
         break   

  T=True
  while(T==True):
    try:
       z=int(input("player2,choose position from (0-8) :\n\n"))
    except:
        print("It is not a number..please,TRY AGAIN!!!\n\n")
        continue
    if z in range(0,9):
        T==False
    else:
        print("This number is not in board..please,TRY AGAIN!!!\n\n")
        continue
    if a[z]!="X" and a[z]!="O":
        a[z]="O"
        showa()
      
        T=False 
    else:
         print("Sorry,this place has already taken!!\n\n")

  
  if(a[0]==a[1]==a[2]=="O" or a[0]==a[4]==a[8]=="O" or a[0]==a[3]==a[6]=="O" or 
    a[2]==a[4]==a[6]=="O" or a[6]==a[7]==a[8]=="O" or a[2]==a[5]==a[8]=="O" or
    a[1]==a[4]==a[7]=="O" or a[3]==a[4]==a[5]=="O" ):
            print("Player2 has won!")
            break
if(count1==5):
  print("Draw")
      

