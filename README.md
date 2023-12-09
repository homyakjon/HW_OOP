## Проект "Телефон"

### Класс Phone

Класс `Phone` представляет собой простой телефон со следующими возможностями:

- Поле для описания номера телефона.
- Метод для установки номера телефона.
- Защищенное поле для счетчика входящих звонков.
- Метод для получения количества принятых звонков.
- Метод для принятия звонка и увеличения счетчика.

### Пример использования

```python
from phone import Phone

p1 = Phone()
p2 = Phone()
p3 = Phone()

p1.set_number_phone("111-229-445")
p2.set_number_phone("444-555-666")
p3.set_number_phone("777-888-999")

p1.accept_call()
p1.accept_call()
p1.accept_call()
p2.accept_call()
p2.accept_call()
p2.accept_call()
p3.accept_call()
p3.accept_call()
p3.accept_call()

print(f'Общее количество принятых звонков: {count_obj([p1, p2, p3])}')

p1.save_numbers("phone1_number.csv")
p2.save_numbers("phone2_number.csv")
p3.save_numbers("phone3_number.csv")


# ChessFigures

Проект "ChessFigures" представляет собой реализацию базовых фигур для игры в шахматы.

## Класс ChessFigures

`ChessFigures` - это базовый класс, представляющий общие характеристики фигур шахмат. 
Он включает в себя методы для изменения цвета,
установки координат и выполнения шага. Подклассы реализуют конкретные виды фигур:
`Pawn`, `Horse`, `Officer`, `Tour`, `Queen` и `King`.

### Пример использования

```python
from chess_figures import Pawn, Horse, Officer, Tour, Queen, King, figures_list

p = Pawn()
h = Horse()
of = Officer()
t = Tour()
q = Queen()
k = King()

x, y = 2, 4
step_figures = figures_list([p, h, of, t, q, k], x, y)
if not step_figures:
    print(f"Ни одна фигура не может дойти до клетки за один шаг")
else:
    print("Фигуры, которые могут дойти до клетки за один шаг:")
    for f in step_figures:
        if f.x_coord == x and f.y_coord == y:
            print(f"{f.__class__.__name__} - {f.get_step_validation()}")

Установка
Клонировать репозиторий: git clone https://github.com/ваш-юзернейм/ваш-репо.git
