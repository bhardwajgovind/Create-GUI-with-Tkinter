# Create-GUI-with-Tkinter
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Requirement already satisfied: requests in c:\\programdata\\anaconda3\\lib\\site-packages (2.22.0)\n",
      "Requirement already satisfied: chardet<3.1.0,>=3.0.2 in c:\\programdata\\anaconda3\\lib\\site-packages (from requests) (3.0.4)\n",
      "Requirement already satisfied: idna<2.9,>=2.5 in c:\\programdata\\anaconda3\\lib\\site-packages (from requests) (2.8)\n",
      "Requirement already satisfied: certifi>=2017.4.17 in c:\\programdata\\anaconda3\\lib\\site-packages (from requests) (2019.9.11)\n",
      "Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in c:\\programdata\\anaconda3\\lib\\site-packages (from requests) (1.24.2)\n",
      "Note: you may need to restart the kernel to use updated packages.\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "WARNING: You are using pip version 20.1.1; however, version 20.2.2 is available.\n",
      "You should consider upgrading via the 'C:\\ProgramData\\Anaconda3\\python.exe -m pip install --upgrade pip' command.\n"
     ]
    }
   ],
   "source": [
    "pip install requests"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Requirement already satisfied: Pillow in c:\\programdata\\anaconda3\\lib\\site-packages (6.2.0)\n",
      "Note: you may need to restart the kernel to use updated packages.\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "WARNING: You are using pip version 20.1.1; however, version 20.2.2 is available.\n",
      "You should consider upgrading via the 'C:\\ProgramData\\Anaconda3\\python.exe -m pip install --upgrade pip' command.\n"
     ]
    }
   ],
   "source": [
    "pip install Pillow"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "metadata": {},
   "outputs": [],
   "source": [
    "from tkinter import*\n",
    "\n",
    "height=600\n",
    "width=500\n",
    "\n",
    "\n",
    "root = Tk()\n",
    "\n",
    "canvas = Canvas(root, height= height, width = width)\n",
    "canvas.pack()\n",
    "\n",
    "frame = Frame(root, bg='skyblue')\n",
    "#frame.place(relheight=1, relwidth=1)\n",
    "frame.place(relx=0.1, rely=0.1, relheight=0.8, relwidth=0.8 )\n",
    "\n",
    "#button = Button(root, text='My Button', bg='white', fg='black')\n",
    "button = Button(frame, text='My Button', bg='white', fg='black')\n",
    "button.pack(side='bottom')\n",
    "\n",
    "label = Label(frame, text='My first GUI')\n",
    "label.pack()\n",
    "\n",
    "entry = Entry(frame)\n",
    "entry.pack()\n",
    "\n",
    "root.mainloop()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [],
   "source": [
    "from tkinter import *\n",
    "\n",
    "root =Tk()\n",
    "\n",
    "height=500\n",
    "width=600\n",
    "\n",
    "canvas = Canvas(root, height= height, width = width)\n",
    "canvas.place()\n",
    "\n",
    "frame = Frame(root, bg='skyblue')\n",
    "frame.place(relx = 0.1, rely = 0.1, relheight=0.8, relwidth = 0.8)\n",
    "\n",
    "label = Label(frame, text='GUI')\n",
    "label.grid(row=0, column=0)\n",
    "\n",
    "button = Button(frame, text='Button')\n",
    "button.grid(row=1, column=0)\n",
    "\n",
    "root.mainloop()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Using place over grid.\n",
    "\n",
    "from tkinter import *\n",
    "\n",
    "root = Tk()\n",
    "\n",
    "canvas = Canvas(root, height= 250, width = 300)\n",
    "canvas.pack()\n",
    "\n",
    "frame = Frame(root, bg = 'gray')\n",
    "frame.place(relx = 0.1, rely = 0.1, relheight=0.8, relwidth = 0.8)\n",
    "\n",
    "label = Label(frame, text='GUI')\n",
    "label.place(relx=0,rely=0, relheight= 0.20, relwidth = 0.25)\n",
    "\n",
    "entry = Entry(frame)\n",
    "entry.place(relx=0.3, rely = 0, relheight= 0.20, relwidth = 0.25 )\n",
    "\n",
    "root.mainloop()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 99,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Weather\n",
    "\n",
    "from tkinter import *\n",
    "\n",
    "height= 500\n",
    "width = 600\n",
    "\n",
    "root = Tk()\n",
    "\n",
    "canvas= Canvas(root, height=height, width = width)\n",
    "canvas.pack()\n",
    "\n",
    "#background_image = PhotoImage(file=r'C:\\Users\\bhard\\Desktop\\Python\\GUI\\Amp 1.PNG')\n",
    "#background_label = Label(root, image=background_image)\n",
    "#background_label.place(relheight=1, relwidth = 1)\n",
    "\n",
    "frame =Frame(root,bg='skyblue', bd=5)\n",
    "frame.place(relx = 0.5, rely =0.1, relheight=0.1, relwidth = 0.75, anchor='n')\n",
    "\n",
    "entry = Entry(frame, font=40)\n",
    "entry.place(relwidth = 0.65, relheight=1)\n",
    "\n",
    "button = Button(frame, text='Test Button')\n",
    "button.place(relx=0.7, relheight=1, relwidth = 0.3 )\n",
    "\n",
    "lower_frame = Frame(root,bg='skyblue', bd=10)\n",
    "lower_frame.place(relx = 0.5, rely = 0.3, relheight=0.6, relwidth = 0.75, anchor = 'n')\n",
    "\n",
    "label = Label(lower_frame, bg='white')\n",
    "label.place(relx= 0.5, rely = 0,relheight=1, relwidth = 1, anchor='n')\n",
    "\n",
    "\n",
    "root.mainloop()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 89,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "C:\\Users\\bhard\\Desktop\\Python\\GUI\n"
     ]
    }
   ],
   "source": [
    "import os\n",
    "print(os.getcwd())"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.4"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
