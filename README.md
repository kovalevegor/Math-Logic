# <p align="center">Лекция 1 </p>
### <p align="center">Логика высказываний. Язык высказываний</p>

<p align="center">Существуют языки первого и второго порядков</p>

<br>


+ Алфавит: ${S,\\&, \bigvee, \neg, \to, (.), \Delta}$
+ Высказывания: $S_n\equiv(S \underbrace{\Delta...\Delta}_{n})$
+ Формулы: 
    1. высказывания являются формулами;
    2. если $\Phi, \Psi$ - формулы то слова $(\Phi \bigvee \Psi), (\Phi \\&  \Psi), (\Phi \to \Psi), \neg\Phi$ являются формулами, где $\\& , \bigvee, \to, \neg$ - логические связки, семантика которых будет определена далее 

<br>

### <p align="center">Конъюнкция формул A & B</p>
+ Конъюнкция моделирует следующие языковые выражения
    1. "A и B"
    2. "как А, так и В"
    3. "А, а также В"
    4. "А хотя и В"
    5. "А, несмотря на В"
+ Определение конъюнкции через таблицу истинности

$\\&$ | 0 | 1
---|---|---
0 | 0 | 0
1 | 0 | 1

<br>

Примеры:
1. `Хотя Гена и был крокодилом, он был добрым`
2. `Если Вася умный, то о Пете этого не скажешь`

### <p align="center">Дизъюнкция формул A V B</p>
+ Дизъюнкция моделирует следующие языковые выражения
    1. "A или B"
    2. "А или/и В"
    3. "либо А, либо В, либо то и другое"
    4. "возможно А, возможно В"
+ Определение дизъюнкции через таблицу истинности

$\bigvee$ | 0 | 1
---|---|---
0 | 0 | 1
1 | 1 | 1

<br>

Примеры:
1. `Дождь идет или сыветит солнце`
2. `По крайней мере кто-то из этих двоих, Васи и Пети, - студент`

### <p align="center">Отрицание формулы</p>
+ Отрицание моделирует следующие языковые выражения
    1. "не A"
    2. "не верно, что А"
    3. "не выполняется А"
+ Определение отрицания через таблицу истинности

$\neg$ | $f$
---|---
0 | 1 
1 | 1 

<br>

Примеры:
1. `Кит - не рыба`
2. `Что я глупый, это ложь`

### <p align="center">Импликация формул A -> B</p>
+ Импликация моделирует следующие языковые выражения
    1. "из А следует В"
    2. "А достаточное условия для В"
    3. "В необходимое условия для А"
    4. "если А, то В"
    5. "из А вытекает В"
+ Определение Импликации через таблицу истинности

$\to$ | 0 | 1
---|---|---
0 | 1 | 1
1 | 0 | 1

<br>

Примеры:
1. `Если я не ошибаючь, то ты дурак`
2. `Джон бросился бы под поезд и погиб`

<br><br>

### <p align="center">Интерпретация высказываний/p>

+ Интерпретация множества высказываний ${S_n}:f:{S_n}\to {0,1}$
+ Истинностное значение формулы $\Psi$ при интерпретации $f:$

    если $\Psi \equiv S_n$ , то $f(\Psi) = f(S_n)$

    если $\Psi \equiv (\Psi_1 \bigvee \Psi_2)$ , то $f(\Psi) = f(\Psi_1 \bigvee \Psi_2)$

    если $\Psi \equiv (\Psi_1 \\& \Psi_2)$ , то $f(\Psi) = f(\Psi_1 \\& \Psi_2)$

    если $\Psi \equiv (\Psi_1 \to \Psi_2)$ , то $f(\Psi) = f(\Psi_1 \to \Psi_2)$

    если $\Psi \equiv \neg\Psi_1$ , то $f(\Psi) = f(\neg\Psi_1)$

<br>

### <p align="center">Интерпретация высказываний</p>

**Предложение.** Для любой интерпретации $f$, любой формулы $\Phi$ выполняетя ровно одно из условий $f(\Phi)=0$ , $f(\Phi) = 1$

**Доказательство**
Проведем доказательство индукцией по глубине формул

`(i)` Базис индукции: $\Phi \equiv S_n, f:\{S_n\} \to \{0,1\}$ - отображение

`(ii)` Шаг индукции: $\Phi \equiv \Phi_1 \\& \Phi_2$ , по индуктивному предположению $f(\Phi_1) = \sigma$ , $f(\Phi_2)=\tau$. По определению конъюнкции однозначно определяется $f(\Phi)$. Остальное аналогично




<br>

### <p align="center">Язык высказываний </p>

+ Формула называется *тождественно истинной* (тавтологией), если при всех интерпретациях входящий в нее высказываний она будет принимать значение истины $(1)$+ Формула называется *тождественно ложной*, если при всех интерпретациях входящий в нее высказываний она будет принемать занчение ложь $(0)$

+ Формула называется *выполнимой*, если существует интерпретация ее высказываний, при которых она принимает значение истины $(1)$

+ Формула называется *опровержимой*, если при всех интерпретациях входящий в нее высказываний она будет принемать занчение ложь $(0)$

```
Замечание! Приоритет логических операций
```

$$
\neg,\\&,\bigvee,\to
$$

<br>

+ Формулы $\Phi$ и $\Psi$ называются *эквивалентным*, если при любой интерпретации высказыаний $X(\Phi) \bigcup X(\Psi)$ их истинные значения совпадают, $X(\Phi)$ - множество всех высказываний, входящий в $\Phi$

```
Пример
```
$A\\& B=B\\& A$ ; $(A\\&B)\\& C=A\\& (B\\& C)$ ; $A = (A\bigvee)\\& A$

```
Мы можем опускать скобки в формулах, где имеются повторяющиеся конъюнкции (дихъюнкции)
```

$A\\& B)\\& C=A\\& B\\& C$
