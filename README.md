# Digital-Clock
Digital clock using C++





#include<iostream>
#include<windows.h>

using namespace std;
int main() 
{
    int h,s,m,a,err;
    a=err=0;

    while (err==0)
    {
        cout << "Enter Hour: "<< endl;
        cin >> h;

        cout << "Enter Minute: "<< endl;
        cin >> m;

        cout << "Enter Second: "<< endl;
        cin >> s;

        if ( h<24 && m<50 && s<60 )
        err++;

        else
        system ("cls");
    }
    while (a==0)
    {
        system ("cls");
        cout << h << ":" << m << ":" << s << endl;
        Sleep(1000);
        s++;

        if (s>59)
        {
            s=0;
            s++;
        }
        if (m>59)
        {
            m=0;
            m++;
        }
        if (h>23)
        {
            h=0;
            h++;
        }
    }
    return 0;
}
