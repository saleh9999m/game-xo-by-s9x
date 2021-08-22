# game-xo-by-s9x
#welcome to xo by s9x

import os
os.system ("clear")
print ("welcome to s9x by s9x ")
import os
a=[]
o='\033[1;41m O \033[1;46m'
x='\033[1;42m X \033[0;46m'
s='\033[1;47m   \033[1;46m'
for r in range(9):
	a.append(s)
def rt(f):
	os.system('clear')
	print('''\033[1;46m
                       
       |       |       
  '''+f[0]+'  |  '+f[1]+'  |  '+f[2]+'''  
       |       |       
———————·———————·—————— 
       |       |       
  '''+f[3]+'  |  '+f[4]+'  |  '+f[5]+'''  
       |       |       
———————·———————·—————— 
       |       |       
  '''+f[6]+'  |  '+f[7]+'  |  '+f[8]+'''  
       |       |       
                       
\033[0;37m''')
q=1
def win(gg):
	d=[[0,1,2],[3,4,5],[6,7,8],[0,4,8],[2,4,7],[0,3,6],[1,4,7],[3,5,8]]
	h=False
	for g in d:
		if gg[g[0]]==gg[g[1]]==gg[g[2]]:
			if gg[g[0]]==gg[g[1]]==gg[g[2]]==x:
				h=True
				for h in range(len(gg)):
					gg[h]=s
				gg[g[0]]=x;gg[g[1]]=x;gg[g[2]]=x
				rt(gg)
				print('اللاعب x فاز ')
				break
			if gg[g[0]]==gg[g[1]]==gg[g[2]]==o:
				h=True
				for h in range(len(gg)):
					gg[h]=s
				gg[g[0]]=o;gg[g[1]]=o;gg[g[2]]=o
				rt(gg)
				print('اللاعب o فاز ')
				break
	return h
rt(a)
kn=[1,2,3,4,5,6,7,8,9]
while True:
	y=int(input('دور اللاعب x'))
	while True:
		if y in kn:
			kn.pop(kn.index(y))
			a[y-1]=x
			print('...')
			break
		else :
			print(f'الاماكن المتاحه : {kn}')
			print('يرجي اختيار احد منها ')
			y=int(input('دور اللاعب x مره اخري'))
	if win(a):
		break
	rt(a)
	for tt in a:
		w=0
		if tt!=s:
			w+=1
		if w==9:
			print('لم يفز احد')
			break
	y=int(input('دور اللاعب o'))
	while True:
		if y in kn:
			kn.pop(kn.index(y))
			a[y-1]=o
			print('...')
			break
		else :
			print(f'الاماكن المتاحه : {kn}')
			print('يرجي اختيار احد منها ')
			y=int(input('دور اللاعب o مره اخري'))
	if win(a):
		break
	rt(a)
	for tt in a:
		w=0
		if tt!=s:
			w+=1
		if w==9:
			print('لم يفز احد')
			break
