#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    setlocale(LC_ALL, "Russian");
    
    int lox1, lox2;
    char opr;
    
    cout << "Введите два числа: ";
    cin >> lox1 >> lox2;
    
    cout << "Введите оператор: + (сложение), - (вычитание), * (умножение), / (деление): ";
    cin >> opr;
    
    cout << endl;
    cout << lox1 << " " << opr << " " << lox2 << " = ";
    
    switch (opr) {
        case '+':
            cout << lox1 + lox2 << endl;
            break;
        case '-':
            cout << lox1 - lox2 << endl;
            break;
        case '*':
            cout << lox1 * lox2 << endl;
            break;
        case '/':
            if (lox2 != 0)
                cout << lox1 / lox2 << endl;
            else
                cout << "ОШИБКА, НА НОЛЬ ДЕЛИТЬ НЕЛЬЗЯ" << endl;
            break;
        default:
            cout << "Неправильная операция" << endl;
    }
    
    return 0;
}
