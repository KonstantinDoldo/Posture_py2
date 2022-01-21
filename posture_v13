# -*- coding: utf-8 -*-
import Tkinter
import random

class Reminder():
    def __init__(self):
        #create root window
        self.root = Tkinter.Tk()
        frame = Tkinter.Frame(self.root, width=300, height=50).pack()
        self.positionWindow()
        self.root.after_idle(self.show)  # Schedules self.show() to be called when the mainloop starts

    def positionWindow(self):
        w=300
        h=50
        sw = self.root.winfo_screenwidth()
        sh = self.root.winfo_screenheight()
        x = sw-w - w/4
        y = sh-h - h
        self.root.geometry('%dx%d+%d+%d' % (w, h, x, y))
                
    def hide(self):
        self.root.withdraw()  # Hide the window
        self.label.place_forget()
        self.root.after(1000 * self.hide_int, self.show) # Schedule self.show() in hide_int seconds

    def show(self):        
        self.hide_int = 3600  # In seconds
        self.show_int = 5  # In seconds

        #self.root is parent widget for Frame and Label
        RxDict={1: "встань из-за компьютера и погуляй 1 минуту    ",
                2: "",
                3: "",
                4: "",
                5: "",
                6: "",
                7: "",
                8: "",
                9: "",
                10:"",
                11:"",
                12:"",
                13:"",
                14:"",
                15:"",}
        self.label = Tkinter.Label(self.root, text=RxDict.get(random.randint(1, len(RxDict))))
        self.label.place(x=10, y=10)
                
        self.root.deiconify() # Show the window        
        self.root.after(1000 * self.show_int, self.hide)  # Schedule self.hide in show_int seconds

    def start(self):
        self.root.mainloop()

if __name__ == "__main__":
    r = Reminder()
    r.start()
