import tkinter as tk
from tkinter import ttk
from tkinter import messagebox
import math

root=tk.Tk()
root.title("Calculator")

tabcontrol=ttk.Notebook(root)
tab1=ttk.Frame(tabcontrol)
tab2=ttk.Frame(tabcontrol)
tab3=ttk.Frame(tabcontrol)

tabcontrol.add(tab1,text="ARTIMATIC CALCULATION",padding=20)
tabcontrol.add(tab2,text="TRIGONOMETRY CALCULATION ",padding=20)
tabcontrol.add(tab3,text="INVERSE TRIGONOMETRY CALCULATION",padding=20)
root.resizable(0, 0)
def evaluate(op):
    try:
        a=int(e11.get())
        b=int(e12.get())
        c=str(eval('a'+op+'b'))
        messagebox.showinfo("Answer","The Answer is "+c)
        if op!='%':
            e11.delete(0,tk.END)
            e12.delete(0,tk.END)
            e11.insert(0,c)
        else:
            e11.delete(0,tk.END)
            e12.delete(0,tk.END)
                
    except:
        messagebox.showerror("Warning","Please input Number in valid format")
        e11.delete(0,tk.END)
        e12.delete(0,tk.END)

def add():
    evaluate('+') 
def sub():
    evaluate('-')
def mul():
    evaluate('*')
def div():
    evaluate('/')
def rem():
    evaluate('%')

def tri(par):
    try:
        a=int(e21.get())
        if par==1:
            c=str(math.degrees(a))
        elif par==2:
            c=str(math.sin(a))   
        elif par==3:
            c=str(math.cos(a))
        elif par==4:
            c=str(math.tan(a))
        messagebox.showinfo("Answer","The Answer is "+c)
            
    except:
        messagebox.showerror("Warning",'Please input degree in Valid format')
        e21.delete(0,tk.END)
        

def Itri(par):
    try:
        a=int(e31.get())
        if par==1:
            c=str(math.asin(math.radians(a)))
        elif par==2:
            c=str(math.acos(math.radians(a)))   
        elif par==3:
            c=str(math.atan(math.radians(a)))
        elif par==4:
            c=str(1/(math.asin(math.radians(a))))
        messagebox.showinfo("Answer","The Answer is "+c)
            
    except:
        messagebox.showerror("Warning",'Please input degree in Valid format')
        e31.delete(0,tk.END)   

    
    
tk.Label(tab1,text="Enter the value of A --: ",fg="Red",font=35,padx=40,pady=15).grid(row=0)
e11=tk.Entry(tab1,relief='sunken',bd=5)
e11.focus()
e11.grid(row=0,column=1)



tk.Label(tab1,text="Enter the value of B --: ",fg='Red',font=35,padx=40,pady=15).grid(row=1)
e12=tk.Entry(tab1,relief='sunken',bd=5)
e12.grid(row=1,column=1)

tk.Label(tab1,text="PERFORM FOLLOWING OPERATION ON DATA;",font=35,pady=15).grid(row=2,column=1)



tk.Button(tab1,text="ADDITION",fg='blue',font=10,command=add,width=25,pady=15).grid(row=3,column=1)
tk.Button(tab1,text="SUBTRACTION",fg='blue',font=10,command=sub,width=25,pady=15).grid(row=4,column=1)
tk.Button(tab1,text="MULTIPLICATION",fg='blue',font=10,command=mul,width=25,pady=15).grid(row=5,column=1)
tk.Button(tab1,text="DIVISION",fg='blue',font=10,command=div,width=25,pady=15).grid(row=6,column=1)
tk.Button(tab1,text="MODULUS(REMINDER)",fg='blue',font=10,command=rem,width=25,pady=15).grid(row=7,column=1)

    
tk.Label(tab2,text="Enter the value of Angle in Degree --: ",fg="Red",font=35,padx=20,pady=15).grid(row=0)
e21=tk.Entry(tab2,relief='sunken',bd=5)
e21.focus()
e21.grid(row=0,column=1)  

tk.Label(tab2,text="\nPERFORM FOLLOWING OPERATION ON DATA\n",font=35).grid(row=1,column=1)
Toperations=["CONVERT TO DEGREE","SINE","COSINE","TANGENT"]

for index,value in enumerate(Toperations):
    tk.Button(tab2,text=value,fg='blue',font=10,command=(lambda e=index+1:tri(e)),width=25,pady=15).grid(row=2+index,column=1)
    

tk.Label(tab3,text="Enter the value of Angle in Degree --: ",fg="Red",font=35,padx=20,pady=15).grid(row=0)
e31=tk.Entry(tab3,relief='sunken',bd=5)
e31.focus()
e31.grid(row=0,column=1) 

tk.Label(tab3,text="\nPERFORM FOLLOWING OPERATION ON DATA:\n",font=35).grid(row=1,column=1)

Ioperations=["SINE INVERSE","COSINE INVERSE","TANGENT INVERSE","COSINE INVERSE"]

for index,value in enumerate(Ioperations):
    tk.Button(tab3,text=value,fg='blue',font=10,command=(lambda e=index+1:Itri(e)),width=25,pady=15).grid(row=2+index,column=1)
    

tabcontrol.grid()


root.mainloop()
