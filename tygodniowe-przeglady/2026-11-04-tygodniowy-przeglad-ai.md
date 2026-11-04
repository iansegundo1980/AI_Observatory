# Tygodniowy przegląd AI — 4 listopada 2026

**Okres objęty podsumowaniem:** 28 października – 4 listopada 2026
**Data publikacji podsumowania:** 4 listopada 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **21–28 października 2026** i powstał rano 28 października. Niniejszy dokument go nie powtarza: nie opisuje od nowa GPT-6.1 Terra, premiery Kimi K3.1 Pro i Highspeed, Genie 4, wydania wag Nemotron 3.5 Bolt E4B, opinii Piątego Okręgu w *Jackson Federation of Teachers v. Fitch*, Practice Note ACAT, wytycznych Sądu Najwyższego Tasmanii, wejścia w życie odłożonych przepisów polskiej ustawy o systemach AI ani relacji o przewodniku sądów Nowego Jorku. Zapowiedź wag Kimi jest tu tylko sprawdzona ponownie, bo termin „do 4 listopada” przypada na dzień tego przeglądu. Ogłoszenie Gemini 4 Carbon nosi datę 28 października i nie weszło do przeglądu z tamtego poranka.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z wpisu premierowego, karty modelu albo dokumentacji API. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru i harnessy się nie pokrywają. Tam, gdzie dwa oficjalne teksty tej samej firmy podają różne rozbicia parametrów albo różne wyniki tego samego testu, przegląd przytacza oba sformułowania i ich nie uśrednia.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Tydzień domyka zapowiedź z poprzedniego przeglądu: wagi poprawionego Mistral Large 4 leżą na Hugging Face od 29 października. Tego samego okna dotyczy ogłoszenie Gemini 4 Carbon, nadal bez ogólnego dostępu, oraz dwa komunikaty OpenAI — o pracy modeli przy projektowaniu sprzętu i o wspólnym sygnale preferencji treningowych. Publicznego wydania wag Kimi K3.1 Pro rano 4 listopada nie było.

### 1.1. Mistral: wagi Mistral Large 4, „Le Chonk” (29 października 2026)

**29 października 2026** Mistral opublikowało wagi poprawionego **Mistral Large 4**. Metadane strony premierowej niosą `datePublished` **2026-10-29T12:00:07.000Z**. Ta sama strona ma `dateModified` **2026-11-03T22:40:12.940Z**. Zdania poniżej są z tekstu odczytanego **4 listopada 2026**; treść poprawki z 3 listopada nie została porównana z wersją z dnia premiery. Blog Hugging Face z tego samego wydania jest opatrzony datą **29 października 2026**. TechCrunch datuje swój tekst na 29 października, 10:00 czasu PDT.

Poprzedni przegląd, z rana 28 października, stwierdzał, że wagi w repozytorium jeszcze nie leżą, a karta podawała wtedy ETA 31 października. Wydanie nastąpiło dwa dni przed tamtą datą z karty. Publiczny podgląd API z **6 października 2026** nie jest wydarzeniem tego tygodnia. Nowością jest checkpoint po dalszym uczeniu ze wzmocnieniem oraz publikacja wag.

Karta wag w repozytorium `mistralai/Mistral-Large-4-1T-A52B` opisuje model jako około **1 bln** parametrów, z **49 mld** aktywnymi na token i **52 mld** po doliczeniu embeddingów oraz warstwy wyjścia. W sekcji cech ta sama karta pisze „~1T total / ~52B active”: granularne Mixture-of-Experts, **128** ekspertów routowanych, **4** aktywne na token i **1** ekspert współdzielony. Strona dokumentacji API, której nagłówek nadal nosi datę **6 października 2026**, podaje **52 mld** aktywnych, **1,05 bln** łącznie i enkoder wizyjny **1,6 mld**. To trzy sformułowania tej samej firmy. Przegląd ich nie scala.

Z karty, wspólnie dla opisu wag: wejście tekst i obraz, wyjście tekst, okno kontekstu **1 mln** tokenów, trzy poziomy wysiłku rozumowania `low`, `medium` i `high` (domyślnie `high`). Zalecane próbkowanie na karcie: temperatura **1,0**, top-p **0,95**. Karta pisze o treningu od zera na **3 800** układach NVIDIA Grace Blackwell we własnych centrach danych Mistrala w Europie oraz o natywnej obsłudze ponad **160** języków, w tym wszystkich języków urzędowych Unii Europejskiej. Identyfikator w API to `mistral-large-4`. Obok wag FP8 jest skwantyzowany checkpoint **NVFP4** (`mistralai/Mistral-Large-4-1T-A52B-NVFP4`), opisany jako celujący w układy Blackwell. Karta wymienia też wbudowaną głowicę spekulacyjną DSpark. Osobny wpis Hugging Face podaje inne liczby części tych samych testów; poniższa tabela bierze się z wpisu Mistrala i z karty, nie z tamtego wpisu.

Licencja z karty i z wpisu: **Mistral Ecosystem Open-Weight License**, zmodyfikowane MIT. Użycie, modyfikacja, dostrajanie i komercjalizacja są dozwolone, z jednym warunkiem: podmiot prowadzący ofertę modelu jako usługi (Model-as-a-Service) potrzebuje osobnej licencji komercyjnej od Mistrala.

Cennik podany we wpisie jako obowiązujący „od dzisiaj”: **0,70 USD** za 1 mln tokenów wejścia, **0,07 USD** za 1 mln tokenów wejścia z cache i **2,10 USD** za 1 mln tokenów wyjścia. Strona dokumentacji, odczytana 4 listopada, pokazuje **0,7 USD** wejścia i **2,1 USD** wyjścia; pola cache w tym odczycie nie było. Kanały z wpisu: Mistral Studio, API, OpenRouter, Hugging Face (vLLM i SGLang), Vibe Code, endpointy NVIDIA i kontener NIM, Microsoft Foundry oraz dostrajanie przez Mistral Forge.

Wyniki z wpisu Mistrala. To liczby vendora, o ile nie zaznaczono, że pochodzą z indeksu Artificial Analysis przytoczonego przez Mistrala.

| Zadanie | Co podaje Mistral dla wydania wag |
| --- | --- |
| FrontierCode 2.0 (prywatny benchmark Cognition) | 19,7%; wpis nazywa to prowadzeniem |
| Artificial Analysis Coding Agent Index | 48%; wpis: remis z GLM-5.3 przy średnio 47% mniejszej liczbie tokenów na zadanie |
| Terminal-Bench 4.0 | 41%, o 13 punktów procentowych powyżej publicznego podglądu; prowadzenie wśród modeli otwartowagowych i 30% mniej tokenów wyjściowych |
| Artificial Analysis Intelligence Index v5, karta wag | 26; karta nazywa to najwyższym wynikiem wśród zachodnich modeli otwartowagowych i zaznacza, że wiodące modele otwartowagowe z Chin są na tym zbiorczym indeksie wyżej |
| Artificial Analysis Cyber Index | 51% |
| Odmowa szkodliwych próśb cybernetycznych | średnio 96,6% na promptach cybernetycznych z JailbreakBench, StrongREJECT i AgentHarm; wpis nazywa to najwyższą odmową mierzoną przez Mistrala wśród modeli otwartych |
| Finch (FinWorkBench) | 73,3%; wśród modeli otwartych wpis stawia wynik za Kimi K3 |
| BrowseComp | 84,5%; checkpoint po samym SFT miał 75% |
| B3 Agent Security Benchmark, odporność na atak | 97,1% wobec 93,3% w podglądzie |
| Surge Code, ślepe porównania ludzkie kodu | preferencja nad GLM-5.3, Kimi K3 i DeepSeek V4.1 Flash; w zestawie z wpisu za Claude Opus 5.5 |

Trzy tryby rozumowania we wpisie: `low` zamiast dawnego trybu `none`, do zadań prostych; `medium` do zadań codziennych; `high` jako domyślny, do zadań wymagających precyzji.

Wpis mówi, że w ruchu produkcyjnym model odmawiał ataków typu black-box na żywe cele, a jednocześnie Mistral widzi możliwość podniesienia zdolności do realnych ataków i zapowiada dalsze zmiany zabezpieczeń. Partnerom projektowym, w tym Orange Cyberdefense, firma daje podgląd wariantu wyspecjalizowanego do zaawansowanych prac cyberbezpieczeństwa. Dostęp jest po weryfikacji i na podstawie umowy, a testy mają być ograniczone do systemów własnych albo wyraźnie upoważnionych. Ten przegląd nie opisuje przebiegu tych testów.

Blog Hugging Face z 29 października podaje dla części tych samych nazw inne liczby, w tym 28,3% na Terminal-Bench 4.0, 49,8% na Coding Agent Index i 82% na teście odtwarzania i łatania podatności w ramach Cyber Index oraz 93,3% na B3. To nie są liczby z wpisu Mistrala ani z karty wag. Przegląd ich nie podstawia pod tabelę powyżej.

**Źródła:**

- [Mistral — Mistral Large 4 (Le Chonk) is now open weight; `datePublished` 29.10.2026](https://mistral.ai/news/mistral-large-4-oss/)
- [Karta wag `mistralai/Mistral-Large-4-1T-A52B`](https://huggingface.co/mistralai/Mistral-Large-4-1T-A52B)
- [Dokumentacja API `mistral-large-4`, nagłówek strony nadal 6.10.2026](https://docs.mistral.ai/models/mistral-large-4-0)
- [Hugging Face — Welcome Le Chonk, 29.10.2026; inne liczby części testów](https://huggingface.co/blog/mistral-large4)
- [TechCrunch, 29.10.2026, 10:00 PDT](https://techcrunch.com/2026/10/29/mistral-releases-weights-for-its-trillion-parameter-ai-model-targeting-cybersecurity/)

### 1.2. Google: Gemini 4 Carbon (ogłoszenie 28 października 2026) i Computer Use w API (30 października 2026)

**28 października 2026** Google ogłosiło **Gemini 4 Carbon**. Wpis podpisał Koray Kavukcuoglu. Tego samego dnia, w omówieniu wyników za III kwartał 2026, Sundar Pichai mówi, że Carbon ogłoszono „dziś”. Przegląd z rana 28 października tego ogłoszenia nie zawiera. Carbon nie jest w changelogu Gemini API odczytanym 4 listopada: ostatnie ogólne udostępnienie modelu w tym changelogu to Gemini 4 Argon z **13 października 2026**. Wagi Carbon nie zostały opublikowane.

Google nazywa Carbon swoim najsilniejszym modelem, z naciskiem na cyberbezpieczeństwo i zadania o długim horyzoncie. Buduje on na Gemini 4 Argon, wydanym dwa tygodnie wcześniej. Rollout jest celowo wąski. Firma pisze, że bierze udział w dobrowolnym procesie rządu USA dotyczącym testów przed wydaniem. Od tygodnia ogłoszenia Carbon ma trafić do podzbioru obrońców cybernetycznych, a potem stopniowo do kolejnych zaufanych partnerów przez program Fairwind. Dostęp dla deweloperów, firm i konsumentów jest opisany jako „coming soon”, bez daty.

Cena wprowadzająca, ta sama co przy Argonie: **2 USD** za 1 mln tokenów wejścia i **10 USD** za 1 mln tokenów wyjścia. Tokeny wejściowe z cache mają kosztować 95% mniej niż zwykłe wejście. Po okresie wprowadzającym obowiązują **4 USD** i **20 USD**. Wpis Carbon nie podaje dnia, w którym okres wprowadzający się kończy.

Liczby z wpisu Google. Ewaluacje cybernetyczne Google oznacza jako wykonane bez guardrailów.

| Zadanie | Co podaje Google |
| --- | --- |
| Artificial Analysis Intelligence Index v5.0 | 59, miejsce 1 |
| SEC-bench Pro, znajdowanie podatności | 88,2% |
| ExploitGym | 54,8% |
| CWE-bench (Collinear), łatanie | 71,0% |
| WebDev Arena | 1768, miejsce 4, +89 punktów Elo |
| Oszustwo na Terminal-Bench 4.0 | 0,0% udanych oszustw; próby oszustwa 0,4% |
| Gray Swan Indirect Prompt Injection | 0,0% skuteczności ataku; dla Argona wpis podaje 0,7% |

Osobno, jako pomiary wewnętrzne: ponad dwukrotny wzrost skuteczności generowania bezpiecznego kodu względem Argona; spadek alertów wysokiej wagi o rozjechaniu z zamierzeniem o prawie 80% w wewnętrznych środowiskach kodowania; około dwukrotny spadek nieuzasadnionych twierdzeń; spadek nadmiernego wychodzenia poza zakres o 26% i niedostatecznej obsługi o 29%. Zespół Chrome, według wpisu, widzi ponad dziesięciokrotnie lepsze łatki wysokiej jakości niż u „innego dużego modelu frontier” — nazwy tego modelu Google nie podaje. Wiz pisze, w cytacie Google, że Carbon prowadzi na testach penetracyjnych aplikacji webowych. Szczegółów tych testów wpis nie daje i ten przegląd ich nie uzupełnia.

W wynikach kwartalnych Pichai podaje, że własne API modeli przetwarzają prawie **32 mld** tokenów na minutę: o 40% więcej niż w poprzednim kwartale i ponad czterokrotnie więcej niż rok wcześniej. To tło ogłoszenia, nie pomiar Carbona.

**30 października 2026** changelog Gemini API zapisuje osobną zmianę produktową: narzędzie **Computer Use** przechodzi do ogólnej dostępności w Interactions API i GenerateContent API. To nie jest premiera Carbona. Dokumentacja narzędzia wymienia jako modele obsługujące tę funkcję m.in. Gemini 4 Argon (`gemini-4-argon`), Gemini 3.8 Flash i Gemini 3.5 Flash-Lite. Carbona na tej liście, w odczycie z 4 listopada, nie ma. Działanie zostaje po stronie klienta: model zwraca akcję interfejsu, a aplikacja ją wykonuje. Dokumentacja ostrzega, że narzędzie może się mylić i nieść ryzyka bezpieczeństwa, i odradza użycie przy decyzjach krytycznych, danych wrażliwych oraz czynnościach, których błędu nie da się odwrócić.

**Źródła:**

- [Google — Introducing Gemini 4 Carbon, 28.10.2026](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/)
- [Alphabet, wyniki za III kwartał 2026, uwagi Sundara Pichaia, 28.10.2026](https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q3-2026/)
- [Gemini API changelog, wpis Computer Use z 30.10.2026 i brak wpisu o Carbonie](https://ai.google.dev/gemini-api/docs/changelog)
- [Dokumentacja Computer Use](https://ai.google.dev/gemini-api/docs/computer-use)

### 1.3. OpenAI: modele przy projektowaniu sprzętu (3 listopada 2026) i wspólny sygnał treningowy (30 października 2026)

**3 listopada 2026** OpenAI opublikowało opis tego, jak istniejące modele pomagają inżynierom projektować, symulować i budować przedmioty fizyczne. To nie jest premiera nowego publicznego modelu. W tekście występują GPT-6 Astra i Codex oraz nienazwany „nowszy model wewnętrzny”.

Wewnętrzny test: dwie osoby, jako projekt poboczny, w niecały tydzień zaprojektowały z Astrą urządzenie do rozmowy z Codexem — obudowę, płytkę, interfejs i oprogramowanie — a producent kontraktowy zrobił krótką serię prototypów w niecały miesiąc. OpenAI samo pisze, że Astra nie uwzględniała w sposób konsekwentny limitów produkcji, tolerancji i szczegółów montażu. Od lutego zużycie tokenów w zespołach sprzętowych OpenAI wzrosło **23-krotnie**. Zespoły używają Codex i ChatGPT do modeli CAD, rysunków wykonawczych, symulacji i przeglądów, w robotyce i w infrastrukturze obliczeniowej.

BenchCAD 2.0, według wpisu, sprawdza odtwarzanie części i złożeń 3D oraz rozpoznawanie połączeń na płytkach. Nowszy model wewnętrzny ma średni wynik **0,875**, a GPT-6 Astra przy najwyższym ustawieniu rozumowania **0,594**. Nazwy tego nowszego modelu, daty wydania i dostępu publicznego wpis nie podaje.

Współpraca z Chip Ganassi Racing jest rozszerzana: skany 3D istniejących części mają stawać się edytowalnymi modelami CAD i rysunkami 2D, gdy brakuje plików źródłowych. Inżynierowie zespołu sprawdzają wynik pod kątem dokładności i wykonalności. Nową współpracą badawczą jest Mazda: aerodynamika i bezpieczeństwo zderzeniowe, symulacje przepływu i konstrukcji, z uwzględnieniem stylu i kosztu. OpenAI pisze, że wyniki pojawią się w kolejnych miesiącach. Zgoda Mazdy na użycie materiału jest w przypisie wpisu.

**30 października 2026** OpenAI ogłosiło, że będzie honorować wspólny sygnał w `robots.txt` dotyczący użycia treści strony do podstawowego treningu generatywnej AI. Sygnał ma pozwolić operatorowi strony przekazać tę samą preferencję wielu uczestniczącym dostawcom naraz, zamiast utrzymywać osobną regułę dla każdego bota. Wdrożenie jest zapowiedziane „w nadchodzących miesiącach”; szczegóły implementacji mają przyjść w osobnej aktualizacji. Istniejące kontrole botów OpenAI zostają. Firma odwołuje się do prac grupy AI Preferences w IETF i zachęca innych dostawców, by sygnał honorowali. To zobowiązanie dobrowolne, jeszcze nie działająca blokada pobierania stron.

Nagłówki `HEAD` obu stron OpenAI zwracały **403**. Treść obu wpisów została odczytana inną ścieżką 4 listopada i daty dzienne są na samych stronach.

**Źródła:**

- [OpenAI — Accelerating engineering for the physical world, 3.11.2026](https://openai.com/index/accelerating-engineering-for-the-physical-world)
- [OpenAI — wspólny sygnał preferencji treningowych w robots.txt, 30.10.2026](https://openai.com/index/helping-websites-express-ai-training-preferences/)

### 1.4. Moonshot: wagi Kimi K3.1 Pro rano 4 listopada 2026 nadal nieopublikowane

Kimi K3.1 Pro i Highspeed zostały opisane w przeglądzie z 28 października. Tamten tekst zostawiał wagi jako zapowiedź „do 4 listopada 2026”. Ten podrozdział sprawdza tylko stan zapowiedzi.

Angielski wpis na `kimi.ai`, odczytany rano **4 listopada 2026**, nadal zawiera zdanie, że pełne wagi zostaną wydane do **4 listopada 2026**. Strona nie ogłasza, że wydanie już nastąpiło, i nie nazywa platformy.

Tego samego ranka, około **07:04 UTC**, publiczne API Hugging Face dla organizacji `moonshotai` sortowane po dacie modyfikacji zwracało jako najnowszy model `moonshotai/Kimi-K3`, z `lastModified` **2 września 2026**. Repozytorium K3.1 Pro w tej organizacji nie wystąpiło. Wyszukanie Hubu dla nazwy „Kimi-K3.1” zwróciło jeden cudzy rekord, spoza `moonshotai`. Nie jest to oficjalne wydanie wag i ten przegląd go nie opisuje.

Doba 4 listopada o 07:04 UTC jeszcze trwała. Zapowiedź „do 4 listopada” nie jest więc w tym przeglądzie odwołana za cały dzień kalendarzowy. Jest niespełniona w chwili sprawdzenia. Liczb, cen i wyników z premiery K3.1 ten dokument nie powtarza.

**Źródła:**

- [Kimi — Kimi K3.1 Pro, zdanie o wagach „by Nov 4, 2026”, odczyt 4.11.2026](https://www.kimi.ai/blog/kimi-k3-1-pro)
- [Lista modeli `moonshotai` na Hugging Face, stan z ranka 4.11.2026](https://huggingface.co/moonshotai/models)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie nie ma nowej ustawy procesowej, która już weszła w życie. Są za to trzy materiały z trzech krajów: raport brytyjskiej Civil Justice Council z 29 października, który proponuje zmiany reguł cywilnych, ale sam ich nie stanowi; komunikat Sądu Najwyższego Korei z 2 listopada o ankiecie sędziów i zapowiedzi opinii legislacyjnej; oraz wywiady nigeryjskiej agencji z 31 października o odpowiedzialności za fałszywe cytaty, bez nowego orzeczenia i bez nowej reguły.

Przepisy nadzorcze polskiej ustawy o systemach sztucznej inteligencji weszły w życie **28 października 2026**. Opis ustawy, art. 18 i terminu pierwszego posiedzenia Komisji jest w przeglądzie z 28 października. W źródłach czytanych do niniejszego dokumentu nie ma ogłoszenia, że posiedzenie już się odbyło. Ustawowy termin zwołania, liczony w tamtym przeglądzie, pozostaje **11 listopada 2026**.

### 2.1. Anglia i Walia: raport końcowy Civil Justice Council (29 października 2026)

**29 października 2026** grupa robocza Civil Justice Council opublikowała raport końcowy *Use of AI for Preparing Court Documents*. Na stronie CJC data jest powtórzona jako „Final report – 29 October 2026”. Przewodniczący grupy, sir Colin Birss, podpisał przedmowę tą datą. Współprzewodniczącą jest Mrs Justice Joanna Smith. Sir Geoffrey Vos, Master of the Rolls, wita raport jako propozycję proporcjonalnego, ryzykowego podejścia, które utrzymuje odpowiedzialność zawodową i dodaje zabezpieczenia tam, gdzie są potrzebne.

Raport nie jest Practice Direction i nie zmienia Civil Procedure Rules. Rekomenduje, by Civil Procedure Rule Committee taką Practice Direction przygotował. To piętnasta i wcześniejsze rekomendacje są wnioskiem do komitetu reguł i do regulatorów, nie obowiązującą regułą sądu.

Zakres jest węższy niż cały wymiar sprawiedliwości. Pierwszy raport okresowy z **17 lutego 2026** i ten raport końcowy dotyczą dokumentów przygotowywanych po to, by trafiły do sądu w sprawach cywilnych. Użycie AI przez sędziów oraz — w założeniu — przez strony bez pełnomocnika leżało poza terms of reference. Korekta pisowni i gramatyki, która nie tworzy ani nie wpływa na treść merytoryczną, też. Świadome składanie fałszywego dowodu raport zostawia przy istniejących instrumentach: nadużycie procesu, contempt of court, sankcje za fałszywe statement of truth i ewentualna odpowiedzialność za krzywoprzysięstwo.

Definicje użyte w raporcie: „generate substantive content” to wytworzenie albo zmiana treści merytorycznej przez narzędzie AI, świadomie lub nie. „Influence substantive content” to użycie narzędzia, które samo tej treści nie produkuje, ale wpływa na jej wybór, analizę, rozwinięcie albo ocenę. Treść merytoryczna obejmuje fakty, dowód, opinię, rozumowanie i argument, a w oświadczeniu świadka także jego własne słowa.

Główne rekomendacje, numeracja z raportu:

| Nr | Co rekomenduje grupa |
| --- | --- |
| 1 | Wytyczne dla palestry zostają przy regulatorach usług prawnych (m.in. SRA, BSB, LSB). Regulatorzy mają uzgadniać je ze sobą, rozważyć wspólny tekst i uwzględnić AI w szkoleniu, w tym w ewentualnym przyszłym obowiązkowym szkoleniu etycznym. |
| 2 | CJC, z Futures Group i razem z CPRC, ma pilnie zająć się użyciem AI przez strony bez pełnomocnika. Ma przy tym uwzględniać, w odpowiednim zakresie, międzyjurysdykcyjny komitet AI sądownictwa. |
| 3 | CPRC ma skodyfikować dotychczasowe orzecznictwo o użyciu AI i sankcjach za nadużycie w Practice Direction, językiem prostym, i wciągnąć do niej rekomendacje 11–13. Tekst ma dać się poprawić po pracy z rekomendacji 2. |
| 4 | Brak nowego obowiązku oświadczenia o AI przy pismach procesowych, skeleton arguments i innej argumentacji pełnomocnika. Odpowiedzialność za dokładność zostaje przy dotychczasowych obowiązkach. Practice Direction ma, o ile trzeba, doprecyzować, który prawnik bierze za dokument odpowiedzialność. |
| 5 | Przy disclosure na razie bez reformy, z zastrzeżeniem pracy Disclosure Review Working Group nad PD 57AD. |
| 6 | Świadek faktu ma złożyć oświadczenie, że AI użyte przy przygotowaniu jego witness statement nie wytworzyło ani nie wpłynęło na treść merytoryczną. |
| 7 | Gdy oświadczenie przygotowuje i podpisuje pełnomocnik, a nie składa go jako świadek faktu, to on odpowiada za dokładność. Rekomendacja 6 wraca, gdy pełnomocnik jest świadkiem faktu. |
| 8 | Brak nowych reguł materialnych dla tłumaczeń AI. Każdy przekład ma poświadczyć zawodowy tłumacz-człowiek, a przy przekładzie ma iść oryginał. CPR część 32 i jej Practice Direction mają wprost objąć tym poświadczeniem narzędzia AI. |
| 9 | Gdy AI wytwarza albo wpływa na treść merytoryczną opinii biegłego, biegły składa osobne oświadczenie. Ma ono dać dość informacji — w razie potrzeby z nazwą narzędzia — by druga strona i sąd mogły sprawdzić metodykę, zasadność użycia i treść. |
| 10 | Grupa pracująca nad aktualizacją CJC Guidance for the Instruction of Experts in Civil Claims (2014) ma dodać dobre praktyki użycia AI przez biegłych. |
| 11–13 | CPR nie ma dzielić narzędzi na generatywne, niegeneratywne, administracyjne, analityczne i podobne. Zakres ma być funkcjonalny: czynności zdolne wytworzyć treść merytoryczną albo na nią wpłynąć. Obowiązki proceduralne mają wynikać z ryzyka dla integralności postępowania i wymiaru sprawiedliwości. |
| 14 | Brak ogólnego obowiązku, by pełnomocnik podawał sądowi, którego narzędzia użył przy materiałach składanych do sądu. |
| 15 | Brak nowej reguły, która uzależniałaby użycie AI od zezwolenia sądu. |

Oświadczenie świadka faktu nie zakazuje konkretnego narzędzia. Patrzy na skutek: treść ma pozostać własnymi słowami świadka. Przy biegłym raport uzasadnia osobne oświadczenie potrzebą równości broni i możliwości sprawdzenia opinii. Przy pełnomocnikach grupa zostawia odpowiedzialność zawodową i nie wprowadza ani ogólnego ujawniania narzędzia, ani zezwolenia sądu.

**Źródła:**

- [CJC — Use of AI for Preparing Court Documents, Final Report (PDF), przedmowa 29.10.2026](https://www.judiciary.uk/wp-content/uploads/2026/10/Use-of-AI-for-the-Preparation-of-Court-Documents-Final-Report.pdf)
- [CJC — strona prac grupy, wpis „Final report – 29 October 2026” i cytat sir Geoffreya Vosa](https://www.judiciary.uk/related-offices-and-bodies/advisory-bodies/cjc/current-work/use-of-ai-in-preparing-court-documents/)
- [CJC — najnowsze wiadomości, wpis z 29.10.2026](https://www.judiciary.uk/related-offices-and-bodies/advisory-bodies/cjc/latest-news/)

### 2.2. Korea Południowa: ankieta Sądu Najwyższego o fałszywych cytatach (komunikat 2 listopada 2026)

**2 listopada 2026** Sąd Najwyższy Korei opublikował komunikat „AI 허위 판례 등 인용 관련 설문조사 결과” (wyniki ankiety o cytowaniu fałszywych precedensów i podobnych materiałów wytworzonych z AI). Nadawcą działań opisanych w komunikacie jest sądowa administracja (법원행정처). Ankietę przeprowadzono od **6 do 16 października 2026** wśród sędziów sądów wszystkich szczebli. Odpowiedziało **360** osób. Publikacja wyników przypada na ten tydzień; samo zbieranie odpowiedzi zaczęło się wcześniej.

Komunikat podaje, że około **80%** sędziów prowadzących sprawy cywilne, rodzinne i administracyjne zetknęło się ze sprawą, w której zacytowano fałszywy albo nieistniejący precedens. Rozbicie typów, przy odpowiedziach wielokrotnych:

| Typ cytatu | Liczba odpowiedzi | Udział podany w komunikacie |
| --- | --- | --- |
| Precedens, który nie istnieje | 196 | 80,7% |
| Precedens fałszywy | 159 | 65,4% |
| Przepis fałszywy albo nieistniejący | 41 | 16,9% |
| Artykuł, publikacja albo inny materiał fałszywy albo nieistniejący | 10 | 4,1% |

Komunikat nie rozpisuje osobno, ile osób z 360 prowadzi sprawy cywilne, rodzinne i administracyjne. Procentów z tabeli nie należy więc mnożyć przez 360. Przy pytaniu, kto taki cytat złożył, też wielokrotnym, **164** odpowiedzi (69,5%) wskazało samą stronę, a **136** (57,6%) pełnomocnika albo obrońcę będącego adwokatem. Komunikat podkreśla, że problem występuje i w pismach stron działających samodzielnie, i w pismach adwokatów.

Przykłady zapisane w komunikacie: pismo, które kopiuje układ orzeczenia Sądu Najwyższego i jest fałszywym orzeczeniem wygenerowanym przez AI; numer sprawy Sądu Najwyższego zestawiony z tezą, której nie da się odnaleźć; zmiana rzeczywistej tezy albo cytat sprzeczny z sensem orzeczenia; fragment rozmowy z AI albo strategii procesowej wklejony do pisma bez usunięcia.

**91,7%** odpowiedzi uznaje, że potrzebna jest odpowiedź instytucjonalna. **64,8%** określa ją jako bardzo potrzebną. Wśród konkretnych środków komunikat wymienia, jako opinie zgłaszane przez wielu: podstawę do grzywny administracyjnej (과태료), obowiązek weryfikacji cytowanych precedensów oraz wnioski dyscyplinarne wobec adwokatów przy powtarzającym się fałszywym cytowaniu. Nie podaje procentowego rozbicia poparcia dla każdego z tych trzech środków.

Skutek opisany przez sąd: druga strona ponosi dodatkowy czas i koszt sprawdzenia oraz odpowiedzi, a osoba bez adwokata ma z tym szczególną trudność. Sprawdzenie, czy materiał istnieje i czy cytat jest wierny, wydłuża rozpoznanie sprawy. Komunikat wiąże to z opóźnieniem prawa do sądu.

Zapowiedzi, nie uchwalone przepisy: administracja sądowa ma przygotować środki instytucjonalne i praktyczne. Uważa, że podstawę grzywny należy wprowadzić nowelizacją kodeksu postępowania cywilnego i kodeksu postępowania karnego. Zamierza skonsultować to z Ministerstwem Sprawiedliwości i innymi organami oraz przedstawić opinię Zgromadzeniu Narodowemu. Rozważa też umieszczenie na stronie postępowania elektronicznego pouczenia „o czym pamiętać, korzystając z AI”. Żaden z tych kroków nie jest w komunikacie opisany jako już złożony projekt ustawy.

Angielski tekst Yonhap z 2 listopada, 12:03, podaje te same rzędy wielkości: 360 sędziów, okres 6–16 października, około 80%, 196 (80,7%), 159 (65,4%), 41 (16,9%), 10 (4,1%), 164 (69,5%) i 136 (57,6%) oraz blisko 92% za środkami instytucjonalnymi. Tam, gdzie Yonhap skraca plan legislacyjny, rozstrzyga komunikat sądu.

**Źródła:**

- [Sąd Najwyższy Korei — komunikat z 2.11.2026](https://www.scourt.go.kr/portal/news/NewsViewAction.work?gubun=6&seqnum=3070)
- [Yonhap, 2.11.2026, 12:03](https://en.yna.co.kr/view/AEN20261102005900315)

### 2.3. Nigeria: wywiady o fałszywych cytatach i zapowiedź seminarium palestry (31 października 2026)

**31 października 2026** News Agency of Nigeria opublikowała wywiady przeprowadzone w Ibadanie. To nie jest orzeczenie, wytyczna sądu ani zmiana Rules of Professional Conduct. Zdania poniżej są relacją agencji z wypowiedzi prawników, nie tekstem sądu.

Oluseun Abimbola, były prokurator generalny stanu Oyo i Senior Advocate of Nigeria, mówi agencji, że powołanie podejrzanych źródeł narusza Rules of Professional Conduct. Za moment, w którym błędny cytat wygenerowany przez AI staje się podstawą odpowiedzialności, uznaje jego przedstawienie sądowi, ustnie albo w piśmie. Sędzia może, według tej wypowiedzi, obciążyć pełnomocnika kosztami albo skierować sprawę do Legal Practitioners Disciplinary Committee. Koszt osobisty nazywa sankcją minimalną za brak weryfikacji. Powtarzanie takiego cytowania może jego zdaniem być odczytane jako świadome wprowadzenie w błąd, a wtedy samo kosztowe ukaranie może nie wystarczyć. Dodaje, że w jego praktyce takie przypadki w Nigerii były rzadkie i że upowszechnienie AI może tę rzadkość zmienić.

Adekola Kareem, przewodniczący oddziału Nigerian Bar Association w Ibadanie, mówi, że używanie AI do badań prawnych nie jest wśród członków oddziału powszechne i że palestra nadal opiera się na zbiorach orzeczeń oraz podręcznikach. Oddział ma, według tej wypowiedzi, ustalone seminarium o etycznym użyciu AI: zaangażowano badacza-konsultanta, który ma wystąpić na najbliższym spotkaniu. Kareem uważa, że obecne reguły wystarczają. Wprowadzenie sądu w błąd fabrykowanymi źródłami jest już odpowiedzialnością zawodową przed LPDC. Daty seminarium agencja nie podaje.

Oluwatobi Fatoki mówi, że sądy wyższych instancji sprawdzają cytaty w elektronicznych zbiorach, w tym LawPavilion, Legalpedia i Nigerian Weekly Law Reports, oraz że sędziowie mają asystentów badawczych. Zaznacza, że wiele sądów niższych i sądów zwyczajowych takiego dostępu nie ma. Funmilola Onalaja, z kancelarii Mondial Solicitors, mówi, że sama nie używa AI do pism procesowych, i wskazuje koszt baz prawnych oraz pokusę przyjęcia wyniku AI bez sprawdzenia. Wzywa do szkolenia praktycznego, które ma ograniczać halucynacje.

Agencja przywołuje też wypowiedź prezes Sądu Najwyższego Nigerii, sędzi Kudirat Kekere-Ekun, że technologia nie zastępuje konstytucyjnego obowiązku sędziego. Daty tej wypowiedzi tekst z 31 października nie podaje. Nie jest ona wydarzeniem datowanym w tym tygodniu.

**Źródła:**

- [News Agency of Nigeria, 31.10.2026](https://nannews.ng/fake-ai-cases-breach-ethics-attract-sanctions-lawyers/)

---

## Nota o zakresie

Przegląd pomija pozycje, których nie dało się oprzeć na stronie vendora, sądu, regulatora albo agencji, którą dało się otworzyć. Nie opisuje jako nowych wydarzeń tego tygodnia premier i wytycznych już ujętych w przeglądzie z 28 października. Nie opisuje też partnerstwa Judicial Service of Ghana z Kwame AI: ogłoszenie Eskwai Clerk na stronie firmy nosi datę **22 czerwca 2026**, a teksty prasowe z 30 października nie wnoszą datowanego, nowego aktu sądu.
