# Zadanie 5

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
