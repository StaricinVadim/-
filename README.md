# -
import tkinter as tk
from tkinter import *
from tkinter import messagebox
from math import *
def op():
    if operand.get()=='корень':
        square.pack()
        calс_btn = Button(text='Посчитать', command = sqrt_res)
        calс_btn.pack()
    elif operand.get()=='простое математическое выражение':
        summ1.pack()
        summ2.pack()
        oper.pack()
        calс_btn = Button(text='Посчитать', command = simple)
        calс_btn.pack()
    elif operand.get()=='модуль': 
        modul.pack()
        calс_btn = Button(text='Посчитать', command = abs_res)
        calс_btn.pack()
    elif operand.get()=='степень': 
        stepen1.pack()
        stepen2.pack()
        calс_btn = Button(text='Посчитать', command = step_res)
        calс_btn.pack()
    elif operand.get()=='логарифм':
        log1.pack()
        log2.pack()
        calс_btn = Button(text='Посчитать', command = log_res)
        calс_btn.pack()
    elif operand.get()=='синус':
        sin1.pack()
        calс_btn = Button(text='Посчитать', command = sinus_res)
        calс_btn.pack()
    elif operand.get()=='косинус':
        cos1.pack()
        calс_btn = Button(text='Посчитать', command = cos_res)
        calс_btn.pack()
    elif operand.get()=='тангенс':
        tg1.pack()
        calс_btn = Button(text='Посчитать', command = tg_res)
        calс_btn.pack()
    elif operand.get()=='факториал':
        fa1.pack()
        calс_btn = Button(text='Посчитать', command = fact_res)
        calс_btn.pack()
    
        
def sqrt_res():
    res = sqrt(float(square.get()))
    messagebox.showinfo('Ответ', f'Корень числа {square.get()} = {res} ')
def simple():
    if oper.get()=='+':
        count = float(summ1.get())+float(summ2.get())
        messagebox.showinfo('Ответ', f'Сумма чисел {summ1.get()} и {summ2.get()} = {count} ')
    elif oper.get()=='-':
        count = float(summ1.get())-float(summ2.get())
        messagebox.showinfo('Ответ', f'Разность чисел {summ1.get()} и {summ2.get()} = {count} ')
    elif oper.get()=='*':
        count = float(summ1.get())*float(summ2.get())
        messagebox.showinfo('Ответ', f'Произведение чисел {summ1.get()} и {summ2.get()} = {count} ')
    elif oper.get()=='/':
        count = float(summ1.get())/float(summ2.get())
        messagebox.showinfo('Ответ', f'Деление чисел {summ1.get()} и {summ2.get()} = {count} ')
def step_res():
    r = float(stepen1.get())**float(stepen2.get())
    messagebox.showinfo('Ответ', f'Степень числа {stepen1.get()} в {stepen2.get()} = {r} ')

def log_res():
    re = log(float(log1.get()),float(log2.get()))
    messagebox.showinfo('Ответ', f'Логорифм числа {log1.get()} по основанию {log2.get()} = {re} ')

def sinus_res():
    res = sin(float(sin1.get()))
    messagebox.showinfo('Ответ', f'Cинус числа {sin1.get()} = {res} ')

def abs_res():
    res = abs(float(modul.get()))
    messagebox.showinfo('Ответ', f'Модуль числа {modul.get()} = {res} ')
def cos_res():
    res = cos(float(cos1.get()))
    messagebox.showinfo('Ответ', f'Косинус числа {cos1.get()} = {res} ')

def tg_res():
    res = tan(float(tg1.get()))
    messagebox.showinfo('Ответ', f'Тангенс числа {tg1.get()} = {res} ')

def fact_res():
    res = factorial(int(fa1.get()))
    messagebox.showinfo('Ответ', f'Факториал числа {fa1.get()} = {res} ')
window = Tk()
window.title('Калькулятор')
window.geometry('900x350')
calc_lbl = Label(text='ЧТО ВЫ ХОТИТЕ СДЕЛАТЬ? Найти (корень, модуль, степень, логарифм, синус, косинус, тангенс, факториал, простое математическое выражение)')
calc_lbl.pack()
operand = Entry()
operand.pack()
calс_btn = Button(text='Посчитать', command = op)
calс_btn.pack()
square = Entry()
summ1 = Entry()
summ2 = Entry()
modul = Entry()
abs1 = Entry()
stepen1 = Entry()
stepen2 = Entry()
step = Entry()
log1 = Entry()
log2 = Entry()
sin1 = Entry()
tg1 = Entry()
fa1 = Entry()
cos1 = Entry()
oper = Entry()
window.mainloop()        
