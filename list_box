from tkinter import *
from collections import OrderedDict
xxx = 8990
xy=0
f = {'big number': 51, 'small number': 1}#numbers only

def the_dict(a):#does nothing, ignore it
    d = {}
    if 1 == 1:
        for key, value in d.items():#orderdict breaks it if there are letters now
            f[int(key)] = value
        d = OrderedDict(sorted(f.items(), key=lambda x:int(x[1]), reverse=True))
        f['changing value'] = 0+xy#see below comment
        f['changing value 2'] = 0+xy+xy**2#updates every time the dictionary is called lol
    return d
##############################;
def CLEAR():
    add_values()
def value(x):
    print(the_dict(2)[x])#this is where the function goes when it works
def add_values():
    global xy
    xy+=1
    dictionary = the_dict('sfdl')

    listbox2 = listbox = Listbox(frame, width=20, height=20)
    listbox.grid(column=2, row=3, rowspan=6)
    for lol in the_dict(2):
        listbox2.insert(END, the_dict(2)[lol])#tries to list the values of dict in order

    items = StringVar(value=tuple(dictionary.keys()))#makes the list
    listbox = Listbox(frame, listvariable=items, width=20, height=20)
##        if xy != 1:
##            listbox.delete(0, END)
##            listbox2.delete(0, END)
    listbox.grid(column=0, row=2, rowspan=6, sticky=("e", "s"))
    listbox.focus()
    listbox.bind('<Double-1>', lambda x: value(listbox.get(ACTIVE)))#click click
    listbox.update_idletasks()


#################
while True:
    master = Tk()
    frame = Frame(master)
    frame.pack()
    add_values()
    z = Button(master, text="refresh values",fg= 'blue',  command= lambda: CLEAR()).pack(side=BOTTOM)

    mainloop()
