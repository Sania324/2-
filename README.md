//2 вариант(средний уровень).
//№поезда.Пункт и время прибытия. Пункт и время отбытия. Вывести сведенья о поездах ,время пребывания в пути которых превышает 7 часов 20 минут.
#include <iostream>
#include <stdio.h>
#include <cmath>
using namespace std;

struct Book
{
    char surname[50];
    char group[50];
    int physics;
    int it;
    int history;
    
    
};

void task2()
{
    int N = 3;
    Book mas[N];
    for (int i = 0; i < N; i++)
{
        cout <<"\nInput surname:";
        cin.ignore(cin.rdbuf()-> in_avail());
        cin.getline(mas[i].surname, sizeof(mas[i].surname));
        
        cout <<"\nInput group:";
        cin.ignore(cin.rdbuf()-> in_avail());
        cin.getline(mas[i].group, sizeof(mas[i].group));
        
        cout <<"\nInput physics:";
        cin >> mas[i].physics;
        
        cout <<"\nInput it:";
        cin >> mas[i].it;
        
        cout <<"\nInput history:";
        cin >> mas[i].history;
}
for (int i = 0; i < N; i++)
{
if (((mas[i].physics + mas[i].it + mas[i].history)/3) > 4)
{
cout <<"Students with a score higher than 4: \n";

        cout <<"\nBook surname:" << mas[i].surname;
        cout <<"\nBook group:" << mas[i].group;
        cout <<"\nBook physics:" << mas[i].physics;
        cout <<"\nBook it:" << mas[i].it;
        cout <<"\nBook history:" << mas[i].history;
        
}
}
}
int main()
{
    task2();
}

