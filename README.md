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




Код для задания 3 на с++
#include <stdio.h>
#include <iostream>
int compute(int a, int m, int n)
{
setlocale (LC_ALL, "Russian");
    int r;
    int y = 1;

    while (m > 0)
    {
        r = m % 2;
        if (r == 1) {
            y = (y * a) % n;
        }
        a = a * a % n;
        m = m / 2;
    }

    return y;
}

int main()
{
    int p = 23;       
    int g = 5;        

    int a, b;    
    int A, B;    

    a = 6;        

    A = compute(g, a, p);

    b = 15;      

    B = compute(g, b, p);


    int keyA = compute(B, a, p);
    int keyB = compute(A, b, p);

    printf("Секретный ключ Алисы %d\nСекретный ключ Боба %d", keyA, keyB);

    return 0;
}
