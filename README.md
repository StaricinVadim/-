# -
import tkinter as tk
from tkinter import *
from tkinter import messagebox
from math import *
def op():
     otvet.insert(0, eval(gtext.get()))

window = Tk()
window.title('Вычисление выражения')
window.geometry('350x200')
calc_lbl = Label(text='Выражение:')
calc_lbl1 = Label(text='Результат')
calc_lbl.grid(row = 2, column = 1)
calc_lbl1.grid(row = 2, column = 3)
gtext = Entry()
gtext.grid(row = 3, column = 1)
otvet = Entry()
otvet.grid(row = 3, column = 3)
calс_btn = Button(text='->', command = op)
calс_btn.grid(row = 3, column = 2)
window.mainloop()     
