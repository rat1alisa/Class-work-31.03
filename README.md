# Class-work-31.03
#include <iostream>
#include <string>
using namespace std;

class STR
{
public:
    char* str;
    int strsize;
    STR() {};
    // | - конструктор
    STR(const STR &s)
    {
        str = s.str;
    }
    // | - конструктор копирывания
    /*STR()
    {
        str = new char[80];
        strsize = 80;
    }*/
    STR(int n1)
    {
        str = new char[n1];
        strsize = n1;
    }
    STR(string str1)
    {
        str = new char[str1.size()];
        for(int i = 0; i < str1.size(); i++)
        {
            str1[i] = str[i];
        }
        strsize = str1.size();
    }
    void Output()
    {
        for(int i = 0; i < strsize; i++)
        {
            cout << str[i];
        }
    }
    void Input()
    {
        for(int i = 0; i < strsize; i++)
        {
            cin >> str[i];
        }
    }
};

int main()
{
    STR A("I love me");
    A.Output();
    STR B = A;
    B.Output();
}
