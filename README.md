# WarsawJS Workshop #36 Podstawy JavaScript

## Wymagania
* Node.js
* npm
* git
* Przeglądarka (np. Google Chrome)
* Edytor kodu

Informacje jak je zainstalować możesz znaleźć tu: https://warsawjs.github.io/workshop-setup/36/

## Przygotowanie
1. Sfrokuj to repozytorium – ([Jak to zrobić](https://help.github.com/en/articles/fork-a-repo))
2. Sklonuj je na swój komputer  – ([Jak to zrobić](https://help.github.com/en/articles/cloning-a-repository))
3. W terminalu (lub Git Bash) przejdź do nowopowstałego folderu z projektem o nazwie `warsawjs-workshop-36-js-basics` przy użyciu komendy [`cd`](https://www.computerhope.com/unix/ucd.htm) i zainstaluj zależności komendą `npm install`

## W trakcie warsztatów
1. Nasze mini-projekty będziemy trzymać w folderze `zadania/`
2. Serwer który będzie odświeżał stronę gdy zmienią się pliki odpalisz komendą `npm start`
3. Pamiętaj o dobrej zabawie!

---

## Zadanie 1

### Zmienne

1. Napisz program który pobierze i zapisze imię użytkownika do zmiennej i cię przywita
> Do pobrania imienia możesz użyć funkcji [`prompt`](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt)

2. Dodaj możliwość podania wieku. Na jego podstawie policz ile brakuje użytkownikowi do emerytury (65 lat)

### Instrukcje warunkowe

3. Dzisiaj mamy niedzielę i do tego niehandlową. Dla tego jest dzisiaj wolne. Sprawdźmy czy użytkownik ma wolne od `podstawówki`, `liceum`, czy `pracy/studiów`. Jeśli jest emerytem to ma wolne cały czas – nie musimy mu o tym przypomniać.

4. Dzisiaj imieniny ma Joachim. Ma tak na imię? Złóżm mu życzenia!

### Tablice

5. Nie ma tak łatwo i każdego dnia imieniny ma więcej niż jedna osoba. Maurycy i Tomasz też mają urodziny. Jeśli ma na imię Joachim, Maurycy lub Tomasz – złóż życzenia

7. Określ jak bardzo użytkownik jest miłośnikiem zwierząt – jeśli lubi więcej niż 1 to bardzo je lubi, jeśli więcej niż 3 to za nimi szaleje, a jeśli więcej niż 5 to jest honorowym miłośnikiem zwierząt WarsawJS

6. Dodaj możliwość podania przez użytkownika ulubionego zwierzaka. Daj znać, że ostatniemu podanemu zwierzakowi jest przykro, bo użytkownik pomyślał o nim na samym końcu
> do pobrania listy zwierzaków znów użyj [`prompt`](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt), a żeby zamienić podaną listę na tablicę użyj [`.split(' ')`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)

### Pętle

7. Zamieńmy sprawdzanie czy użytkownik ma imieniny aby używać pętli i byśmy mogli sprawdzać wszystkie imiona dla dzisiejszego dnia – `['Joachim', 'Maurycy', 'Tomasz', 'Bazyla', 'Daria', 'Digna', 'Eksuperiusz', 'Emeryta', 'Emmeram', 'Emmeran', 'Feliks', 'Ignacy', 'Imbram', 'Innocenty', 'Jonasz', 'Józefa', 'Kandyd', 'Prosimir', 'Tacjusz', 'Wiktor', 'Witalis']`

8. Użytkownik ma psa? Niech ten zwierzak da nam znać i niech zaszczeka.

## Zadanie 2

Przy deklarowaniu zmiennych staraj się używać `const` kiedy to tylko możliwe.

1. Wypełnij tablicę wszystkimi liczbami parzystymi od 1 do 100

2. Wybierz wszystkie liczby podzielne przez 6
> do sprawdzenia użyj reszty z dzielenia (operator `%`, np. `5 % 2` jest równe, bo `5 - 2 * 2 = 1`)

3. Do każdej z tych liczb dodaj 1

4. Policz sumę tych wszystkich liczb

## Zadanie 3

1. Wypisz X (5x5) w konsoli przy użyciu pętli
```
X   X
 X X
  X
 X X
X   X
```

## Zadanie 4

Załóżmy razem sklep ze sprzętem elektronicznym. Nazwijmy go W-kom (patent pending)

1. Musimy jakoś umożliwić użytkownikowi dowiedzieć się o szczegółach produktów. Przy użyciu tego obiektu opisz ten komputer

```
MacBook Pro (2017, 4 porty USB)
Procesor: 3.1 GHz Intel Core i5 (2 rdzenie)
Pamięć: 16 GB
Karta graficzna: Intel Iris Plus Graphics 650 1.5 GB
```

```javascript
const computer = {
  name: 'MacBook Pro',
  releaseYear: 2017,
  specs: {
    numberOfUsbs: 4,
    cpu: {
      name: 'Intel Core i5',
      cores: 2,
      frequency: 3.1
    },
    memory: 16,
    gpu: {
      memory: 1.5,
      name: 'Intel Iris Plus Graphics 650'
    }
  }
};
```

2. Każdy sklep stacjonarny musi mieć dokumentację. Z listy pracowników:
```javascript
const employees = [
  {
    name: 'Andrzej Małek',
    position: 'manager',
    responsibleForRoom: 102,
    age: 41
  },
  {
    name: 'Sławomierz Furmanek',
    position: 'bathroomCleaner',
    responsibleForRoom: 101,
    age: 35
  },
  {
    name: 'Ludomir Michalik',
    position: 'shopAssistant',
    age: 31
  },
  {
    name: 'Żytomir Sekula',
    position: 'shopAssistant',
    age: 25,
  },
  {
    name: 'Balbina Trzcinska',
    position: 'customerSatisfactionSpecialist',
    responsibleForRoom: 100,
    age: 23,
  },
]
```

Stwórz opis sklepu:

```javascript
const shop = {
  rooms: [102, 101, 100],
  manager: {
    name: 'Andrzej Małek',
  },
  customerSatisfactionSpecialist: {
    name: 'Balbina Trzcinska',
  },
  shopAssistants: [
    {
      name: 'Ludomir Michalik',
    },
    {
      name: 'Żytomir Sekula',
    },
  ],
  bathroomCleaners: {
    name: 'Sławomierz Furmanek',
  },
  averageAge: 31
}
```

3. Wakacje się już skończyły, ale powakacyjna promocja może być zawsze prawda? Dajmy rabat wszystkim uczniom których ważona średnia ocen jest wyższa od 4.5

Napisz funkcję która sprawdzi czy klient dostanie rabat. Wagi ocen:
```
Polski: 4
Matematyka: 4
Fizyka: 3
Historia: 3
Geografia: 3
Chemia: 3
WF: 2
Religia: 2
```

Argumentem funkcji będzie obiekt w formie
```json
{
  "polski": 4,
  "matematyka": 4,
  "fizyka": 3,
  "historia": 3,
  "geografia": 3,
  "chemia": 3,
  "wf": 2,
  "religia": 2
}
```

## Zadanie 5

1. Napisz prosty formularz rejestracji przy użyciu znaczników HTML `input`, `form` i `button`. Powinien on mieć pola `email` i `hasło`

2. Po naciśnięciu na przycisk zarejestruj się email i hasło powinny zostać wypisane w konsoli.
> znacznik form jest tak zbudowany, aby automatycznie wysyłał formularz i przeładowywał stronę. Żeby temu zapobiec w event listenerze dla event `submit` dodaj na samym początku `e.preventDefault()`

3. Po wysłaniu formularza powinniśmy sprawdzać czy email nie jest już użyty (sprawdzamy względem tablicy emaili)

4. Przy wysyłaniu formularza sprawdźmy czy hasło nie jest zbyt słabe. Jeśli hasło pasuje do któregoś z następujących wyświetl odpowiedni komunikat w konsoli

```javascript
const poorPasswords = {
  password: "już 'hasło' by było bezpieczniejsze",
	qwerty: "Bo przecież nikt z nas nie ma klawiatury...",
  123: "słabe hasło masz ty!",
	admin: "to nie logowanie do routera",
  football: "Według randomowej strony którą znalazłem w internecie piłka nożna ma 4 miliardy fanów na świecie. Na pewno nikt nie wpadł żeby uzyć takiego hasła 🤔"
}
```

5. Zamieńmy sprawdzanie po wysłaniu formularza na sprawdzanie podczas wpisywania
> event 'input', albo 'change'

6. Dodajmy opisy pod polami – wyświetlajmy w nich błędy zamiast w konsoli

7. [🌟 Zadanie dodatkowe] Jeśli użytkownik poda hasło `purr` wyświetl obrazek kota pod formularzem
> możesz do tego użyć tej strony ze zdjęciami kotów http://placekitten.com/200/300

## Zadanie 6

Znamy już trochę tego JSa może warto by było użyć jakiegoś API? Ale jakiego? Znajdźmy jakieś dla siebie!

1. Zrób zapytanie `GET` do `https://api.apis.guru/v2/list.json` i wyświetl jego wynik w konsoli

2. Dodaj diva w pliku html o id `list`

3. Dla każdego api stwórz nowy `div` (jako kontener) do którego dodasz `h1` którego treścią będzie nazwa api
> do dostania tablicy kluczy i wartości obiektu użyj [Object.entries(array)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries)

4. Do każdego api dodaj jeszcze link do dokumentacji api `versions.swaggerUrl` i wyświetl logo danego api `versions.info.x-logo.url`
> do dostania się do najnowszej wersji danego api użyj tej funkcji
> ```javascript
> const getInfo = versions => versions[Object.keys(versions)[0]];
> ```
