В предыдущей версии предполагается, что для типа T определены оператор присваивания и конструктор по умолчанию. При создании шаблонных классов контейнеров (вроде Array и не только) разумно стараться минимизировать требования к типам шаблонных параметров. Поэтому усложним задачу, реализуйте класс Array не полагаясь на то, что для типа T определен оператор присваивания и конструктор по умолчанию. Конструктор копирования у типа T есть.

Hints: используйте placement new и явный вызов деструктора (смотрите урок 3.4), чтобы создавать и уничтожать объекты, аллоцировать правильно выровненную память можно с помощью new char[N * sizeof(T)], где N - количество элементов массива.