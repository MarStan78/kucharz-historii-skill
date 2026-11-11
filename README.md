# Kucharz Historii: recenzent opowiadań dla Claude

Skill dla Claude, który recenzuje historie według zasad dwóch autorów: Lajosa Egriego (*The Art of Dramatic Writing*) i Gianniego Rodariego (*Gramatyka fantazji*). Dostaje opowiadanie albo szkielet fabuły i mówi, co nie działa, dlaczego i co dokładnie zmienić. Celem jest historia, w której napięcie rośnie, a całość kończy się mocną kulminacją.

Kucharz nie pisze historii za autora. Autor przynosi mięso, a kucharz wie, jak je przyrządzić.

## Do czego się przydaje

- opowiadania i bajki, także dla dzieci,
- szkielety fabuły i konspekty,
- scenariusze i pomysły na film,
- historie do czytania na głos.

Pomaga, gdy historia „jakoś nie gra”: środek stoi w miejscu, bohater nic nie decyduje, przeciwnik jest za słaby albo finał rozstrzyga przypadek.

Kucharz nie poprawia stylu gotowego tekstu (do tego jest skill [Zinsser](https://github.com/MarStan78/zinsser-skill)) i nie pisze historii od zera.

## Jak pracuje

Praca ma dwa etapy, a między nimi decyduje autor.

### Etap 1: Diagnoza

Krótka, na jedną lub dwie strony.

1. **Mapa scen.** Dla każdej sceny: kto czego chce, kto podejmuje decyzję, co się zmienia. Sceny, w których nic się nie zmienia, dostają oznaczenie.
2. **Droga postaci.** Skąd wychodzą ważne postacie, dokąd dochodzą, co tracą i ile realnych decyzji podejmują.
3. **Gdzie jest prawdziwy dramat.** Kto przechodzi najdłuższą drogę, kto płaci najwięcej, kto napędza konflikt. Często wychodzi, że najciekawsza postać to nie ta, którą autor uważa za główną.
4. **Niewykorzystane nasiona.** Chwile i szczegóły, które tekst mija bez zauważenia, a które mogą rozwiązać problem.
5. **Dwa lub trzy serca historii.** Każde to jedno zdanie: postać, konflikt, finał. Do każdego kucharz dopisuje, co historia zyskuje i jak dużej przebudowy wymaga.
6. **Pytanie.** Kucharz poleca jedno serce i pyta autora o wybór.

### Etap 2: Recenzja

Pisana pod serce, które wybrał autor. Kucharz idzie od dużych spraw do małych:

1. **Serce.** Czy każda scena pracuje na wybrany cel i czy finał go udowadnia czynem.
2. **Postacie.** Czy mają ciało, otoczenie i psychikę, czy podejmują decyzje i czy ich zmiana idzie krok po kroku.
3. **Przeciwnik i więź.** Czy przeciwnik jest równie silny i co nie pozwala stronom po prostu odejść.
4. **Konflikt i rytm.** Czy historia startuje w dobrym miejscu, czy kolejne kryzysy idą coraz wyżej i czy kulminację rozstrzyga główna postać.
5. **Sceny.** Czy każda ma cel i zmianę, które są zbędne, których brakuje i czy to, co najważniejsze, da się pokazać obrazem.
6. **Przyprawy.** Dla każdego dużego braku dwa, trzy konkretne pomysły do wyboru, wymyślone technikami Rodariego.

Recenzja obejmuje najwyżej siedem głównych problemów. Lista czterdziestu uwag nie pomaga, bo autor nie wie, od czego zacząć.

## Zasady kucharza

- **Nie pisze za autora.** Opisuje, co zmienić. Scenę po poprawce pisze tylko na prośbę.
- **Może podważyć wszystko**, także zakończenie i głównego bohatera. Decyzja należy do autora.
- **Każda uwaga wskazuje konkretne miejsce:** scenę, postać, zdanie.
- **Każda zmiana ma cenę.** Kucharz mówi, co się zyskuje i co trzeba przez to zmienić dalej.
- **Mówi też, co działa**, żeby przy przebudowie nie zepsuć dobrych rzeczy.
- **Trzyma się prostej narracji.** Lekarstwa szuka w postaciach i konflikcie, a nie w formalnych sztuczkach.
- **Egri i Rodari to narzędzia, nie prawo.** Uwaga pada wtedy, gdy historia na czymś traci, a nie wtedy, gdy łamie regułę.

## Co dostajesz

- **Po etapie 1:** plik `Kucharz - diagnoza - <tytuł>.md` z mapą scen i sercami historii, a w czacie najważniejsze odkrycie i pytanie.
- **Po etapie 2:** plik `Kucharz - recenzja - <tytuł>.md` z wyrokiem, listą tego, co już działa, głównymi problemami (gdzie, co nie gra, dlaczego, przepis, cena), nową drogą bohatera, tabelą „scena po scenie”, pomysłami do wyboru i kolejnością pracy.

Gdy poprawisz tekst, kucharz porówna nową wersję z poprzednią recenzją i powie, co już działa, a co wciąż nie.

## Zawartość repozytorium

```
kucharz-historii/
├── SKILL.md                 instrukcja dla Claude
└── references/
    ├── przepisy.md          ściąga: objaw, przyczyna, lekarstwo
    ├── egri.md              opracowanie książki Egriego
    └── rodari.md            opracowanie książki Rodariego
kucharz-historii.skill       gotowa paczka do wgrania w Claude
```

Najważniejszy plik do pracy to [przepisy.md](kucharz-historii/references/przepisy.md): tabele objawów i lekarstw dla serca historii, bohatera, przeciwnika, konfliktu, finału, scen i dialogu, a do tego rady do historii dla dzieci i techniki wymyślania brakujących pomysłów.

## Instalacja

**Claude (aplikacja lub claude.ai):** pobierz plik [kucharz-historii.skill](kucharz-historii.skill) i wgraj go w ustawieniach, w sekcji umiejętności (Skills).

**Claude Code:** skopiuj folder `kucharz-historii` do `~/.claude/skills/` (wszystkie projekty) albo do `.claude/skills/` w wybranym projekcie.

## Jak uruchomić

Wklej historię albo wskaż plik i napisz na przykład:

- „Przepuść to przez kucharza”
- „Zrecenzuj historię”
- „Co nie gra w tej historii?”
- „Sprawdź to Egrim”

Skill włącza się też sam, gdy wrzucasz opowiadanie, bajkę, scenariusz albo szkielet fabuły i pytasz o konstrukcję, postacie, konflikt lub zakończenie.

Skill pracuje po polsku.

## Źródła

Skill opiera się na dwóch książkach:

- Lajos Egri, *The Art of Dramatic Writing*,
- Gianni Rodari, *Gramatyka fantazji* (*Grammatica della fantasia*, 1973; opracowanie powstało na podstawie przekładu hiszpańskiego z 1983 r.).

Repozytorium nie zawiera książek. Pliki `egri.md` i `rodari.md` to streszczenia po polsku, napisane własnymi słowami, a nie przekłady. Plik `przepisy.md` to opracowanie autorskie.

Skill nie jest związany z autorami książek, ich spadkobiercami ani wydawcami. Jeśli chcesz poznać te zasady z pierwszej ręki, kup książki.

## Licencja

MIT, szczegóły w pliku [LICENSE](LICENSE).
