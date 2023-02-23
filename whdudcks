import time

import googletrans
import googletrans as gt


class ChatBot:
    def __init__(self):
        pass

    def calculator(self, expression):
        from fractions import Fraction
        if expression.find("f(x)=") == 0:
            expression_2 = input("::: ")
            if expression_2.find("y") == -1:
                if expression.find("+") != -1:
                    num_f = int(expression[expression.find("+"):len(expression)])
                    num_f2 = int(expression[expression.find("=") + 1:expression.find("+") - 1])
                else:
                    num_f = int(expression[expression.find("-"):len(expression)])
                    num_f2 = int(expression[expression.find("=") + 1:expression.find("-") - 1])
                return num_f2 * int(expression_2[2:len(expression_2) - 1]) + num_f
            if expression_2 == "y=f(x)":
                import turtle
                import tkinter

                def draw_function():
                    turtle.pencolor('red')
                    turtle.pensize(3)
                    expression_lll = []
                    if expression.find("+") != -1:
                        expression_list = expression[expression.find("=") + 1:expression.find("+") - 1]
                        num_f = expression[expression.find("+"):len(expression)]
                    else:
                        expression_list = expression[expression.find("=") + 1:expression.find("-") - 1]
                        num_f = expression[expression.find("-") + 1:len(expression)]
                    expression_lll.append(expression_list)
                    expression_lll.append('*')
                    expression_lll.append('x')
                    expression_lll.append(num_f)
                    formula = "".join(expression_lll)
                    turtle.penup()
                    x = -100
                    y = eval(formula)
                    turtle.goto(x, y)
                    turtle.pendown()

                    for x in range(-100, 101):
                        y = eval(formula)
                        turtle.goto(x, y)

                axis_size = 350
                speed = 0
                turtle.speed(speed)
                turtle.hideturtle()
                for i in range(4):
                    turtle.setheading(90 * i)
                    turtle.forward(axis_size)
                    turtle.home()

                window = turtle.getcanvas()
                frame_title = tkinter.Frame(window)
                frame_title.grid(row=1, column=0)
                frame_bottom = tkinter.Frame(window)
                frame_bottom.grid(row=2, column=0)

                draw_function()
                turtle.mainloop()
                return "finish"
        if expression.find("r") == 0:
            return int(expression[expression.find("t") + 2:len(expression)]) ** 0.5
        if expression.find('y') != -1:
            if expression[0:2] == 'y=':
                import turtle
                import tkinter

                def draw_function():
                    turtle.pencolor('red')
                    turtle.pensize(3)
                    formula = entry_formula.get()
                    turtle.penup()
                    x = -100
                    y = eval(formula)
                    turtle.goto(x, y)
                    turtle.pendown()

                    for x in range(-100, 101):
                        y = eval(formula)
                        turtle.goto(x, y)

                axis_size = 350
                speed = 0
                turtle.speed(speed)
                turtle.hideturtle()
                for i in range(4):
                    turtle.setheading(90 * i)
                    turtle.forward(axis_size)
                    turtle.home()

                window = turtle.getcanvas()
                frame_title = tkinter.Frame(window)
                frame_title.grid(row=1, column=0)
                frame_bottom = tkinter.Frame(window)
                frame_bottom.grid(row=2, column=0)

                label_text = '예: y=2*x+1'
                tkinter.Label(frame_title, text=label_text).grid(row=0, column=0)
                tkinter.Label(frame_bottom, text='y=').grid(row=0, column=0)
                entry_formula = tkinter.Entry(frame_bottom, width=20)
                entry_formula.grid(row=0, column=1, padx=10, pady=10)
                tkinter.Button(frame_bottom, text='그리기', command=draw_function).grid(row=0, column=2)
                turtle.done()
                return "finish"
            else:
                import numpy as np
                expression_down = input("::: ")
                nd = int(expression_down[expression_down.find("x") + 1:expression_down.find('=') - 1])
                nu = int(expression[expression.find("x") + 1:expression.find('=') - 1])
                num_2 = int(expression_down[expression_down.find('=') + 1:len(expression_down)])
                xy = [[int(expression[:expression.find("x")]), nu],
                      [int(expression_down[:expression_down.find("x")]), nd]]
                result = str(np.linalg.solve(xy, [int(expression[expression.find('=') + 1:len(expression)]), num_2]))
                result_list = ['x = ', result[1:result.find(' ')], '  y = ', result[result.find(' ') + 1:len(result) - 1]]
                return "".join(result_list)
        equation = expression.find('=')
        equation_list = []
        expression_1 = expression[0:equation]
        add_1 = expression_1.find("+")
        if equation != -1:
            if not expression.find("<") == -1 and not expression.find(">") == -1:
                if not add_1 == -1:
                    if expression.find('>') != -1 or expression.find('<') != -1:
                        equation_list.append(expression_1[0:add_1 - 1])
                        equation_list.append(expression_1[add_1 + 1:len(expression_1) - 1])
                    else:
                        equation_list.append(expression_1[0:add_1 - 1])
                        equation_list.append(expression_1[add_1 + 1:len(expression_1)])
                else:
                    if not expression_1[0] == '-':
                        add_2 = expression_1.find("-")
                        if expression.find('>') == -1 or expression.find('<') == -1:
                            equation_list.append(expression_1[0:add_2 - 1])
                            equation_list.append(expression_1[add_2:len(expression_1) - 1])
                        else:
                            equation_list.append(expression_1[0:add_2 - 1])
                            equation_list.append(expression_1[add_2:len(expression_1)])
                    else:
                        if expression.find('>') != -1 or expression.find('<') != -1:
                            equation_list.append(expression_1[0:add_1 - 2])
                            equation_list.append(expression_1[add_1 - 1:len(expression_1) - 1])
                        else:
                            equation_list.append(expression_1[0:add_1 - 2])
                            equation_list.append(expression_1[add_1:len(expression_1)])
                expression_2 = expression[equation + 2:len(expression)]
                add_3 = expression_2.find("+")
                if add_3 != -1:
                    equation_list.append(expression_2[0:add_3 - 1])
                    equation_list.append(expression_2[add_3 + 1:len(expression_2)])
                else:
                    if not expression_2[0] == '-':
                        add_3 = expression_2.find("-")
                        equation_list.append(expression_2[0:add_3 - 1])
                        equation_list.append(expression_2[add_3:len(expression_2)])
                    else:
                        equation_list.append(expression_2[0:add_3 - 2])
                        equation_list.append(expression_2[add_3 - 1:len(expression_2)])
            else:
                if not add_1 == -1:
                    if expression.find('>') != -1 or expression.find('<') != -1:
                        equation_list.append(expression_1[0:add_1 - 1])
                        equation_list.append(expression_1[add_1 + 1:len(expression_1) - 1])
                    else:
                        equation_list.append(expression_1[0:add_1 - 1])
                        equation_list.append(expression_1[add_1 + 1:len(expression_1)])
                else:
                    if not expression_1[0] == '-':
                        add_2 = expression_1.find("-")
                        if expression.find('>') == -1 or expression.find('<') == -1:
                            equation_list.append(expression_1[0:add_2 - 1])
                            equation_list.append(expression_1[add_2:len(expression_1) - 1])
                        else:
                            equation_list.append(expression_1[0:add_2 - 1])
                            equation_list.append(expression_1[add_2:len(expression_1)])
                    else:
                        if expression.find('>') != -1 or expression.find('<') != -1:
                            equation_list.append(expression_1[0:add_1 - 2])
                            equation_list.append(expression_1[add_1 - 1:len(expression_1) - 1])
                        else:
                            equation_list.append(expression_1[0:add_1 - 2])
                            equation_list.append(expression_1[add_1:len(expression_1)])
                expression_2 = expression[equation + 1:len(expression)]
                add_3 = expression_2.find("+")
                if add_3 != -1:
                    equation_list.append(expression_2[0:add_3 - 1])
                    equation_list.append(expression_2[add_3 + 1:len(expression_2)])
                else:
                    if not expression_2[0] == '-':
                        add_3 = expression_2.find("-")
                        equation_list.append(expression_2[0:add_3 - 1])
                        equation_list.append(expression_2[add_3:len(expression_2)])
                    else:
                        equation_list.append(expression_2[0:add_3 - 2])
                        equation_list.append(expression_2[add_3 - 1:len(expression_2)])
            x = int(equation_list[0]) - int(equation_list[2])
            num = int(equation_list[3]) - int(equation_list[1])
            if equation != -1:
                if expression.find('>') == -1 and expression.find('<') == -1:
                    if abs(num % x) == 0:
                        if x > 0:
                            return "x = %s" % (num / x)
                        else:
                            return "x = %s" % (num / x)
                    if not abs(num % x) == 0:
                        if x > 0:
                            return "x = %s" % (Fraction(num, x))
                        else:
                            return "x = %s" % (Fraction(num, x))
                else:
                    inequality_1 = expression.find('>')
                    inequality_2 = expression.find('<')
                    if inequality_1 == -1:
                        if abs(num / x) == 0:
                            if x > 0:
                                return "x <= %s" % (num / x)
                            else:
                                return "x >= %s" % (num / x)
                        else:
                            if x > 0:
                                return "x <= %s" % (Fraction(num, x))
                            else:
                                return "x >= %s" % (Fraction(num, x))
                    if inequality_2 == -1:
                        if abs(num / x) == 0:
                            if x > 0:
                                return "x >= %s" % (num / x)
                            else:
                                return "x <= %s" % (num / x)
                        else:
                            if x > 0:
                                return "x >= %s" % (Fraction(num, x))
                            else:
                                return "x <= %s" % (Fraction(num, x))
        if expression.find("<") != -1:
            equation = expression.find('<')
            equation_list = []
            expression_1 = expression[0:equation]
            add_1 = expression_1.find("+")
            if not add_1 == -1:
                equation_list.append(expression_1[0:add_1 - 1])
                equation_list.append(expression_1[add_1 + 1:len(expression_1)])
            else:
                if not expression_1[0] == '-':
                    add_2 = expression_1.find("-")
                    equation_list.append(expression_1[0:add_2 - 1])
                    equation_list.append(expression_1[add_2:len(expression_1)])
                else:
                    equation_list.append(expression_1[0:add_1 - 2])
                    equation_list.append(expression_1[add_1:len(expression_1)])
            expression_2 = expression[equation + 1:len(expression)]
            add_3 = expression_2.find("+")
            if add_3 != -1:
                equation_list.append(expression_2[1:add_3 - 1])
                equation_list.append(expression_2[add_3 + 1:len(expression_2)])
            else:
                if not expression_2[0] == '-':
                    add_3 = expression_2.find("-")
                    equation_list.append(expression_2[1:add_3 - 1])
                    equation_list.append(expression_2[add_3:len(expression_2)])
                else:
                    equation_list.append(expression_2[1:add_3 - 2])
                    equation_list.append(expression_2[add_3 - 1:len(expression_2)])
            x = int(equation_list[0]) - int(equation_list[2])
            num = int(equation_list[3]) - int(equation_list[1])
            if abs(num / x) == 0:
                if x > 0:
                    return "x < %s" % (num / x)
                else:
                    return "x > %s" % (num / x)
            else:
                if x > 0:
                    return "x < %s" % (Fraction(num, x))
                else:
                    return "x > %s" % (Fraction(num, x))
        if expression.find(">") != -1:
            equation = expression.find('>')
            equation_list = []
            expression_1 = expression[0:equation]
            add_1 = expression_1.find("+")
            if not add_1 == -1:
                equation_list.append(expression_1[:add_1 - 1])
                equation_list.append(expression_1[add_1:len(expression_1)])
            else:
                if not expression_1[0] == '-':
                    add_2 = expression_1.find("-")
                    equation_list.append(expression_1[0:add_2 - 1])
                    equation_list.append(expression_1[add_2:len(expression_1)])
                else:
                    equation_list.append(expression_1[0:add_1 - 2])
                    equation_list.append(expression_1[add_1:len(expression_1)])
            expression_2 = expression[equation + 1:len(expression)]
            add_3 = expression_2.find("+")
            if add_3 != -1:
                equation_list.append(expression_2[:add_3 - 1])
                equation_list.append(expression_2[add_3 + 1:len(expression_2)])
            if add_3 == -1:
                if not expression_2[0] == '-':
                    add_3 = expression_2.find("-")
                    equation_list.append(expression_2[0:add_3 - 1])
                    equation_list.append(expression_2[add_3:len(expression_2)])
                else:
                    equation_list.append(expression_2[0:add_3 - 2])
                    equation_list.append(expression_2[add_3 - 1:len(expression_2)])
            x = int(equation_list[0]) - int(equation_list[2])
            num = int(equation_list[3]) - int(equation_list[1])
            if abs(num / x) == 0:
                if x > 0:
                    return "x > %s" % (num / x)
                else:
                    return "x < %s" % (num / x)
            else:
                if x > 0:
                    return "x > %s" % (Fraction(num, x))
                else:
                    return "x < %s" % (Fraction(num, x))
        if expression.find(",") != -1:
            num1 = int(expression[:expression.find(",")])
            num2, data = int(expression[expression.find(",") + 1:len(expression)]), []
            for i in range(1, num1 + 1):
                if (num1 % i == 0) & (num2 % i == 0):
                    data.append(i)
            print("공약수: ", data)
            data1, data2, cam = [], [], []
            for i in range(1, num2 + 1):
                data1.append(i * num1)
            for i in range(1, num1 + 1):
                data2.append(i * num2)
            cnt = 0
            for i in data1:
                if i in data2:
                    cnt += 1
                    cam.append(i)
                    if cnt == 10:
                        break
            return "공배수: %s" % (cam)
        ex = expression.find('=')
        if ex == -1:
            return "%s = %s" % (expression, eval(expression))

    def chat_bot(self, chat):
        import webbrowser
        import playsound as py
        tr = gt.Translator()
        cnt = 0
        xnt = 0
        memory = str(chat)
        expression = []
        en = 'qwertyuiopasdfghjklzxcvbnm'
        for eng in en:
            if eng in chat:
                xnt += 1
        if xnt > 2:
            chat = tr.translate(chat, dest='ko')
            chat = chat.text
        for j in chat:
            for l in range(10):
                if j == str(l):
                    cnt += 1
        if '개' in chat or 'lqkf' in chat or '발' in chat or '끼' in chat or '년' in chat or '놈' in chat:
            return '당신은 그런말은 안돼요.'
        elif '불러' in chat:
            return ''
        elif '편지' in chat or '한마디' in chat:
            space = chat.find(' ')
            name = chat[0:space - 2]
            qwer = chat[space + 1:len(chat)]
            latter = [name, '  ', qwer[0:4]]
            qwer = qwer[qwer.find(' '):len(qwer)]
            latter.append('%s합니다' % (qwer[0:4]))
            return " ".join(latter)
        elif '삼각' in memory and '넓' in memory:
            if memory.find('높이') != -1:
                if memory.find('높이') < memory.find('변'):
                    h = memory[memory.find('높이') + 3:memory.find('c')]
                    memory = memory[memory.find('c') + 2:len(memory)]
                    s = memory[memory.find('변') + 3:memory.find('c')]
                else:
                    h = memory[memory.find('변') + 3:memory.find('c')]
                    memory = memory[memory.find('c') + 2:len(memory)]
                    s = memory[memory.find('높이') + 3:memory.find('c')]
                return "넓이: %s" % (int(s) * int(h) / 2)
        elif '사각' in memory:
            if '사각' in memory and '넓' in memory:
                if memory.find('높이') != -1:
                    if memory.find('높이') < memory.find('변'):
                        h = memory[memory.find('높이') + 3:memory.find('c')]
                        memory = memory[memory.find('c') + 2:len(memory)]
                        s = memory[memory.find('변') + 3:memory.find('c')]
                    else:
                        h = memory[memory.find('변') + 3:memory.find('c')]
                        memory = memory[memory.find('c') + 2:len(memory)]
                        s = memory[memory.find('높이') + 3:memory.find('c')]
                    return "넓이: %s" % (int(s) * int(h))
        elif '원' in chat:
            if '넓' in chat:
                if '지름' in chat:
                    if '반' in chat:
                        if 'cm' in chat:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                            return "%sπcm²" % (r ** 2)
                        else:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                            return "%sπ" % (r ** 2)
                    else:
                        if 'cm' in chat:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                            return "%sπcm²" % ((r / 2) ** 2)
                        else:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                            return "%sπ" % ((r / 2) ** 2)
            else:
                if '지름' in chat:
                    if '반' in chat:
                        if 'cm' in chat:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                            return "%sπcm" % (r * 2)
                        else:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                            return "%sπ" % (r * 2)
                    else:
                        if 'cm' in chat:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                            return "%sπcm" % (float(r))
                        else:
                            r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                            return "%sπ" % (float(r))
        elif '어떤수' in memory:
            if '가' in memory:
                memory1 = memory[0:memory.find('가')]
            else:
                memory1 = memory[0:memory.find('는')]
            if '배' in memory1:
                if '두' in memory1:
                    expression.append('2x')
                if '세' in memory1:
                    expression.append('3x')
                if '네' in memory1:
                    expression.append('4x')
                if '다섯' in memory1:
                    expression.append('5x')
                if '여' in memory1:
                    if '섯' in memory1:
                        expression.append('6x')
                    else:
                        expression.append('8x')
                if '일' in memory1:
                    expression.append('7x')
                if '아' in memory1:
                    expression.append('9x')
                if '열' in memory1:
                    expression.append('10x')
            else:
                expression.append('1x')
            if '더' in memory1:
                if '-' in memory1:
                    expression.append("-%s" % (int(memory1[memory1.find('더') - 4:memory1.find('더') - 2])))
                else:
                    expression.append("+%s" % (int(memory1[memory1.find('더') - 4:memory1.find('더') - 2])))
            elif '뺀' in memory1:
                if '-' in memory1:
                    if memory1[memory1.find('뺀') - 4] == '-':
                        expression.append("+%s" % (int(memory1[memory1.find('뺀') - 3:memory1.find('뺀') - 2])))
                    else:
                        expression.append("+%s" % (int(memory1[memory1.find('뺀') - 4:memory1.find('뺀') - 2])))
                else:
                    expression.append("-%s" % (int(memory1[memory1.find('뺀') - 4:memory1.find('뺀') - 2])))
            else:
                expression.append('+ 0')
            if memory.find('가') == -1:
                memory = memory[memory.find('는') + 1:len(memory)]
            else:
                memory = memory[memory.find('가') + 1:len(memory)]
            expression.append('=')
            if '배' in memory:
                if '두' in memory:
                    expression.append('2x')
                if '세' in memory:
                    expression.append('3x')
                if '네' in memory:
                    expression.append('4x')
                if '다섯' in memory:
                    expression.append('5x')
                if '여' in memory:
                    if '섯' in memory:
                        expression.append('6x')
                    else:
                        expression.append('8x')
                if '일' in memory:
                    expression.append('7x')
                if '아' in memory:
                    expression.append('9x')
                if '열' in memory:
                    expression.append('10x')
            else:
                expression.append('1x')
            if '더' in memory:
                if '-' in memory:
                    expression.append("-%s" % (int(memory[memory.find('더') - 4:memory.find('더') - 2])))
                else:
                    expression.append("+%s" % (int(memory[memory.find('더') - 4:memory.find('더') - 2])))
            elif '뺀' in memory:
                if '-' in memory:
                    if memory[memory.find('뺀') - 4] == '-':
                        expression.append("+%s" % (int(memory[memory.find('뺀') - 3:memory.find('뺀') - 2])))
                    else:
                        expression.append("+%s" % (int(memory[memory.find('뺀') - 4:memory.find('뺀') - 2])))
                else:
                    expression.append("-%s" % (int(memory[memory.find('뺀') - 4:memory.find('뺀') - 2])))
            else:
                expression.append('+0')
            expression = "".join(expression)
            return self.calculator(expression=expression)
        elif '공약' in memory:
            if '와' in memory:
                num1 = int(memory[0:memory.find('와')])
            else:
                num1 = int(memory[0:memory.find('과')])
            if '와' in memory:
                num2 = int(memory[memory.find('와') + 2:memory.find('의')])
            else:
                num2 = int(memory[memory.find('과') + 2:memory.find('의')])
            data = []
            for i in range(1, num1 + 1):
                if (num1 % i == 0) & (num2 % i == 0):
                    data.append(i)
            data1 = []
            for j in data:
                data1.append(str(j))
            return ", ".join(data1)
        elif '공배' in memory:
            if '와' in memory:
                num1 = int(memory[0:memory.find('와')])
            else:
                num1 = int(memory[0:memory.find('과')])
            if '와' in memory:
                num2 = int(memory[memory.find('와') + 2:memory.find('의')])
            else:
                num2 = int(memory[memory.find('과') + 2:memory.find('의')])
            data1, data2, cam = [], [], []
            for i in range(1, num2 + 1):
                data1.append(i * num1)
            for i in range(1, num1 + 1):
                data2.append(i * num2)
            cnt = 0
            for i in data1:
                if i in data2:
                    cnt += 1
                    cam.append(str(i))
                    if cnt == 10:
                        break
            return ", ".join(cam)
        elif 'x' in chat and 'y' in chat:
            memory = chat[:chat.find('y')]
            expression = []
            if '배' in memory:
                if '두' in memory:
                    expression.append('2x')
                if '세' in memory:
                    expression.append('3x')
                if '네' in memory:
                    expression.append('4x')
                if '다섯' in memory:
                    expression.append('5x')
                if '여' in memory:
                    if '섯' in memory:
                        expression.append('6x')
                    else:
                        expression.append('8x')
                if '일' in memory:
                    expression.append('7x')
                if '아' in memory:
                    expression.append('9x')
                if '열' in memory:
                    expression.append('10x')
            else:
                expression.append('1x')
            memory = chat[chat.find('y'):chat.find('것')]
            if memory.find('더') != -1:
                expression.append('+')
            if memory.find('뺀') != -1:
                expression.append('-')
            if '배' in memory:
                if '두' in memory:
                    expression.append('2y')
                if '세' in memory:
                    expression.append('3y')
                if '네' in memory:
                    expression.append('4y')
                if '다섯' in memory:
                    expression.append('5y')
                if '여' in memory:
                    if '섯' in memory:
                        expression.append('6y')
                    else:
                        expression.append('8y')
                if '일' in memory:
                    expression.append('7y')
                if '아' in memory:
                    expression.append('9y')
                if '열' in memory:
                    expression.append('10y')
            else:
                expression.append('1y')
            if chat.find('은') != -1:
                if '고' in memory:
                    memory = chat[chat.find('은'):chat.find('고') - 3]
                else:
                    memory = chat[chat.find('은'):chat.find(',') - 4]
            elif '가' in memory:
                if '고' in memory:
                    memory = chat[chat.find('가'):chat.find('고') - 3]
                else:
                    memory = chat[chat.find('가'):chat.find(',') - 4]
            else:
                if '고' in memory:
                    memory = chat[chat.find('이'):chat.find('고') - 3]
                else:
                    memory = chat[chat.find('이'):chat.find(',') - 4]
            expression.append("=%s" % (memory[1:len(memory)]))
            expression1 = "".join(expression)
            if '고' in chat:
                chat = chat[chat.find('고'):len(chat)]
            elif ',' in chat:
                chat = chat[chat.find(','):len(chat)]
            expression = []
            memory = chat[:chat.find('y')]
            if '배' in memory:
                if '두' in memory:
                    expression.append('2x')
                if '세' in memory:
                    expression.append('3x')
                if '네' in memory:
                    expression.append('4x')
                if '다섯' in memory:
                    expression.append('5x')
                if '여' in memory:
                    if '섯' in memory:
                        expression.append('6x')
                    else:
                        expression.append('8x')
                if '일' in memory:
                    expression.append('7x')
                if '아' in memory:
                    expression.append('9x')
                if '열' in memory:
                    expression.append('10x')
            else:
                expression.append('1x')
            memory = chat[chat.find('y'):chat.find('를')]
            if chat.find('더') != -1:
                expression.append('+')
            if chat.find('뺀') != -1:
                expression.append('-')
            if '배' in memory:
                if '두' in memory:
                    expression.append('2y')
                if '세' in memory:
                    expression.append('3y')
                if '네' in memory:
                    expression.append('4y')
                if '다섯' in memory:
                    expression.append('5y')
                if '여' in memory:
                    if '섯' in memory:
                        expression.append('6y')
                    else:
                        expression.append('8y')
                if '일' in memory:
                    expression.append('7y')
                if '아' in memory:
                    expression.append('9y')
                if '열' in memory:
                    expression.append('10y')
            else:
                expression.append('1y')
            if chat.find('은') != -1:
                if '고' in chat:
                    memory = chat[chat.find('은'):chat.find('고') - 4]
                else:
                    memory = chat[chat.find('은'):chat.find(',') - 5]
            elif '가' in chat:
                if '고' in chat:
                    memory = chat[chat.find('가'):chat.find('고') - 4]
                else:
                    memory = chat[chat.find('가'):chat.find(',') - 5]
            else:
                if '고' in chat:
                    memory = chat[chat.find('이'):chat.find('고') - 4]
                else:
                    memory = chat[chat.find('이'):chat.find(',') - 5]
            expression.append("=%s" % (memory[1:len(memory)]))
            expression2 = "".join(expression)
            import numpy as np
            expression = expression1
            expression_down = expression2
            nd = int(expression_down[expression_down.find("x") + 1:expression_down.find('=') - 1])
            nu = int(expression[expression.find("x") + 1:expression.find('=') - 1])
            num_2 = int(expression_down[expression_down.find('=') + 1:len(expression_down)])
            xy = [[int(expression[:expression.find("x")]), nu], [int(expression_down[:expression_down.find("x")]), nd]]
            result = str(np.linalg.solve(xy, [int(expression[expression.find('=') + 1:len(expression)]), num_2]))
            result_list = ['x = ', result[1:result.find(' ')], '  y = ', result[result.find(' ') + 1:len(result) - 1]]
            return "".join(result_list)
        elif '바보' in chat or '멍청' in chat:
            return '아니요, 전 천재입니다.'
        elif '천재' in chat:
            return '네'
        elif '이름' in chat:
            return '저는 천재 입니다'
        elif '살' in chat:
            return '1살'
        elif '그만' in chat or '끝' in chat or '잘가' in chat:
            return '안녕히 계세요'
        elif '안' in chat and '녕' in chat:
            return '안녕하세요'
        elif '번역' in chat:
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                str1 = input("text >>> ")
            else:
                str1 = input("번역할 말 >>> ")
            cnt = 0
            for h in en:
                if h in str1:
                    cnt += 1
            if cnt > 2:
                result = tr.translate(str1, dest='ko')
                return str1, f" => {result.text}"
            else:
                result = tr.translate(str1, dest='en', src='auto')
                return str1, f" => {result.text}"
        elif '이야기' in chat:
            if '무서' in chat:
                print('어떤 학생이 시험을 보고 집에왔다.')
                time.sleep(2)
                print("그날 저녁, 학생은 밥을 먹고 시험지를 서랍에 넣고 잠자리에 든다.")
                time.sleep(2)
                print("    그때,    ")
                time.sleep(2)
                print('"숨기면 모를줄 알았니?"')
            time.sleep(2)
            print("어느 날 아기 돼지 삼형제는 어머니로부터 독립하여 살게 된다.")
            time.sleep(2)
            print("세 마리의 아기 돼지들은 자신만의 집을 짓기로 약속한다.")
            time.sleep(2)
            print("첫째 돼지는 지푸라기, 둘째 돼지는 나무로 허술하게 집을 지었지만 셋째 돼지는 벽돌로 튼튼하게 집을 짓게 된다.")
            time.sleep(2)
            print("어느 날, 그들을 잡아 먹으려고 하는 늑대가 나타나 허술하게 지어진 첫째, 둘째 돼지의 집을 단숨에 무너뜨려 그들을 잡아먹는다.")
            time.sleep(2)
            print("그러나 튼튼한 셋째 돼지의 집만은 무너지지 않았다. 집이 무너지지 않는다는 것을 깨달은 늑대는 셋째 돼지를 밖으로 유인하려 했다.")
            time.sleep(2)
            print("늑대는 순무 밭, 사과나무, 시장으로 가서 셋째 돼지를 유인하려 했으나 셋째 돼지가 늑대와의 약속 시간보다 한 시간 일찍 나간 탓에 계획은 실패하고 말았다.")
            time.sleep(2)
            print("늑대는 셋째 돼지의 집 굴뚝으로 들어가는 계획을 세우지만 결국 그것을 눈치 챈 셋째 돼지가 뜨거운 솥을 놓아 늑대는 죽게 된다.")
        elif '고백' in chat:
            time.sleep(2)
            f = open('pymemo.txt', 'r')
            for i in f:
                print(i)
                time.sleep(2)
            return '끝'
        elif '계산기' in chat:
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                print('yes.')
            else:
                print('네')
            time.sleep(2.5)
            import tkinter as tk

            root = tk.Tk()
            root.title("Calculator")
            root.geometry("350x500")

            upper_frame = tk.Frame(root, width=400, height=70)
            upper_frame.pack(pady=40)

            down_frame = tk.Frame(root, width=400, height=100)
            down_frame.pack(padx=10, pady=10)

            entry = tk.Entry(upper_frame, width=20, font=("Courier", 18), borderwidth=5)
            entry.pack()
            entry.insert(0, "")

            answer = []

            def button_clicked(number):
                current = entry.get()
                entry.delete(0, tk.END)
                entry.insert(0, str(current) + str(number))
                answer.append(number)

            def button_clear():
                entry.delete(0, tk.END)
                answer.clear()

            def button_add():
                entry.delete(0, tk.END)
                answer.append('+')

            def button_sub():
                entry.delete(0, tk.END)
                answer.append('-')

            def button_mul():
                entry.delete(0, tk.END)
                answer.append('*')

            def button_div():
                entry.delete(0, tk.END)
                answer.append('/')

            def button_equal():
                entry.delete(0, tk.END)
                aa = str(''.join(map(str, answer)))
                entry.insert(0, eval(aa))

            btn7 = tk.Button(down_frame, text='7', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(7))
            btn7.grid(column=0, row=0, padx=5, pady=5)
            btn8 = tk.Button(down_frame, text='8', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(8))
            btn8.grid(column=1, row=0, padx=5, pady=5)
            btn9 = tk.Button(down_frame, text='9', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(9))
            btn9.grid(column=2, row=0, padx=5, pady=5)

            btn4 = tk.Button(down_frame, text='4', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(4))
            btn4.grid(column=0, row=1, padx=5, pady=5)
            btn5 = tk.Button(down_frame, text='5', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(5))
            btn5.grid(column=1, row=1, padx=5, pady=5)
            btn6 = tk.Button(down_frame, text='6', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(6))
            btn6.grid(column=2, row=1, padx=5, pady=5)

            btn1 = tk.Button(down_frame, text='1', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(1))
            btn1.grid(column=0, row=2, padx=5, pady=5)
            btn2 = tk.Button(down_frame, text='2', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(2))
            btn2.grid(column=1, row=2, padx=5, pady=5)
            btn3 = tk.Button(down_frame, text='3', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(3))
            btn3.grid(column=2, row=2, padx=5, pady=5)

            btn_pm = tk.Button(down_frame, text='+/-', padx=5, pady=10, font=("Courier", 15),
                               command=lambda: button_clicked('-'))
            btn_pm.grid(column=0, row=3, padx=5, pady=5)
            btn0 = tk.Button(down_frame, text='0', padx=15, pady=10, font=("Courier", 15),
                             command=lambda: button_clicked(0))
            btn0.grid(column=1, row=3, padx=5, pady=5)
            btn_p = tk.Button(down_frame, text='.', padx=15, pady=10, font=("Courier", 15),
                              command=lambda: button_clicked('.'))
            btn_p.grid(column=2, row=3, padx=5, pady=5)

            btn_mul = tk.Button(down_frame, text='×', padx=15, pady=10, font=("Courier", 15), command=button_mul,
                                bg='orange')

            btn_mul.grid(column=3, row=0, padx=5, pady=5)

            btn_sub = tk.Button(down_frame, text='-', padx=15, pady=10, font=("Courier", 15), command=button_sub,
                                bg='orange')

            btn_sub.grid(column=3, row=1, padx=5, pady=5)

            btn_add = tk.Button(down_frame, text='+', padx=15, pady=10, font=("Courier", 15), command=button_add,
                                bg='orange')

            btn_add.grid(column=3, row=2, padx=5, pady=5)

            btn_div = tk.Button(down_frame, text='÷', padx=15, pady=10, font=("Courier", 15), command=button_div,
                                bg='orange')

            btn_div.grid(column=3, row=3, padx=5, pady=5)

            btn_c = tk.Button(down_frame, text='C', padx=15, pady=10, font=("Courier", 15), command=button_clear,
                              bg='orange')

            btn_c.grid(column=2, row=4, padx=5, pady=5)

            btn_res = tk.Button(down_frame, text='=', padx=15, pady=10, font=("Courier", 15), command=button_equal,
                                bg='orange')
            btn_res.grid(column=3, row=4, padx=5, pady=5)

            root.mainloop()
        elif '계산' in chat or cnt > 3 or '+' in chat or '-' in chat or '*' in chat or '/' in chat:
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                str1 = input("only expression >>> ")
            else:
                str1 = input("식만 써주세요. >>> ")
            return self.calculator(expression=str1)
        elif '타이' in chat:
            times = int(input("얼만큼? "))
            print(times)
            time.sleep(1)

            def hello(num):
                if num == 0:
                    return num
                print(num - 1)
                time.sleep(1)
                hello(num - 1)

            return hello(times)
        elif '게임' in chat:
            time.sleep(3)
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                print('yes.')
            else:
                print("네")

            self.game()
            return "    "
        elif 'ㅋ' in chat or 'ㅎ' in chat:
            time.sleep(2)
            return '뭐가 그렇게 웃긴가요?'
        elif '만화' in chat:
            return '그것으 저작권 침해이기 때문에 할 수 없습니다.'
        elif '해킹' in chat:
            return '그것는 불법이기 때문에 할 수 없습니다.'
        elif '노래' in chat:
            time.sleep(3)
            print("네")
            py.playsound("C:\Download\y2mate.com - 노래를 부르면서 삼각함수를 공부하여 보자.mp3")
            return '끝'
        elif '영화' in chat:
            return '아바타'
        elif '검색' in chat:
            print("여기에 검색하세요.")
            time.sleep(2)
            self.search()
            return None
        elif '실' in chat and '검' in chat:
            url = 'https://signal.bz/news'
            webbrowser.open(url=url)
            return None
        elif '..' in chat:
            return '말해보세요.'
        elif '야' in chat:
            return '네?'
        elif '답' in chat:
            chat = input('무슨 일이 있었서 답답한가요?')
            return '%s다니 그럴 수 있지요.' % (chat)
        elif '화' in chat and '나' in chat:
            return '그 마음 이해 합니다.'
        elif '좋' in chat:
            return '그말을 들으니 저도 기분이 좋네요.'
        elif '서러' in chat or '슬' in chat:
            return '그 마음 이해 합니다.'
        elif '서' in chat and '슬' in chat:
            return '안타깝네요.'
        elif '심' in chat or '뭐' in chat:
            return 'TV 보거나 산책 하는 것은 어때요?'
        elif '힘' in chat:
            return '그럴 수 있지요'
        elif '고' in chat:
            return '네'
        elif '메모' in chat:
            g = open('pythontest.txt', 'r')
            if '내용' in chat:
                for lin in g:
                    print(lin)
            if '검색' in chat:
                qwer = input()
                for lin in g:
                    if qwer in lin:
                        print(lin)
            g_list = []
            for i in g:
                g_list.append(i)
            g = open('pythontest.txt', 'w')
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                mem = input("text >>>")
            else:
                mem = input("내용 >>> ")
            for j in g_list:
                g.write(j)
            g.write(mem)
            g.close()
            return ' 완료'
        elif '문제' in chat:
            en = 'qwertyuiopasdfghjklzxcvbnm'
            for eng in en:
                if eng in chat:
                    xnt += 1
            if xnt > 2:
                memory = input("problem >>> ")
                memory = tr.translate(memory, dest='ko', src='auto').text
            else:
                memory = input("문제 내용 >>> ")
            expression = []
            if 'x' in chat and 'y' in chat:
                memory = chat[:chat.find('y')]
                expression = []
                if '배' in memory:
                    if '두' in memory:
                        expression.append('2x')
                    if '세' in memory:
                        expression.append('3x')
                    if '네' in memory:
                        expression.append('4x')
                    if '다섯' in memory:
                        expression.append('5x')
                    if '여' in memory:
                        if '섯' in memory:
                            expression.append('6x')
                        else:
                            expression.append('8x')
                    if '일' in memory:
                        expression.append('7x')
                    if '아' in memory:
                        expression.append('9x')
                    if '열' in memory:
                        expression.append('10x')
                else:
                    expression.append('1x')
                memory = chat[chat.find('y'):chat.find('것')]
                if memory.find('더') != -1:
                    expression.append('+')
                if memory.find('뺀') != -1:
                    expression.append('-')
                if '배' in memory:
                    if '두' in memory:
                        expression.append('2y')
                    if '세' in memory:
                        expression.append('3y')
                    if '네' in memory:
                        expression.append('4y')
                    if '다섯' in memory:
                        expression.append('5y')
                    if '여' in memory:
                        if '섯' in memory:
                            expression.append('6y')
                        else:
                            expression.append('8y')
                    if '일' in memory:
                        expression.append('7y')
                    if '아' in memory:
                        expression.append('9y')
                    if '열' in memory:
                        expression.append('10y')
                else:
                    expression.append('1y')
                if chat.find('은') != -1:
                    if '고' in memory:
                        memory = chat[chat.find('은'):chat.find('고') - 3]
                    else:
                        memory = chat[chat.find('은'):chat.find(',') - 4]
                elif '가' in memory:
                    if '고' in memory:
                        memory = chat[chat.find('가'):chat.find('고') - 3]
                    else:
                        memory = chat[chat.find('가'):chat.find(',') - 4]
                else:
                    if '고' in memory:
                        memory = chat[chat.find('이'):chat.find('고') - 3]
                    else:
                        memory = chat[chat.find('이'):chat.find(',') - 4]
                expression.append("=%s" % (memory[1:len(memory)]))
                expression1 = "".join(expression)
                if '고' in chat:
                    chat = chat[chat.find('고'):len(chat)]
                elif ',' in chat:
                    chat = chat[chat.find(','):len(chat)]
                expression = []
                memory = chat[:chat.find('y')]
                if '배' in memory:
                    if '두' in memory:
                        expression.append('2x')
                    if '세' in memory:
                        expression.append('3x')
                    if '네' in memory:
                        expression.append('4x')
                    if '다섯' in memory:
                        expression.append('5x')
                    if '여' in memory:
                        if '섯' in memory:
                            expression.append('6x')
                        else:
                            expression.append('8x')
                    if '일' in memory:
                        expression.append('7x')
                    if '아' in memory:
                        expression.append('9x')
                    if '열' in memory:
                        expression.append('10x')
                else:
                    expression.append('1x')
                memory = chat[chat.find('y'):chat.find('를')]
                if chat.find('더') != -1:
                    expression.append('+')
                if chat.find('뺀') != -1:
                    expression.append('-')
                if '배' in memory:
                    if '두' in memory:
                        expression.append('2y')
                    if '세' in memory:
                        expression.append('3y')
                    if '네' in memory:
                        expression.append('4y')
                    if '다섯' in memory:
                        expression.append('5y')
                    if '여' in memory:
                        if '섯' in memory:
                            expression.append('6y')
                        else:
                            expression.append('8y')
                    if '일' in memory:
                        expression.append('7y')
                    if '아' in memory:
                        expression.append('9y')
                    if '열' in memory:
                        expression.append('10y')
                else:
                    expression.append('1y')
                if chat.find('은') != -1:
                    if '고' in chat:
                        memory = chat[chat.find('은'):chat.find('고') - 4]
                    else:
                        memory = chat[chat.find('은'):chat.find(',') - 5]
                elif '가' in chat:
                    if '고' in chat:
                        memory = chat[chat.find('가'):chat.find('고') - 4]
                    else:
                        memory = chat[chat.find('가'):chat.find(',') - 5]
                else:
                    if '고' in chat:
                        memory = chat[chat.find('이'):chat.find('고') - 4]
                    else:
                        memory = chat[chat.find('이'):chat.find(',') - 5]
                expression.append("=%s" % (memory[1:len(memory)]))
                expression2 = "".join(expression)
                import numpy as np
                expression = expression1
                expression_down = expression2
                nd = int(expression_down[expression_down.find("x") + 1:expression_down.find('=') - 1])
                nu = int(expression[expression.find("x") + 1:expression.find('=') - 1])
                num_2 = int(expression_down[expression_down.find('=') + 1:len(expression_down)])
                xy = [[int(expression[:expression.find("x")]), nu],
                      [int(expression_down[:expression_down.find("x")]), nd]]
                result = str(np.linalg.solve(xy, [int(expression[expression.find('=') + 1:len(expression)]), num_2]))
                result_list = ['x = ', result[1:result.find(' ')], '  y = ',
                               result[result.find(' ') + 1:len(result) - 1]]
                return " ".join(result_list)
            if '삼각' in memory and '넓' in memory:
                if memory.find('높이') != -1:
                    if memory.find('높이') < memory.find('변'):
                        h = memory[memory.find('높이') + 3:memory.find('c')]
                        memory = memory[memory.find('c') + 2:len(memory)]
                        s = memory[memory.find('변') + 3:memory.find('c')]
                    else:
                        h = memory[memory.find('변') + 3:memory.find('c')]
                        memory = memory[memory.find('c') + 2:len(memory)]
                        s = memory[memory.find('높이') + 3:memory.find('c')]
                    return "S = %s" % (int(s) * int(h) / 2)
            elif '사각' in memory:
                if '사각' in memory and '넓' in memory:
                    if memory.find('높이') != -1:
                        if memory.find('높이') < memory.find('변'):
                            h = memory[memory.find('높이') + 3:memory.find('c')]
                            memory = memory[memory.find('c') + 2:len(memory)]
                            s = memory[memory.find('변') + 3:memory.find('c')]
                        else:
                            h = memory[memory.find('변') + 3:memory.find('c')]
                            memory = memory[memory.find('c') + 2:len(memory)]
                            s = memory[memory.find('높이') + 3:memory.find('c')]
                        return "넓이: %s" % (int(s) * int(h))
            elif '원' in chat:
                if '넓' in chat:
                    if '지름' in chat:
                        if '반' in chat:
                            if 'cm' in chat:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                                return "%sπcm²" % (r ** 2)
                            else:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                                return "%sπ" % (r ** 2)
                        else:
                            if 'cm' in chat:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                                return "%sπcm²" % ((r / 2) ** 2)
                            else:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                                return "%sπ" % ((r / 2) ** 2)
                else:
                    if '지름' in chat:
                        if '반' in chat:
                            if 'cm' in chat:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                                return "%sπcm" % (r * 2)
                            else:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                                return "%sπ" % (r * 2)
                        else:
                            if 'cm' in chat:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 4])
                                return "%sπcm" % (float(r))
                            else:
                                r = int(chat[chat.find('름') + 3:chat.find('원') - 2])
                                return "%sπ" % (float(r))
            elif '어떤수' in memory:
                memory1 = memory[0:memory.find('가')]
                if '배' in memory1:
                    if '두' in memory1:
                        expression.append('2x')
                    if '세' in memory1:
                        expression.append('3x')
                    if '네' in memory1:
                        expression.append('4x')
                    if '다섯' in memory1:
                        expression.append('5x')
                    if '여' in memory1:
                        if '섯' in memory1:
                            expression.append('6x')
                        else:
                            expression.append('8x')
                    if '일' in memory1:
                        expression.append('7x')
                    if '아' in memory1:
                        expression.append('9x')
                    if '열' in memory1:
                        expression.append('10x')
                else:
                    expression.append('1x')
                if '더' in memory1:
                    if '-' in memory1:
                        expression.append("-%s" % (int(memory1[memory1.find('더') - 5:memory1.find('더') - 2])))
                    else:
                        expression.append("+%s" % (int(memory1[memory1.find('더') - 4:memory1.find('더') - 2])))
                elif '뺀' in memory1:
                    if '-' in memory1:
                        expression.append("+%s" % (int(memory1[memory1.find('뺀') - 5:memory1.find('뺀') - 2])))
                    else:
                        expression.append("-%s" % (int(memory1[memory1.find('뺀') - 5:memory1.find('뺀') - 2])))
                else:
                    expression.append('+0')
                memory = memory[memory.find('가') + 1:len(memory)]
                if memory.find('가') == -1:
                    memory = memory[memory.find('는') + 1:len(memory)]
                expression.append('=')
                if '배' in memory:
                    if '두' in memory:
                        expression.append('2x')
                    if '세' in memory:
                        expression.append('3x')
                    if '네' in memory:
                        expression.append('4x')
                    if '다섯' in memory:
                        expression.append('5x')
                    if '여' in memory:
                        if '섯' in memory:
                            expression.append('6x')
                        else:
                            expression.append('8x')
                    if '일' in memory:
                        expression.append('7x')
                    if '아' in memory:
                        expression.append('9x')
                    if '열' in memory:
                        expression.append('10x')
                else:
                    expression.append('1x')
                if '더' in memory:
                    if '-' in memory:
                        expression.append("-%s" % (int(memory[memory.find('더') - 5:memory.find('더') - 2])))
                    else:
                        expression.append("+%s" % (int(memory[memory.find('더') - 5:memory.find('더') - 2])))
                elif '뺀' in memory:
                    if '-' in memory:
                        expression.append("+%s" % (int(memory[memory.find('뺀') - 5:memory.find('뺀') - 2])))
                    else:
                        expression.append("-%s" % (int(memory[memory.find('뺀') - 5:memory.find('뺀') - 2])))
                else:
                    expression.append('+0')
                expression = "".join(expression)
                return self.calculator(expression=expression)
            elif '공약' in memory:
                if '와' in memory:
                    num1 = int(memory[0:memory.find('와')])
                else:
                    num1 = int(memory[0:memory.find('과')])
                num2, data = int(memory[memory.find('과') + 2:memory.find('의')]), []
                for i in range(1, num1 + 1):
                    if (num1 % i == 0) & (num2 % i == 0):
                        data.append(i)
                data1 = []
                for j in data:
                    data1.append(str(j))
                return ", ".join(data1)
            elif '공배' in memory:
                if '와' in memory:
                    num1 = int(memory[0:memory.find('와')])
                else:
                    num1 = int(memory[0:memory.find('과')])
                num2 = int(memory[memory.find('과') + 2:memory.find('의')])
                data1, data2, cam = [], [], []
                for i in range(1, num2 + 1):
                    data1.append(i * num1)
                for i in range(1, num1 + 1):
                    data2.append(i * num2)
                cnt = 0
                for i in data1:
                    if i in data2:
                        cnt += 1
                        cam.append(str(i))
                        if cnt == 10:
                            break
                return ", ".join(cam)
        else:
            return '이해할 수 없습니다'

    def Run(self):
        f1 = open('stdout.txt', 'r')
        lists = []
        for line in f1:
            lists.append(line)
        f11 = open('내꺼.txt', 'r')
        listss = []
        for line in f11:
            listss.append(line)
        f = open('stdout.txt', 'w')
        ff = open('내꺼.txt', 'w')
        for line in listss:
            ff.write(line)
        while True:
            self.chatting = input(" >>> ")
            if '불러' in self.chatting:
                for line in lists:
                    print(line)
                    f.write(line)

            xnt = 0
            en = 'qwertyuiopasdfghjklzxcvbnm'
            tr = googletrans.Translator()
            result = self.chat_bot(chat=self.chatting)
            self.result = result
            for eng in en:
                if eng in self.chatting:
                    xnt += 1
            if xnt > 2:
                if 'ranslate' in self.chatting:
                    print(self.result)
                else:
                    self.result = tr.translate(result, dest='en').text
                    print(self.result)
            else:
                print(self.result)
            if '그만' in self.chatting or '끝' in self.chatting or '잘가' in self.chatting:
                time.sleep(1)
                break
            f.write(">>> " + self.chatting)
            f.write("""
 """)
            f.write(str(self.result))
            f.write("""
""")
            ff.write(">>> " + self.chatting)
            ff.write("""
 """)
            ff.write(str(self.result))
            ff.write("""
""")
        f.close()
        ff.close()


    def game(self):
        import webbrowser
        time.sleep(2)
        webbrowser.open(url='https://classic.minecraft.net/?join=XqbiL2-611QDfn7m')


    def search(self):
        import webbrowser
        webbrowser.open(url='https://www.google.com')

Bot = ChatBot()

Bot.Run()


qu_chatbot = ['x의 ?배에 y의 ?배를 더한것은 ?과 같고, x의 ?배에 y의 ?배를 뺀것은 ?과 같다',
      '어떤수의 ?배는 어떤수의 ?배에 ?을 ?것과 같다', '안녕~~~', '문제 풀어줘',
      '이름이 뭐니?', '이야기 들려줘', '전 대화 내용 불러오기', '메모장 열어줘',
      '게임하고 싶어', '??? 를 계산해줘', '나 ~~~해서 너무 ~~해',
      '밑변이 ? 높이가 ?인 사각형/삼각형 의 넓이', '반지름/지름 이 r인 원의 넓이/둘레',
      '영화 추천해줘', '계산기 실행시켜줘', '~~~를번역해줘', '노래 들려줘', '해킹해줘',
      '?와 ?의 공배수/공약수 를 구해줘', '타이머 해줘', '??에게 ??해서 ???하다고 편지써줘',
      '@#$#%@$%', '~~~~~~~~~~~~~~~~', '그외 영어도 가능']
