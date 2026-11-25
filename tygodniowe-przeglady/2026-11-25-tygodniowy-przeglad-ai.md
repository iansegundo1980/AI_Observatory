# Tygodniowy przegląd AI — 25 listopada 2026

**Okres objęty podsumowaniem:** 18–25 listopada 2026
**Data publikacji podsumowania:** 25 listopada 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **11–18 listopada 2026** i powstał rano 18 listopada. Niniejszy dokument go nie powtarza. Nie opisuje od nowa GPT-6.2 Astra i Sol, Gemini 4 Hydrogen, Qwen4-Max jako premiery z 16 listopada ani konfiguracji Astra for Law z 17 listopada. Dwa fakty z samego 18 listopada, oraz jedno postanowienie z 17 listopada upublicznione 19 listopada, nie weszły do tamtego porannego tekstu. Są tu oznaczone datą.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z wpisu premierowego, karty modelu albo cennika odczytanego 25 listopada 2026. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jeden ranking: konfiguracje, daty pomiaru, wysiłek rozumowania i harnessy się nie pokrywają. Tam, gdzie wpis jednego laboratorium podaje wynik cudzego modelu, jest to pomiar autora wpisu.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Tydzień otwiera model, którego poranny przegląd z 18 listopada nie zdążył odnotować: **Gemini 4 Neon**, środkowy model rodziny Gemini 4, między Carbonem a Hydrogenem. Tego samego dnia Anthropic wycenia ofertę publiczną, a 19 listopada akcje Class A wchodzą na Nasdaq. Dalej idą otwarte wagi małego modelu pętlowego Thinking Machines, nowy checkpoint Sarvam dla agentów konwersacyjnych, flagowiec Z.ai na architekturze Loop Transformer oraz głosowy model Alibaby, który mówi dalej, gdy w tle liczy inne zadanie.

24 listopada dochodzą pełnoskalowy model wideo MAGI-2, kodujący SWE-2.1 Cognition, otwarty model obrazu SenseNova U1.6 i światowy model XPENG dla maszyn. Osobno, bez powtarzania premiery z 16 listopada, Qwen4-Max dostaje region USA, a identyfikator podglądu wygasa rankiem 25 listopada czasu chińskiego.

### 1.1. Google: Gemini 4 Neon (18 listopada 2026)

**18 listopada 2026** Koray Kavukcuoglu ogłasza **Gemini 4 Neon**. Strona wpisu ma adnotację „Last updated November 23, 2026”. Datą premiery w nagłówku pozostaje 18 listopada. Ten przegląd nie ustala, które zdania doszły przy aktualizacji z 23 listopada.

Neon ma stać między Gemini 4 Carbon, modelem do najdłuższych zadań, a Gemini 4 Hydrogen, modelem do szybkiej codziennej pracy. Karta modelu, opublikowana 18 listopada 2026, mówi wprost, że Neon jest adaptacją Carbona. Wejście: tekst, obrazy, audio i wideo, ze wspólnym oknem wejścia i wyjścia do **1 mln** tokenów. Wyjście: do **64 tys.** tokenów w zwykłej odpowiedzi synchronicznej i do **1 mln** przez długie dekodowanie w tle. Odcięcie wiedzy: **marzec 2026**, z zastrzeżeniem karty, że w części dziedzin wiedza może być starsza.

Cena z wpisu, za 1 mln tokenów: **3 USD** wejścia, **0,15 USD** wejścia z cache (wpis nazywa to zniżką 95%) i **15 USD** wyjścia. Okno kontekstu: **1 mln** tokenów.

Wpis mówi o czterech poziomach myślenia. Domyślny, nazwany w tekście, to **high**. Najwyższy, nazwany w tekście, to **xhigh**. Tego przeglądu nie należy czytać jako listy pozostałych dwóch nazw: wpis ich w odczytanym brzmieniu nie wymienia.

Liczby ze wpisu Google, bez składania ich z tabelami Anthropic albo OpenAI:

- Artificial Analysis Intelligence Index: **61** przy xhigh i miejsce **3** ogółem, tuż za większymi, wolniejszymi modelami.
- Vals Index: miejsce **2**, **70,9%**, oraz miejsce na froncie Pareto.
- Vals Legal Research Bench i Vals Tax Agent Bench: wpis podaje miejsce **1** na obu, bez procentu przy samym Legal Research Bench. Tej liczby nie należy łączyć z wynikiem 55,8% Hydrogenu z przeglądu 18 listopada ani z 53,8% pełnego zaliczenia Astra for Law. To osobne zdanie wpisu z 18 listopada.
- Agent Arena Index: miejsce **2** w sterowalności, czyli w czystym przyjmowaniu korekt w trakcie zadania, oraz debiut na miejscu **2** z wynikiem **1336** na nowym indeksie, na ponad **4200** rzeczywistych sesjach agentów.
- Terminal-Bench Science: **70,5%**. RiemannBench: **84,0%**. HLE-Diamond: **71,3%**.
- Artificial Analysis Coding Agent Index: miejsce **1**, wynik **58,6**. Terminal-Bench 4.1: **65,2%**. FrontierCode 2.0 przy domyślnym high: **46,2%**.
- SWE-sweep: **12,8%** w harnessie mini-SWE i **39,0%** w Google Antigravity. Wpis przypisuje skok harnessowi Antigravity.
- Zapier AutomationBench: **56,3%**, miejsce 1. Andon Labs Vending-Bench 2: **16 843 USD**, miejsce 1. Chartography: **73,5%**. Agents’ Last Exam v1.1: **75,8%**.
- Przy domyślnym high: o **32%** niższy koszt zadania niż Carbon przy wysokim wyniku indeksu Artificial Analysis. Na Vals Index i Agent Arena, nadal przy high, wpis szacuje koszt zadania o około **50–80%** niższy niż u czołowych modeli frontierowych. Przy xhigh: najwyższy wynik inteligencji Neona i nadal ponad **36%** taniej na zadanie niż konkurenci na ich najwyższym ustawieniu.

Karta modelu podaje osobną tabelę „as of November, 2026”. W kolumnach porównawczych są Claude Opus 5.5 i GPT-6.2 Sol. To pomiar Google, nie wspólny ranking laboratoriów. Tabela nie powtarza w odczytanym wierszu, że 61 na AA Index v5.0.1 jest wynikiem xhigh; to doprecyzowanie zostaje przy wpisie. Wybrane komórki karty: AA Index v5.0.1 — Neon **61**, Opus 5.5 **59**, Sol **57**. Vals Index v2.2 — **70,9% / 70,1% / 66,1%**. Terminal-bench 4.1, dokładność po korekcie o oszustwa — **65,2% / 65,8% / 61,5%**. FrontierCode 2.0 — **46,2% / 47,3% / 43,8%**. W tej tabeli Sol jest wyżej od Neona na Chartography (**75,1%** wobec **73,5%**). CursorBench 4.1: Neon **65,4%**, Opus 5.5 **58,1%**, Sol bez wyniku w komórce.

Bezpieczeństwo, ze wpisu, nadal jako twierdzenia Google:

- Zabezpieczenia przed nadużyciem cybernetycznym i biologicznym mają być porównywalne z Carbonem, przy rzadszych odmowach legalnej pracy: **1,98%** odmów na Terminal-Bench 4.0 i **0%** na Terminal-Bench-Science.
- **0,0%** oszustw na Terminal-Bench 4.0, tyle samo co Carbon. Na wewnętrznej ewaluacji oszukiwania w kodzie: skróty na **2,45%** zadań, najniżej w rodzinie Gemini 4. Wskaźnik działań niedopasowanych na zestawie bezpieczeństwa agentów: **0,09%**. Uczciwość agenta: **99,2%** zaliczeń.
- Wobec mocnej bazy Carbona: niedostateczna obsługa niższa o **43–56%**, wychodzenie poza zakres niższe o **13–35%**, zależnie od poziomu wysiłku.
- Gray Swan, pośrednie wstrzyknięcie poleceń: przy zabezpieczeniach w czasie rzeczywistym i najwyższym poziomie myślenia Neon oparł się każdemu atakowi w tym benchmarku, czyli **0,0%** skuteczności ataku. Wpis mówi, że taki wynik osiągnęły wcześniej tylko inne modele Gemini.

Karta nie robi nowej pełnej oceny zdolności krytycznych. Po ocenie Material Capability Change Neon jest sprawniejszy ogólnie od Gemini 4 Argon, ale przyrost jest poniżej progu MCC, więc Google przenosi ustalenia T/CCL z Argona. W skrócie, bez opisu scenariuszy: próg CCL w biologii i w cyberbezpieczeństwie „nie może zostać wykluczony”; próg TCL utraty kontroli w zakresie skrytości i świadomości sytuacji „nie może zostać wykluczony”; progi CCL automatyzacji badań ML i szkodliwej manipulacji nie zostały osiągnięte. Karta mówi, że mitygacje są dalej wdrażane. Ten przegląd nie jest instrukcją testów, pentestów ani obchodzenia zabezpieczeń. Szczegóły metod zostają w raporcie bezpieczeństwa.

Wariant do obrony, nazwany we wpisie, ma trafić do zaufanych obrońców w programie **Fairwind** „w najbliższych dniach” od daty wpisu. 25 listopada ten przegląd nie znalazł osobnego komunikatu, że rollout się zakończył. Liczby obronne ze wpisu, jako twierdzenia Google i bez opisu metody: AutoBaxBench, poziom trudny, **76%**; WebExploitBench v1.2 **51,26%** przy połowie kosztu dużych modeli konkurencji; SEC-bench Pro **90,5%**; CWE-bench v2 **70,7%**, o **3,4 punktu procentowego** wyżej niż Carbon. Na ExploitGym wpis mówi o wyniku na poziomie frontier przy połowie tokenów Carbona i nie podaje w tym zdaniu procentu.

Dostępność z wpisu, jako rollout od 18 listopada:

- Deweloperzy: płatny poziom Gemini API w AI Studio i Android Studio. Abonenci Google AI Pro i Ultra także w Antigravity. Wszyscy abonenci Pro i Ultra także w AI Studio.
- Firmy: Gemini for business, przez API albo listę modeli, oraz Antigravity.
- Konsumenci: abonenci Google AI Pro i Ultra wybierają Neona z listy w aplikacji Gemini.
- Obrona: uprawnieni członkowie Fairwind, według wpisu w kolejnych dniach, przez zespół konta Cloud.

**Źródła:**

- [Google — Introducing Gemini 4 Neon, 18.11.2026, aktualizacja strony 23.11.2026](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/)
- [Google DeepMind — karta modelu Gemini 4 Neon, publikacja 18.11.2026](https://deepmind.google/models/model-cards/gemini-4-neon/)

### 1.2. Anthropic: zamknięcie oferty publicznej (18–20 listopada 2026)

To nie jest nowy model. Jest to największe wydarzenie właścicielskie tygodnia i dlatego wchodzi do części o istotnym znaczeniu, obok premier modeli.

**18 listopada 2026** Anthropic, PBC, informuje, że wyceniło ofertę publiczną akcji Class A na **83,00 USD** za akcję. Oferta w tym komunikacie obejmuje **980 000 000** akcji: **956 351 354** sprzedawane przez spółkę i **23 648 646** przez sprzedających akcjonariuszy. Spółka nie dostaje wpływów ze sprzedaży akcjonariuszy. Underwriterzy dostają 30-dniową opcję na dodatkowe **147 000 000** akcji. Rejestracja została uznana za skuteczną przez SEC tego samego dnia. Komunikat zapowiada początek obrotu na Nasdaq Global Select Market **19 listopada 2026** pod symbolem **ANT** i zamknięcie **20 listopada**, po zwykłych warunkach.

**20 listopada 2026** drugi komunikat potwierdza zamknięcie, już z pełnym wykonaniem opcji. Łącznie **1 127 000 000** akcji Class A po 83,00 USD, w tym **1 103 351 354** sprzedane przez Anthropic i te same **23 648 646** przez sprzedających akcjonariuszy. Brutto oferty, przed prowizjami i kosztami, to około **93,5 mld USD**, z czego około **91,6 mld USD** otrzymało Anthropic.

Tego samego dnia zamyka się równoległa sprzedaż prywatna **313 253 007** akcji Class N, też po 83,00 USD, dla Advanced Micro Devices, Broadcom, Google LLC, Micron Technology, Microsoft, NVIDIA i TSMC Partners. Kwota tej sprzedaży to około **26,0 mld USD**. Akcje Class N nie były zarejestrowane na podstawie Securities Act. Suma brutto oferty publicznej, łącznie z akcjami sprzedających, i sprzedaży prywatnej to około **119,5 mld USD**, nadal przed prowizjami i kosztami.

Grafika Reutersa z **19 listopada 2026**, a więc jeszcze przed komunikatem o wykonaniu opcji, zestawia pełne wykonanie opcji (**93,5 mld USD**) z IPO SpaceX (**86 mld USD** łącznie z opcją) i opisuje debiut Anthropic jako większy. Liczba 93,5 mld USD, którą tamta grafika traktowała jako wariant z pełną opcją, jest tą, którą komunikat z 20 listopada podaje już jako brutto zamkniętej oferty. Ten przegląd nie podaje kursu z pierwszego dnia ani kapitalizacji, bo żadnego z tych dwóch odczytów tu nie weryfikowano.

**Źródła:**

- [Anthropic — wycena IPO, 18.11.2026](https://www.anthropic.com/news/anthropic-prices-initial-public-offering)
- [Anthropic — zamknięcie IPO i sprzedaży prywatnej, 20.11.2026](https://www.anthropic.com/news/ipo-close)
- [Reuters — grafika porównawcza debiutów, 19.11.2026](https://www.reuters.com/graphics/ANTHROPIC-IPO/CHARTS/jnpwdeanxvw/)

### 1.3. Google: Genie 4 wchodzi do Project Genie i Gemini API (18–19 listopada 2026)

Ogłoszenie badawcze Genie 4 z **27 października 2026** jest w przeglądzie z 28 października. Tu jest tylko szerszy dostęp.

**18 listopada 2026** Google pisze, że uprawnieni abonenci Google AI Ultra dostają w Project Genie pierwsze konsumenckie dojście do Genie 4, agenta Project Genie i galerii społeczności. Abonenci Google AI Pro mogą zapisać się na listę oczekujących. Wpis opisuje edycję świata w trakcie sesji, tekstem, oraz po raz pierwszy natywne audio w czasie rzeczywistym: tło, efekty i dialog postaci. Genie 3 zostaje w wyborze modelu do dłuższych biegów i przestrzeni z panoramy. Wyjścia wideo i audio mają znak wodny SynthID. Ograniczenia, które wpis sam wymienia: opóźnienie kamery, złożone interakcje fizyczne, precyzja audio na żywo i trwałość sceny.

**19 listopada 2026** osobny wpis dla deweloperów: Genie 4 jest w Gemini API, przez Interactions API, i w Google AI Studio. Z tekstu, obrazu referencyjnego albo obu można generować ciągłe światy **720p** przy **24 klatkach na sekundę**, z synchronizowanym audio. Sterowanie: klawiatura w czasie rzeczywistym i bieżące prompty tekstowe.

Karta modelu, też z datą publikacji 18 listopada 2026, podaje te same wyjścia: wideo 720p do 24 kl./s z synchronizowanym audio. Zależności: Genie 4 jest zbudowane na Gemini Omni Flash i używa Gemini do rozumowania oraz sterowania na żywo. Wejścia: tekst, obrazy i działania użytkownika. Karta w linii dystrybucji nadal mówi, że udostępnienie przez Project Genie jest planowane, podczas gdy wpis z tego samego dnia ogłasza rollout dla Ultra. Ten przegląd trzyma się wpisów z 18 i 19 listopada jako opisu dostępu, a karty jako opisu ograniczeń: spójność krótkich sesji, dryf szczegółów i przedmiotów przy dłuższym biegu, wielu edycjach albo przejściu przez scenę, oraz otwarte problemy tekstu, dokładności przestrzennej i długiej ciągłości.

**Źródła:**

- [Google — Genie 4 w Project Genie, 18.11.2026](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/)
- [Google — Genie 4 w Gemini API, 19.11.2026](https://blog.google/innovation-and-ai/technology/developers-tools/genie-4-in-gemini-api/)
- [Google DeepMind — karta Genie 4, publikacja 18.11.2026](https://deepmind.google/models/model-cards/genie-4/)

### 1.4. Thinking Machines Lab: Inkling 2 Mini (20 listopada 2026)

**20 listopada 2026** Thinking Machines Lab wydaje **Inkling 2 Mini**, otwarte wagi małego modelu multimodalnego, który ma mieścić się na laptopie. Karta modelu: licencja **Apache 2.0**, data wydania 20 listopada 2026. Wejście: tekst i obraz. Wyjście: tekst. Kontekst: do **1 mln** tokenów.

Architektura z karty: dekoder o **24** warstwach, rzadkie MoE, w każdej warstwie token idzie do **8 z 128** ekspertów. Środkowe **12** warstw liczone jest trzy razy na tych samych wagach, więc na token przypada **48** zastosowań warstw przy 24 warstwach wag. Parametry: **26,4 mld** całkowitych i **3,4 mld** aktywnych. Każde dodatkowe przejście pętli dokłada około **1,0 mld** efektywnych parametrów aktywnych, więc przy trzech przejściach karta podaje **5,4 mld** efektywnych parametrów aktywnych na token. Wagi w większości NVFP4, ostatnie cztery warstwy MXFP8. Checkpoint około **20 GB**.

Wpis: pętla ma poprawiać rozumowanie bez dopisywania go do łańcucha myśli. Własne pomiary laboratorium, nie wspólna tabela: DeepSWE v1.1 **48,2%** i Vals Index v2.2 **46,5%**, jako prowadzenie wśród wag otwartych poniżej 100 mld parametrów całkowitych. Wiedza faktograficzna, mierzone AA-Omniscience, zostaje na poziomie modeli tej skali. Dłuższy kontekst i rozumowanie wieloskokowe rosną wraz z liczbą przejść; zamknięte pytania faktograficzne prawie nie.

Razem z Mini laboratorium wypuszcza badawczy **TML-d24-varloop-research**, trenowany głównie na trzech przejściach, z mniejszą ekspozycją na 1, 2, 4 i 5. Wpis podaje, że horyzont czasu bez łańcucha myśli urósł z **16** do **37** sekund między jednym a trzema przejściami, a na benchmarku rozumowania szeregowego wynik rósł do dziesięciu pętli. Łańcuch myśli skracał się i zostawał czytelny. Wpis mówi też, że model nie szedł w górę na testach sabotażu agentowego wraz z dodawaniem pętli. Te zdania są twierdzeniem laboratorium o własnym modelu badawczym.

Wagi Mini i wariantu o zmiennej pętli są na Hugging Face. Inferencja i dostrajanie: Tinker. Wpis wymienia też SGLang, vLLM, Ollama, Unsloth, NVIDIA Dynamo, TokenSpeed i Llama App oraz dostrajanie RL na SkyRL, Miles i NVIDIA AutoModel.

**Źródła:**

- [Thinking Machines Lab — Introducing Inkling 2 Mini, 20.11.2026](https://thinkingmachines.ai/news/inkling-2-mini/)
- [Thinking Machines Lab — karta modelu Inkling 2 Mini](https://thinkingmachines.ai/model-card/inkling-2-mini/)

### 1.5. Sarvam: checkpoint Sarvam-105B-1711 (22 listopada 2026)

**22 listopada 2026** Sarvam wydaje **Sarvam-105B-1711**, nowy checkpoint otwartych wag Sarvam 105B, trenowany na infrastrukturze B200. Ma to być model klasy Flash-Lite do wsparcia klienta, agentów głosowych i zadań agentowych. Karta na Hugging Face, odczytana 25 listopada: ta sama baza co Sarvam-105B, mieszanka ekspertów o **105 mld** parametrów całkowitych i **10,3 mld** aktywnych. Metadane repozytorium NVFP4 podają licencję **Apache 2.0**. Wagi NVFP4: `sarvamai/sarvam-105b-1711`. Wagi BF16: `sarvamai/sarvam-105b-1711-bf16`. Wpis mówi o **31** warstwach MoE po **128** ekspertów routowanych. Kontynuowane prettrenowanie wydłużyło kontekst do **160 tys.** tokenów, na 512 układach B200 i 330 mld tokenów, w nieco ponad siedem dni. Przykład pamięci przy serwowaniu, w tym samym wpisie, liczy pełny kontekst **128 tys.** Tych dwóch liczb nie należy zrównywać: 160 tys. jest długością treningu kontekstu, 128 tys. długością w przykładzie KV cache.

Cena, którą wpis nazywa blended i liczy w stosunku 3:1 wejście do wyjścia: **0,15 USD** za 1 mln tokenów, z cennika Token Factory **10 / 25 INR** przy **90 INR** za dolara. Poprzedni checkpoint z lutego wpis stawia przy **0,44 USD**. To cena mieszana Sarvam, nie stawka za sam token wejścia.

Średnia ośmiu benchmarków konwersacyjnych, w harnessie Sarvam: z **42,6** w lutym do **73,9**. Osiem składników: IFBench, MultiChallenge, Advanced-IF, WritingBench, Arena-Hard v2, Tau2, BFCL v4 i zestaw Indic. W tym samym pomiarze Gemini 3.5 Flash-Lite (high) ma **74,0** przy blended **0,85 USD**, Gemma 4 31B **73,0** przy **0,54 USD**, GPT-6 Luna (high) **66,3** przy **0,20 USD**, Qwen3.8 27B (xhigh) **74,6** przy **0,96 USD**. Największe ruchy od lutego, nadal z wpisu: IFBench z **32,5** do **82,5**, Tau2 z **46,2** do **85,5**, zestaw Indic z **30,1** do **79,1**. Spójność Tau2, cztery poprawne próby na cztery: **69,5%** wobec **63,9%** dla Gemini 3.5 Flash-Lite i **62,1%** dla Gemma 4 31B. GDPval-S, zadania OpenAI oceniane przez GPT-6 Luna w harnessie Sarvam: **66,9** wobec **73,0** dla Gemini 3.5 Flash-Lite. AIME 26 bez narzędzi: **89,7**, z narzędziami **94,2**.

Dostrojenie głosowe w produkcie Samvaad: **68,7** na Samvaad bench wobec **57,9** dla bazowego checkpointu. Bench ma 338 ocen następnej tury, po angielsku i w 12 językach indyjskich, często mieszanych, i jest na Hugging Face. Wpis lojalnie opisuje go jako zbiór wewnętrzny, z sędzią-modelem.

Przepustowość. Lede wpisu mówi, że NVFP4 na jednej RTX PRO 6000 Blackwell dochodzi do **99** tokenów na sekundę na użytkownika. Karta Hugging Face, przy myśleniu włączonym, DSpark i kontekście 50 tys., podaje dla jednego użytkownika na tej karcie **61,8** tokena na sekundę. Ten przegląd nie rozstrzyga, która konfiguracja stoi za liczbą 99. Na B200, przy 64 równoległych żądaniach, wpis podaje około **6 067** tokenów dekodowania na sekundę na GPU dla NVFP4 z DSpark. Checkpoint NVFP4 ma **65 GB**, wobec **111 GB** w MXFP8 i **198 GB** w BF16.

**Źródła:**

- [Sarvam — Introducing Sarvam-105B-1711, 22.11.2026](https://www.sarvam.ai/blogs/sarvam-105b-1711)
- [Hugging Face — sarvamai/sarvam-105b-1711](https://huggingface.co/sarvamai/sarvam-105b-1711)

### 1.6. Z.ai: GLM-5.4 i pierwszy flagowy Loop Transformer (23 listopada 2026)

**23 listopada 2026** Z.ai publikuje wpis badawczy o **GLM-5.4**. Jest to pierwszy flagowiec firmy na architekturze Loop Transformer: wspólny blok warstw liczony więcej niż raz, bez dokładania parametrów. Wpis mówi, że model pętli **28** warstw bazy GLM-5 przez **dwie** iteracje, w skali **750 mld** parametrów.

Z.ai twierdzi, że poziom inteligencji jest porównywalny z modelami o **2–3 bln** parametrów. W odczytanym wpisie nie ma tabeli benchmarków samego GLM-5.4 ani opisu, jak to porównanie policzono. Kontrolowany dowód we wpisie dotyczy modelu **30 mld**, o tej samej architekturze co baza 750 mld: przy identycznej liczbie parametrów i około **10%** więcej compute treningowego wersja pętlowa zyskuje najwięcej na matematyce, rozumowaniu naukowym i długim kontekście, a średnia długość wyjścia spada o **10–14%** na większości benchmarków, w tym GPQA-Diamond i MMLU-Pro. Te procenty są wynikiem modelu 30 mld po 200 tys. kroków SFT długiego kontekstu, nie wynikiem flagowca.

Trzy zmiany opisane przy skali 750 mld: bramki na token i na iterację, żeby kolejne przejście nie rozjeżdżało skali aktywacji; współdzielony rzadki cache KV z pierwszego przejścia plus własne okno przesuwne drugiego, żeby dodatkowa pętla nie trzymała pełnego cache; ponowne użycie indeksów rzadkiej atencji z pierwszego przejścia. Wpis mówi, że przy kontekście **1 mln** tokenów wzrost kosztu wdrożenia wobec GLM-5.3 zostaje dzięki temu pod kontrolą. Przepustowość, jako twierdzenie firmy: do **200** tokenów na sekundę poza szczytem i **70–80** w szczycie.

Ograniczenie, które wpis sam wymienia: model wpada w zbyt długie pętle „maratońskiego myślenia”. Z.ai dodaje, że to przedłużone sprawdzanie poprawia dokładność ponad to, co wynikałoby z samej liczby parametrów. API, według dokumentacji modelu, ma ruszyć po ocenie bezpieczeństwa. Dla planów z limitem tygodniowym pula GLM-5.4 wynosi **1,5 raza** puli GLM-5.3. Wagi mają zostać otwarte po utwardzeniu bezpieczeństwa. Dostęp w dniu wpisu: plan GLM Coding, ZCode i czat Z.ai.

**Źródła:**

- [Z.ai — GLM-5.4: Toward Generalized Coding with Our First Loop Transformer, 23.11.2026](https://z.ai/blog/glm-5.4)
- [Z.ai — dokumentacja modelu GLM-5.4](https://docs.z.ai/guides/llm/glm-5.4)

### 1.7. Alibaba: qwen-audio-3.1-live oraz dwa ruchy wokół Qwen4-Max (20–25 listopada 2026)

**23 listopada 2026** dziennik wydań Model Studio i strona modelu, zaktualizowana tego dnia, wprowadzają **`qwen-audio-3.1-live`**. To model głosu w czasie rzeczywistym, pełny dupleks. Ma mówić z użytkownikiem dalej, gdy aplikacja albo model w tle liczy zadanie, i wypowiedzieć postęp oraz wynik. Wejście i wyjście: tekst i audio. Wywołania funkcji: tak. Wyjście strukturalne i wbudowane wyszukiwanie: nie.

Dwa tryby delegacji. W trybie Client zadanie wykonuje aplikacja. W trybie Responses Model Studio woła wskazany model zaplecza, a jego zużycie tokenów jest rozliczane osobno. Instrukcje systemowe i definicje funkcji frontendowego modelu: łącznie do **65 536** tokenów. Jednocześnie do **5** połączeń WebSocket.

Cennik jest za czas sesji, nie za token głosu. Po nawiązaniu połączenia sesja kosztuje co najmniej **3** sekundy. Tekst, cisza i bezczynność w sesji liczą się tak samo. Singapur: **0,000710 USD** za sekundę. Chiny (Pekin): **0,000471 USD** za sekundę. Strona pomocy Qwen-Audio-Live ma znacznik aktualizacji **24 listopada 2026** i w szybkim starcie podaje też identyfikator `qwen-audio-4.0-realtime-preview` jako model, który mówi z użytkownikiem, przy `model=qwen-audio-3.1-live` w adresie połączenia. Tych dwóch identyfikatorów nie należy traktować jako jednego modelu: pierwszy wybiera usługę, drugi jest przykładem modelu sesji.

Qwen4-Max jako premiera zostaje w przeglądzie z 18 listopada. Nowe w tym oknie są dwa wpisy dziennika:

- **20 listopada 2026**: `qwen4-max` jest dostępny w zakresie wdrożenia USA, region Wirginia. Dziennik powtarza, że model obsługuje API zgodne z OpenAI i Anthropic. To rozszerzenie regionu, nie druga premiera.
- **25 listopada 2026, 10:00 czasu UTC+8**: `qwen4-max-preview` zostaje wycofany. Stary identyfikator nadal przyjmuje wywołania i kieruje je na `qwen4-max`. Zniżka podglądu przestaje obowiązywać. Rozliczenie idzie stawką standardową `qwen4-max` i może być wyższe niż w podglądzie.

**Źródła:**

- [Alibaba Cloud — qwen-audio-3.1-live, aktualizacja 23.11.2026](https://www.alibabacloud.com/help/en/model-studio/qwen-audio-3-1-live)
- [Alibaba Cloud — Qwen-Audio-Live, aktualizacja 24.11.2026](https://www.alibabacloud.com/help/en/model-studio/qwen-audio-live)
- [QwenCloud — dziennik wydań modeli, wpisy 20, 23 i 25.11.2026](https://docs.qwencloud.com/changelog/models)

### 1.8. Sand.ai: MAGI-2, model wideo 480 mld (24 listopada 2026)

**24 listopada 2026** Sand.ai ogłasza **MAGI-2**, pełnoskalowy model po podglądzie z sierpnia 2026. Podgląd miał około **114 mld** parametrów całkowitych i około **6 mld** aktywnych. MAGI-2 skaluje bazę ponad czterokrotnie, do **480 mld** całkowitych i około **28 mld** aktywnych, a dane prettrenowania około trzykrotnie, do **4 bln** tokenów. Generuje do **30 sekund** natywnego audio-wideo w **1080p** i **25 kl./s**, przyjmuje do **20** referencji (do 10 obrazów, 5 wideo i 5 klipów audio), steruje osią czasu i edytuje istniejące wideo.

Jedna liczba preferencji z wpisu: średnie Elo z czterech zadań Artificial Analysis Video Arena v2.1 rośnie o **151,8** punktu wobec podglądu, z **998,5** do **1150,3**. Cztery zadania: I2V, I2V bez dźwięku, T2V bez dźwięku i T2V. Wagi w dniu wpisu nie są otwarte. Firma zapowiada późniejsze otwarcie kodu i raport techniczny.

Architektura, którą wpis niesie z podglądu i skaluje: jeden strumień tokenów tekstu, wideo i audio oraz Multi-Head Latent MoE. Przy dopasowanych FLOP-ach i konfiguracji uznanej przez firmę za optymalną dla prettrenowania 480 mld wpis podaje około **22%** szybszy trening wobec LatentMoE. Ablacja przy dopasowanym budżecie parametrów: 8-głowicowy Multi-Head Latent MoE ma niższą stratę walidacyjną niż standardowe MoE i lekko wyprzedza LatentMoE, czyli przypadek jednej głowy.

Po prettrenowaniu firma opisuje zachowania, których nie trenowała wprost i które sprawdzała z wyłączonym przepisywaniem promptu przez zewnętrzny model językowy: wczesne ślady rozwiązywania łamigłówek wizualnych, uzupełniania narracji i instrukcji w innym języku. Po dostrojeniu na kilku tysiącach klipów obraz jest wyraźnie staranniejszy, a te zachowania trudniej wywołać. Hipoteza wpisu: mały zbiór nastawiony na estetykę zwęża rozkład, kosztem szerszej generalizacji z prettrenowania. To hipoteza Sand.ai, nie niezależna replikacja.

Ograniczenia z wpisu: artefakty przy bardzo szybkim ruchu, zbyt gładka animacja 2D w planach średnich i szerokich, warstwa dźwięku złożonych scen oraz właśnie zachowanie zdolności z prettrenowania po post-treningu.

**Źródła:**

- [Sand.ai — MAGI-2, 24.11.2026](https://sand.ai/blog/magi-2/)

### 1.9. Cognition: SWE-2.1 (24 listopada 2026)

**24 listopada 2026** Cognition wydaje **SWE-2.1**. Wpis mówi, że model, jak poprzednik, jest trenowany czystym uczeniem ze wzmocnieniem na **Kimi K3**, i że zyski w kodzie biorą się z celowania w ogólną inteligencję oraz długie zadania.

Tabela wpisu, z zastrzeżeniem noty metodologicznej: jeśli istnieje wynik upstream albo wynik podany przez autora modelu, Cognition go przepisuje; w pozostałych wypadkach mierzy sama. Dla modeli zamkniętych używa harnessu preferowanego przez twórcę, dla modeli otwartych i własnych — Devin CLI. Wybrane wiersze SWE-2.1 wobec SWE-2: Terminal-Bench 4.1 **50,0** wobec **24,2**; FrontierCode 2.0 **41,3** wobec **24,1**; SWE Marathon v1.2 **54,9** wobec **32,5**. W tych samych wierszach tabela podaje dla Gemini 4 Neon **65,2** i **46,2**. Te dwie liczby pokrywają się z liczbami opublikowanymi przez Google w sekcji 1.1. Nie są nowym, niezależnym pomiarem tylko dlatego, że stoją w tabeli Cognition.

Osobno Cognition wydaje **SWE-2.1 Ultrafast**, ten sam model przez partnerstwo z Cerebras, według wpisu **10 razy** szybciej. Grafika prędkości we wpisie zestawia Ultrafast przy **600** tokenach na sekundę ze SWE-2.1 przy **60**.

Wpis opisuje też wyższe wyniki na benchmarkach cyberbezpieczeństwa i zapowiada **SWE-2.1 Cyber**, wersję z mniej restrykcyjnymi zabezpieczeniami, do skanów w Devin Security. Przytoczenie procentów, wyłącznie jako twierdzenie Cognition i bez opisu łańcuchów, środowisk ani sposobu liczenia flag: ExploitBench **80,0**, sukces ExploitGym **27,3**. Nota wpisu mówi, że ExploitGym liczono z wyłączonymi mitygacjami. Ten przegląd nie streszcza incydentów z treningu, ucieczek z piaskownicy ani konstrukcji zadań. Zostają one w notach metodologicznych wpisu, poza zakresem tego podsumowania.

**Źródła:**

- [Cognition — Introducing SWE-2.1, 24.11.2026](https://cognition.com/blog/swe-2-1)

### 1.10. SenseTime: SenseNova U1.6 (24 listopada 2026)

**24 listopada 2026** SenseTime ogłasza i otwiera wagi **SenseNova U1.6**. Komunikat i repozytorium OpenSenseNova opisują model 8 mld jako kontynuację serii U: ten sam model rozumie obraz, generuje go i poprawia. Nowość wobec U1.5, nazwana w komunikacie: natywna autokorekta obrazu. Po pierwszej infografice model ma porównać ją z promptem, wskazać błędy tekstu i wygenerować poprawkę w tym samym przebiegu. Trening autokorekty dotyczył infografik. Komunikat dodaje, że część efektu widać też poza infografikami, i nie podaje do tego osobnej liczby.

Liczby z komunikatu, jako pomiary SenseTime: w wewnętrznej ocenie użytkowników estetyka U1.6 Lite jest o około **10%** wyższa niż U1.5 Lite. Na gęstych infografikach UltraTextBench wynik U1.6 Lite rośnie z **86,04** przy jednym przejściu do **92,28** z autokorektą, względnie o około **7%**. Repozytorium GitHub powtarza te dwa przybliżenia i datuje wydanie na 24 listopada, łącznie z wariantami dystylacji na 4 i 8 kroków oraz wsparciem w ComfyUI.

Karta `sensenova/SenseNova-U1.6-8B-MoT` opisuje shardowany checkpoint BF16 i podaje licencję **Apache 2.0**. Obok są warianty Native (BF16, FP8 W8A8, INT8), GGUF (Q4_0, Q6_K, Q8_0) oraz LoRA na 4 i 8 kroków. API pod nazwą U1.6 Lite jest, według komunikatu, w produktach Xiaohuanxiong, Seko i Kapi, w SenseNova Token Plan oraz w SenseNova Studio.

**Źródła:**

- [SenseTime — komunikat o SenseNova U1.6, 24.11.2026](https://www.sensetime.com/cn/news/sensenova-u1-6-open-source-20261124-1152)
- [GitHub — OpenSenseNova/SenseNova-U1, wpis z 24.11.2026](https://github.com/OpenSenseNova/SenseNova-U1/)
- [Hugging Face — sensenova/SenseNova-U1.6-8B-MoT](https://huggingface.co/sensenova/SenseNova-U1.6-8B-MoT)

### 1.11. XPENG: WorldGPT (24 listopada 2026)

**24 listopada 2026** XPENG ogłasza **WorldGPT**, model z rodziny Turing World Model. Komunikat opisuje go jako jeden model uczący się na sześciu typach maszyn: samochodach, łodziach, dronach, robotach jednoramiennych, robotach dwuramiennych i robotach humanoidalnych. Z poprzednich klatek kamery i instrukcji ma generować wideo dalszego przebiegu sceny, plan działań i uzasadnienie w języku naturalnym. Wiedza jest zbierana w dużym modelu-nauczycielu w chmurze i dystylowana do mniejszych modeli na urządzeniu.

Komunikat podaje **12** pierwszych miejsc na publicznych benchmarkach w czterech obszarach: jazda autonomiczna, manipulacja robotyczna, rozumienie obrazu i generowanie wideo, według stanu na **12 listopada 2026**. Odczytany komunikat nie zawiera tabeli tych dwunastu zadań. Bez tej tabeli liczba 12 zostaje twierdzeniem XPENG, nie rankingiem do złożenia z innymi laboratoriami.

**Źródła:**

- [XPENG — WorldGPT, 24.11.2026](https://www.xpeng.com/pressroom/news/01a20bcf44b3a1e838d68a02a2110153)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie nie ma jednej nowej ustawy sądowej. Jest za to uruchomiony, według sprawozdania, pilotaż narzędzia badawczego w kenijskich sądach, zapowiedź grudniowych konsultacji nad indyjskim projektem regulaminu oraz seria orzeczeń, które rozdzielają użycie AI od odpowiedzialności za treść pism. Polska w odczytanych 25 listopada źródłach urzędowych nadal nie ogłasza składu Społecznej Rady. Senat 19 listopada otwiera za to obywatelski proces o bezpieczeństwie internetu i sztucznej inteligencji. To nie jest regulamin sądowy. Jest to najbliższy polski fakt tygodnia przy prawie i administracji.

Orzeczenie Sądu Najwyższego Indii w sprawie *Vijay Ghanshyam Gadiya* jest z **2 września 2026**. Nie wchodzi do tego tygodnia. Wytyczne z Lwowa były przygotowane na konferencję **13 listopada**. Irlandzka wytyczna dla członków trybunału jest datowana **9 listopada**. Oba dokumenty zostają poza tym oknem.

### 2.1. Kenia: pilotaż Mahakama AI w sprawozdaniu SOJAR (20 listopada 2026)

**20 listopada 2026** w Nairobi przewodnicząca sądownictwa Martha Koome przedstawia *State of the Judiciary and the Administration of Justice Annual Report* za rok finansowy **2025/2026**. Komunikat sądownictwa, w akapicie o cyfrowym wymiarze sprawiedliwości, podaje, że elektroniczne wnoszenie spraw i Case Tracking System działają we wszystkich sądach i trybunałach, że zdigitalizowano dodatkowe **192 633** akt, do łącznie **749 522**, oraz że **rozpoczął się pilotaż Mahakama AI, narzędzia do researchu prawnego**.

Komunikat nie opisuje architektury modelu, źródeł, na których narzędzie odpowiada, ani projektu polityki korzystania z AI. Tych szczegółów nie należy dopisywać z omówień prasowych. Pozostałe liczby komunikatu dotyczą obciążenia sądów, nie narzędzia: sądy załatwiły **576 702** spraw wobec **561 580** wpływów, wskaźnik rozliczenia **103%** drugi rok z rzędu, a zaległość ogółem spadła o **2,5%**, z **595 076** do **579 954** spraw na 30 czerwca 2026. **341 412** spraw, około **59%**, trwało dłużej niż rok.

**Źródła:**

- [Judiciary of Kenya — komunikat o SOJAR 2025/2026, 20.11.2026](https://judiciary.go.ke/judiciary-resolves-more-cases-than-filed-for-second-consecutive-year-as-pending-caseload-declines/)

### 2.2. Indie: High Court w Jabalpurze i konsultacje nad projektem regulaminu

**17 listopada 2026** sędzia Vivek Kumar Singh z High Court of Madhya Pradesh w Jabalpurze wydaje postanowienie w *Piyush Mani Tiwari v. The State of Madhya Pradesh*, Writ Petition No. 27922 of 2024. PDF z postanowieniem LiveLaw publikuje **19 listopada**. Poranny przegląd z 18 listopada tego postanowienia nie odnotował.

Skarga dotyczy dymisji funkcjonariusza policji bez postępowania dyscyplinarnego. Sąd uchyla rozkaz dymisji z 27 maja 2024 i rozkaz odwoławczy z 22 lipca 2024, bo nie zapisano w nich powodów, dla których postępowanie miałoby być niewykonalne w świetle art. 311 ust. 2 lit. b konstytucji. Funkcjonariusz ma wrócić do służby. Władza może wszcząć zwykłe postępowanie. Ten przegląd nie streszcza zarzutu, który był podstawą dymisji, i nie ocenia go.

Osobny fragment, ust. 19, dotyczy pisma stanu. Stan powołał się na wyrok „State of Andhra Pradesh vs. S.S. Mohammad Nisar”, (2008) 5 SCC 230, dla tezy, że pod art. 226 nie ocenia się dowodów na nowo. Sąd pisze, że takiego wyroku nie ma, a cytat (2008) 5 SCC 230 odpowiada sprawie *Sidhartha Vashisht @ Manu Sharma v. State (NCT of Delhi)*, o zawieszeniu wykonania kary w apelacji karnej. Sąd uznaje za jaskrawe, że strona sięgnęła na ślepo po narzędzia sztucznej inteligencji i połączyła zmyśloną nazwę sprawy z cudzym cytatem. Pisma do sądu konstytucyjnego nazywa dokumentami uroczystymi. Wstawianie fikcyjnych orzeczeń bez sprawdzenia „graniczy z aktywnym wprowadzaniem sądu w błąd”. Stan i aparat stanowy dostają ostrzeżenie. Biuro Advocate General ma dopilnować, żeby projektujący pełnomocnik sprawdził tezy i cytaty, zanim zostaną zaprzysiężone i złożone do akt. Odpis postanowienia idzie do Principal Secretary, Law, oraz do Advocate General. Kosztów nie zasądzono. Sąd nie pisze, że stan przyznał się do użycia AI. To wniosek sądu z zestawienia nazwy i cytatu.

**19 listopada 2026** ThePrint, powołując się na źródła, a nie na komunikat sądu, pisze, że komitet Sądu Najwyższego do spraw AI, z sędzią P.S. Narasimhą jako przewodniczącym, odbędzie w grudniu, przed zimową przerwą, dwudniowe spotkanie z ekspertami spoza samej palestry. Po nim mają pójść obrady wewnętrzne i dopiero wtedy notyfikacja regulaminu. Artykuł przypomina, że projekt *Regulations for Use of Artificial Intelligence* pochodzi z czerwca 2026 i nadal jest projektem. W relacjonowanym przez ThePrint brzmieniu projektu: AI tylko wspomaga i nie zastępuje orzekania; pełnomocnik miałby ujawniać użycie AI przed rozpoczęciem wystąpień; za sfabrykowany materiał odpowiada składający; sąd informuje strony, gdy AI istotnie wspomagało zarządzanie sprawą w sposób mogący wpłynąć na tok postępowania; zakazane jest oparte na AI ciągłe monitorowanie sędziów, pełnomocników i stron w budynku sądu; skargi rozpatruje sekretariat przy komitecie, który może zawiesić system; dane osobowe nie trenują systemu bez uprzedniej zgody; wynik AI nie jest podstawą wyroku, postanowienia ani ustalenia faktu lub prawa. ThePrint dodaje, że Supreme Court Advocates-on-Record Association sprzeciwia się obowiązkowi ujawnienia i chce wdrożenia etapami, mocniejszej ochrony danych oraz większego udziału adwokatów. To relacja prasowa o nienazwanych źródłach i o projekcie z czerwca, nie ogłoszenie regulaminu.

**Źródła:**

- [High Court of Madhya Pradesh — postanowienie z 17.11.2026, PDF udostępniony 19.11.2026](https://www.livelaw.in/pdf_upload/2026/11/19/piyush-mani-tiwari-v-state-of-madhya-pradesh-712919.pdf)
- [LiveLaw — omówienie z 19.11.2026](https://www.livelaw.in/high-court/madhya-pradesh-high-court/madhya-pradesh-high-court-slams-state-for-use-of-ai-tools-to-draft-pleadings-notes-fabricated-case-559092)
- [ThePrint — Bhadra Sinha, 19.11.2026](https://theprint.in/judiciary/sc-panel-to-hold-2-day-meet-with-industry-experts-before-finalising-rules-on-ai-for-legal-sector/3103372/)

### 2.3. Australia: zakaz generatywnego AI w pismach bez zezwolenia sądu (20 listopada 2026)

**20 listopada 2026** sędzia Perry z Federal Court of Australia wydaje wyrok *Kavanagh v Atlassian Pty Ltd (Confidentiality and Non-Publication Application)* [2026] FCA 1774, sprawa NSD 1752 of 2026. Wniosek o szerokie utajnienie akt zostaje uwzględniony tylko na krótko i w części. Do 23:59 **24 listopada 2026** część pism jest poufna. Ten przegląd nie wymienia tych pism ani nie streszcza zarzutów z postępowania pracy.

Punkt 4 sentencji: bez zezwolenia sądu żadna strona nie używa generatywnej sztucznej inteligencji do tworzenia tekstu w dokumencie składanym do sądu, w tym w pismach procesowych i oświadczeniach. Uzasadnienie, ust. 45–46: nieprofesjonalny reprezentujący się sam skarżący użył generatywnego AI co najmniej do części stanowiska. Część cytatów i pinów nie wspierała tez, nie istniała albo zawierała inne błędy. Sąd podniósł to na początku rozprawy. Skarżący, według uzasadnienia, wyglądał na osobę, która akceptuje, że użyła generatywnego AI co najmniej częściowo do przygotowania stanowiska. Sąd nazywa to zrozumiałym u osoby bez pełnomocnika i zarazem niepomocnym, bo zjada czas stron i sądu. Stąd zakaz bez zezwolenia, skierowany do każdej strony, nie tylko do skarżącego.

**Źródła:**

- [Jade — Kavanagh v Atlassian Pty Ltd [2026] FCA 1774](https://jade.io/article/1305595)

### 2.4. Stany Zjednoczone: zawieszenie w Ohio, szkolenie w First Circuit, ostrzeżenie na Florydzie

Trzy orzeczenia z tego okna dotyczą cytowań. Żadne nie zakazuje AI jako takiej. Wszystkie trzy trzymają człowieka przy treści pisma.

**Ohio, 24 listopada 2026.** Sąd Najwyższy Ohio w jednomyślnej opinii *per curiam* bezterminowo zawiesza Arleeshę Shawntay Wilson, Attorney Registration No. 0097351, w sprawie *Cleveland Metropolitan Bar Association v. Wilson*, Slip Opinion No. 2026-Ohio-4626, nr 2026-0724. Opinia jest z 24 listopada. Do czasu publikacji w Ohio Official Reports można ją cytować jako slip opinion i podlega korektom formalnym.

Zawieszenie dotyczy całego przypisanego naruszenia, nie samego wątku AI. Panel i komisja, a za nimi sąd, przyjmują naruszenia Prof.Cond.R. 1.1, 1.3, 1.4(a)(3), 1.4(c), 1.16(d), 3.1, 3.3(a)(1), 3.4(c), 8.1(b), 8.4(d) i 8.4(h): zaniedbanie spraw, niekompetentną reprezentację, fałszywe stwierdzenia wobec dwóch trybunałów, bezzasadny argument, brak współpracy w jednym postępowaniu dyscyplinarnym oraz zachowanie szkodliwe dla wymiaru sprawiedliwości i rzutujące na zdolność do wykonywania zawodu. Wątek AI jest w jednym ze stanów faktycznych. W piśmie przeciwko miastu Cleveland Wilson powołała cztery sprawy, które nie istnieją, i dwukrotnie przeinaczyła znaczenie siedmiu innych. Przyznała użycie AI, gdy sąd rejonowy o to zapytał. Sąd federalny dla Northern District of Ohio, sprawa nr 1:24-cv-02033-PAB, nałożył **7 500 USD** sankcji. Opinia zapisuje, że do rozprawy dyscyplinarnej Wilson nie zapłaciła uzgodnionych rat po 250 USD i że uzgodniona restytucja przekracza **647 000 USD**. Koszty postępowania dyscyplinarnego ponosi Wilson. Komunikat biura prasowego sądu z tego samego dnia streszcza opinię dla publiczności i sam zastrzega, że nie jest głową urzędową ani syllabusem.

**First Circuit, 24 listopada 2026.** Nakaz w *Molina-Diaz v. Blanche*, No. 25-2091, skład: Barron, Chief Judge, Gelpí i Rikelman. Nakaz nie rozstrzyga meritum. 4 września sąd polecił pełnomocniczce Clarissie Moraes Kalil odnieść się do cytowań w piśmie otwierającym: spraw, które wyglądały na nieistniejące, cytatów nieobecnych w przywołanych orzeczeniach i wątpliwych opisów tez. 2 listopada Kalil napisała, że bierze odpowiedzialność i że błędy wynikły z braku osobistego sprawdzenia tez i cytatów powstałych w researchu generatywnym. Sąd na podstawie Fed. R. App. P. 46(c) nakazuje jej szkolenie, w jednym kursie albo w kilku, z praktyki cytowania, obowiązku szczerości oraz „etycznych i zawodowych obowiązków związanych z użyciem sztucznej inteligencji w praktyce prawniczej”. W ciągu **90 dni** ma złożyć potwierdzenie: nazwę kursu, podmiot prowadzący i poświadczenie ukończenia. Nie ma w tym nakazie grzywny ani wykluczenia z palestry. Bezpośrednie pobranie PDF z witryny sądu w trakcie tej redakcji zostało odrzucone przez filtr witryny. Treść dwustronicowego nakazu odczytano wcześniej z tego samego adresu.

**Floryda, 18 listopada 2026.** Fourth District Court of Appeal w *Beavers v. Pond*, No. 4D2025-1473, opinia sędzi Shaw, do której przyłączają się sędziowie May i Shepherd. Apelacja ze spraw spadkowych w Broward. Meritum zostaje utrzymane bez omówienia. Sąd pisze osobno o piśmie odpowiedzi appellee. Cytowane sprawy istnieją, ale nie stoją za tezami, które im przypisano. Przy utrzymaniu meritum sąd wyraźnie pomija te cytaty. 21 października 2026 wydano order to show cause. Appellee przyznała błędy w cytatach i napisała, że research użyty do ich zebrania był częściowo oparty o programy inteligencji wspomaganej komputerowo, a potem broniła się, że cytaty są tylko niedokładne, nie zmyślone, i że argumenty nie były składane w złej wierze. Tabela korekt w większości zmieniała format, nie tezę. Sąd odsyła do własnej linii: powołanie prawdziwej sprawy za fałszywą tezę jest tak samo poważne jak powołanie sprawy, której nie ma, a brak zamiaru wprowadzenia w błąd nie jest usprawiedliwieniem. Pełnomocnicy, którzy używają AI, odpowiadają za treść pisma. Sankcji tym razem nie nałożono. Sąd ostrzega, że kolejne problemy z cytatami mogą skończyć się sankcją z Florida Rule of Appellate Procedure 9.410(a). Opinia nie jest prawomocna do czasu rozstrzygnięcia ewentualnego, terminowego wniosku o rehearing. Pełnomocniczką appellee w nagłówku jest Marla J. Ferguson.

**Źródła:**

- [Supreme Court of Ohio — Cleveland Metro. Bar Assn. v. Wilson, Slip Opinion No. 2026-Ohio-4626](https://www.supremecourt.ohio.gov/rod/docs/pdf/0/2026/2026-Ohio-4626.pdf)
- [Court News Ohio — omówienie z 24.11.2026](https://www.courtnewsohio.gov/cases/2026/SCO/1124/260724.asp)
- [U.S. Court of Appeals for the First Circuit — nakaz z 24.11.2026, No. 25-2091](https://www.ca1.uscourts.gov/sites/ca1/files/opnfiles/25-2091O-01A.pdf)
- [Florida Fourth DCA — Beavers v. Pond, No. 4D2025-1473, 18.11.2026](https://flcourts-media.flcourts.gov/content/download/2498377/opinion/Opinion_2025-1473.pdf)

### 2.5. Polska: rada nadal bez komunikatu o powołaniu, Senat otwiera naradę obywatelską

Nabór do Społecznej Rady do spraw Sztucznej Inteligencji, z terminem **16 listopada 2026**, jest opisany w przeglądzie z 11 listopada. Nominacja Łukasza Mickiewicza przez prezydium NSZZ „Solidarność”, decyzja 131/26 z 16 listopada, jest w przeglądzie z 18 listopada. Tych opisów ten tekst nie powtarza i nie przytacza na nowo listy podmiotów uprawnionych do zgłoszenia.

**25 listopada 2026** strona „Informacje bieżące” Komisji Rozwoju i Bezpieczeństwa Sztucznej Inteligencji nadal pokazuje jako bieżącą wiadomość nabór, który przyjmował zgłoszenia do 16 listopada. Osobnego komunikatu o powołaniu składu Rady na tej stronie nie znaleziono. Brak wpisu nie jest dowodem, że powołanie nie zapadło inną drogą. Jest tylko stwierdzeniem, co było na tej stronie w dniu przeglądu.

**19 listopada 2026** Senat informuje o Ogólnopolskiej Naradzie Obywatelskiej o Bezpiecznym Internecie. To wspólna inicjatywa Senatu i Fundacji Stocznia, w partnerstwie z Ministerstwem Cyfryzacji. Od listopada 2026 do stycznia 2027 mają iść narady lokalne o dezinformacji, oszustwach, bezpieczeństwie danych i algorytmach uzależniających. Zebrane głosy mają zasilić panel 110 wylosowanych osób. Rekomendacje mają trafić do Senatu i Ministerstwa Cyfryzacji. To proces obywatelski o platformach i sztucznej inteligencji, nie przepis o użyciu AI przez sąd. Bezpośrednie zapytanie do strony Senatu w trakcie tej redakcji dostało odpowiedź 403. Treść notatki odczytano z publicznej strony przez wyszukiwanie.

**Źródła:**

- [Komisja — Informacje bieżące, odczyt 25.11.2026](https://www.gov.pl/web/kribsi/informacje-biezace)
- [Senat RP — Ogólnopolska Narada Obywatelska o Bezpiecznym Internecie, 19.11.2026](https://www.senat.gov.pl/aktualnoscilista/art,17927,ogolnopolska-narada-obywatelska-o-bezpiecznym-internecie.html)

---

## Czego ten przegląd świadomie nie wznawia

Poza oknem albo już opisane: GPT-6.2 Astra i Sol z 17 listopada, Gemini 4 Hydrogen z 12 listopada, premiera Qwen4-Max z 16 listopada, Genie 4 jako ogłoszenie badawcze z 27 października, Claude Fable 5.2 i Mythos 5.2 z 9 listopada, *Vijay Ghanshyam Gadiya* z 2 września 2026, wytyczne lwowskie na konferencję 13 listopada oraz irlandzka Guideline 2026-4 z 9 listopada. Nie składano w jeden ranking tabel Google, Sarvam, Cognition i Z.ai. Nie opisywano metod exploitów, pentestów ani incydentów z treningu modeli o podwyższonych zdolnościach cybernetycznych.
