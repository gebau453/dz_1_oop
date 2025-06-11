#include <iostream>
#include <windows.h>// кирилица
using namespace std;

class Kettle {
private:
    string brand;
    int capacity;

public:
    void SetBrand(string new_brand) {
        brand = new_brand;
    }

    string GetBrand() {
        return brand;
    }

    void SetCapacity(int new_capacity) {
        if (new_capacity <= 0 || new_capacity > 10000) {
            cout << " Введите значение от 1 до 10000.\n";
        }
        else {
            capacity = new_capacity;
        }
    }

    int GetCapacity() {
        return capacity;
    }

    Kettle(string b, int c) {
        SetBrand(b);
        SetCapacity(c);
    }

    void info() {
        cout << "Електрочайник: " << brand << ", " << capacity << " мл\n";
    }
};

class Book {
private:
    string title;
    string author;

public:
    void SetTitle(string new_title) {
        title = new_title;
    }

    string GetTitle() {
        return title;
    }

    void SetAuthor(string new_author) {
        author = new_author;
    }

    string GetAuthor() {
        return author;
    }

    Book(string t, string a) {
        SetTitle(t);
        SetAuthor(a);
    }

    void info() {
        cout << "Книга: " << title << " автора " << author << "\n";
    }
};

class Phone {
private:
    string model;
    int storageGB;

public:
    void SetModel(string new_model) {
        model = new_model;
    }

    string GetModel() {
        return model;
    }

    void SetStorageGB(int new_storage) {
        if (new_storage < 0 || new_storage > 2048) {
            cout << " введите значение от 0 до 2048.\n";
        }
        else {
            storageGB = new_storage;
        }
    }

    int GetStorageGB() {
        return storageGB;
    }

    Phone(string m, int s) {
        SetModel(m);
        SetStorageGB(s);
    }

    void info() {
        cout << "Телефон: " << model << ", " << storageGB << " ГБ\n";
    }
};

class Pen {
private:
    string color;
    bool gel;

public:
    void SetColor(string new_color) {
        color = new_color;
    }

    string GetColor() {
        return color;
    }

    void SetGel(bool new_gel) {
        gel = new_gel;
    }

    bool GetGel() {
        return gel;
    }

    Pen(string c, bool g) {
        SetColor(c);
        SetGel(g);
    }

    void info() {
        cout << "Ручка: " << (gel ? "гелева" : "звичайна") << ", колір " << color << "\n";
    }
};

class Banknote {
private:
    int value;
    string currency;

public:
    void SetValue(int new_value) {
        if (new_value <= 0 || new_value > 100000) {
            cout << "Введите значение от 1 до 100000.\n";
        }
        else {
            value = new_value;
        }
    }

    int GetValue() {
        return value;
    }

    void SetCurrency(string new_currency) {
        currency = new_currency;
    }

    string GetCurrency() {
        return currency;
    }

    Banknote(int v, string cur) {
        SetValue(v);
        SetCurrency(cur);
    }

    void info() {
        cout << "Купюра: " << value << " " << currency << "\n";
    }
};

int main() {
    SetConsoleOutputCP(1251);// кирилица
    SetConsoleCP(1251);
    Kettle k("Philips", 1500);
    Book b("Тіні забутих предків", "Михайло Коцюбинський");
    Phone p("iPhone 13", 128);
    Pen pen("синій", true);
    Banknote note(1000, "гривень");

    k.info();
    b.info();
    p.info();
    pen.info();
    note.info();
}

