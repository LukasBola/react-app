# Lekcja 1 (2025-07-03)

## Co zrobiliśmy?
- Utworzyliśmy prosty komponent Message, który wyświetla komunikat "Hello World!" na stronie.
- Skonfigurowaliśmy stylowanie tak, aby wiadomość była wyśrodkowana na środku ekranu.
- Poprawiliśmy importy i strukturę plików, aby style działały prawidłowo.

## Z czym mieliśmy problem?
- Pomimo poprawnych stylów w pliku App.css, napis był wyświetlany w lewym górnym rogu.
- Problem wynikał z tego, że style z App.css nie były ładowane, ponieważ brakowało importu `import './App.css';` w pliku App.tsx.
- Dodatkowo, wcześniejsze style w pliku index.css (na elemencie body) nadpisywały centrowanie, przez co flexbox z App.css nie działał poprawnie.

## Co było błędem?
- Brak importu pliku App.css w pliku App.tsx.
- Style flexbox na body w index.css, które kolidowały z centrowaniem w App.css.

## Wnioski
- Zawsze upewnij się, że pliki CSS są importowane w odpowiednich komponentach.
- Unikaj nakładających się stylów flexbox na różnych poziomach drzewa DOM.
- Testuj zmiany na bieżąco i sprawdzaj, które style faktycznie wpływają na wyświetlanie elementów.
