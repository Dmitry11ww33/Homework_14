# Homework_14

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Ex.1

написать функцию для вычисления периметра n-угольника(проверку на существование фигуры прописать отдельную(ые) функцию(и)), применить эту функцию(и) для вычисления периметра n-угольника

import math

def is_polygon_valid(n, side_length):
    return n >= 3 and side_length > 0
def polygon_perimeter(n, side_length):
    if not is_polygon_valid(n, side_length):
        print("невозможно вычислить периметр")
        return None
    perimeter = n*side_length
    return perimeter
n_sides =5
side_length =8
perimeter =polygon_perimeter(n_sides, side_length)
if perimeter is not None:
    print(f"периметр {n_sides} угольника со стороной {side_length} = {perimeter}.")

 -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 Ex.2

написать функцию num_to_name_week(num_day_week), которая возвращает имя дня недели(строка)
ПРимер 
num_to_name_week(1) -> ‘Понедельник’

 def num_to_name_week(num_day_week):
    days_of_week = {
        1: 'Понедельник',
        2: 'Вторник',
        3: 'Среда',
        4: 'Четверг',
        5: 'Пятница',
        6: 'Суббота',
        7: 'Воскресенье'
    }
    if num_day_week in days_of_week:
        return days_of_week[num_day_week]
    else:
        return 'некорректный номер'
day_number = 1
day_name = num_to_name_week(day_number)
print(f"{day_number} день недели: {day_name}")
