# Zadanie 6

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
