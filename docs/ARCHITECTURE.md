# Zapytaj Hanki — architektura informacji

## Zasada nadrzędna
Struktura ma obsłużyć setki i docelowo tysiące wartościowych poradników bez tworzenia cienkich stron. Polski startuje pierwszy; przyszłe języki mogą korzystać z prefiksów `/pl/`, `/en/`, `/uk/` po decyzji o ekspansji.

## Główna nawigacja
- Pieniądze i kredyt
- Dom
- Samochód
- Praca i podatki
- Emerytura
- Zdrowie
- Dokumenty i urzędy
- Polska ↔ USA
- Stany

## Docelowe huby
### /pieniadze/
Credit score, historia kredytowa, raport kredytowy, karty, bankowość, pożyczki.

### /dom/
Mortgage, down payment, preapproval, closing costs, PMI, escrow, wynajem, property tax, HOA, ubezpieczenie domu.

### /samochod/
Kupno auta, financing, APR, leasing vs financing, title, dealer fees, ubezpieczenie, DMV.

### /praca/ i /podatki/
W-2, 1099, wypłata, overtime, podstawy podatków, IRS. Rozdzielamy huby, ale łączymy je w nawigacji.

### /emerytura/
Social Security, credits, 401(k), IRA, świadczenia małżeńskie i rodzinne, Polska + USA.

### /zdrowie/
Ubezpieczenia zdrowotne, Medicare, deductible, copay, HMO/PPO. Publikacja ostrożna ze względu na zmienność.

### /dokumenty/
REAL ID, SSN, paszport, apostille, formularze, praktyczne sprawy urzędowe.

### /polska-usa/
ZUS + SSA, emerytura transgraniczna, dokumenty i sprawy wymagające kontekstu obu krajów.

### /stany/
Strony tylko wtedy, gdy procedura lub prawo rzeczywiście różnią się między stanami. Bez 50 klonów.

## Nawigacja
Desktop: Tematy ▾ jako mega-menu + Popularne + Stany + O nas.
Mobile: przycisk menu otwierający duży, czytelny panel kategorii.
Search pozostaje główną ścieżką dla użytkownika znającego swój problem.

## URL
- Bez lat w evergreen URL.
- Krótkie, opisowe slugi.
- Jedna intencja / jeden kanoniczny poradnik; warianty zapytań obsługuje ta sama strona.
- Brak duplikatów tworzonych wyłącznie dla synonimów.

## Internal linking
Każdy artykuł linkuje do:
1. huba nadrzędnego,
2. 2–5 bezpośrednio powiązanych poradników,
3. naturalnego kolejnego kroku użytkownika.

Przykład: credit score → credit report → utilization → pierwsza karta → car loan / mortgage.
