# Spis treści
* [Dokumentacja](#Dokumentacja)
* [Struktura zadań programowania liniowego](#Struktura-zadań-programowania-liniowego)
* [Dopuszczalne znaki w kodzie](#Dopuszczalne-znaki-w-kodzie)
* [Identyfikatory (_symbolic names_)](#Identyfikatory-(_symbolic-names_))
* [Literały](#Literały)
	* [Literały napisowe](#Literały-napisowe)
	* [Literały liczbowe](#Literały-liczbowe)
* [Słowa kluczowe](#Słowa-kluczowe)
* [Ograniczniki wyrażeń (_expression delimiters_)](#Ograniczniki-wyrażeń-(_expression-delimiters_))
* [Komentarze](#Komentarze)
* [Wyrażenia](#Wyrażenia)
	* [Wyrażenia numeryczne](#Wyrażenia-numeryczne)
	* [Parametr indeksowany (_subscripted parameter_)](#Parametr-indeksowany-(_subscripted-parameter_))
	* [Wyrażenia symboliczne](#Wyrażenia-symboliczne)
	* [Wyrażenia indeksujące (_indexing expressions_) i indeksy nieme (_dummy indices_)](#Wyrażenia-indeksujące-(_indexing-expressions_)-i-indeksy-nieme-(_dummy-indices_))
	* [Wyrażenia zbiorowe (_set expressions_)](#Wyrażenia-zbiorowe-(_set-expressions_))
	* [Wyrażenia logiczne (_logical expressions_)](#Wyrażenia-logiczne-(_logical-expressions_))
	* [Wyrażenia liniowe (_linear expressions_)](#Wyrażenia-liniowe-(_linear-expressions_))
* [Operatory](#Operatory)
	* [Operatory arytmetyczne (_arithmetic operators_)](#Operatory-arytmetyczne-(_arithmetic-operators_))
	* [Hierarchia operatorów arytmetycznych](#Hierarchia-operatorów-arytmetycznych)
	* [Operatory symboliczne (znakowe)](#Operatory-symboliczne-(znakowe))
	* [Hierarchia operatorów symbolicznych](#Hierarchia-operatorów-symbolicznych)
	* [Operatory zbiorów](#Operatory-zbiorów)
	* [Hierarchia operatorów symbolicznych](#Hierarchia-operatorów-symbolicznych) 
	* [Operatory logiczne](#Operatory-logiczne)
	* [Hierarchia operatorów logicznych](#Hierarchia-operatorów-logicznych)
	* [Operatory wyrażeń liniowych](#Operatory-wyrażeń-liniowych)
	* [Hierarchia operatorów wyrażeń liczbowych](#Hierarchia-operatorów-wyrażeń-liczbowych)
* [Instrukcje (_statements_)](#Instrukcje-(_statements_))
	* [Deklaracje zbiorów](#Deklaracje-zbiorów)
	* [Deklaracja parametrów](#Deklaracja-parametrów)
	* [Deklaracja zmiennych (_variable statements_)](#Deklaracja-zmiennych-(_variable-statements_))
	* [Deklaracje ograniczeń (_constraing statement_)](#Deklaracje-ograniczeń-(_constraing-statement_))
	* [Deklaracje celu (_objective statement_)](#Deklaracje-celu-(_objective-statement_))
	* [Instrukcja ``solve`` (_solve statement_)](#Instrukcja-solve-(solve-statement))
	* [Instrukcja ``check`` (_check statement_)](#Instrukcja-check-(check-statement))
	* [Instrukcja ``display`` (_display statement_)](#Instrukcja-``display``-(_display-statement_))
	* [Instrukcja ``printf`` (_printf statement_)](#Instrukcja-``printf``-(_printf-statement_))
	* [Instrukcja ``for`` (_for statement_)](#Instrukcja-``for``-(_for-statement_))
	* [Instrukcja ``table`` (_table statement_)](#Instrukcja-``table``-(_table-statement_))
* [Model danych](#Model-danych)
	* [Sposoby definiowania modelu i danych](#Sposoby-definiowania-modelu-i-danych)
	* [Wczytywanie modelu i danych](#Wczytywanie-modelu-i-danych)
	* [Blok danych](#Blok-danych)
* [Sufiksy (przyrostki)](#Sufiksy-(przyrostki))
	* [Przyrostki zmiennych](#Przyrostki-zmiennych)
	* [Przyrostki celów](#Przyrostki-celów)
* [Funkcje związane z datą i czasem](#Funkcje-związane-z-datą-i-czasem)
	*	[gmtime()](#gmtime())
	*	[str2time](#str2time)
	*	[time2str](#time2str)



# Dokumentacja[^](#Spis-treści)

[http://gusek.sourceforge.net/gmpl.pdf](http://gusek.sourceforge.net/gmpl.pdf)

# Struktura zadań programowania liniowego[^](#Spis-treści)

Funkcja celu -- do zmaksymalizowania lub zminimalizowania:

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=z = c_1 x_1 + c_2 x_2 + ... c_n x_n + c_0">
 
Ograniczenia liniowe (s.t. -- subject to):

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=L_1 <= a_11 x_1 + a_12 x_2 + ... + a_1n x_n <= U_1">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=L_2 <= a_21 x_1 + a_22 x_2 + ... + a_2n x_n <= U_2">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=...">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=L_m <= a_m1 x_1 + a_m2 x_2 + ... + a_mn x_n <= U_m">  

Ograniczenia zmiennych:

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=l_1 <= x_1 <= u_1">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=l_2 <= x_2 <= u_2">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=...">

<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=l_n <= x_n <= u_n">

gdzie:
-   <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x_1, x_2, ..., x_n"> -- zmienne    
-   <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=z"> -- warto

# Dopuszczalne znaki w kodzie[^](#Spis-treści)

- wielkie litery ASCII: ``A B C D E F G H I J K L M N O P Q R S T U V W X Y Z``;
- małe litery ASCII: ``a b c d e f g h i j k l m n o p q r s t u v w x y z``;
- cyfry: ``0 1 2 3 4 5 6 7 8 9 ``;
- znaki specjalne ASCII: ``~ ! # ^ & * ( ) _ + - = [ ] { } | ; : ' " , . / < >``.

# Identyfikatory (_symbolic names_)[^](#Spis-treści)

Pierwszy znak: 

- mała litera, np. ``alpha123``;
- wielka litera, np. ``Alpha123``;
- podkreślnik, np. ``_alpha123``.

# Literały[^](#Spis-treści)

## Literały napisowe

- Pojedynczy cudzysłów, np. ``'abc'``
- Podwójny cudzysłów, np. ``"abc"``
- Sekwencja ucieczki dla apostrofu, np. ``'that''s all'``
- Sekwencja ucieczki dla cudzysłowu, np. ``"he said ""hello"""``

## Literały liczbowe

- ``123``
- ``123.123``
- ``.123``
- ``123.E+123``
- ``123.123e-123``

# Słowa kluczowe[^](#Spis-treści)

Zarezerwowane słowa kluczowe (nie mogą być identyfikatorami): 

``and   or   if   else   by   cross   diff   div   in   inter   less   mod   not   symdiff   then   union   within``

# Ograniczniki wyrażeń (_expression delimiters_)[^](#Spis-treści)

``+   -  *   **   &   &&   =   ==   /   <   <=   <>   >>   <-   >   >=   !=   !   |   ||   ^   .   ..   ,   :   :   ;=   ~   (   )   [   ]   {   }``

Wieloznakowe ograniczniki nie mogą zawierać spacji.

Niektóre ograniczniki nie mają znaczenia: ułatwiają tylko czytanie kodu i można je pominąć. 

# Komentarze[^](#Spis-treści)

- Jednowierszowe, np. ``# abc``
- Wielowierszowe, np. ``/* abc */``

# Wyrażenia[^](#Spis-treści)

- Numeryczne (_numeric expressions_)
- Symboliczne (_symbolic expressions_)
- Indeksujące (_indexing expressions_)
- Zbiorowe (_set expressions_)
- Logiczne (_logical expressions_)
- Liniowe (_linear expressions_)

## Wyrażenia numeryczne[^](#Spis-treści)

Formuła zwracająca wartość pojedynczej zmiennej typu zmiennoprzecinkowego. 

Szczególne przypadki: 

### Literały liczbowe

Np. ``123``, ``123.123``, ``.123``, ``123.123e-123``.

### Indeksy

Np. ``i`` w ``a[i]``.

### Parametry

Np. ``alpha``, ``time_start``, ``x``, ``a[i]``.

### Wyrażenia warunkowe (_conditional expressions_)

Kod: 

```if i in I then 2 * p else q[i + 1]```

Zapis w języku ``C#``:

```csharp
if (I.contains(i))
	return 2*p;
else
	return q[i+1];
```

Kod: 

```if i == 2 then 3```

-- jeśli <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i \neq 2">, wyrażenie ma wartość <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=0">.

### Wywołania funkcji (_function references_)

| Składnia | Funkcja |
| --- | --- | 
| ``abs(x)`` | wartość bezwzględna <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``atan(x)`` | _arcus tangens_ z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``atan(x, y)`` | _arcus tangens_ z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\frac{y}{x}"> |
| ``card(X)`` | moc zbioru (_cardinality_) -- liczba elementów zbioru <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X"> |
| ``ceil(x)`` | sufit (_ceiling_), zaokrąglenie w górę do najbliższej całkowitej |
| ``cos(x)`` | _cosinus_ z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``exp(x)`` | eksponenta, funkcja <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=e^x"> |
| ``floor(x)`` | podłoga (_floor_), zaokrąglenie w dół do najbliższej całkowitej |
| ``gmtime()`` | liczba sekund od północy 1 stycznia 1970 do teraz |
| ``length(s)`` | długość napisu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=s"> (liczba znaków) |
| ``log(x)`` | logarytm naturalny z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``log10(x)`` | logarytm przy podstawie 10 z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``max(a_1,a_2,...,a_n)`` | maksymalna wartość z podanych |
| ``min(a_1,a_2,...,a_n)`` | minimalna wartość z podanych |
| ``round(x)`` | zaokrąglenie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> to najbliższej całkowitej |
| ``round(x, n)`` | zaokrąglenie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n"> liczb po przecinku |
| ``sin(x)`` | _sinus_ z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``sqrt(x)`` | pierwiastek kwadratowy z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``str2time(s, f)`` | konwersja napisu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=s"> na datę w formacie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=f"> |
| ``tan(x)`` | _tangens_ z <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``trunc(x)`` | odcięcie cyfr po przecinku (bez zaokrąglania) |
| ``trunc(x, n)`` | odcięcie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n"> cyfr po przecinku (bez zaokrąglania) |
| ``Irand224()`` | liczba pseudolosowa z przedziału <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 2^{24})"> |
| ``Uniform01()`` | liczba pseudolosowa z przedziału <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 1)"> |
| ``Uniform(a, b)`` | liczba pseudolosowa z przedziału <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[a, b)"> |
| ``Normal01()`` | generate Gaussian pseudo-random variate with <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\mu = 0"> and <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\sigma = 1"> |
| ``Normal(u, s)`` | generate Gaussian pseudo-random variate with given <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=u"> and <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=s"> |



### Wyrażenia iterowane (_iterated expressions_)

Kod: 

```sum{i in S diff T} a[i] * b[i, j]```

Zapis matematyczny:

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\sum_{i \in S \setminus T} {a_i b_{ij} }">

Kod: 

```prod{i in I} f(i)``

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\prod_{i \in I} f(i)">

Kod: 

```min{i in I} f(i)```

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=min_{i_1, ..., i_n \in I} f(i)">

-- minimalna wartość funkcji <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=f"> obliczanej dla parametrów od <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i_1"> do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i_n"> ze zbioru <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=I">. 

Kod: 

```max{i in I} f(i)```

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=max_{i_1, ..., i_n \in I} f(i)">

## Parametr indeksowany (_subscripted parameter_)[^](#Spis-treści)

Kod: 

```a[i, j]```

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=a_{ij}">

Kod: 

```a['maj 2003', j + 1]```

Możliwe zapisy w języku ``C#``:

```csharp
a.Where(date = "maj 2003" && index = j+1);

a["maj 2008"][j+1]; //z przeciążeniem indeksatora
```

## Wyrażenia symboliczne[^](#Spis-treści)

Wyrażenia zwracające ciągi znaków. 

Przypadki szczególne: 

### Literały

Np. ``abc``, ``1 maja 2020``.

### Indeksy

Np. ``i`` w ``nazwy[i]``.

### Parametry

Np. ``x``, ``nazwy``, ``nazwy['a']``, ``nazwy[3]``.

### Wyrażenia warunkowe

Jak wyżej. 

### Wywołania funkcji

| Składnia | Funkcja |
| --- | --- | 
| ``substr(s, x)`` | Fragment napisu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=s"> zaczynający się od znaku <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x"> |
| ``substr(s, x, y)`` | Jw., ale o długości <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=y"> |
| ``time2str(t, f)`` | Konwersja czasu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=t"> na napis w formacie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=f"> |

## Wyrażenia indeksujące (_indexing expressions_) i indeksy nieme (_dummy indices_)[^](#Spis-treści)

Przeliczalne (enumerowalne) kolekcje elementów. 

| Składnia | Zawartość | 
| --- | --- |
| ``i in S`` | zbiór jednoelementowych krotek z indeksem niemym <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i"> |
| ``(i_1, i_2, ..., i_n) in S`` | zbiór n-elementowych krotek z ideksami niemymi <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i_1">, <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i_2"> do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i_n"> |
| ``S`` | zbiór o nazwie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=S"> |
| ``{ a, b, c }`` | zbiór bez nazwy |
| ``{ a, b, c : >= 0 }`` | zbiór bez nazwy z ograniczeniem |
| ``{ i in I, (i, j) in B}`` | zbiór składający się ze zbioru jednoelementowych krotek (<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=I">) i zbioru dwuelementowych krotek (<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=B">) |

### Indeksy nieme

Nie są stosowane do wskazania elementu kolekcji, ale tylko wskazują, że mamy do czynienia ze zbiorem. Można jednak stosować je jako zmienną w operacjach. 

| Operator niemy w GNU MathProg | operator niemy w językach programowania |
| --- | --- |
| ``i in I`` |``I.select(i => i); //C#`` |
| ``action{ i in A, (j, k) in B, l in C } x(i, j, k, l)`` | ``for i in A: #Python``<br/>&nbsp;&nbsp;&nbsp;``for (j, k) in B:``<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;``for l in C:``<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;``x = (i, j, k, l)``<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;``action(x)`` |

Widoczność indeksu niemego ogranicza się do wyrażenia, np. 

``i in I i ^^ 2; # OK``

``i in I; i ^^ 2; # błąd: i jest niezdefiniowane``

Przykłady: 

- Suma wyrażeń

Kod: 

``sum{i in A, (j, k) in B, l in C} p[i, j, k, l]``

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\sum_{i \in A, (j, k) \in B, l \in C} p_{ijkl}">

* Iloczyn kartezjański

Kod:

``{A, B, C}``

Zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=A \times B \times C = \{  (i, j, k, l) : i \in A, (j, k) \in B, l \in C \}">

Przykładowe wartości zbiorów: 

* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=A = { 1, 2 }">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=B = { (a, 1), (b, 2) }">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=C = { x, y, z }">

Wartości iloczynu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=A \times B \times C">: 

* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 1, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 1, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 1, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 2, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 2, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, a, 2, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 1, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 1, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 1, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 2, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 2, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, b, 2, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 1, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 1, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 1, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 2, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 2, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, a, 2, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 1, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 1, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 1, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 2, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 2, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, b, 2, z}">

<br/>

* Parametr zawierający zbiory

Kod: 

``param p{i in A, (j, k) in B, l in C};``

Analogiczny obiekt w języku ``C#``:

```csharp
var p = new
{
	A = new int[2],
	B = new (int, string)[2],
	C = new string[3]
};
```

* Indeks niemy wykorzystany w dalszej części wyrażenia: 

Kod: 

``{ i in A, (i - 1, k) in B, l in C }``

Analogiczna konstrukcja w języku ``Python``:

```python
for i in A:
   for (i - 1, k) in B:
      for l in C:
         pass
```

Przykładowe wartości zbiorów: 

* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=A = { 1, 2 }">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=B = { (2, a), (3, b) }">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=C = { x, y, z }">

Wartości kodu ``{ i in A, (i - 1, k) in B, l in C }``: 

* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, a, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, a, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, a, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, b, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, b, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 1, b, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, a, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, a, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, a, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, b, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, b, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={1, 2, b, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, a, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, a, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, a, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, b, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, b, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 1, b, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, a, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, a, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, a, z}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, b, x}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, b, y}">
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math={2, 2, b, z}">

<br/>

* Wyrażenia indeksujące z ograniczeniami (predykatami)

Kod: 

``action{ i in A, (j, k) in B, l in C: i <= 5 and k <> 'a' }``

Analogiczny kod w języku ``Python``:

```python
for i in A:
	for (i, j) in B:
		for l in C:
			if (i <= 5 and k != 'a'):
				action()
```

## Wyrażenia zbiorowe (_set expressions_)[^](#Spis-treści)

Wyrażenia przetwarzające zbiory.

| Składnia | Objaśnienie |
| --- | --- |
| ``{(123,'a'),(i+1,'b'),(j-1,'c')}`` | literał zbiorowy |
| ``{ }`` | jw. (zbiór pusty) |
| ``{ 1, 2, 3 }`` | jw. (zbiór krotek jednoelementowych |
| ``{ (1, 'a'), (2, 'b') }`` | jw. (zbiór krotek dwuelementowych |
| ``I``, ``DOGS`` | zbiory bez indeksów |
| ``S[i, j-1]`` | zbiór z indeksami |
| ``1..t-1 by 2`` | zbiór arytmetyczny |
| ``{t in 1..T, (t+1, j) in S: (t, j) in F}`` | wyrażenie indeksujące |
| ``setof{i in I, j in J}(i+1, j-1)`` | iterowane wyrażenie zbiorowe |
| ``if i < j then S[i,j] else F diff S[i,j]`` | warunkowe wyrażenie zbiorowe |
| ``(1..10 union 21..30)`` | wyrażenie zbiorowe w nawiasach |

### Zbiory arytmetyczne

| Przykład składni | Wartość |
| --- | --- |
| ``1..7`` | ciąg liczb od 1 do 24: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{ 1, 2, 3, 4, 5, 6, 7 \}"> |
| ``1..7 by 2`` | co druga liczba od 1 do 6: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{ 1, 3, 5, 7 \}"> |

Krok ``k`` w składni ``a..b by k`` może być ujemny (wtedy ciąg będzie malejący), ale nie może być równy 0 (wtedy ciąg będzie nieskończony).

### Wyrażenia iterowane (_iterated expressions_)

Składnia: 

```
setof{ ZBIOR_A, ZBIOR_B... }( element_a, element_b... )
```

* ``ZBIOR_A``, ``ZBIOR_B`` -- wyrażenia indeksowane (_indexing-expressions_) z niemymi indeksami; 
* ``element_a``, ``element_b`` -- (_integrands_) wyrażenia numeryczne lub symboliczne (napisowe) wyodrębnione w zbiorach, występujące:
	* pojedynczo -- całe wyrażenie oznacza zbiór jednoelementowych krotek;
	* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n"> razy -- całe wyrażenie oznacza zbiór _n_-elementowych krotek

Przykłady: 

<mark><code>setof{i in I, j in J}(i+1, j-1)</code></mark>

* wybierz kolejny (<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=i+1">) i poprzedni (<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=j-1">) element ze zbiorów <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=I"> i <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=j">
* analogiczny kod w języku ``Python``:

```python
for i in I:
	for j in J:
		foo(i+1, j-1)
```

* zapis matematyczny:

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\forall_{i \in I} \forall_{j \in J} f(i+1, j-1)">

<mark><code>setof{k in nodes, (i,k) in steps[s-1], (k,j) in steps[s-1]}(i,j)</code></mark>

* elementami ``k`` ze zbioru ``nodes`` przeszukujemy zbiór ``steps``,
* z każdego ``s - 1`` elementu zbioru ``steps`` bierzemy _i_-ty i _k_-ty element, 
* z każdego ``s - 1`` elementu zbioru ``steps`` bierzemy _k_-ty i _j_-y  element, 
* wybieramy ostatecznie elementy _i_ oraz _j_;
* analogiczny kod w języku ``Python``:

```python
for k in nodes:
	for (i, k) in steps:
		for (k, j) in steps:
			foo(i, j)
```

* zapis matematyczny: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\forall_{k \in N} \forall_{ik \in S_{s-1}} \forall_{kj \in S_{s-1}} f(i, j)">

gdzie: 
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=N"> -- ``nodes``
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=S"> -- ``steps``
* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=f"> -- jakaś funkcja działająca na elementach _i_ oraz _j_

### Wyrażenia warunkowe (_conditional expressions_)

Jw.

## Wyrażenia logiczne (_logical expressions_)[^](#Spis-treści)

Mają wartość logiczną -- prawda lub fałsz. 

Przykłady składni

* ``a[i, j] < 1.5``

-- wyrażenie porównujące: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=a_{ij} < 1,5"> 

* ``s[i + 1, j - 1] <> 'marzec' & rok``

-- porównujące; matematycznie: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=s_{i+1 j-1} \neq"> 'marzec' + rok

* ``(i + 1, 'luty') not in I cross J`` 

-- porównujące; ``C#``:

```csharp
if (!I.Except(J).Contains((i+1, "luty")))
```

* ``S union T within A[i] inter B[j]`` 

-- porównujące;``C#``: 

```csharp
if (A[i].Union(B[j]).Contains(S.Union(T))
```

* ``forall{i in I, j in J} a[i, j] < .5 * b[i]``

-- iterowane wyrażenie logiczne; matematycznie: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\forall_{i \in I, j \in J} a_{ij} < \frac{b_i}{2} ">

-- ``C#``: 

```csharp
I.Union(J).Where(i < b[i]/2 && j < b[i]/2)
```

* ``(a[i,j] < 1.5 or b[i] >= a[i,j])`` 

-- ``C#``: 

```csharp
for (int i = 0, int j = 0; i < a.GetLength(0) && j < a.GetLength(1) && i < b.Length; i++, j++)
{
	if (a[i, j] < 1.5 || b[i] >= a[i, j])
		//jakaś funkcja
}
```

* ``not (a[i,j] < 1.5 or b[i] >= a[i,j]) and (i,j) in S``

-- ``C#``: 

```csharp
for (int i = 0, int j = 0; i < a.GetLength(0) && j < a.GetLength(1); i++, j++)
{
	if (!(a[i, j] < 1.5 || b[i] >= a[i, j])) && S.Contains((i, j)))
		//jakaś funkcja
}
```

### Wyrażenia porównujące

Przykłady

* ``x < y``
* ``x <= y``
* ``x = y`` lub ``x == y``
* ``x >= y``
* ``x <> y`` lub ``x != y``
* ``x in Y`` -- w ``C#``: ``Y.Contains(x)``
* ``(x_1, x_2, x_3) in Y``
* ``x not in Y`` lub ``x !in Y`` -- w ``C#``:  ``!Y.Contains(x)``
* ``(x_1, x_2) not in Y`` lub ``(x_1, x_2) !in Y``
* ``X within Y`` -- zawieranie się lub równość zbiorów: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \subseteq Y">[^zbiory]
* ``X not within Y`` lub ``X !within Y`` -- <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \nsubseteq Y">[^zbiory]

[^zbiory]: Zbiory _X_ i _Y_ muszą zawierać taką samą liczbę elementów. 

### Wyrażenia iterowane (_iterated expressions_)

Składnia:

```operator wyrażenie_indeksujące warunki``

Przykłady: 

* ``forall { i in I, j in J} a[i, j] < 0.5 * b[i]``

```csharp
foreach (int i in I)
	foreach (int j in J)
		if (a[i, j] < b[i]/2)
			//jakaś funkcja
```

## Wyrażenia liniowe (_linear expressions_)[^](#Spis-treści)

Wyrażenia działające jak funkcja liniowa. 

Przykłady: 

* ``sum{j in J} (a[i, j] * x[i, j] + 3 * y[i -1])``

```csharp
double sum = 0;

foreach (int j in J)
{
	for (int i = 1; i < a.GetLength(0)+1 && i < x.GetLength(0)+1 && i < y.Length; i++)
		sum += a[i-1, j] * x[i-1, j] + 3 * y[i]; 
}
```

* ``if i in I then x[i, j] else 1.5 * z + 3.25``

```csharp

for (int i = 0; i < 100; i++)
{
	for (int j = 0; j < x.Length; i++, j++)
		if (I.contains(i)) 
			yield return x[i, j];
		else
			yield return 1.5 * z + 3.25;
}
```

* ``(- x[i,j] + 3.5 * y[k]) / sum{t in T} abs(d[i,j,t])``

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\frac{-x_{ij} + 3,5 \times y_k }{\sum_{t \in T} |d_{ijt}|}">

```csharp
double dzielnik = 0;

for (int i = 0; i < d.GetLength(0); i++)
	for (int j = 0; j < d.GetLength(1); j++)
		for (int t = 0; t < 100; t++)
			if (T.Contains(t))
				dzielnik += Math.Abs(d[i, j, t]);

for (int i = 0; i < x.GetLength(0); i++)
	for (int j = 0; j < x.GetLength(1); j++)
		for (int k = 0; k < y.Length; k++)
			yield return (-x[i, j] + 3.5 * y[k]) / dzielnik;
```

Przypadki szczególne

### Zmienne bez indeksów (_unsubscripted variables_)

Przykład: ``2 * x - 4 / y + 2.5``

### Zmienne z indeksami (_subscripted variables_)

Przykład: ``2 * x[i-1, j+1] - 4 / y[k] + 2.5``

Indeksy mogą być wyrażeniami liczbowymi (standardowymi indeksami typu <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x_1">) lub symbolicznymi (napisami, etykietami, np. słowniki w ``C#``). 

### Wyrażenia iterowane (_iterated expressions_)

Składnia: 

```sum wyrażenie_indeksujące operacje_lub_warunki```

Przykłady

* ``sum{i in I} abs(d[i])``

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=\sum_{i \in I} |d_i|">

```csharp
var I = new[] {0, 2, 4}.ToList();
var d = new[] {-1, -2, -3, -4, -5, -6};

int suma = 0;
I.ForEach(i => suma += Math.Abs(d[i])); //suma = 9
```




# Operatory[^](#Spis-treści)

## Operatory arytmetyczne (_arithmetic operators_)[^](#Spis-treści)

| Składnia | Liczba argumentów | Funkcja |
| --- | --- | --- |
| ``+x`` | 1 | zmiana znaku |
| ``-x`` | 1 | zmiana znaku | 
| | | |
| ``x + y`` | 2 | dodawanie |
| ``x - y`` | 2 | odejmowanie | 
| ``x less y`` | 2 | odejmowanie dodatnie: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=0">, jeśli <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x - y < 0">, w przeciwnym razie <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x - y">[^a] |
| ``x * y`` | 2 | mnożenie | 
| ``x / y`` | 2 | dzielenie rzeczywiste |
| ``x div y`` | 2 | dzielenie całkowite |
| ``x mod y`` | 2 | reszta z dzielenia |
| ``x ** y``, ``x ^ y`` | 2 | potęgowanie (<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=x^y">) |

[^a]: Przykłady:
``3 less 1`` <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math==2"> 
``3 less 2`` <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math==1">
``3 less 3`` <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math==0"> 
``3 less 4`` <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math==0">
``3 less 5`` <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math==0"> 

## Hierarchia operatorów arytmetycznych[^](#Spis-treści)

1. Funkcje, np. ``abs``, ``ceil``.
2. Potęgowanie: ``x ** y``, ``x ^ y``.
3. Zmiana znaku: ``-x``, ``+x``.
4. Mnożenie, dzielenie, reszta z dzielenia: ``x * y``, ``x / y``, ``x div y``, ``x mod y``.
5. Operatory iteracyjne: ``sum``, ``prod``, ``min``, ``max``.
6. Dodawanie i odejmowanie: ``x + y``, ``x - y``, ``x less y``.
7. Wyrażenia warunkowe: ``if x then y``, ``if x then y else z``.

## Operatory symboliczne (znakowe)[^](#Spis-treści)

| Składnia | Liczba argumentów | Funkcja |
| --- | --- | --- |
| ``a & b`` | 2 | Konkatenacja (złączenie) napisów <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=a"> i <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=b"> |

## Hierarchia operatorów symbolicznych[^](#Spis-treści)

1. Funkcje. 
2. Konkatenacja. 
3. Wyrażenia warunkowe. 

## Operatory zbiorów[^](#Spis-treści)

| Składnia | Liczba argumentów | Funkcja |
| --- | --- | --- |
| ``X union Y`` | 2 | suma zbiorów: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \cup Y"> |
| ``X diff Y`` | 2 | różnica zbiorów: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \setminus Y">[^roznica] |
| ``X symdiff Y`` | 2 | różnica symetryczna: <br/><img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \bigoplus Y = (X \setminus Y) \cup (Y \setminus X)">[^roznica_symetryczna] |
| ``X inter Y`` | 2 | część wspólna zbiorów: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \cap Y"> |
| ``X cross Y`` | 2 | iloczyn kartezjański: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X \times Y">[^iloczyn_kartezjanski] |

[^roznica]: To, co w zbiorze <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X">, ale nie w zbiorze <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=Y">. 

[^roznica_symetryczna]: Suma elementów obu zbiorów za wyjątkiem elementów wspólnych (wszystko, co należy do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X">, ale nie do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=Y">, razem z wszystkim, co należy do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=Y">, ale nie należy do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=X">). 

[^iloczyn_kartezjanski]: Dopasowanie każdy z każdym. 

## Hierarchia operatorów symbolicznych[^](#Spis-treści) 

1. Ustalenie wartości wyrażeń z operatorami numerycznymi. 
2. Ustalenie wartości wyrażeń z operatorami symbolicznymi.
3. Ustalenie wartości operatora ``setoff``
4. Iloczyn kartezjański ``cross``
5. Część wspólna zbiorów ``inter``
6. Suma i różnice zbiorów ``union``, ``diff``, ``symdiff``
7. Wyrażenia warunkowe ``if then``, ``if then else``

## Operatory logiczne[^](#Spis-treści)

| Składnia | Liczba argumentów | Funkcja |
| --- | --- | --- |
| ``not x`` | 1 | negacja: <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\neg x"> |
| ``!x`` | 1 | jw. |
| ``x and y`` | 2 | logiczne "i": ``x && y`` |
| ``x && y`` | 2 | jw. |
| ``x or y`` | 2 | lobiczne "lub": ``x || y`` |
| ``x || y`` | 2 | jw. |

## Hierarchia operatorów logicznych[^](#Spis-treści)

1. Ustalenie wartości działań na liczbach
2. Ustalenie wartości działań na symbolach (napisach)
3. Ustalenie wartości działań na zbiorach
4. Porównania, np. ``>``, ``<=``, ``=``
5. Negacja ``not``, ``!``
6. Suma logiczna ``and``, ``&&``
7. Kwantyfikatory ``forall`` i ``exists``
8. Iloczyn logiczny ``or``, ``||``

## Operatory wyrażeń liniowych[^](#Spis-treści)

Takie same jak w przypadku wyrażeń liczbowych. 

## Hierarchia operatorów wyrażeń liczbowych[^](#Spis-treści)

Taka sama jak w przypadku operatorów wyrażeń liczbowych. 

# Instrukcje (_statements_)[^](#Spis-treści)

Podstawowe jednostki operacji. 

Rodzaje: 

* deklaracje -- zadeklarowanie:
	* zbioru
	* parametru
	* zmiennej
	* ograniczenia
	* celu
* operacje (_functional statements_):
	* rozwiąż ``solve``
	* sprawdź ``check``
	* wyświetl ``display``, wydrukuj ``printf``
	* wykonuj w pętli ``loop``
	* tabela (_table_) 

## Deklaracje zbiorów[^](#Spis-treści)

Składnia: ``set nazwa alias dziedzina, atrybut1, atrybut2...;``

* _alias_ -- opcjonalny
* _dziedzina_ -- opcjonalna 
* _atrybuty_ -- opcjonalne: 
	* ``dimen n`` -- liczba elementów w krotkach tworzących zbiór (domyślnie 1)
	* ``within wyrażenie`` -- ograniczenie nałożone na zbiór
	* ``:= wyrażenie`` 
		* wskazanie elementów zbioru;
		* jeśli nie podano, elementy zbioru muszą być wskazane w sekcji ``data;``
	* ``default wyrażenie`` -- domyślne elementy zbioru (jeśli nie przypisano innych w deklaracji lub sekcji ``data;``)

Przykłady

* ``set nodes;`` 
	* deklaracja zbioru o nazwie ``nodes`` 
* ``set arcs within nodes across nodes;`` 
	* zbiór ``arcs`` zawierający elementy zbioru ``nodes`` dopasowane do samych siebie
* ``set A{i in I, j in J},``<br/>``within B[i+1] cross C[j-1],``<br/>``within D diff E,``<br/>``default {('abc',123), (321,'cba')}`` 
	* zbiór ``A`` zawierający dwuelementowe krotki o indeksach _i_, _j_
	* zawierający elementy zbioru ``B`` (bez pierwszego) dopasowane do każdego elementu zbioru ``C`` (bez ostatniego) 
	* oraz elementy zbioru ``D`` różne od elementów zbioru ``D``
	* domyślnie zbiór zawiera 2 krotki: ``('abc',123)`` i ``(321,'cba')`` |

## Deklaracja parametrów[^](#Spis-treści)

Składnia: ``param nazwa alias dziedzina, atrybut1, atrybut2...;``

* ``alias`` -- opcjonalny;
* ``dziedzina`` -- opcjonalna; wyrażenie indeksujące wskazujące typ danych (tablica jedno- lub wielowymiarowa);
* ``atrybuty`` -- opcjonalne (przecinki można pominąć): 
	* nieokreślony -- parametr jest dowolną liczbą 
	* ``integer`` -- parametr jest liczbą całkowitą
	* ``binary`` -- parametr jest liczbą binarną (przyjmuje wartości 0 lub 1)
	* ``symbolic`` -- parametr jest liczbą lub napisem
	* wyrażenie porównujące z atrybutami ``<``, ``<=``< ``=`` lub ``==``, ``>=``, ``>``, ``<>`` lub ``!=`` -- warunek ograniczający wartości parametru
	* ``in wyrażenie`` -- zbiór, z którego pochodzą elementy parametru
	* ``:= wyrażenie`` -- określa wartość przypisaną parametrowi
	* ``default wyrażenie`` -- domyślna wartość parametru

Przykłady:

* ``param units{raw, prd} >= 0;``
	* parametr ``units`` zawierający zmienne ``raw`` i ``prd``, o ile są nieujemne
* ``param profit{prd, 1..T+1};``
	* parametr ``profit`` zawierający zmienną ``prd`` i ciąg liczb od 1 do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=T+1">
* ``param N := 20 integer >= 0 <= 100;``
	* parametr ``N`` o wartości (początkowej) 20 i ograniczeniach: 
		* liczba całkowita
		* liczba nieujemna
		* liczba nie większa niż 100
* ``param comb 'n choose k' {n in 0..N, k in 0..n} :=``<br/>``if k = 0 or k = n then 1``<br/>``else comb[n-1,k-1] + comb[n-1,k];``
	* parametr ``comb`` o aliasie ``n choose k`` zawierający zbiór elementów:
		* <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=1">, jeśli indeks elementu wynosi <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=0"> lub <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n">
		* sumę elementów o indeksach <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n-1, k-1"> i <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=n-1, k">
* ``param p{i in I, j in J},``<br/>``integer,``<br/>``>=0,``<br/>``<= i+j,``<br/>``in A[i] symdiff B[j],``<br/>``in C[i,j],``<br/>``default 0.5 * (i + j);``
	* parametr ``p`` zawierający ciąg liczb ze zbiorów ``I`` oraz ``J`` takich, że: 
		* są liczbami całkowitymi 
		* są nieujemne
		* pochodzą z niewspólnych elementó zbiorów ``A`` i ``B``
		* pochodzą ze zbioru ``C``
		* są mniejsza niż suma indeksów zbioru ``A`` i ``B`` 
		* domyślnie to ciąg średnich wartości indeksów _i_ oraz _j_ 
* ``param miesiac symbolic default 'maj' in {'luty', 'maj', 'lipiec'};``
	* parametr napisowy o nazwie ``miesiac`` o wartości domyślnej ``'maj'`` i przyjmujący jedną z 3 wartości: ``'luty'``, ``'maj'`` lub ``'lipiec'``

## Deklaracja zmiennych (_variable statements_)[^](#Spis-treści)

Składnia: ``var nazwa alias dziedzina, atrybut1, atrybut2...;``

* alias -- jw.
* dziedzina -- jw.
* atrybuty -- opcjonalne (przecinki można pominąć): 
	* ``integer`` -- jw.
	* ``binary`` -- jw.
	* ograniczenia: 
		* ``>= wyrażenie`` -- dolne ograniczenie
		* ``<= wyrażenie`` -- górne ograniczenie 
		* ``= wyrażenie`` -- wartość stała 

Przykłady:

* ``var x >= 0;``
	* nieujemna zmienna ``x``
* ``var y{I, J};``
	* zmienna ``y`` przyjmująca wartości ze zbiorów ``I`` oraz ``J``
* ``var marka{p in produkt}, integer, >= kupione[p], <= na_rynku[p];``
	* zmienna ``marka`` przyjmująca wartości całkowite ze zbioru ``produkt`` nie mniejsza niż wartości ze zbioru ``kupion`` i nie większa niż wartości ze zbioru ``na_rynku``
* ``var magazyn{surowce, 1..T+1} >= 0;``
	* zmienna ``magazyn`` zawierająca ciąg liczb od ``surowce``, przez <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=1"> do <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=T+1"> 
* ``var z{i in I, j in J} >= i+j;``
	* zmienna ``z`` zawierające kolejne liczby ze zbiorów ``I`` oraz ``J`` pod warunkiem, że są nie mniejsza niż suma indeksów tych liczb

## Deklaracje ograniczeń (_constraing statement_)[^](#Spis-treści)

Składnia: 

``s.t. nazwa alias dziedzina: wyrażenie, ogranicz1, ogranicz2;``

(przecinki można pominąć)

* ``s.t.`` -- opcjonalny skrót od słów kluczowych ``subject to`` lub ``subj to``, które można używać zamiennie z ``s.t.``; 
* ``alias`` -- jw.
* ``dziedzina`` -- jw.; 
	* jeśli pominięta, ograniczenie dotyczy liczb rzeczywistych; 
	* jeśli wskazana, ograniczenie dotyczy tablic (wektorów lub macierzy) -- zbiorów _n_-elementowych krotek
* ``wyrażenie`` -- wyrażenie liniowe (_linear expression_) do obliczenia, czy warunek ograniczający został spełniony
* ``ogranicz1``:
	* ``= wyrażenie`` -- ścisłe ogranicznie
	* ``<= wyrażenie`` -- górne ograniczenie
	* ``>= wyrażenie`` -- dolne ograniczenie
* ``ogranicz2`` -- dodatkowe, opcjonalne ograniczenie: 
	* ``<= wyrażenie`` -- górne ograniczenie
	* ``>= wyrażenie`` -- dolne ograniczenie
	* **``ogranicz2`` musi mieć ten sam operator porównania co ``ogranicz1``, możliwe są zatem następujące kombinacje:**
		* ``s.t. nazwa : wyrażenie, <= ogranicz1, <= ogranicz2;``
		* ``s.t. nazwa : wyrażenie, >= ogranicz1, >= ogranicz2;``

Przykłady

* ``.s.t. r: x + y + z, >= 0, <= 1;``
	* ograniczenie o nazwie ``r`` takie, że suma zmiennych/parametrów ``x``, ``y``, ``z`` musi się mieścić w przedziale <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 1]">
* ``limit{t in 1..T}: sum{j in produkty} marka[j, t] <= max_produkt;``
	* ograniczenie o nazwie ``limi`` takie, że
	* suma elementów zbioru ``marka`` nie może przekroczyć wartości ``max_produkt``
	* zbiór ``marka`` jest tablicą (macierzą) dwuwymiarową z indeksami ``j`` i ``t`` takimi, że:
		* indeks ``t`` mieści się w przedziale <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, T]"> 
		* indeks ``j`` mieści zawarty jest w zbiorze ``produkty`` 
* ``subject to bilans{i in surowce, t in 1..T}:``<br/>``magazyn[i, t+1] =``<br/>``magazyn[i,t] - sum{j in produkty} jednostki[i,j] * marki[j, t];``
	* ograniczenie o nazwie ``bilans`` takie, że
	* każdy element tablicy ``magazyn`` musi być równy różnicy
		* wartości elementu z tablicy ``magazyn``
		* i sumie elementów z tablicy ``jednostki``
	* indeksy tablicy ``magazyn`` pochodzą ze zbioru ``surowce`` i przedziału <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, T]">
	* indeksy tablicy ``jednostki`` pochodzą ze zbioru ``surowce`` i zbioru ``produkty`` 
* ``subject to dniowka 'standardowa dniowka' {t in czas}:``<br/>``sum{p in produkt} produkt_czas[p] * zwykly_produkt[p, t]``<br/>``<= 1.3 * wytworzenie_produktu[t] * pracownicy[t];``
	* ograniczenie o nazwie ``dniowka`` z aliasem ``standardowa dniowka`` takie, że:
		* suma iloczynów elementów listy ``produkt_czas`` i ``zwykly_produkt`` 
		* nie może przekroczyć 130% iloczynu elementów list ``wytworzenie_produktu`` i ``pracownicy``
	* elementy listy ``produkt`` są indeksowane wartościami ze zbioru ``produkt``
	* elementy tablicy ``zwykly_produkt`` są indeksowane wartościami ze zbioru ``produkt`` i zbioru ``czas``
	* elementy list ``wytworzenie_produktu`` i ``pracownicy`` są indeksowane wartościami ze zbioru ``czas``
* ``s.t. ogr: {i in 0...n} sum{a[i+1] * x[i+1]} <= 1.5``
	* matematycznie: 

<img style="min-width: 400px; display: block; margin-left: auto; margin-right: auto;" src="https://render.githubusercontent.com/render/math?math=a_1 x_1 + a_2 x_2 + ... + a_n x_n <= 1.5 ">

## Deklaracje celu (_objective statement_)[^](#Spis-treści)

Model może zawierać tylko jedną deklarację celu. Jeśli zadeklarowano więcej niż jeden cel, program bierze pod uwagę tylko pierwszą deklarację. 

Składnie: 
``minimize nazwa alias dziedzina : wyrażenie;``
``maximize nazwa alias dziedzina : wyrażenie;``

* ``alias`` -- jw.
* ``dziedzina`` -- jw.; jeśli nie wskazana, cel definiuje pojedynczą wartość; jeśli wskazana, cel jest wektorem lub macierzą _n_-elementowych krotek;
* ``wyrażenie`` -- wyrażenie liniowe.

Przykłady: 
* ``minimize cel: x + 1.5 * (y + z);``
* ``maximize zysk_calk: sum{p in produkty} zysk[p] * marka[p];``

## Instrukcja ``solve`` (_solve statement_)[^](#Spis-treści)

Składnia: ``solve;``

Opcjonalna. Jeśli jej nie podano, program traktuje model tak, jakby instrukcja znajdowała się na końcu modelu. 

Może być użyta tylko raz w modelu. Powoduje rozwiązanie zadania i obliczenie wartości wszystkich zmiennych w modelu. 

Deklaracje nie mogą się pojawić poniżej instrukcji ``solve``.

## Instrukcja ``check`` (_check statement_)[^](#Spis-treści)

Składnia: ``check dziedzina : wyrażenie;``

* ``dziedzina`` -- jw.; 
	* jeśli nie zdefiniowano, program sprawdza warunek tylko 1 raz (dla 1 zestawu wartości);
	* jeśli zdefiniowano, warunek jest sprawdzany dla wielu wartości; 
* ``wyrażenie`` -- wyrażenie logiczne do sprawdzenia (dwukropek można pominąć). 

Przykłady: 

* ``check: x + y <= 1 and x >= 0 and y >= 0;``
* ``check sum{i in DOSTAW} zapas[i] = sum{j in ODBIOR} zamow[j];``
* ``check {i in I, j in 1..10}: S[i, j] in U[i] union V[j];``

Instrukcja ``check`` pozwala sprawdzić, czy uzyskany wynik zgodny jest z określonymi warunkami. Jeśli wynik nie spełnia wymagań, program zwraca błąd. 

## Instrukcja ``display`` (_display statement_)[^](#Spis-treści)

Składnia: ``display dziedzina : element, element, ... element;``

* ``dziedzina`` -- jw.
* ``element`` -- obiekty, których wartość ma być wyświetlona (dwukropek można pominąć).

Przykłady: 

* ``display: 'x =', x, 'y =', y, 'z =', z;``
* ``display sqrt(x ** 2 + y ** 2 + z ** 2);``
* ``display {i in I, j in J}: i, j, a[i, j], b[i, j];``

## Instrukcja ``printf`` (_printf statement_)[^](#Spis-treści)

Instrukcja podobna do ``display``, ale umożliwia formatowanie danych.

Składnie: 

``printf dziedzina : format, wyrażenie, ..., wyrażenie;``

``printf dziedzina : format, wyrażenie, ..., wyrażenie > plik;``

``printf dziedzina : format, wyrażenie, ..., wyrażenie >> plik;``

* ``dziedzina`` -- jw.
* ``format`` -- wyrażenie napisowe określające sposób wyświetlenia wartości; 
* ``wyrażenie`` 
	* wyrażenia, których wartości mają być wyświetlone w podanym formacie; 
	* dopuszczalne typy: numeryczny, napisowy, logiczny; 
* ``plik`` -- nazwa pliku, w którym ma zostać zapisany wynik; 
* ``>`` -- flaga utworzenia nowego, pustego pliku; 
* ``>>`` -- dodanie wartości na końcu istniejącego pliku; 

Przykłady: 

* ``printf 'Hello, world!\n';``
* ``printf: "x = %.3f; y = %.3f; z = %.3f\n", x, y, z > "wynik.txt";``
* ``printf {i in I, j in J}: "przepływa z %s do %s wynosi %d\n",``<br/>``i, j, x[i, j]``<br/>``>> plik_wynikowy & ".txt";``
* ``printf{i in I} 'calkowity przeplyw z %s wynosi %g\n',``<br/>``i, sum{j in J} x[i, j];``
* ``printf{k in K} "x[%s] = " & (if x[k] < = then "?" else "%g"),``<br/>``k, x[k];``

Modyfikatory formatu: 

| Znak kontrolny | Formta |
| --- | --- |
| ``%d``, ``%i`` | liczba całkowita |
| ``%f``, ``%F`` | liczba typu ``double`` |
| ``%e``, ``%E`` | zapis naukowy typu ``0.3e-4`` |
| ``%g``, ``%G`` | liczba rzeczywista zapisana tradycyjnie lub w formacie naukowym[^g] |
| ``%s`` | napis |

[^g]: Program automatycznie wybiera lepszy zapis. 

## Instrukcja ``for`` (_for statement_)[^](#Spis-treści)

Składnie:

``for dziedzina : instrukcja;``

``for dziedzina : { instrukcja; instrukcja; ... instrukcja; }``

* ``dziedzina`` -- wyrażenie indeksujące (dwukropek można pominąć); 
* ``instrukcja`` 
	* pojedyncze lub wielokrotne instrukcje; 
	* w przypadku wielu instrukcji należy ująć je w klamry ``{ }``
	* dopuszczalne instrukcje: 
		* ``check``
		* ``display``
		* ``printf``
		* ``for``

Przykłady: 

```for {(i, j) in E: i != j}
{ 	printf "przeplyw z %s do %s w %g\n", i, j, x[i, j];
	check x[i, j] >= 0;
}
```

```
for {i in 1..n}
{	for {j in 1..n} printf " %s", if x[i, j] then "Q" else ".";
	printf("\n");
}
```

```
for {1..72} printf("*");
```
-- wyświetla 72 gwiazdki.

## Instrukcja ``table`` (_table statement_)[^](#Spis-treści)

Składnie: 

```
table nazwa alias IN sterownik arg1, arg1... argN :  
	set <- [ fld, ..., fld ], par ~ fld, ..., par ~fld;
```

```
table nazwa alias dziedzina OUT sterownik arg1, arg1... argN :  
	wyrażenie ~ fld, ..., wyrażenie ~ fld;
```

* ``alias`` -- jw.
* ``dziedzina`` -- wyrażenie indeksujące;
* ``IN`` -- odczyt danych z tabeli wejściowej; 
* ``OUT`` -- zapis danych do tabeli wyjściowej;
* ``sterownik`` -- wyrażenie napisowe; określa sposób dostępu do tabeli; 
* ``arg`` -- opcjonalne wyrażenia napisowe przekazywane do tabeli;
* ``set <-`` -- nazwa opcjonalnego zbioru kontrolnego; 
* ``~ fld`` -- opcjonalna nazwa pola: 
	* w nawiasach kwadratowych musi się znaleźć przynajmniej 1 nazwa; 
	* jeśli pominięta, wówczas pole otrzymuje nazwę modelu; 
* ``par`` -- napis; nazwa parametru zawierającego model danych;
* ``wyrażenie`` -- wyrażenie liczbowe lub napisowe.

Przykłady: 

* ``table dane IN "CSV" "dane.csv": S <- [Z,DO], d~ODL, c~KOSZT;`` 
	* zapis do pliku ``.csv`` o nazwie ``dane.csv``
	* zapisywane kolumny: ``Z``, ``DO``, ``ODL``, ``KOSZT``
	* kolumny ``Z``, ``DO`` wchodzą do zbioru kontrolnego ``S``
	* wartości z kolumny ``ODL`` są przypisane do parametru ``d``
	* wartości z kolumny ``KOSZT`` są przypisane do parametru ``c``
	* przykładowa tabela: 

| Z | DO | ODL | KOSZT |
| - | - | - | - |
| Seattle | New-York | 2.5 | 0.12 |
| Seattle | Chicago | 1.7 | 0.08 |
| Seattle | Topeka | 1.8 | 0.09 |
| San Diego | New-York | 2.5 | 0.15 |

* ``table wyniki{(f, t) in S} OUT "CSV" "wyniki.csv":``<br/>``f~Z, t~DO, x[f,t]~PRZEPLYW;``
	* zapis do pliku ``.csv`` o nazwie ``wyniki.csv``
	* zapis każdego rekordu dla krotki ``(f, t)`` ze zbioru ``S``
	* tabela wyjściowa składa się z 3 kolumn: 
		* ``Z`` -- wartości indeksu ``f``
		* ``DO`` -- wartości indeksu ``t`` 
		* ``PRZEPLYW`` -- wartości parametru lub zmiennej ``x`` zawierającej ciąg 2-elementowych krotek 

Sterowniki: 

* ``"CSV"`` -- pliki ``.csv``
* ``"xBASE"`` -- pliki ``.dbf``
* ``"ODBC"`` lub ``"iODBC"`` 
* ``"MySQL"``

# Model danych[^](#Spis-treści)

## Sposoby definiowania modelu i danych[^](#Spis-treści)

1. W pojedynczym pliku: 

```
# model -------------------------
instrukcja;
instrukcja;
...
instrukcja;

# dane  -------------------------
data;

dane;
dane;
...
dane;

end;
```

2. W osobnych plikach: 

* plik ``.mod``

```
instrukcja;
instrukcja;
...
instrukcja;

end;
```

* plik ``.dat``

```
data;

dane;
dane;
...
dane;

end;
```

## Wczytywanie modelu i danych[^](#Spis-treści)

### Model i dane w 1 pliku

```
glpsol.exe --model plik.mod
```

### Model i dane w osobnych plikach

```
glpsol.exe --model plik_z_modelem.mod --data plik_z_danymi.dat
```

Jeśli model zawiera sekcję ``data;``, jest ona ignorowana w przypadku załadowania pliku ``.dat``. 

### Zapis danych do pliku zewnętrznego 

```
glpsol.exe --model plik.mod --display wyniki.out
```

* plik ``wyniki.out`` będzie zawierał wartości zwrócone przez funkcje ``display`` i ``printf``. 

```
glpsol.exe --model plik.mod --output wyniki.sol
```

* zapis wyłącznie wyników.

### Sprawdzenie modelu bez wykonywania obliczeń

```
glpsol.exe --check --model plik.mod --wlp problem.lp
```

Zapis problemu wygenerowanego przez model może być zapisany do pliku ``.lp``, nie jest to jednak konieczne.




## Blok danych[^](#Spis-treści)

Sekcja lub plik z danymi nie może zawierać instrukcji (_statements_). 

### Zbiory

Składnie: 

``set nazwa := rekord1, rekord2, ..., rekordn;``

``set nazwa [symbol1, ..., symboln ] := rekord1, ..., rekordn;``

* ``symbol`` -- indeksy wskazujące element zbioru (jeśli dane wejściowe są zbiorem); 
* ``rekord`` -- właśnie dane:  
	* ``:=`` -- opcjonalnie (dla zwiększenia czytelności kodu)
	* ``(przekrój)``
		* rekord kontrolny o składni: ``(el1, el2, ..., eln)``
		* elementy ``el`` mogą być:
			* liczbami
			* napisami
			* gwiazdką ``*``
		* liczba elementów musi odpowiadać liczbie elementów w każdej krotce
		* gwiazdka jest _placeholderem_ dla elementów podanych dalej, np. zapis ``(a, *, b) 1, 2, 3`` pozwoli utworzyć zbiór <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{(a, 1, b), (a, 2, b), (a, 3, b)\}">
		* przekrój bez gwiazdki zostanie dodany do zbioru, np. ``(a, b, c) 1, 2, 3`` --> <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{(a, b, c), (1, 2, 3)\}">
	* ``proste_dane`` -- zapis elementów pojedynczej krotki _n_-elementowej, np. ``set dane := a b c d`` --> <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{(a, b, c, d)\}"> lub <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=\{a, b, c, d\}"> 
	* ``: dane_w_macierzy`` -- dane w postaci macierzy
	* ``(tr) : dane_w_macierzy`` -- dane w postaci macierzy transponowanej

Przecinki mogą być pominięte. 

Przykłady: 

* proste listy (wektory): 
	* ``set miesiac := sty lut mar kwi maj cze;``
	* ``set miesiac 'sty', 'lut', 'mar', 'kwi', 'maj', 'cze';``
	* ``set miesiac "sty", "lut", "marz";``
* zbiory krotek:
	* ``set A [3, mar] := (1, 2), (2, 3), (2, 2);``
	* ``set A [3, 'mar'] := 1 2 2 3 2 2;``
	* ``set B := (1,2,3) (1,3,2) (2,3,1) (2,1,3);``
	* ``set B := (*, *, *) 1 2 3, 1 3 2, 2 3 1, 2 1 3;``
	* ``set B := (1, * 2) 3 2 (2, *, 1) 3 1 (1, 2, 3) (2, 1, 3) (1, 1, 1);``
* macierz: 
	* ``set A [3, 'mar']``<br/>``: 1 2 3 4 :=``<br/>``1 - + - -``<br/>``2 - + + -``<br/>``3 + - - +``<br/>``4 - + - +;``
	* ``set B := (1, *, *)``<br/>``: 1 2 3 :=``<br/>``1 + - -``<br/>``2 - + +``<br/>``3 - + -``<br/>``(2, *, *)``<br/>``: 1 2 3 :=``<br/>``1 + - +``<br/>``2 - - -``<br/>``3 + - -;``

### Zbiory w postaci macierzy

Składnia rekordu danych: 

```
:  c1  c2  ... cn   :=
r1 a11 a12 ... a1n
r2 a21 a22 ... a2n
...
rm am1 am2 ... amn;
```

* ``r`` -- numery lub etykiety (napisy) wierszy; 
* ``c`` -- numbery lub etykiety (napisy) kolumn; 
* ``a`` 
	* wartości: ``+`` lub ``-``
	* krotka dwuelementowa składająca się z indeksów ``(r, c)``
	* ``+`` w zapisie oznacza, że krotka ``(r, c)`` skłądająca się z odpowiednich indeksów jest częścią danych; 
* ograniczniki ``:`` oraz ``:=`` mogą być pominięte

### Zbiory w postaci macierzy transponowanej

Składnia rekordu danych: 

```
(tr): c1  c2  ... cn   :=
r1    a11 a12 ... a1n
r2    a21 a22 ... a2n
...
rm    am1 am2 ... amn;
```

Działanie analogiczne do zwykłej macierzy; jedyna różnica -- krotki oznaczone ``+`` mają przestawione indeksy: ``(c, r)``.

Ograniczniki ``:`` oraz ``:=`` mogą być pominięte

### Parametry

Składnie: 

``param nazwa, rekord, rekord, ..., rekord;``

``param nazwa default wartość, rekord, ..., rekord;``

``param : dane_tabelaryczne;``

``param default wartość: dane_tabelaryczne;``

* ``wartość`` -- opcjonalnie: domyślna wartość parametru;
* ``rekord`` -- dane składające się z elementów: 
	* ``:=`` -- opcjonalnie (zwiększa czytelność kodu),
	* ``[przekrój]`` -- definiuje przekrój danych,
	* ``proste_dane`` -- rekord postaci ``el1, el2, el3...``
	* ``: dane_tabelaryczne`` (_tabular data record_) -- dane w formacie tabelarycznym, np. 
    
    ``param : kol1 kol2 kol3 :=``<br/>``w1 rek rek rek``<br/>``w2 rek rek rek;``
    
    | | kol1 | kol2 | kol3 |
    | - | - | - | - |
    | w1 | rek | rek | rek | 
    | w2 | rek | rek | rek |
         
    * ``(tr) : dane_tabularyczne`` (_transposed tabular data record_) -- jw., ale z dodatkową transpozycją.
	* dane etykietowane (_tabbing data format_) -- dane w foramcie: 
    ``: param default wartość : przekrój : kol1, kol2, kol3 :=``<br/>`` et11, et12, et13, rek11, rek12, rek13``<br/>``et21, et22, et23, rek21, rek22, rek23;`` 
		* ``wartość`` -- wartość domyślna (opcjonalnie)
    * przecinki i dwukropek można pominąć.

Przykłady: 

* ``param T := 4;``
* ``param miesiac := 1 sty 2 lut 3 mar 4 kwi 5 maj;``
* ``param zapas := zelazo 7.32 nikiel 35.8;``
* ``param zapas [*] zelazo 7.32 nikiel 35.8;``
* ``param zapas [zelazo] 7.32 [nikiel] 35.8;``
	* 3 powyższe <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math== \{ zelazo, 7,32, nikiel, 35,8 \}">
* ``param : stan cena wartosc :=``<br/>``zelazo 7.32 .025 -.1``<br/>``nikiel 35.8 .03 .02;``

| | stan | cena | wartosc |
| - | - | - | - |
| zelazo | 7.32 | 0.025 | -0.1 | 
| nikiel | 35.8 | 0.03 | 0.02 |

* ``param : surowiec : stan cena wartosc :=``<br/>``zelazo 7.32 .025 -.1``<br/>``nikiel 35.8 .03 .02;``

| surowiec | stan | cena | wartosc |
| - | - | - | - |
| zelazo | 7.32 | 0.025 | -0.1 | 
| nikiel | 35.8 | 0.03 | 0.02 |

* ``param demand default 0 (tr)``<br/>``: FRA DET LAN WIN STL FRE LAF :=``<br/>``bands 300 . 100 75 . 225 250``<br/>``coils 500 750 400 250 . 850 500``<br/>``plate 100 . . 50 200 . 250 ;``

| FRA | DET | LAN | WIN | STL | FRE | LAF |
| - | - | - | - | - | - | - |
| bands | 300 | 0 | 100 | 75 | 0 | 225 | 250 | 
| coils | 500 | 750 | 400 | 250 | 0 | 850 | 500 |
| plate | 100 | 0 | 0 | 50 | 200 | 0 | 250 |

# Sufiksy (przyrostki)[^](#Spis-treści)

Pozwalają uzyskać dodatkowe wartości ze zmiennych (_variables_), ograniczeń (_constraints_) i celów (_objectives_). 

Składnia: ``.sufiks``

Przykład: ``x[i, j].lb`` -- najniższa wartość tablicy ``x``

## Przyrostki zmiennych[^](#Spis-treści)

| Sufiks | Wartość |
| - | - |
| ``.lb`` | (_lower bound_) najniższa wartość |
| ``.ub`` | (_upper bound_) najwyższa wartość |
| ``.status`` | wynik rozwiązania:<br/>``0`` -- nieokreślony<br/>``1`` -- podstawowy<br/>``2`` -- najniższa wartość<br/>``3`` -- najwyższa wartość<br/>``4`` -- dowolna wartość<br/>``5`` -- stała wartość |

## Przyrostki celów[^](#Spis-treści)

Jw. oraz dodatkowe: 

| Sufiks | Wartość |
| - | - |
| ``.val`` | _primal value of the linear form in the solution_ |
| ``.dual`` | _dual value (reduced cost) of the linear form in the solution_ |

Przyrostki ``.status``, ``.val``, ``.dual`` mogą się znaleźć tylo poniżej instrukcji ``solve;``

# Funkcje związane z datą i czasem[^](#Spis-treści)

## gmtime()

*  ``param utc := gmtime();``  
	* aktualna data i czas UTC
* ``param Berlin := gmtime() + 3600;`` 
	* jw., ale z przesunięciem do strefy czasowej Berlina
* ``param Chicago := gmtime() - 5 * 3600;`` 
	* jw., ale dla Chicago

## str2time

* ``param s, symbolic, := "07/14/98 13:34";``<br/>``param t := str2time(s, "%m/%d/%y %H:%M");``<br/>``display t; #900424020``
	* konwersja daty i czasu w postaci napisu ``s`` do typu liczbowego 

Oznaczenia formatu daty i czasu

| Element | Oznaczenie | Przedział/zapis |
| - | - | - |
| rok | ``%y`` | rok bez wieku |
| miesiąc | ``%m`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, 12]"> |
| miesiąc | ``%b``, ``%h`` | zapis skrócony |
| dzień | ``%d`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, 31]"> |
| godzina | ``%H`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 23]"> | 
| minuta | ``%M`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 59]"> |
| sekunda | ``%S`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 60]">(!) |
| przesunięcie względem GMT | ``%z`` | |
| sekwencja ucieczki dla ``%`` | ``%%`` | |

## time2str

* ``param s, symbolic, := time2str(gmtime(), "%FT%TZ");``<br/>``display s; # s = '2008-12-04T00:23:45Z'``
	* konwersja daty w postaci liczbowej na napis wg formatu

Oznaczenia formatu daty i czasu

| Element | Oznaczenie | Przedział/zapis |
| - | - | - |
| wiek | ``%C`` | | 
| rok | ``%g``, ``%y`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[00, 99]"> |
| rok | ``%G`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1900, 2099]">(?) |
| miesiąc | ``%b``, ``%h`` | postać skrócona (3 znaki) |
| miesiąc | ``%B`` | postać pełna |
| miesiąc | ``%m`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[01, 12]"> |
| tydzień | ``%U`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[00, 53]">[^tydz] |
| tydzień | ``%V`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[01, 53]">[^tydzISO] |
| tydzień | ``%W`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[00, 53]">[^tydz2] |
| dzień roku | ``%j`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[001, 366]"> |
| dzień miesiąca | ``%d`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[01, 31]"> |
| dzień miesiąca | ``%e`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, 31]"> |
| dzień tygodnia | ``%a`` | postać skrócona (2 znaki) |
| dzień tygodnia | ``%A`` | postać pełna |
| dzień tygodnia | ``%u`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[1, 7]"> |
| dzień tygodnia | ``%w`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 6]">[^dtyg] |
| pełna data | ``%D`` | format ``mm/dd/yy`` |
| pełna data | ``%F`` | format ``yyyy-mm-dd`` |
| | 
| ``AM``, ``PM`` | ``%p`` ||
| godzina | ``%H`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[00, 23]"> |
| godzina | ``%k`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[0, 23]"> |
| godzina | ``%I`` | <img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=[01, 12]"> |
| godzina | ``<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math=l`` | ">[1, 12]<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math= |
| minuta | ``%M`` | ">[00, 59]<img style="min-width: 300px;" src="https://render.githubusercontent.com/render/math?math= |
| sekunda | ``%S`` | ">[00, 59]$ |
| godzina i minuta | ``%R`` | format ``gg:mm`` |
| godzina, minuta, sekunda | ``%T`` | format ``gg:mm:ss`` |

[^tydz]: Tydzień ``01`` rozpoczyna się od pierwszej niedzieli roku. Tydzień poprzedni ma numer ``00``. 

[^tydzISO]: Tydzień ``01`` to tydzień mający przynajmniej 4 dni nowego roku, a więc zawierający przynajmniej 4 stycznia. Pierwszy tydzień może zawierać dni z poprzedniego roku. Ostatni tydzień roku może mieć numer ''52'' lub ''53''.  Ostatni tydzień roku może pokrywać się z pierwszym tygodniem nowego roku. 

[^dtyg]: Niedziela ma numer ``0``. 

[^tydz2]: Tydzień ``01`` to tydzień zaczynający się od poniedziałku w nowym roku. Dni nowego roku poprzedzające ten poniedziałek są w tygodniu ``00``. 

Zakres wartości zmiennej liczbowej przechowującej datę i czas: 

* minimum: ``-62 135 596 800`` -- północ 1 stycznia 0001 r.
* maksimum: ``+64 092 211 199`` -- 23:59:59 31 grudnia 4000 r.














> Written with [StackEdit](https://stackedit.io/).


