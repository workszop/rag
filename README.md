# rag

Symulator systemu RAG dla wsparcia technicznego / Tech Support RAG System Simulator.

Jeden plik `index.html` (bez kroku budowania, działa z `file://`), przygotowany do prezentacji na jednym ekranie 16:9. Po lewej czat, czyli to, co widzi klient. Po prawej „Za kulisami”, sześć kroków RAG:

1. Osadzanie dokumentów – start od 8 dokumentów tekstowych; „Dalej” zamienia je w bazę wektorową (rekordy z wektorem o 4 wymiarach).
2. Pytanie klienta – pytanie trafia do czatu.
3. Osadzanie pytania – ten sam model, te same wymiary.
4. Wyszukiwanie – ta sama baza wektorowa z podświetlonymi znalezionymi dokumentami (maks. 3, próg 0.30).
5. Budowanie promptu – prompt systemowy + dokumenty w sekcji KONTEKST + pytanie.
6. Odpowiedź – w czacie, z linkami do dokumentów źródłowych (otwierają panel dokumentów).

- Język: polski (domyślny) i angielski, przełącznik PL/EN w nagłówku, wybór zapamiętany w `localStorage`.
- Skróty: `→` dalej, `←` wstecz, `R` od nowa, `D` dokumenty, `L` język; `Enter` w czacie przechodzi wszystkie kroki automatycznie.
- Styl: edulab (Editorial Color).
