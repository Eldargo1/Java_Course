# Урок 1. Знакомство с языком программирования Java

* Для написание многострочного коментария можно использовать следущее 
```sh
/*
* тут пиешм что нужно закоментировать
/*
```
* А можно использовать класический метод это использование двойних слжшов '//' что и используется в СиШарп

* Типа данных деляться на 2 это 
- Ссылочный тип данных (это у нас Class - ы )(это те данные которые храняться в heap то есть в управляемой куче )
- Премитвный (значемый) типа данных (это те данные которые хранятся только в stack-e)(это у нас int,bool,float и.т.д)
* Создание переменной, и присваевание значение переменной тоже самое как и в СиШарп
* ДЛя вещественных типов типа - 'float ' в Java  в обьязательном порядке должны использовать суффикс 'f' пример (то есть в коные нужно ставить f)
```sh
float e = 4.4f;
```
* А в (double ) - это можно не делать потомучто по умолчанию число значение воспринимается как типа double
* типа данных bool в Java пишется как (boolean а не bool как в С#)
* Неявная типизация в Java тоже используется типа данных (Var)
* Классы-оберкти 
* В Java  что работать детально (точне использовать какие то библиотеки  для данной переменной, например как в СИШарп int.MaxValue(выводит максимальное значение и.т.д)) то нужно использовать обертку данной переменной например 
```sh
int - Integer
short - Short
long - Long
byte - Byte
float - Float
double - Double
char - Character
boolean - Boolean
```
* Операция в Java
- Присваевание: '='
- Арефмитические:'*','/', '-','%','++', '--'
- Операция сравнение:'<', '>', '==', '!=', '>=', '<='
- Логические операции:'||', '&&', '^', '!'
- ПОбитовые операции:'<<', '>>', '&', '|', '^'

* Массивы - Оброщение и заполнение создание массива такой же что и в С# 
* Многмерные массивы заполняются чуть по другому пример 
```sh
int[] array[] = new int [1][2];
```
* Получение данных из терминала тут по другому выводится результат
```sh
import java.util.Scanner;
public class Program {
 public static void main(String[] args) {
 Scanner iScanner = new Scanner(System.in);
 System.out.printf("name: ");
 String name = iScanner.nextLine();
 System.out.printf("Привет, %s!", name);
 iScanner.close();
 }
}
```

* Некоторые примитивы
```sh
import java.util.Scanner;
public class Program {
 public static void main(String[] args) {
 Scanner iScanner = new Scanner(System.in);
 System.out.printf("int a: ");
 int x = iScanner.nextInt();
 System.out.printf("double a: ");
 double y = iScanner.nextDouble();
 System.out.printf("%d + %f = %f", x, y, x + y);
 iScanner.close();
}}
```

* Проверка на соответствие получаемого типа
```sh
import java.util.Scanner;
public class Program {
 public static void main(String[] args) {
 Scanner iScanner = new Scanner(System.in);
 System.out.printf("int a: ");
 boolean flag = iScanner.hasNextInt();
 System.out.println(flag); 
 int i = iScanner.nextInt();
 System.out.println(i); 
 iScanner.close();
 } }
 ```

 * Форматированный вывод
 ```sh
public class Program {
 public static void main(String[] args) {
 int a = 1, b = 2;
 int c = a + b;
 String res = a + " + " + b + " = " + c;
 System.out.println(res);
 }
}
```
* В этом методе вывода результата на экран мы получается передали данные с int в string  и вывели на экран результат 

* Либо же так 
```sh
ublic class Program {
 public static void main(String[] args) {
 int a = 1, b = 2;
 int c = a + b;
 String res = String.format("%d + %d = %d \n", a, b, c);
 System.out.printf("%d + %d = %d \n", a, b, c);
 System.out.println(res);
 }
}
```

* Виды спецификаторов 
```sh
%d: целочисленных значений
%x: для вывода шестнадцатеричных чисел
%f: для вывода чисел с плавающей точкой
%e: для вывода чисел в экспоненциальной форме, 
например, 3.1415e+01
%c: для вывода одиночного символа
%s: для вывода строковых значений
```

* Управляющие конструкции:условный оператор
```sh
public class Program {
 public static void main(String[] args) {
 int a = 1;
 int b = 2;
 int c;
 if (a > b) {
 c = a;
 } else {
 c = b;
 }
 System.out.println(c);
 }
}

```
* А можно написать так 
```sh
public class Program {
 public static void main(String[] args) {
 int a = 1;
 int b = 2;
 int c = 0;
 if (a > b) c = a;
 if (b > a) c = b;
 System.out.println(c);
 }
}
```