# Iteration.py
# Assignment 5
# Oluwapelumi Omidiji
# 10/29/2024

def print_hello(n):
    for _ in range(n):
        print("Hello")
    

def print_hello_alt(n):
    print("Hello\n" * n, end= '')


def print_hello_recursion(n):
    if n > 0:
        print("Hello")
        print_hello_recursion(n-1)
    

def power_list(arr):
    for num in arr:
        print(num)
    for num in arr:
        print(f"{num} {num ** 2}")
    

def power_list_recursion(arr, index=0):
    if index < len(arr):
        print(arr[index])
        power_list_recursion(arr, index + 1)
        print(f"{arr[index]} {arr[index] ** 2}")
    

def draw_polygon(sides, length, line_color, fill_color):
    import turtle
    turtle.color(line_color, fill_color)
    turtle.begin_fill()
    for _ in range(sides):
        turtle.forward(length)
        turtle.left(360 / sides)
        turtle.end_fill()


def problem_4():
    for i in range(1, 51):
        if i % 3 == 0 and i % 5 == 0:
            print ("Divisible by both")
        elif i % 3 == 0:
            print("Divisible by three")
        elif i % 5 == 0:
            print("Divisible by five")
        else: 
            print(i)

    
def main():
        n = 100
        print_hello(n)
        print_hello_alt(n)
        print_hello_recursion(n)
        power_list([1, 2, 3, 4, 5])
        power_list_recursion([1, 2, 3, 4, 5])
        draw_polygon(5, 100, 'blue', 'red')
        problem_4()


main()
