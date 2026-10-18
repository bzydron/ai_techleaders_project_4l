# DevMentor: wybór sesji z mentorem

- Date: 2026-09-24; odświeżony 2026-10-18
- Mode: own
- Status: odświeżony po dwóch sesjach `om-synthetic-users` (2026-10-18). Wyniki syntetyczne są tylko w sekcji Hypotheses.
- Zakres: wycinek opisu produktu przygotowany na podstawie dołączonych materiałów. Nie zastępuje pełnego briefu ani aktualnego stanu aplikacji.
- Pochodzenie: [SOURCES.md](research/SOURCES.md). Notatki i decyzje są materiałami dostarczonymi. Nie potwierdzono niezależnie opisanych rozmów.
- Evidence basis: dwie notatki od dwóch osób (pilny problem przed wydaniem; niepilny problem rozwiązany samodzielnie) i zapisy decyzji D07, D09, D21, D22, D27, N01, N02. D21, D22 i D27 zapisano z rekomendacji agenta; osoba prowadząca sesję 2026-10-18 zgłosiła w sesji, że założyciel A je potwierdził (bez podpisanego zapisu, D28). Najbardziej istotne nieprzetestowane założenie: A02.
- Coverage: 31 claims — 23 sourced (interview 5, data 0, document 18, product 0, benchmark 0), 0 synthetic, 8 assumed; 3 entries on the collection plan
- Synthetic hypotheses outside Coverage: 3
- Definition of Ready signed by: nie podpisane; podpis należy do założyciela A (D28); gotowość: zbieranie materiału (Now), nie planowanie implementacji.
- Sources: [SOURCES.md](research/SOURCES.md); raporty paneli w `research/walkthroughs/` (tylko Hypotheses).

## Decision summary

Ćwiczenie ma wskazać możliwe bariery przy ocenie oferty i wyborze sesji. Nie rozstrzyga o budowie ani o popycie (Goals).

Podstawa to dwie notatki od dwóch osób i zapisy decyzji. Dwie sesje panelu syntetycznego, po jednym przebiegu i z dwiema personami, dały trzy hipotezy H1–H3. Żadna nie jest ustaleniem: jeden przebieg, a każda persona wynika z jednej notatki.

Najbardziej mogą zmienić ocenę: czy kolejność po dostępności, z profilem mentora albo bez niego, pozwala wybrać mentora (H1, A02: czy płatna konsultacja pasuje do problemu) i co się dzieje, gdy żaden termin nie pasuje (H3, A04: czy termin pozwala dostać pomoc, gdy jest jeszcze użyteczna). Decyzja D28, wybrana w sesji 2026-10-18 na podstawie rekomendacji agenta: Now to zbieranie materiału, a planowanie implementacji wycinka czeka na wyniki rozmów i na podpis Definition of Ready (DoR). Następny krok to trzy rozmowy z Collection plan; ich właścicielem jest założyciel A, termin jest nieznany. D21, D22 i D27: osoba prowadząca sesję zgłosiła potwierdzenie przez założyciela A; podpisanego zapisu nie ma.

## Product

DevMentor pozwala deweloperowi znaleźć mentora i wybrać termin konsultacji. Mentor publikuje ofertę i dostępne terminy. Użytkownik może przejść z listy mentorów albo przez link do konkretnego profilu. `[DOCUMENT]` [D21](research/decisions/D21-finding-a-mentor.md)

Sesja trwa 25 albo 50 minut. Mentor ustala ceny obu długości w granicach operatora. W tym wycinku nie wskazujemy konkretnej oferty cenowej. `[DOCUMENT]` [D09](research/decisions/D09-pricing.md)

Można wybrać opublikowany termin rozpoczynający się co najmniej dwie godziny po rezerwacji. Nie oznacza to gwarancji wolnego terminu dokładnie za dwie godziny. `[DOCUMENT]` [D22](research/decisions/D22-session-timing.md)

Konsultacja ma formę tekstową i odbywa się w ekranie sesji wewnątrz DevMentora. `[DOCUMENT]` [N01](research/decisions/N01-no-video.md), [D27](research/decisions/D27-session-channel.md)

## Target group

- Deweloper z pilnym problemem przy wydaniu produktu, bez dostępnej pomocy seniora. Podstawą tej perspektywy jest jedna dostarczona notatka. `[INTERVIEW]` [working-dev](research/2026-08-20-interview-working-dev.md)
- Deweloper z niepilnym problemem konfiguracji, dla którego samodzielne rozwiązanie i pomoc wewnątrz zespołu pozostają alternatywą. Podstawą tej perspektywy jest osobna dostarczona notatka. `[INTERVIEW]` [platform-dev](research/2026-09-02-interview-platform-dev-solves-alone.md)

Nie znamy udziałów tych sytuacji w populacji ani częstości korzystania z płatnej pomocy. Dobór panelu demonstracyjnego nie jest próbą reprezentatywną. `[ASSUMPTION]` Brak danych o proporcjach.

## Problems

W notatce working-dev błąd TypeScript pojawia się przed wydaniem produktu, a senior jest nieobecny. Po 40 minutach szukania i dwóch sprzecznych odpowiedziach na Discordzie opisano obejście problemu z TODO. Notatka zawiera potrzebę pomocy „within the hour”; znaczenie tego czasu wymaga doprecyzowania. `[INTERVIEW]` [working-dev](research/2026-08-20-interview-working-dev.md)

W notatce platform-dev opisano problem z konfiguracją reguł linta i samodzielne dojście do rozwiązania. Materiał wskazuje małą pilność tego epizodu. Warunkowe odpowiedzi o innym, trudniejszym problemie nie są obserwacją zakupu. `[INTERVIEW]` [platform-dev](research/2026-09-02-interview-platform-dev-solves-alone.md)

## Goals

Cel demonstracyjnej analizy: poznać możliwe bariery podczas oceny oferty i wyboru sesji. `[ASSUMPTION]` Zakres ćwiczenia, bez zadanej z góry odpowiedzi.

Wynik analizy ma pomóc przygotować pytania do sprawdzenia z ludźmi. Nie określa prognozy sprzedaży ani poziomu popytu. `[ASSUMPTION]` Sposób wykorzystania wyniku ćwiczenia.

## Key flows

### Future state, booking and session (1.0), decided steps

1. Użytkownik loguje się przez GitHub lub używa e-maila i hasła. `[DOCUMENT]` [D07](research/decisions/D07-login.md)
2. Znajduje mentora na liście z filtrem po technologii albo otwiera link do jego profilu. Lista jest uporządkowana według ostatnio opublikowanej dostępności. `[DOCUMENT]` [D21](research/decisions/D21-finding-a-mentor.md)
3. Ocenia ofertę, wybiera długość 25 albo 50 minut i odczytuje cenę ustaloną przez mentora. Konkretna cena nie jest podana w tym materiale. `[DOCUMENT]` [D09](research/decisions/D09-pricing.md)
4. Wybiera spośród opublikowanych terminów. Wybrany start musi przypadać co najmniej dwie godziny po rezerwacji. Dokładny dostępny termin wymaga danych konkretnej oferty. `[DOCUMENT]` [D22](research/decisions/D22-session-timing.md)
5. W umówionym terminie bierze udział w tekstowej konsultacji wewnątrz DevMentora. `[DOCUMENT]` [N01](research/decisions/N01-no-video.md), [D27](research/decisions/D27-session-channel.md)

Kroki 2, 4 i 5 opierają się na D21, D22 i D27, zapisanych z rekomendacji agenta. Potwierdzenie założyciela A zgłosiła osoba prowadząca sesję; podpisanego zapisu nie ma.

To narracyjny wycinek wyboru konsultacji. Nie opisuje wyglądu ekranów, obsługi płatności ani rozliczeń po sesji. Pominięcie tych elementów w ćwiczeniu nie oznacza, że produkt ich nie ma. `[ASSUMPTION]` Granice demonstracji.

## Business rules

| ID | Reguła | Źródło |
|---|---|---|
| R01 | Długość konsultacji wynosi 25 albo 50 minut. | `[DOCUMENT]` [D09](research/decisions/D09-pricing.md) |
| R02 | Mentor ustala cenę w granicach operatora. Tu nie ma konkretnego cennika oferty. | `[DOCUMENT]` [D09](research/decisions/D09-pricing.md) |
| R03 | Najwcześniejszy dopuszczalny początek to dwie godziny po rezerwacji; dostępność zależy od opublikowanych slotów. | `[DOCUMENT]` [D22](research/decisions/D22-session-timing.md) |
| R04 | Sesja jest tekstowa i odbywa się w produkcie. | `[DOCUMENT]` [N01](research/decisions/N01-no-video.md), [D27](research/decisions/D27-session-channel.md) |
| R05 | Logowanie: GitHub albo e-mail i hasło. | `[DOCUMENT]` [D07](research/decisions/D07-login.md) |

## Scope

W ćwiczeniu analizujemy perspektywę osoby wybierającej konsultację. Korzystamy z opisu, bez przeglądarki i bez transakcji. Nie podajemy modelowi stanu ekranu, którego nie zaobserwowano. `[ASSUMPTION]` Zakres demonstracji.

- **Now:** zbieranie materiału: trzy rozmowy z Collection plan, sprawdzenie H1–H3 i odpowiedzi na Q01–Q03. `[DOCUMENT]` [D28](research/decisions/D28-now-is-collecting-material.md)
- **Later:** planowanie implementacji wycinka (lista, wybór terminu, sesja tekstowa) po wynikach rozmów i podpisie Definition of Ready; wymaga oczekiwanego wyniku i sposobu jego sprawdzenia, których brief nie ma.
- **Not doing:** zob. Non-goals.

## Non-goals

Poza tym wycinkiem są onboarding mentorów, wybór nowych cen, płatności, anulowanie, wypłaty i notatka po konsultacji. Analiza nie sprawdza działania interfejsu ani kodu. `[ASSUMPTION]` Zakres demonstracji.

Właściciel wyłączeń: założyciel A, wskazany w sesji 2026-10-18 (D28); jego akceptacji nie zapisano.

## Domain glossary

- Mentee: osoba rozważająca konsultację z mentorem.
- Mentor: osoba publikująca ofertę konsultacji i terminy.
- Długość sesji: czas trwania konsultacji.
- Termin: opublikowany moment rozpoczęcia konsultacji.
- Rezerwacja: wybór konkretnego terminu i długości w opisanym procesie.

Definicje porządkują opis ćwiczenia. `[DOCUMENT]` D07, D09, D21, D22 i D27.

## Riskiest assumptions

- A02: oferta płatnej konsultacji pasuje do problemu, z którym przychodzi deweloper. `[ASSUMPTION]` Wymaga obserwacji odpowiednich do decyzji o zakupie.
- A04: dostępny termin pozwala uzyskać pomoc, gdy jest jeszcze użyteczna. `[ASSUMPTION]` Sama decyzja o wyprzedzeniu rezerwacji nie potwierdza dopasowania do sytuacji.

Te założenia określają obszar pytań koordynatora. Nie są opisem cech persony i nie powinny trafiać do jej kontekstu.

## Hypotheses

Źródła: [raport sesji 002](research/walkthroughs/2026-10-18-future-state-booking-and-session-1-0-decided-steps-session-002/report.md), profile po audycie względem notatek, i [raport sesji 001](research/walkthroughs/2026-10-18-future-state-booking-and-session-1-0-decided-steps-session-001/report.md). Sesja 002 koryguje 001: teza, że pilność i płacąca firma odwracają decyzję persony P02, opierała się na linii profilu bez podstawy w notatce i nie jest tu użyta. Obie sesje: stance adversary, narracyjny przepływ bez ekranów, jeden przebieg, dwie persony, każda z jednej notatki. Obie sesje używają tych samych dwóch notatek, więc nie są niezależnym potwierdzeniem. Status każdej hipotezy: Seen once.

- H1 `[SYNTHETIC]` Sama kolejność po ostatnio opublikowanej dostępności (krok 2, D21) nie pozwala wskazać mentora, który robił dokładnie taki problem. Użytkownik wybrałby po znanym nazwisku albo odszedł. Zgłosiły to obie persony w obu sesjach (P01: „too thin for a decision”; P02: oceniłby po tym, „co zrobił”). Zastrzeżenie: persony nie widziały N02 (link do pracy publicznej i opis na stronie mentora), więc luka może leżeć w opisie przepływu, nie w produkcie. Dotyczy A02. Sprawdzenie: Collection plan, wpis 1.
- H2 `[SYNTHETIC]` Zatrudniony deweloper płaciłby osobie tylko za zadanie jednorazowe, kosztujące dzień, znalezione w pięć minut i opłacone przez firmę. Notatka podaje te warunki bez kolejności, a opis kroku 3 nie mówi, kto płaci. Zgłosiła to tylko P02 (sesja 002, krok 3 i wybór C2). Dotyczy A02. Sprawdzenie: Collection plan, wpis 2.
- H3 `[SYNTHETIC]` Brak ścieżki „żaden termin nie pasuje” (krok 4) kończy próbę u pilnego użytkownika. Obie persony zadały to pytanie w obu sesjach (P01: „an option to ask for help sooner than the published slots”; P02: „what happens if the mentor has no slot”). Że użytkownik by odszedł albo sprawdził innego mentora, mówi tylko P01 (wybór C3a). Tę samą hipotezę obejmuje minimalny start po rezerwacji kontra „within the hour” u P01 w obu sesjach; D22 sam mówi, że szybkości nie obiecuje. Dotyczy A04. Sprawdzenie: Collection plan, wpis 3.

## Open questions

| Id | Question | Blocking | Who can answer | Status |
|---|---|---|---|---|
| Q01 | Jak deweloper ocenia, czy mentor robił dokładnie taki problem? Lista jest filtrowana po tagu technologii i uporządkowana według ostatnio opublikowanej dostępności (D21). Link do pracy publicznej i opis na stronie mentora (N02) nie występują w Key flow. `[DOCUMENT]` [D21](research/decisions/D21-finding-a-mentor.md), [N02](research/decisions/N02-no-ratings.md) | nie dla Now (D28); tak dla planowania listy w Later | deweloperzy wybierający pomocnika; właściciel D21 | open |
| Q02 | Kto płaci za sesję osoby zatrudnionej w firmie z kanałem wewnętrznym i na jakich warunkach firma zwraca koszt? Notatka zawiera wypowiedź warunkową („nie płacę za rzeczy do pracy sam”), nie zakup. Nie wiemy, co ta osoba robi, gdy kanał wewnętrzny nie odpowiada. `[INTERVIEW]` [platform-dev](research/2026-09-02-interview-platform-dev-solves-alone.md) | nie | deweloperzy platformowi w firmach z kanałem wewnętrznym | open |
| Q03 | Co widzi użytkownik, gdy żaden opublikowany termin nie pasuje? Krok 4 tego nie opisuje; D22 mierzy czas od rezerwacji do startu, nie rezygnację. `[DOCUMENT]` [D22](research/decisions/D22-session-timing.md) | nie dla Now (D28); tak dla planowania ścieżki zapasowej w Later | właściciel D22; deweloperzy po blokadzie przed wydaniem | open |

Wcześniejsze otwarte kwestie, bez id: znaczenie czasu opisanego w notatce, rzeczywista dostępność konkretnego mentora, cena konkretnej oferty oraz sposób podjęcia decyzji wymagają odpowiednich danych. Nie uzupełniamy ich fikcyjnymi wartościami.

## Collection plan

### Na co patrzysz, wybierając osobę do pomocy z problemem technicznym, i skąd wiesz, że zna ten problem?

- What decision or work needs it: H1, Q01 (kształt listy, krok 2)
- Who can answer it: deweloperzy, którzy w ostatnich miesiącach wybierali osobę do pomocy z problemem technicznym
- How: rozmowa o ostatnim razie („Opowiedz o ostatnim razie…”). Drugorzędna sonda, tylko po części o przeszłości: pokazanie kolejności listy z profilem mentora (N02) i bez niego oraz pytanie, na co by patrzyli
- Owner and by when: założyciel A (D28); termin unknown
- Template: `research/templates/interview-note.md`

### Kto zdecydował i zapłacił za pomoc osoby spoza zespołu ostatnim razem, jak to rozliczono, a gdy kanał wewnętrzny milczał, co zrobiłeś?

- What decision or work needs it: H2, Q02 (krok 3, kto płaci)
- Who can answer it: deweloperzy platformowi w firmach z kanałem wewnętrznym
- How: rozmowa o ostatnim razie, z pytaniem o rozliczenie i o moment ciszy na kanale
- Owner and by when: założyciel A (D28); termin unknown
- Template: `research/templates/interview-note.md`

### Opowiedz o ostatnim razie, gdy znaleziona pomoc była dostępna później, niż jej potrzebowałeś. Co zrobiłeś dalej?

- What decision or work needs it: H3, Q03, A04 (krok 4)
- Who can answer it: deweloperzy po blokadzie przed wydaniem, bez dostępnego seniora
- How: rozmowa o ostatnim razie; pytanie sprawdza też, kiedy pomoc przestaje być użyteczna
- Owner and by when: założyciel A (D28); termin unknown
- Template: `research/templates/interview-note.md`
