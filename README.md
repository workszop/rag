# rag

Symulator systemu RAG dla wsparcia technicznego / Tech Support RAG System Simulator.

Jeden plik `index.html` (bez kroku budowania, działa z `file://`), przygotowany do prezentacji na jednym ekranie 16:9. Po lewej czat, czyli to, co widzi klient. Po prawej „Za kulisami”, osiem kroków:

1. Jak działa RAG – animowany schemat całej drogi (na pełną szerokość, przycisk „Odtwórz”).
2. Osadzanie dokumentów – tekst 8 dokumentów zamienia się na wektory po 32 liczby i trafia do bazy wektorowej.
3. Pytanie klienta – pytanie trafia do czatu.
4. Osadzanie pytania – wektor pytania (32 liczby) i wyjaśnienie, że znaczenie niesie cały układ liczb, a nie pojedyncze wymiary.
5. Wyszukiwanie – ta sama baza wektorowa z podświetlonymi znalezionymi dokumentami (maks. 3, próg 0.30).
6. Budowanie promptu – prompt systemowy + dokumenty w sekcji KONTEKST + pytanie.
7. Odpowiedź – w czacie, z linkami do dokumentów źródłowych (otwierają panel dokumentów).
8. Co się wydarzyło – ten sam schemat z danymi z bieżącego pytania; kliknięcie etapu wraca do niego.

Model osadzeń jest zabawkowy: ukryte tematy (słowa kluczowe PL/EN) są mieszane stałym losowym obrotem w 32 gęste liczby, więc żadna liczba nie oznacza „laptopa”, a podobne teksty dostają podobne wektory.

- Język: polski (domyślny) i angielski, przełącznik PL/EN w nagłówku, wybór zapamiętany w `localStorage`.
- Krok po kroku: przycisk „Dalej: …” pod kartą kroku (lub `→`) przechodzi o jeden krok; „Wyślij” w czacie (`Enter`) tylko wysyła pytanie, dalsze kroki uruchamia użytkownik.
- Przycisk „Schemat” w nagłówku (`M`) otwiera schemat całej drogi z zaznaczonym bieżącym krokiem („Tu jesteś”); osiągnięte etapy pokazują dane z bieżącego pytania i są klikalne.
- Skróty: `→` dalej, `←` wstecz, `M` schemat, `P` odtwórz animację, `R` od nowa, `D` dokumenty, `L` język.
- Styl: edulab (Editorial Color).
