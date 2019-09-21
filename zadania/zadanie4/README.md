# Zadanie 4

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
