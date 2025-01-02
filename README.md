# Ответы на вопросы из 5 теста Чабанова

## Вопросы
1) Выберите все выражения, которые не вызовут ошибку, при условии, что переменная a объявлена как: <code>int a = 4;</code><br>

Ответ: <code> int& r1 = a; </code><br>
<code> int&& r4 = a + 1; </code><br>
<code> int& r5 = r1; </code><br>
<code> int& r7 = r4; </code>

2) Как обозначается r-value ссылка на значение типа int в С++?<br>

Ответ: <code> int&& </code><br>

3) Как обозначается r-value ссылка на значение типа int в С++?
```cpp
class A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

class B: public A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

B obj;
obj.set_value(5);
std::cout << obj.value;
```
Ответ: <code> 5 </code>

4) Что такое горутина в Go?<br>

Ответ: <code> Легковесный поток выполнения </code>

5) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    ~A(){
        std::cout << 'A';
    }
};

class B{
public:
    ~B(){
        std::cout << 'B';
    }
};

class C: public A, public B{
public:
    ~C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> CBA </code>

6) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
};

C obj;
obj.get();
```
Ответ: <code> Ошибка </code>

7) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    int value = 1;
    B(int value){
        this->A::value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

8) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    A(){
    	value = 5;
    }
    A(int value){
    	value = 9;
    }
};

class B: public A{
public:
    B(int value):A(value){};
};

B obj(1);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

9) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    ~A(){
        std::cout << 'A';
    }
};

class B{
public:
    ~B(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    ~C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> CAB </code>

10) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    void set_value(int value){
        this->value = value;
    }
};

class B: public A{
public:
    int value = 1;
};

B obj;
obj.set_value(5);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

11) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    void get(){
        std::cout << 'C';
    }
};

C obj;
obj.get();
```
Ответ: <code> C </code>

12) Что из перечисленного является объявлением конструктора копирования класса <code>SomeClass</code>?<br>

Ответ: <code> SomeClass(const SomeClass& other); </code>

13) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
};

class C: public B, public A{
};

C obj;
obj.get();
```
Ответ: <code> A </code>

14) Как заблокировать мьютекс в Go?<br>

Ответ: <code> mutex.Lock() </code>

15) Что такое мьютекс в Go?<br>

Ответ: <code> Механизм синхронизации доступа горутин к общим ресурсам </code>

16) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: private A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

17) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
class A{
private:
    int valueA = 1;
};

class B: public A{
public:
    int valueB = 5;
};
```
Ответ: <code> поле не доступно </code>

18) Что из перечисленного является объявлением конструктора перемещения класса <code>SomeClass</code>?<br>

Ответ: <code> SomeClass(SomeClass&& other); </code>

19) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    A(int value){
        this->value = value;
    }
    int value = 1;
};

struct B: A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

20) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    A(){
        std::cout << 'A';
    }
};

class B{
public:
    B(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ: <code> Ничего </code>

21) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
public:
    void get(){
        B::get();
    }
};

C obj;
obj.get();
```
Ответ: <code> B </code>

22) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    B(int value){}
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> 1 </code>

23) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    A(){
    	value = 5;
    }
    A(int value){
    	this->value = 9;
    }
};

class B: public A{
public:
    B(int value):A(value){};
};

B obj(1);
std::cout << obj.value;
```
Ответ: <code> 9 </code>

24) Как запустить горутину в Go?<br>

Ответ: <code> go funcName() </code>

25) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    A(){
        std::cout << 'A';
    }
};

class B{
public:
    B(){
        std::cout << 'B';
    }
};

class C: public A, public B{
public:
    C(){
        std::cout << 'C';
    }
};

C obj();
```
Ответ: <code> Ничего </code>

26) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
};

class B{
public:
    int value = 5;
};

class C: public A, public B{
public:
    int value = 9;
};

C obj;
std::cout << obj.value;
```
Ответ: <code> 9 </code>

27) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ: <code> 5 </code>

28) Что будет выведено на экран в результате работы этого кода?
```cpp
#include <iostream>

void foo(int& a){
    std::cout << "+" << std::endl;
}

void foo(int&& a){
    std::cout << "-" << std::endl;
}

int main(){
    int a = 4;
    foo(a + 1);
}
```
Ответ: <code> - </code>

29) Как разблокировать мьютекс в Go?<br>

Ответ: <code> mutex.Unlock() </code>

30) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
class A{
public:
    int valueA = 1;
};

class B: private A{
public:
    int valueB = 5;
};
```
Ответ: <code> private </code>

31) Как обозначается l-value ссылка на значение типа int в С++?<

Ответ: <code> int& </code>

32) Дан фрагмент кода на языке С++. Какой модификатор доступа у <code>valueA</code> в классе <code>B</code> ?
```cpp
struct A{
    int valueA = 1;
};

class B: protected A{
public:
    int valueB = 5;
};
```
Ответ: <code> protected </code>

33) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
};

class B{
public:
    int value = 5;
};

class C: public A, public B{
};

C obj;
std::cout << obj.value;
```
Ответ: <code> Ошибка </code>

34) Какие из следующих вариантов использования мьютекса в Go являются правильными (считаем, что в процессе работы с данными ошибки быть не может)?<br>

Ответ:
```cpp
func foo() {
    mutex.Lock()
    defer mutex.Unlock()
    // работа с данными
}
```
```cpp
func foo() {
    mutex.Lock()
    // работа с данными
    mutex.Unlock()
}
```

35) Что будет выведено на экран в результате работы этого кода?
```cpp
#include <iostream>

void foo(int& a){
    std::cout << "+" << std::endl;
}

void foo(int&& a){
    std::cout << "-" << std::endl;
}

int main(){
    int a = 4;
    foo(a);
}
```
Ответ:<code> + </code>

36) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    A(){
        std::cout << 'A';
    }
};

class B{
public:
    B(){
        std::cout << 'B';
    }
};

class C: public A, public B{
public:
    C(){
        std::cout << 'C';
    }
};

C obj;
```
Ответ:<code> ABC </code>

37) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    int value = 1;
    A(){
    	value = 5;
    }
    A(int value){
    	value = 9;
    }
};

class B: public A{
public:
    B(int value){};
};

B obj(1);
std::cout << obj.value;
```
Ответ:<code> 5 </code>

38) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B, public A{
};

C obj;
obj.get();
```
Ответ:<code> Ошибка </code>

39) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
struct А{
    int value = 1;
};

struct B: A{
    int value = 1;
    B(int value){
        this->value = value;
    }
};

B obj(5);
std::cout << obj.value;
```
Ответ:<code> 5 </code>

# Ответы на вопросы из 4 теста Чабанова

## Вопросы
1) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << a;
}

void print(std::string a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 0 </code>

2) Дан фрагмент кода на С++. Как инстанцировать данный шаблон?
```cpp
template<typename T>
T foo(T a, T b){
    auto res = a + b;
    return res;
}
```
Ответ: <code> foo<int>(3.0, 0.1415); </code><br>
<code> foo(3, 0); </code><br>
```cpp
foo<double>(3, 0.1415);
```
```cpp
foo<int>(3.0, 0.1415);
```


3) Язык С++. Какой модификатор доступа у <code>some_field</code>?
```cpp
struct SomeClass{
    int some_field;
};
```
Ответ: <code> public </code>

4) Есть ли в языке Go возможность указать параметру значение по умолчанию?<br>

Ответ: <code> Нет </code>

5) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
class Point{
    ~Point(){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
Ответ: <code> Ошибка. Не доступен деструктор </code>

6) Есть ли в языке С++ механизм перегрузки функций?<br>

Ответ: <code> Да </code>

7) Дана функция на языке С++. Выберите всё варианты, которые являются допустимым объявлением этой функции:
```cpp
void print(int x, int y=10){
    std::cout << "x: " << x << '\n';
    std::cout << "y: " << y << '\n';
}
```
Ответ: 
```cpp
void print(int, int);
```
```cpp
void print(int x, int y);
```

8) Язык Go. Выберите все ключевые слова которые являются квалификаторами доступа.<br>

Ответ: <code> В Go нет ключевых слов-квалификаторов доступа </code>

9) Есть ли в языке С++ возможность указать параметру значение по умолчанию?<br>

Ответ: <code> Да </code>

10) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << a;
}

void print(double& a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 99 </code>

11) Есть ли в языке Go механизм перегрузки функций?<br>

Ответ: <code> Нет </code>

12) Язык С++. Член класса расположен в секции с модификатором доступа <code>private</code>. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов класса </code>

13) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(const int  a){
    std::cout << -a;
}

void print(int a){
    std::cout << a;
}

int main()
{
    int i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

14) Язык С++. Член класса расположен в секции с модификатором доступа protected. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов класса </code><br>
<code> Можно использовать в коде методов наследников </code>

15) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
T sum(T a, T b){
    int res = a + b;
    return res;
}

int main()
{
    std::cout << sum(3.0, 0.1415);
}
```
Ответ: <code> 3 </code>

16) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    int i = 10;
    print(i);
}
```
Ответ: <code> 20 </code>

17) Язык С++. Член класса расположен в секции с модификатором доступа <code>public</code>. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов наследников </code><br>
<code> Можно использовать в коде методов класса </code><br>
<code> Можно использовать в коде не относящихся к классу функций </code>

18) Код на С++. Требуется запретить доступ к деструктору класса <code>Point</code> из внешнего кода, как это можно сделать?<br>

Ответ: <code> private: ~Point(); </code>

19) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
class Point{
    char i;
public:
    ~Point(char val){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
Ответ: <code> Ошибка. У деструктора не может быть параметра </code>

20) Код на С++. Сколько деструкторов может быть у класса?<br>

Ответ: <code> Только 1 </code>

21) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << -a;
}

void print(double a){
    std::cout << a;
}

void print(bool a);

int main()
{
    bool i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

22) Язык С++. Какой модификатор доступа у <code>some_field</code>?
```cpp
class SomeClass{
    int some_field;
};
```
Ответ: <code> private </code>

23) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    float i = 10;
    print(i);
}
```
Ответ: <code> 30 </code>

24) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << -a;
}

void print(double a){
    std::cout << a;
}

int main()
{
    bool i = 10;
    print(i);
}
```
Ответ: <code> -1 </code>

25) Дан фрагмент кода на С++. Какой прототип соответствует созданной по шаблону функции?
```cpp
template<typename T, typename U>
U sum(T a, U b){
    auto res = a + b;
    return res;
}

int main(){
    auto i = sum(3, 0.1415);
    std::cout << i;
}
```
Ответ:
```cpp
double sum(int a, double b);
```

26) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
void print(T a){
    std::cout << a;
}

void print(int a){
    std::cout << a;
}

void print(float a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 0.5 </code>

27) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
void print(T a){
    std::cout << "T";
}

template<typename T>
void print(std::vector<T> a){
    std::cout << "vector<T>";
}

int main()
{
    std::vector<std::vector<int> > i;
    print(i);
}
```
Ответ: 
```c
vector<T> 
```

28) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    unsigned int i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

29) Выберите все перегрузки функции <code>void print(double a);</code><br>

Ответ:
```cpp
void print(std::vector<double> a);
```
```cpp
void print(double a, int b);
```
```cpp
void print(float a);
```

30) Дана функция на языке С++. Выберите всё варианты, которые являются допустимым объявлением этой функции:
```cpp
void print(int x, int y){
    std::cout << "x: " << x << '\n';
    std::cout << "y: " << y << '\n';
}
```
Ответ:
```cpp
void print(int, int);
```
```cpp
void print(int, int=10);
```
```cpp
void print(int x, int y);
```
```cpp
void print(int x=10, int y=10);
```
```cpp
void print(int x, int y=5);
```
```cpp
void print(int x, int y=10);
```

31) Язык С++. Что из перечисленного может быть использовано в качестве объявления деструктора для класса <code>SomeClass</code>?<br>

Ответ:<code>~SomeClass(){}</code><br>
<code>~SomeClass() = default;</code>

32) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
T sum(T a, T b){
    auto res = a + b;
    return res;
}

int main()
{
    std::cout << sum(3.0, 0.1415);
}
```
Ответ: <code> 3.1415 </code>


# Ответы на вопросы из 2 теста Чабанова

## Вопросы
1) Дан фрагмент кода на языке С++. Будет ли код работать?
```cpp
int main(){
    print(1, 2, " ");
}

void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ: <code> Нет. Ошибка на этапе компиляции </code>

2) Язык Go. Выберите все верные утверждения касающиеся оператора return в теле функции:<br>

Ответ: <code>Может отсутствовать в некоторых функциях;</code></br>
<code>Может быть указан в теле функции более одного раза;</code></br>
<code>Прерывает исполнение функции и возвращает поток исполнения в точку вызова;</code>

3) Код на языке С++. Выберите все позиции (отмеченные комментарием) в которых разрешено объявлять функцию sum.
```cpp
// 1
#include <iostream>
// 2
int main(){
    // 3
    std::cout << "Don't blink" << std::endl;
    // 4
}
// 5

int sum(int a, int b){
    // 6
    return a + b;
    // 7
}
// 8
```
Ответ: <code> 1 2 3 4 5 6 7 8 </code>

4) Дана функция на языке С++. Выберите все варианты вызова данной функции, при которых произойдёт обмен значениями переменных x и y. Переменные обвялены следующим образом: int x = 1; и int y = 2;:
```cpp
void swap(int& a, int& b){
    int t = a;
    a = b;
    b = t;
}
```
Ответ: <code> swap(y, x); </code><br>
<code> swap(x, y); </code>

5) Дана функция на языке С++. Выберите все варианты вызова данной функции, при которых произойдёт обмен значениями переменных x и y. Переменные объявлены следующим образом: int x = 1; и int y = 2;:
```cpp
void swap(int* a, int* b){
    int t = *a;
    *a = *b;
    *b = t;
}
```
Ответ: <code>swap(&x, &y);</code><br>

6) Дан фрагмент код на на языке Go. Что будет на экране в результате его выполнения:
```go
package main
import "fmt"

func print(){
    fmt.Println(a)
}

func main(){
    a := 10
    print()
}
```
Ответ: <code>Ошибка во время компиляции;</code>

7) Язык С++. Выберите все верные утверждения касающиеся оператора return в теле функции:<br>

Ответ: <code>Может отсутствовать в некоторых функциях;</code></br>
<code>Прерывает исполнение функции и возвращает поток исполнения в точку вызова;</code></br>
<code>Может быть указан в теле функции более одного раза;</code>

8) Дана функция на языке Go. Выберите все верные утверждения:
```go
func min(a, b int) int{
    if a < b {
        return a
    }
    return b
}
```
При условии, что функция вызывается так:
```go
x, y := 10, 0
min(x, y)
```
Ответ: <code>Параметры функции получает локальную копию аргументов;</code><br>
<code>Функция принимает аргументы по значению;</code>

9) Дана функция на языке Go. Выберите все варианты вызова данной функции, при которых произойдёт обмен значениями переменных x и y. Переменные объявлены следующим образом: x := 1; и y := 2;:
```go
func swap(a, b int){
    var t int = a
    a = b
    b = t
}
```
Ответ: <code>Эта функция не может выполнить требуемое действие;</code>

10) Дана функция на языке С++. Выберите все верные утверждения:
```cpp
int mydiv(int a, int b){
    int result = a % b;
    return result;
}
```
При условии, что функция вызывается так:
```cpp
int x = 9, y = 2;
int z = mydiv(x, y);
```
Ответ: <code> В точке вызова будет создана копия локальной переменной result или произойдёт оптимизация (RVO, NRVO);</code><br>
<code> Функция возвращает результат по значению;</code>

11) Дана функция на языке С++. Выберите все верные утверждения:
```cpp
int min(int& a, int& b){
    return a < b ? a : b;
}
```
При условии, что функция вызывается так:
```cpp
int x = 10, y = 0;
min(x, y);
```
Ответ: <code>Функция принимает аргументы по ссылке;</code><br>
<code> Параметры функции становятся вторыми именами для переменных x и y;</code>

12) Код на языке С++. Выберите все позиции (отмеченные комментарием) в которых можно объявить функцию sum, чтобы сделать код рабочим.
```cpp
// 1
#include <iostream>
// 2
int main(){
    // 3
    std::cout << sum(2, 2) << std::endl;
    // 4
}
// 5

int sum(int a, int b){
    // 6
    return a + b;
    // 7
}
// 8
```
Ответ: <code>1 2 3</code>

13) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

int main() {
    std::cout << i;
    int i = 2;
    {
        std::cout << i;
        int i = 3;
    }
    std::cout << i;
}
```
Ответ: <code>122</code>

14) Язык Go. Функция задана сигнатурой:
```go
func maxmin(a, b float64) (max float64, min float64)
```
Каким образом можно выйти из этой функции?<br>

Ответ: <code>return без значений</code><br>
<code>return с двумя значениями</code>

15) Дан фрагмент код на на языке С++. Что будет на экране в результате его выполнения:
```cpp
void print(){
    std::cout << a;
}

int main(){
    int a = 10;
    print();
}
```
Ответ: <code>Ошибка во время компиляции;</code>

16) Язык Go. Выберите сигнатуры всех функций, для которых обязательно наличие оператора return в теле:<br>

Ответ:
```go
func next() float64
```
```go
func strip(src *string) *string
```
```go
func sum(a, b int) int
```

17) Сколько раз, в коде на языке С++, можно писать определение этой функции?
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ: <code>Только один раз в программе;</code>

18) Дана функция на языке Go. Выберите все варианты вызова данной функции, при которых произойдёт обмен значениями переменных x и y. Переменные объявлены следующим образом: x := 1; и y := 2;:
```cpp
func swap(a, b *int){
    var t int = *a
    *a = *b
    *b = t
}
```
Ответ: <code>swap(&x, &y);</code>

19) Дана функция на языке С++. Выберите всё варианты, которые являются вызовом этой функции:
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ: 
```cpp
print(a, b, sep);
```

20) Сколько раз, в коде на языке С++, можно писать объявление этой функции?
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ: <code>Любое количество раз;</code>

21) Дана функция на языке Go. Выберите все верные утверждения:
```go
func mydiv(a, b int) int{
    result := a % b
    return result
}
```
При условии, что функция вызывается так:
```go
x, y := 9, 2
z := mydiv(x, y)
```
Ответ: <code>Функция возвращает результат по значению;</code><br>
<code>В точке вызова будет создана копия локальной переменной result;</code>

22) Дана функция на языке Go. Выберите все верные утверждения:
```go
func min(a, b *int) int{
    if a < b {
        return a
    }
    return b
}
```
При условии, что функция вызывается так:
```go
x, y := 10, 0
min(&x, &y)
```
Ответ: <code>Параметры функции получают адреса, по которым расположены переменные;</code><br>
<code>Функция принимает аргументы по указателю;</code>

23) Код на языке С++. Выберите все позиции (отмеченные комментарием) в которых можно определить функцию sum, чтобы сделать код рабочим.
```cpp
// 1
#include <iostream>
// 2
int main(){
    // 3
    std::cout << sum(2, 2) << std::endl;
    // 4
}
// 5
```
Ответ: <code>1 2</code>

24) Код на языке Go. Выберите все позиции (отмеченные комментарием) в которых можно определить функцию sum, чтобы сделать код рабочим.
```go
// 1
package main
// 2
import "fmt"
// 3
func main() {
    // 4
    fmt.Println(sum(2, 2))
    // 5
}
// 6
```
Ответ: <code>3 6</code>

25) Код на языке С++. Выберите все позиции (отмеченные комментарием) в которых можно определить функцию sum, чтобы сделать код рабочим.
```cpp
int min(int a, int b){
    return a < b ? a : b;
}
```
При условии, что функция вызывается так:
```cpp
int x = 10, y = 0;
min(x, y);
```
Ответ: <code>Параметры функции получает локальную копию аргументов;</code><br>
<code>Функция принимает аргументы по значению;</code>

26) Дан фрагмент кода на Go. Что будет напечатано в результате его выполнения?
```go
package main
import "fmt"

var i int = 1

func main() {
    fmt.Print(i)
    var i int = 2;
    {
        fmt.Print(i)
        var i int = 3;
    }
    fmt.Print(i)
}
```
Ответ: <code>Ошибка</code>

27) Дан фрагмент кода на Go. Что будет напечатано в результате его выполнения?
```cpp
void print(short a, short b, std::string sep);

int main(){
    print(1, 2, " ");
}

void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ: <code>Да. Ошибок нет;</code>

28) Дана функция на языке Go. Выберите все верные утверждения:
```go
func mydiv(a, b int) *int{
    result := a % b
    return &result
}
```
При условии, что функция вызывается так:
```go
x, y := 9, 2
z := mydiv(x, y)
```
Ответ: <code>Функция возвращает результат по указателю;</code><br>
<code>В точке вызова будет получен адрес по которому лежит переменная result;</code>

29) Дан фрагмент кода на языке С++. Будет ли код работать?
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}

int main(){
    print(1, 2, " ");
}
```
Ответ: <code>Да. Ошибок нет;</code>

30) Дана функция на языке С++. Выберите все варианты вызова данной функции, при которых произойдёт обмен значениями переменных x и y. Переменные объявлены следующим образом: int x = 1; и int y = 2;:
```cpp
void swap(int a, int b){
    int t = a;
    a = b;
    b = t;
}
```
Ответ: <code>Эта функция не может выполнить требуемое действие;</code>

31) Язык Go. Функция div должна вернуть вернуть 2 значения. Выберите все допустимые сигнатуры:<br>

Ответ: <code>func div(a, b float64) (float64, error)</code><br>
<code>func div(a, b float64) (res float64, err error)</code>

32) Дана функция на языке С++. Выберите всё варианты, которые являются определением этой функции:
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ:
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```

33) Дана функция на языке С++. Выберите все верные утверждения:
```cpp
int* mydiv(int a, int b){
    int result = a % b;
    return &result;
}
```
При условии, что функция вызывается так:
```cpp
int x = 9, y = 2;
int* z = mydiv(x, y);
```
Ответ: <code>В точке вызова будет получен адрес по которому лежала переменной result во время работы функции mydiv;</code><br>
<code>Функция возвращает результат по указателю;</code>

34) Язык С++. Выберите прототипы функций, для которых обязательно наличие оператора return в теле:<br>

Ответ:
```cpp
std::string& strip(std::string& src);
```
```cpp
double next();
```
```cpp
int sum(int a, int b);
```


35) Дана функция на языке С++. Выберите все верные утверждения:
```cpp
int min(int* a, int* b){
    return *a < *b ? *a : *b;
}
```
При условии, что функция вызывается так:
```cpp
int x = 10, y = 0;
min(&x, &y);
```
Ответ: <code>Параметры функции получают адреса, по которым расположены переменные;</code><br>
<code>Функция принимает аргументы по указателю;</code>

36) Код на языке Go. Выберите все позиции (отмеченные комментарием) в которых можно определить функцию sum.
```go
// 1
package main
// 2
import "fmt"
// 3
func main() {
    // 4
    fmt.Println("Hello World")
    // 5
}
// 6
```
Ответ: <code>6 3</code><br>

37) Дана функция на языке С++. Выберите все верные утверждения:
```cpp
int& mydiv(int a, int b){
    int result = a % b;
    return result;
}
```
При условии, что функция вызывается так:
```cpp
int x = 9, y = 2;
int z = mydiv(x, y);
```
Ответ: <code>Функция возвращает результат по ссылке;</code><br>
<code>В точке вызова будет попытка доступа к не существующей локальной переменной result;</code>

38) Дана функция на языке С++. Выберите всё варианты, которые можно добавить в код в качестве объявления этой функции:
```cpp
void print(short a, short b, std::string sep){
    std::cout << a << sep << b;
}
```
Ответ:
```cpp
auto print(short a, short b, std::string sep) -> void;
```
```cpp
void print(short, short, std::string);
```
```cpp
void print(short b, short a, std::string stop);
```
```cpp
void print(short a, short b, std::string sep);
```

39) Код на языке С++. Выберите все позиции (отмеченные комментарием) в которых можно определить функцию sum.
```cpp
// 1
#include <iostream>
// 2
int main(){
    // 3
    std::cout << "Don't blink" << std::endl;
    // 4
}
// 5
```
Ответ:<code>1 2 5</code><br>

# Ответы на вопросы из 3 теста Чабанова

## Вопросы
1) Дан фрагмент кода на С++. Выберите все верные утверждения:
```cpp
int i = 10;
int j = 20;
int* pi = &i;
pi = &j;
*pi = 30;
```
Ответ: <code> j станет равно 30 </code>

2) Язык С++. Дан код:
```cpp
int array[3] = {5, 1, 3};
int* i = &array[1];
++*i;
std::cout << i[0];
```
Что будет выведено в результате?<br>
Ответ: <code> 2 </code>

3) Язык С++. Дан код:
```cpp
int array[3] = {5, 1, 3};
int* i = &array[1];
cout << i[-1];
```
Что будет выведено в результате?<br>
Ответ: <code> 5 </code>

4) Дан фрагмент кода на С++:
```cpp
int* i = new int{10};
```
Выберите все верные утверждения.<br>
Ответ: <code> new выделяет память под переменную в куче </code>

5) Дан фрагмент кода на С++:
```cpp
struct Point{
    short x;
    int y;
} p{0, 0};

Point* ptr = &p;
```
Выберите все варианты позволяющие получить доступ к полю x структуры p.<br>
Ответ: <code> ptr->x; </code><br>
<code> (*ptr).x; </code>

6) Язык С++. Переменная-указатель p хранит адрес некоторой переменной <code>i</code>. Как получить доступ к значению переменной <code>i</code> по её адресу?<br>

Ответ: <code> Применить к p оператор разыменования </code>

7) Язык С++. Выберите все верные утверждения:<br>

Ответ: <code> sizeof(int *) == sizeof(double *) </code><br>
<code> sizeof(int *) == sizeof(vector<int*> *) </code><br>
<code> sizeof(int *) == sizeof(vector<int> *) </code><br>
<code> sizeof(int *) == sizeof(void *) </code>

8) Дан фрагмент кода на языке С++:
```cpp
int b[8][4][2];
```
Выберите все допустимые выражения.<br>
Ответ: <code> int (*i)[4][2] = b; </code>

9) Дана функция на С++:
```cpp
int* foo(){
    int a = 10;
    return &a;
}
```
Выберите все верные утверждения о выражении:<br>
```cpp
int* p = foo();
```
Ответ: <code> p - висячий указатель </code>

10) Дан фрагмент кода на С++:
```cpp
struct A{
};

struct B: A{
};

struct C: B{
};

A objectA;
B objectB;
C objectC;
```
Выберите все выражения, которые не вызовут ошибки.<br>

Ответ: <code> A* ab = &objectB; </code><br>
<code> B* bc = &objectC; </code><br>
<code> A* ac = &objectC; </code>

11) Язык С++. Дан код:
```cpp
int array[3] = {5, 1, 3};
int* i = &array[1];
cout << *(i+1);
```
Что будет выведено в результате?<br>

Ответ: <code> 3 </code>

12) Язык С++. Выберите все верные утверждения.
```cpp
int const i = 1;
```
Что будет выведено в результате?<br>

Ответ: <code> указатель на i может быть объявлен как const int * pi = &i; </code><br>
<code> указатель на i может быть объявлен как int const * const pi = &i; </code><br>
<code> указатель на i может быть объявлен как int const * pi = &i; </code>

13) Язык С++. Известно, что размер типа int в системе равен 4 байта. Дан код:
```cpp
int a = 10;
int* i = &a;
i += 10;
```
На сколько байт сдвинется указатель?<br>

Ответ: <code> 40 </code>

14) Язык С++. Известно, что переменные объявлены следующим образом:
```cpp
int i = 10;
int *p = &i;
```
Выберите все верные утверждения.<br>

Ответ: <code> p - это указатель на int </code>

15) Каким образом можно преобразовать <code>int* i</code> в <code>double* j</code> ?

Ответ: <code> Это невозможно сделать указанными способами </code>

16) Язык С++. Какой тип данных у переменной <code>pj</code>?
```cpp
int i = 10;
int* pi = &i, pj;
```
Ответ: <code> Просто int </code>

17) Дан фрагмент кода на языке С++:
```cpp
int* p = new int{5};
```
Ответ: <code> delete p; </code>

18) Язык С++. Дан код:
```cpp
int array[3] = {5, 1, 3};
int* i = &array[1];
*++i;
std::cout << i[0];
```
Что будет выведено в результате?<br>

Ответ: <code> 3 </code>

19) Дан фрагмент кода на языке С++. Выберите верные утверждения:
```cpp
int const * p;
```

Ответ: <code> p - это указатель на константный int </code>

20) Язык С++. Дана переменная <code>int i = 10;</code> выберите выражения НЕ вызывающие ошибки:<br>

Ответ: <code> void* a = &i; </code><br>
<code> int* a = &i; </code>

21) Дан фрагмент кода на С++:
```cpp
struct Point{
    short x;
    int y;
} p{0, 0};

Point& ptr = p;
```
Выберите все варианты позволяющие получить доступ к полю x структуры p.<br>

Ответ: <code> ptr.x; </code>

22) Язык С++. Нулевой указатель должен быть инициализирован значением:<br>

Ответ: <code> nullptr </code>

23) Дан фрагмент кода на языке С++:
```cpp
int* p = new int[5] {1, 2, 3, 4, 5};
```
Какой оператор нужно использовать, чтобы освободить выделенную память?<br>

Ответ: <code> delete[] p; </code>

24) Язык С++. Выберите все верные утверждения.
```cpp
int const * const pi = &i;
```
Ответ: <code> i может быть объявлена как int i; </code><br>
<code> Значение pi нельзя менять </code><br>
<code> i может быть объявлена как int const i; </code><br>

25) Язык С++. На какой знак нужно заменить символ # в данном фрагменте кода, чтобы pj стал указателем на int?
```cpp
int i = 10, j = 20;
int* pi, #pj = &j;
```
Ответ: <code> # заменить на * </code>

26) Язык С++. Даны два указателя int* a и int* b. Известно, что в системе тип int занимает 4 байта, а расстояние между указателями 16 байт. Какое число выведется на экран в результате команды:
```cpp
cout << b - a;
```
Ответ: <code> 4 </code>

27) Дан фрагмент кода на С++. Выберите все верные утверждения:
```cpp
int i = 10;
int* pi = &i;
int* pj = &i;
```
Ответ: <code> При помощи указателя pj можно получить доступ к переменной i </code><br>
<code> Выражение pi == pj истинно </code><br>
<code> При помощи указателя pi можно получить доступ к переменной i </code>

28) Дан фрагмент кода на языке С++:
```cpp
int i = 10;
int *p = &i;
std::cout << *p;
```
Ответ: <code> Результат выражения *p в 3й строке - целое число </code><br>
<code> p - хранит адрес переменной i </code><br>
<code> Результат выражения &i во 2й строке - адрес </code><br>
<code> На экране появится 10 </code>

29) Язык С++. Известно, что переменные объявлены следующим образом:
```cpp
int i = 10;
int *p = &i;
```
Ответ: <code> * - часть описания типа переменной </code><br>
<code> & - оператор взятия адреса </code>

30) Язык С++. Указатель объявлен следующим образом:<br>
```cpp
int* i;
```
Какие из следующих утверждений верные?<br>

Ответ:
```cpp
int one;
i = &one;
```
```cpp
int one[10];
i = &one[0];
```
```cpp
int one[10];
i = &one;
```

31) Язык С++. Выберите все выражения НЕ приводящие к ошибке.
```cpp
int i = 10;
double k = 10;
int *a;
double *b;
```
Ответ: <code> a = &i; </code><br>
<code> *b = *a; </code><br>
<code> b = &k; </code>

32) Язык С++. Выберите все допустимые варианты создания ссылок.<br>

Ответ:
```cpp
int& b = /* инициализатор */;
```
```cpp
int (&d)[10] = /* инициализатор */;
```
```cpp
int& *f = /* инициализатор */;
```

33) Язык С++. В функцию foo передаётся переменная a, значение которой НЕ равно 10. Какие функций приведут к изменению значения a ?<br>

Ответ:
```cpp
void foo(int* i){
    *i = 10;
}
```

34) Дан фрагмент кода на С++:
```cpp
int array[7] = {-3, -2, -1, 0, 1, 2, 3};
int* p = array;
while(*p++) std::cout << '+';
```
Сколько символов '+' отобразится на экране.<br>

Ответ: <code> 3 </code>

35) Дан фрагмент кода на С++:
```cpp
int i = 10;
```
Выберите все верные утверждения.

Ответ: <code> Память под переменную выделена в сегменте данных, если она глобальная </code><br>
<code> Память под переменную выделена на стеке, если она локальная </code>

36) Дана функция на С++:
```cpp
int* foo(){
    return new int{10};
}
```
Выберите все верные утверждения о выражении:
```cpp
int* p = foo();
```
Ответ: <code> Нужно освободить память командой delete p </code><br>
 <code> p равно 10 </code><br>
  <code> *p равно 10 </code>

# Ответы на вопросы из 1 теста Чабанова


Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
for (int i = 0; i<1; i++){
    int k = 10;
    cout << i;
}
cout << k;
```
> Правильный ответ: Ошибка


Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
a := 5
b := 10

switch (b-a){
    case  5: fmt.Print("&"); break;
    case 10: fmt.Print("*"); break;
    case 15: fmt.Print("!"); break;
    default: fmt.Print("-");
}
```
> Правильный ответ: &

Дан фрагмент кода на С++. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
int a = 5;
int b = 10;
switch (b-a)
{
    case  5: std::cout << "0";
    case 10: std::cout << "1"; break;
    case 15: std::cout << "2";
    default: std::cout << "3";
}
```
> Правильный ответ: 01

Язык Go. Что делает оператор break вызванный внутри цикла?
> Правильный ответ: Прерывает выполнение цикла

Кокой тип переменных в Go предназначен для хранения логических данных?
> Правильный ответ: bool

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```cpp
for i := 0; i < 3; i++ {
    for j := 0; j < 3; j++ {
        if i == j {
            continue
        }
        fmt.Print(j)
    }
}
```
> Правильный ответ: 120201

Кокой тип переменных в С++ предназначен для хранения логических данных?
> Правильный ответ: bool

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```cpp
for i := 0; i < 10; i++ {
    for i % 3 != 0 {
        i++
    }
    fmt.Print(i)
}
```
> Правильный ответ: 0369

Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента кода?
```go
for i := 1; i < 32; i *= 2 {
    fmt.Print(i)  
} 
```
> Правильный ответ: 124816

Дан фрагмент кода на C++. Цикл будет выполнятся, пока <условие>:
```cpp
while (<условие>){
    <код>
}
```
> Правильный ответ: Верно

Язык С++. Локальная переменная создана следующим образом: Какое значение содержит переменная?
```cpp
int i;
```
> Правильный ответ: Мусорное значение

Язык Go. Локальная переменная создана следующим образом: Какое значение содержит переменная?
```go
var i int;
```
> Правильный ответ: Значение по умолчанию для типа int, т.е. 0

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int x = 5;
if (10 > x > 1) std::cout << 1;
else std::cout << 0;
```
> Правильный ответ: 0

Дан фрагмент кода на Go. Сколько раз выполнится цикл?
```cpp
k := 10
for k != 0 { 
    fmt.Print(1)
    k -= 1
}
```
> Правильный ответ: 10

Дан фрагмент кода на Go Выберите все верные утверждения.
```cpp
var a, b, c = 1, 2, 3

```
> Правильный ответ: переменная a содержит 1; переменная b содержит 2; переменная c содержит 3;

Дан фрагмент кода на C++. Сколько раз выполнится цикл?
```cpp
int k = 10;
while(--k) cout << 0;
```
> Правильный ответ: 9

Дан фрагмент кода на С++. Что будет напечатано в результате выполнения фрагмента кода:
```cpp
int a = 5;
int b = 6;
std::cout << ( (a > b)? b : a );
```
> Правильный ответ: 5

Дан фрагмент кода на С++. Что будет напечатано в результате выполнения следующего фрагмента кода:
```cpp
int a = 5;
int b = 6;
std::cout << a << ( (a > b)? " <> " : " >< " ) << b;
```
> Правильный ответ: 5 >< 6

Даны фрагменты кода на С++. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
int a = 5;
int b = 15;
switch (b-a)
{
    case  5: std::cout << "*";
    case 10:
    case 15:
    default: std::cout << "-";
}
```
> Правильный ответ: -

Выберите все значения, которые могут быть неявно (без использования оператора приведения типов) преобразованы в true. Язык С++.
> Правильный ответ: 5.0 5 -5.0 -5 

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int a = 5;
int b = 15;
if (a < b) std::cout << a;
else; std::cout << b;
```
> Правильный ответ: 515

Дан фрагмент кода на C++. Что будет выведено на экран в результате выполнения данного фрагмента кода?
```cpp
for(int i=0; i < 20; i += 3) cout << i;
```
> Правильный ответ: 0369121518

Язык C++. Выберите правильную форму оператора do while
```cpp
do{
    <код>
}while(<условие>);
```
> Правильный ответ: код выше

Дан фрагмент кода на C++. Что будет напечатано в результате выполнения следующего фрагмента кода?
```cpp
int i = 0;
do{
    i++;
    cout << i;
}while(i<10);
```
> Правильный ответ: 12345678910

Дан фрагмент кода на С++. Что будет напечатано в результате выполнения следующего фрагмента кода:
```cpp
std::cout << true;
```
> Правильный ответ: 1

Дан фрагмент кода на С++. Верно ли, что результатом выражения указанного ниже будет true, если известно, что: int x = -5, y = 3, z = 5;
```cpp
x && y && z > 0;
```
> Правильный ответ: Верно

Выберите все значения, которые могут быть неявно (без использования оператора приведения типов) преобразованы в true. Язык Go.
> Правильный ответ: В Go запрещено преобразование чисел в логический тип.

Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента кода?
```go
for i := 0; i < 20; i += 3 {
    fmt.Print(i)  
} 
```
> Правильный ответ: 0369121518

Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
int i = 0;
for (i = 5; i<11; i++)
  cout << i;
cout << i;
```
> Правильный ответ: 567891011

Дан фрагмент кода на С++. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
int x = 5;
(x != 5) && (std::cout << 11);
std::cout << x;
```
> Правильный ответ: 5

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения фрагмента кода: 
```go
a := 5
b := 15
if a = 3 {
    fmt.Print(a)
} else {
    fmt.Print(b)
}
```
> Правильный ответ: Ошибка

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int a = 0, b = 10;
if (b <= 5 <= a) std::cout << 1;
else std::cout << 0;
```
> Правильный ответ: 1

Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
for (int i = 0; i<11; i++)
  cout << i;
cout << i;
```
> Правильный ответ: Ошибка компиляции

Язык С++. Требуется создать локальную переменную i. Выберите все способы которыми это можно сделать?
> Правильный ответ: `int i = 1;` `auto i = 1;`

Язык C++. Что делает оператор continue вызванный внутри цикла?
> Правильный ответ: Принудительный переход к следующей итерации цикла

Язык Go. Что будет доступно по имени j в следующем коде?
```go
str := "hello, world"
for i, j := range str{
    fmt.Println(i, j)
}
```
> Правильный ответ: Копия символа из строки 

Дан фрагмент кода на C++. Что будет напечатано в результате выполнения данного фрагмента кода?
```cpp
for(int i=0; i <10; i++){
    while(i % 3) i++;
    cout << i;
}
```
> Правильный ответ: 0369

Язык C++. Существует ли форма оператора break позволяющая выйти сразу из 2х или более вложенных друг в друга циклов?
> Правильный ответ: Нет

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int x = 5;
std::cout << (x || x*x);
```
> Правильный ответ: 1

Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
int i = 0;
for (int i = 0, i<11, i++)
  cout << i;
cout << i;
```
> Правильный ответ: Ошибка компиляции

Дан фрагмент кода на С++. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
int a = 5;
int b = 10;
switch (b-a)
{
    case  5: std::cout << "&"; break;
    case 10: std::cout << "*"; break;
    case 15: std::cout << "!"; break;
    default: std::cout << "-";
}
```
> Правильный ответ: &

Дан фрагмент кода на C++. Что будет выведено на экран в результате выполнения данного фрагмента кода?
```cpp
for(int i=1; i < 32; i *= 2) cout << i;
```
> Правильный ответ: 124816

Дан фрагмент кода на Go. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
for i := 0; i < 1; i++ {
    k := 10
    fmt.Print(i)
}
fmt.Print(k)
```
> Правильный ответ: Ошибка

Язык C++. Что делает оператор break вызванный внутри цикла?
> Правильный ответ: Прерывает выполнение цикла

Дан фрагмент кода на C++. Что будет напечатано в результате выполнения данного фрагмента кода?
```cpp
int k = 10;
while(--k){
    if (k == 5) continue;
    cout << k;
}
```
> Правильный ответ: 98764321

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int x = 5;
std::cout << (x && x*x);
```
> Правильный ответ: 1

Даны фрагменты кода на Go. Результатом каких выражений будет true?
> Правильный ответ: `!false != false` `5 == 4 || 10 < 11`

Дан фрагмент кода на C++. Сколько раз выполнится цикл?
```cpp
int k = 10;
while(k--) cout << 0;
```
> Правильный ответ: 10

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int a = 50;
int b = 15;
if (a > b) std::cout << a;
else; std::cout << b;
```
> Правильный ответ: 5015

Дан фрагмент кода на Go. Что будет выведено на экран после выполнения фрагмента кода?
```go
i := 0
for i = 5; i < 11; i++{
    fmt.Print(i)
}
fmt.Print(i)
```
> Правильный ответ: 567891011

Дан фрагмент кода на C++. Что будет выведено в результате выполнения следующего фрагмента кода:
```cpp
for (int i = 0; i < 4; ++i)
{
   switch (i)
   {
        case 0  : cout << "0";
        case 1  : cout << "1"; continue;
        case 2  : cout << "2"; break;
        default : cout << "D"; break;
   }
   cout << ".";
}
```
> Правильный ответ: 0112.D.

Даны фрагменты кода на С++. Что отобразится на экране после его выполнения?
```cpp
int x = 5;
(x != 5) || std::cout << 11;
std::cout << x;
```
> Правильный ответ: 115

Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
int i = 0;
for (int i = 5; i<11; i++)
  cout << i;
cout << i;
```
> Правильный ответ: 56789100

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```go
OUTER:
for i := 0; i < 3; i++ {
    for j := 0; j < 3; j++ {
        if i == j {
            continue OUTER
        }
        fmt.Print(j)
    }
}
```
> Правильный ответ: 001

Язык Go. Существует ли форма оператора break позволяющая выйти сразу из 2х или более вложенных друг в друга циклов?
> Правильный ответ: Да, break с меткой 

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```go
OUTER:
for i := 0; i < 3; i++ {
    for j := 0; j < 3; j++ {
        if i == 1 {
            break OUTER
        }
        fmt.Print(j)
    }
}
```
> Правильный ответ: 012

Язык Go. Что делает оператор continue вызванный внутри цикла?
> Правильный ответ: Принудительный переход к следующей итерации цикла

Даны фрагменты кода на С++. Выберите выражения, которые НЕ вызовут ошибки во время компиляции. Переменная x объявлена следующим образом: int x = 5;
> Правильный ответ: `if (x == 5) std::cout << x; else std::cout << 0;` `if (x == 5) std::cout << 5; else if (x != 5) std::cout << 6;` `if (x == 5) ; else ;` `if (x == 5) std::cout << x; else {std::cout << 0;}`

Дан фрагмент кода на Go. Сколько раз выполнится цикл?
```go
k := 10
for k == 0 { 
    fmt.Print(1)
    k -= 1
}
```
> Правильный ответ: 0

Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента?
```go
a := 5
b := 10
switch (b-a){
    case  5: fmt.Print("0");
    case 10: fmt.Print("1"); break
    case 15: fmt.Print("2");
    default: fmt.Print("3");
}
```
> Правильный ответ: 0 

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```go
k := 10
for k > 0 {
    k -= 1
    if k == 5 {
        continue
    }
    fmt.Print(k)
}
```
> Правильный ответ: 987643210

Даны фрагменты кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента?
```go
a := 5
b := 15

switch (b-a){
    case  5: fmt.Print("*");
    case 10: 
    case 15: 
    default: fmt.Print("-");
}
```
> Правильный ответ: Ничего

Дан фрагмент кода на C++. Что будет выведено на экран после выполнения фрагмента кода?
```cpp
int i = 0;
for (int i = 5; i<11; i++);
  cout << i;
cout << i;
```
> Правильный ответ: 00

Дан фрагмент кода на Go. Что будет напечатано в результате выполнения данного фрагмента кода?
```go
for i := 0; i < 3; i++ {
    for j := 0; j < 3; j++ {
        if i == 1 {
            break
        }
        fmt.Print(j)
    }
}
```
> Правильный ответ: 012012

Даны фрагменты кода на С++. Результатом каких выражений будет true?
> Правильный ответ: `5 == 4 || 10 < 11` `!0 != 0`

Даны фрагменты кода на С++. Выберите выражения, которые НЕ вызовут ошибки во время компиляции. Переменная x объявлена следующим образом: int x = 5;
> Правильный ответ: `if (x = 5) {};` `if (x==5) std::cout << x;` `if (1) {std::cout << x;}` `if (x < 2);`

Дан фрагмент кода на С++ `int a, b, c = (1, 2, 3);` Выберите все верные утверждения.
> Правильный ответ: `переменная a содержит мусорное значение;` `переменная b содержит мусорное значение;` `переменная c содержит 3;`

Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента?
```go
var x = 5
if 10 > x > 1 {
    fmt.Print(1)
}else{
    fmt.Print(0)  
} 
```
> Правильный ответ: Ошибка

Даны фрагменты кода на Go. Выберите выражения, которые НЕ вызовут ошибки во время компиляции. Переменная x объявлена следующим образом: var x = 5
> Правильный ответ: `if x == 5 {fmt.Print(x)}`

Дан фрагмент кода на Go. Что будет выведено в результате выполнения следующего фрагмента кода:
```go
for i := 0; i < 4; i++ {
   switch (i) {
        case 0  : fmt.Print("0")
        case 1  : fmt.Print("1"); continue
        case 2  : fmt.Print("2"); break
        default : fmt.Print("D"); break
   }
   fmt.Print(".")
}
```
> Правильный ответ: 0.12.D.

Язык С++. Выберите все выражения, которые можно использовать как логические операторы И, ИЛИ, НЕ.
> Правильный ответ: `and` `&&` `not` `!` `or` `||`

Дан фрагмент кода на Go. Что будет выведено на экран после выполнения фрагмента кода?
```go
i := 0
for i := 5; i < 11; i++{
    fmt.Print(i)
}
fmt.Print(i)
```
> Правильный ответ: 56789100

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int a = 5;
int b = 15;
if (a < b); std::cout << a;
else; std::cout << b;
```
> Правильный ответ: Ошибка компиляции

Дан фрагмент кода на Go. Какие из следующих циклов являются бесконечными?
> Правильный ответ: `for i := uint8(1); i < 100; { if i == 99 { continue } fmt.Print(i) i += 1 }` `for i := uint8(1); ; i++ { fmt.Print(i) }` `for ; ; { fmt.Print(1) }` `for i := uint8(1); i<100;  { fmt.Print(i) }` `for i := uint8(1); i<100;  { fmt.Print(i) }` 

Дан фрагмент кода на С++. Что будет напечатано в результате выполнения следующего фрагмента кода:
```cpp
int a = 5;
int b = 6;
std::cout << a << ( (a > b)? 1 : " <= " ) << b;
```
> Правильный ответ: Ошибка компиляции

Язык Go. Какие из ниже перечисленных команд, НЕ являются операторами цикла в Go?
> Правильный ответ: `foreach` `do while` `while` `repeat until`

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int x = 5;
if (x = 0 || 5) std::cout << 11;
std::cout << x;
```
> Правильный ответ: 111

Дан фрагмент кода на C++. Сколько раз выполнится цикл?
```cpp
int k = 10;
do{
    cout << 0;
}while(k--);

```
> Правильный ответ: 11

Язык Go. Выберите все выражения, которые можно использовать как логические операторы И, ИЛИ, НЕ.
> Правильный ответ: `!` `&&` `||`

Дан фрагмент кода на С++. Какие из перечисленных вариантов нужно выбрать для того, чтобы результатом выражения было true? Если x задано как: int x = 5;
```cpp
(x < y != 1) && (x = 4 || z == 7);
```
> Правильный ответ: `y любое число <= 5` `z - любое`

Дан фрагмент кода на языке Go. Что будет выведено в результате его работы?
```go
str := "hello, world"
for i := range str{
    fmt.Print(i)
}
```
> Правильный ответ: 01234567891011

Дан фрагмент кода на Go. Что будет выведено на экран в результате выполнения данного фрагмента?
```cpp
a := 5
b := 10
switch (a + b){
    case  5: 
        fmt.Print("0")
        fallthrough
    case 10: 
        fmt.Print("1")
        fallthrough
    case 15: 
        fmt.Print("2")
        fallthrough
    default: 
        fmt.Print("3")
}
```
> Правильный ответ: 23

Дан фрагмент кода на C++. Что будет напечатано в результате выполнения следующего фрагмента кода?
```cpp
do{
    int i = 0;
    i++;
    cout << i;
}while(i<1);
```
> Правильный ответ: Ошибка компиляции

Язык Go. Дан фрагмент кода: `i, j := 1, 1` Требуется изменить значение переменной i. Выберите все варианты, которыми это можно сделать.
> Правильный ответ: `i, k := 2, 2` `i, j = 2, 2` 

Выберите все обязательные элементы switch в С++, только из представленных ниже. Обязательные - это такие, без которых нельзя написать switch который скомпилируется без ошибки.
> Правильный ответ: `switch` `(выражение)`

Язык C++. Какие из ниже перечисленных команд, НЕ являются операторами цикла в C++?
> Правильный ответ: `repeat until` `foreach`

Дан фрагмент кода на C++. Когда закончится данный цикл?
```cpp
int x = 0;
do{
    cin >> x;
// <полезный код НЕ изменяющий x>
}while(x != 0);
```
> Правильный ответ: Когда в цикле x станет равным 0

Язык Go. Требуется создать локальную переменную i. Выберите все способы которыми это можно сделать?
> Правильный ответ: `i := 1;` `var i int = 1;` `var i = 1;`

Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
int a = 5;
int b = 15;
if (a = 3) std::cout << a;
else std::cout << b;
```
> Правильный ответ: 3

# Ответы на вопросы из 6 теста Чабанова

## Вопросы
1) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import . "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имена объявленные в пакете name доступны для использования просто по своему имени</code>

2) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import _ "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имена объявленные в пакете name НЕ доступны для использования</code>

3) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

4) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    bool i = true;
    {
        int i = 5;
        i = !i;
    }
    std::cout << i;
}
```
> Ответ: <code>1</code>

5) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    int i = 1;
    int i = 1;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

6) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace {
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>1</code>

7) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    using namespace A;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

8) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>1</code>

9) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

10) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
        int i = 2;
    }
}

int main() {
    int i = 3;
    A::B::print();
}
```
> Ответ: <code>1</code>

11) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    int i = 1;
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

12) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace {
    int i = 1;
}

int i = 2;

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

13) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имя из пакета name можно использовать так: name.требуемое_имя</code>

14) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int A = 1;

int A(){
    return 2;
}

int main() {
    std::cout << A();
}
```
> Ответ: <code>Ошибка</code>

15) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

16) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int i = 1;

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

17) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>Ошибка</code>

18) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    using A::i;
    std::cout << i;
}
```
> Ответ: <code>1</code>

19) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace D{
    int i = 1;
}

namespace C{
    using namespace D;
    int i = 2;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

20) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;
int main() {
    int i = 1;
    std::cout << i;
}
```
> Ответ: <code>1</code>

21) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using A::i;
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>Ошибка</code>

22) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        int i = 2;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    int i = 3;
    A::B::print();
}
```
> Ответ: <code>2</code>

23) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    int i = 3;
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>3</code>

24) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    const int i = 1;
    {
        int i = i;
        std::cout << i;
    }
}
```
> Ответ: <code>Мусор. Т.к. i неинициализированная переменная</code>

25) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    std::cout << i;
}

int i = 1;
```
> Ответ: <code>Ошибка</code>

26) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int A(){
    int i = 1;
}

int main() {
    int i = 2;
    std::cout << A::i;
}
```
> Ответ: <code>Ошибка</code>

27) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    const int i = 1;
    {
        int i[i] = {};
    }
    std::cout << i;
}
```
> Ответ: <code>1</code>

28) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {    
    std::cout << i;
}
```
> Ответ: <code>2</code>

29) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

int main() {
    std::cout << i;
    int i = 2;
    {
        std::cout << i;
        int i = 3;
    }
    std::cout << i;
}
```
> Ответ: <code>122</code>

30) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    int i = 3;
    {
      using namespace A;      
      std::cout << i;
    }
}
```
> Ответ: <code>3</code>

31) Дан кода на Go. Что будет напечатано в результате его выполнения?
```cpp
package main
import "fmt"

func main() {
    fmt.Print(i)
}

var i int = 1
```
> Ответ: <code>1</code>

32) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int i = 2;

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

33) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using A::i;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

34) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
void A(){
    std::cout << i;  
}

int i = 1;

int main() {
    A();
}
```
> Ответ: <code>Ошибка</code>

35) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>1</code>

36) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    bool i = true;
    {
        int i = 5;
        i = !i;
        std::cout << i;
    }
}
```
> Ответ: <code>0</code>

37) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace D{
    int i = 1;
}

namespace C{
    using namespace D;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

38) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

39) Язык Go. Код программы написан полностью в одном файле. Какое имя пакета должно быть указано в начале файла.<br>

> Ответ: <code>main</code>

40) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

41) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import example "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имя из пакета name можно использовать так: example.требуемое_имя</code>

42) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

43) Язык Go. Может ли код пакета быть разделён на несколько .go файлов?<br>

> Ответ: <code>Да. При условии, что во всех файлах указано одно и тоже имя пакета и они лежат в одной папке</code>

44) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>1</code>

45) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << A::i;
}
```
> Ответ: <code>1</code>

46) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    int i = 3;
    namespace B {
        using C::i;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>2</code>

47) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>
