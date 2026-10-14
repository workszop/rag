# rag

Symulator systemu RAG dla wsparcia technicznego / Tech Support RAG System Simulator.

Jeden plik `index.html` (bez kroku budowania, działa z `file://`). Pokazuje krok po kroku, jak RAG indeksuje dokumenty, zamienia pytanie na wektor, wyszukuje podobne dokumenty (podobieństwo kosinusowe, próg 0.30, top 3) i generuje odpowiedź tylko na ich podstawie.

- Język: polski (domyślny) i angielski, przełącznik PL/EN w nagłówku, wybór zapamiętany w `localStorage`.
- Skróty: `Enter` uruchom, `N` następny krok, `R` reset, `D` dokumenty, `L` język.
- Styl: edulab (Editorial Color).
