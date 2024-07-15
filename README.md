# red
from tkinter import Tk, Button, colorchooser

def choose_color():
    color_code = colorchooser.askcolor(title="Выберите цвет краски")
    if color_code[1] is not None:
        window.config(bg=color_code[1])

# Создаем главное окно
window = Tk()
window.title("Выбор цвета краски")
window.geometry("400x300")

# Устанавливаем начальный цвет фона в RAL 3020
initial_color = "#cc0000"  # RAL 3020
window.config(bg=initial_color)

# Кнопка для вызова диалога выбора цвета
choose_color_button = Button(window, text="Выбрать цвет краски", command=choose_color)
choose_color_button.pack(pady=20)

# Запуск главного цикла обработки событий
window.mainloop()
