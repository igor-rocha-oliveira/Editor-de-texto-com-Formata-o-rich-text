# Editor-de-texto-com-Formata-o-rich-text
from tkinter import Tk, Menu, ttk


def acesso():
    print('colocar função de menu')

main = Tk()
main.title('Editor de texto')

main.geometry('500x500')

class notebook:
    rows = 0
    while rows < 50:
        main.rowconfigure(rows, weight=1)
        main.columnconfigure(rows, weight=1)
        rows += 1


class menu:
    menu = Menu(main)
    main.config(menu=menu)
    subMenu = Menu(menu)

    menu.add_cascade(label='File', menu=subMenu)

    subMenu.add_command(label='New project', command=acesso)
    subMenu.add_command(label='Segundo', command=acesso)
    subMenu.add_separator()
    subMenu.add_command(label='Exit', command=acesso)

    editMenu = Menu(menu)

    menu.add_cascade(label='Exit', menu=editMenu)
    editMenu.add_command(label='Good', command=acesso)


class barr:
    barr = ttk.Progressbar(orient='horizontal', length=30)
    barr.grid(row=50, column=0, columnspan=50, rowspan=49, sticky='News')


main.mainloop()
