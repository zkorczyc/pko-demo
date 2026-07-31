# PKO Bank Polski Executive Demo — Talk Track

**Talia:** `demo-unified/index.html` · **~25–30 min** z pytaniami · **Nawigacja:** ← → lub spacja · **Link bezpośredni:** `#7` otwiera slajd 7 (numeracja od 1)

**Obsada:** Michał Kowalski (pozyskanie + polecenie) · Zofia Wiśniewska (retencja) · Karolina Nowak (praktyczka)

**Jedno zdanie na start:** *Macie już dane i aplikację IKO. Brakuje jednej warstwy, która słucha — i reaguje — jako jedna rozmowa w reklamie, na webie, w aplikacji, e-mailu i SMS-ie.*

---

## Otwarcie (3 slajdy)

### Okładka — *Jedna platforma. Każdy sygnał.*
> "Dziękuję za czas. Dziś pokażę, jak pozyskanie i retencja mogą wyglądać w PKO Banku Polskim na platformie Adobe — nie jako dwa osobne programy, tylko jedna spójna podróż klienta."

### Dwa akty, jedna platforma
> "Pozyskanie znajduje Michała, zanim złoży wniosek. Kilka tygodni później Michał jest już najlepszym klientem — aplikacja sama podpowiada mu polecenie znajomego przez program PKO Polecam. Retencja odzyskuje Zofię, gdy zmienia się jej życie — nie gdy rezygnuje z karty."

### Trzy postacie, jedna platforma
> "Michał to nasza historia pozyskania — PKO Mastercard Platinum. Zofia to retencja — ta sama Przejrzysta karta kredytowa, nowy etap życia. Karolina prowadzi platformę: segmenty, podróże, decisioning i CJA."

---

## Akt 01 — Pozyskanie (~12 min)

### Divider — *Zdobądź właściwego klienta*
> "Akt pierwszy: zasięg bezpieczny dla prywatności, spersonalizowany przekaz, natychmiastowa decyzja, pełna aktywacja na webie i w aplikacji."

### Poznaj Karolinę / Poznaj Michała
> "Michał Kowalski, 38 lat, kierownik projektu w Warszawie. Aktywny użytkownik Allegro — ale nie jest jeszcze klientem PKO. Karolina znajduje go przez RTCDP Collaboration z Allegro — bez wymiany danych osobowych."

### 1–13 · Ścieżka Michała
> "Reklama na Instagramie, spersonalizowany landing, wniosek mobilny, natychmiastowa decyzja, e-mail i SMS z potwierdzeniem, aplikacja IKO i portfel, bogaty profil, ranked ekran główny, web zgodny z aplikacją, mądrzejsze media płatne. Trzynaście kroków — jeden profil."
>
> **Slajd 7 (e-mail):** to jest prawdziwy szablon HTML z `pko/email-templates/` — nie makieta. Warto to podkreślić w sali.

### 14–15 · Epilog: Polecenie
> "Kilka tygodni później Michał regularnie płaci kartą — Experience Decisioning ocenia polecenie jako najlepszą kolejną akcję. Program PKO Polecam: rejestracja w IKO, przekazanie kodu, spełnienie warunków regulaminu — nagroda dla obu stron. Michał nie czeka na kampanię — platforma sama podpowiada moment."

---

## Akt 02 — Retencja (~8 min)

### Divider — *Odzyskaj z trafnością*
> "Zofia nie odeszła, bo zawiedliśmy. Jej życie się zmieniło — a my wciąż mówiliśmy do tej sprzed zmiany."

### Poznaj Zofię / Wtedy vs teraz
> "Zofia Wiśniewska, 34 lata, pięć lat z Przejrzystą kartą kredytową. Zamążpójście, córka, wydatki na BLIK i zakupy spożywcze — wydatki na kartę spadły o 70%, a PKO wciąż wysyłało kampanie modowe."

### 1–7 · Ścieżka Zofii
> "Oś czasu profilu pokazuje zmianę. Karolina buduje segment wysokiego ryzyka odejścia. Experience Decisioning wybiera ofertę rodzinną zamiast mody. Jedna podróż w AJO dla całego segmentu — e-mail, potem SMS. Zofia reaktywuje się przez e-mail, web/aplikację pokazują tę samą ofertę, push zamyka podróż potwierdzeniem."

### Podsumowanie — *Pełny obraz*
> "Cofnijmy się od pojedynczych ekranów. To nie są dwie osobne kampanie — to jeden model operacyjny. Michał mógł zostać kolejnym klientem bez polecenia. Zofia mogła stać się statystyką odejścia. Ten sam profil, ten sam decisioning, ten sam kanwas podróży, którym zarządza Karolina."

---

## Zamknięcie

- **CMO:** "Jedna rozmowa w każdym kanale — i dowód, gdy zapyta zarząd."
- **CIO:** "Współpraca partnerska bez wymiany danych; orkiestracja danych własnych, którą kontrolujecie."

## Uwagi dla prowadzącego

- **Tempo:** ~40–50 sek na slajd fabularny; slajdy person mogą być krótsze.
- **Wizualizacje:** wszystkie ekrany to oznaczone placeholdery (`Zrzut ekranu — …`) — podmień je na realne zrzuty, gdy będą gotowe. Wyjątek: slajd 7 to prawdziwy, działający szablon e-mail.
- **Podgląd lokalny:** `python3 -m http.server 8080` w katalogu `pko/` (nie w `demo-unified/` — e-mail na slajdzie 7 jest ładowany ze ścieżki względnej `../email-templates/`).
