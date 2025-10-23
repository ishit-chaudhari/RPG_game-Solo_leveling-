#Hear i am going to make sung-jin-woo RPG Game
from datetime import datetime
streak = 0
level =0
tasks = []
exp = 0

# step:1 player name
player_name = input("Enter the name of the player: ").capitalize().strip()
print(f"Welcome {player_name}.")
print(f"| Level: {level} | EXP: {exp}|Daily streak: {streak} |")

def addtask():
    while True:
        task_name = input("Task name: ").strip().capitalize()
        try:
            task_point = int(input("Enter the task points: ").strip())
        except ValueError:
            print("Invalid sintext: ")
            return
        task = {"name": task_name, "points" : task_point, "streak" : streak}
        tasks.append(task)
        print(f"Added: {task_name} points {task_point:+d}")

        exc = input("Do you want to continu[y/n]: ").lower().strip()
        if exc == "y":
            continue
        else:
            break

def list_tasks():
    if not tasks:
        print("No task yet.")
        return
    else:
        print("\n-- Task --")
        for i, t in enumerate(tasks,start=1):
            print(f"{i}.) {t['name']} | {t['points']} | streak = {t['streak']}")


def deleat_task():
    if not tasks:
        print("No task exist.")
        return
    else:
        for i, t in enumerate(tasks, start=1):
            print(f"{i}.) {t['name']} | {t['points']:+d}")

    try:
        iddx = int(input("Enter ask number: ").strip())
    except ValueError:
        print("Invalid input")
        return
    if 1 <= iddx <= len(tasks):
        remove = tasks.pop(iddx - 1)
        print(f"Deleted task: {remove["name"]}")
    else:
        print("Out of range.")


def show_status():
    print(f"\n-- STATUS --")
    print(f"Player: {player_name}")
    print(f"Level: {level}")
    print(f"EXP: {exp}")
    print(f"Daily streak: {streak}")


addtask()
deleat_task()
list_tasks()
show_status()
