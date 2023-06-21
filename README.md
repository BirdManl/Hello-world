# Hello-world
Мое задание на практику
Данные для новой ветки
Код для выполнения задания 2:
#include <iostream>
#include <cstdlib>
#include <ctime>
#include <vector>

int main() {
    int p = 7;
    int q = 17;
    int n = (p - 1) * (q - 1);
    srand(time(NULL));
    int e = rand() % (n - 2) + 2;
    int count = 0;
    std::vector<int> d_set;
    int num = 1;
    while (count < 5) {
        if ((num * e) % n == 1) {
            d_set.push_back(num);
            count++;
        }
        num++;
    }
    std::cout << e << std::endl;
    for (int i = 0; i < d_set.size(); i++) {
        std::cout << d_set[i] << " ";
    }
    std::cout << std::endl;
    return 0;
}













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
