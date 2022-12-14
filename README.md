### Яндекс.Практикум: Python-разработчик. Алгоритмы. Финальные задачи.
## A. Ближайший ноль
Тимофей ищет место, чтобы построить себе дом. Улица, на которой он хочет жить, имеет длину n, то есть состоит из n одинаковых идущих подряд участков. Каждый участок либо пустой, либо на нём уже построен дом.

Общительный Тимофей не хочет жить далеко от других людей на этой улице. Поэтому ему важно для каждого участка знать расстояние до ближайшего пустого участка. Если участок пустой, эта величина будет равна нулю — расстояние до самого себя.

Помогите Тимофею посчитать искомые расстояния. Для этого у вас есть карта улицы. Дома в городе Тимофея нумеровались в том порядке, в котором строились, поэтому их номера на карте никак не упорядочены. Пустые участки обозначены нулями.

##### Формат ввода
В первой строке дана длина улицы —– n (1 ≤ n ≤ 106). В следующей строке записаны n целых неотрицательных чисел — номера домов и обозначения пустых участков на карте (нули). Гарантируется, что в последовательности есть хотя бы один ноль. Номера домов (положительные числа) уникальны и не превосходят 109.

##### Формат вывода
Для каждого из участков выведите расстояние до ближайшего нуля. Числа выводите в одну строку, разделяя их пробелами.

#### Реализация алгоритма выглядит так: 
- Создаём список для вывода и заполняем его нулями.
- Получаем список позиций всех пустых участков.
- Пробегаемся по циклу по участкам до первого свободного (0).
- Сохраняем результат явной формулы для расстояния между домом и первым свободным участком.
- Создаём цикл по парам соседних пустых участков.
- Дальше проходимся циклом по всем домам между этими пустыми участками.
- Сохраняем результат формулы для минимального расстояния между домом и пустым участком (0).
- Создаём цикл по позициям домов после последнего пустого участка.
- Сохраняем результат для расстояния между домом и последним пустым участком.
