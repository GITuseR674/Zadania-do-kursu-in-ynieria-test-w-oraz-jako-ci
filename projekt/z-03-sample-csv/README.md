# z-03-sample-csv — Przykładowe dane do Modułu 3

Folder zawiera 6 plików CSV do testowania aplikacji z Zadania 3.

## Format plików

- **Separator:** `;` (średnik)
- **Nagłówek:** `time;value`
- Każdy wiersz: `<czas w sekundach>;<wartość>`

## Nazewnictwo plików

```
<typ>_a_<wartość_a>_b_<wartość_b>.csv
```

| Typ      | Parametr `a` | Parametr `b` | Plik                        |
|----------|--------------|--------------|-----------------------------|
| `linear` | 1            | 8            | `linear_a_1_b_8.csv`        |
| `linear` | 3            | 6            | `linear_a_3_b_6.csv`        |
| `linear` | 4            | 9            | `linear_a_4_b_9.csv`        |
| `exp`    | 1            | 8            | `exp_a_1_b_8.csv`           |
| `exp`    | 3            | 6            | `exp_a_3_b_6.csv`           |
| `exp`    | 4            | 9            | `exp_a_4_b_9.csv`           |

- `linear` — dane liniowe (model: `a*x + b` z szumem)
- `exp` — dane wykładnicze (model: `a*e^x + b` z szumem)

## Użycie w aplikacji

Wczytaj wybrany plik przez dialog wyboru pliku w aplikacji (`student/TestingSuiteApp/`). Dane liniowe (`linear_*`) dobrze nadają się do testowania regresji liniowej. Dane wykładnicze (`exp_*`) przydatne do weryfikacji skali logarytmicznej na wykresie.

## Generowanie dodatkowych danych

Aby wygenerować własne zestawy danych, użyj notatnika: [`generate.ipynb`](generate.ipynb)
