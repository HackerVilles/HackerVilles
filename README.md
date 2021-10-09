from tkinter import *
root = Tk()
root.title("BroscutaVorbareata")
def send():
    send = "You -> "+e.get()
    txt.insert(END, "n"+send)
    user = e.get().lower()
    if(user == "buna"):
        txt.insert(END, "n" + "Broscuta -> buna")

        #animatie de trimis mesajul
        import turtle
        Bot = turtle.Turtle()
        Bot.color("green")
        Bot.shape("turtle")
        Bot.penup()
        Bot.goto(-200, 100)
        Bot.goto(300, 60)
        Bot.hideturtle()

        # face emoji
        import turtle
        pen = turtle.Turtle()
        # function for creation of eye
        def eye(col, rad):
            pen.down()
            pen.fillcolor(col)
            pen.begin_fill()
            pen.circle(rad)
            pen.end_fill()
            pen.up()
        #  fata
        pen.fillcolor('yellow')
        pen.begin_fill()
        pen.circle(100)
        pen.end_fill()
        pen.up()
        # ochii
        pen.goto(-40, 120)
        eye('white', 15)
        pen.goto(-37, 125)
        eye('black', 5)
        pen.goto(40, 120)
        eye('white', 15)
        pen.goto(40, 125)
        eye('black', 5)
        # gura
        pen.goto(-40, 85)
        pen.down()
        pen.right(90)
        pen.circle(40, 180)
        pen.up()
        pen.hideturtle()
        turtle.bye()
    elif(user == "buna ziua" or user == "buna seara" or user == "buna dimineata" ):
        print("\n")
        txt.insert(END, " \n " + "Broscuta -> Salutare" )
        print("\n")
    elif(e.get() == "ce faci?" ):
        print("\n")
        txt.insert(END, " \n " + "Broscuta -> Sunt bine!" )
        print("\n")
    elif(user == "cum te simti?" or user == "esti ok?" or user == "o duci bine?"):
        print("\n")
        txt.insert(END, " \n " + "Broscuta -> Minunat cum te pot ajuta?")
        print("\n")
    elif(e.get() == "unde locuiesti?" ):
        print("\n")
        txt.insert(END, " \n " + "Broscuta -> Eu stau pe un hardisk intr-un calculator.Tu unde locuiesti?")
        print("\n")
    elif(e.get() == "cum o sa fie vremea maine?" ):
        print("\n")
        txt.insert(END, " \n " + "Broscuta -> Maine o sa fie 10 grade si cerul v-a fi inorat")
        print("\n")
    else:
        txt.insert(END, " \n " + " Broscuta -> Scuze,poti repeta?")
        print("\n")
    e.delete(0, END)
txt = Text(root)
txt.grid(row=0, column=0, columnspan=2)
e = Entry(root, width=100)
e.grid(row=1, column=0)
send = Button(root, text="Send", command=send).grid(row=1, column=1)
root.mainloop()



