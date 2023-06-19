# Hello-world
Мое задание на практику
Данные для новой ветки
Код для выполнения задания 2:
import random

def main():
p = 7
q = 17
n = (p - 1) * (q - 1)
e = random.randint(2, n)
count = 0
d_set = list()
num = 1
while count < 5:
if (num * e) % n == 1:
d_set.append(num)
count += 1
num += 1
print(e)
print(d_set)

if __name__ == "__main__":
main()
