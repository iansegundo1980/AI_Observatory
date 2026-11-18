# Tygodniowy przegląd AI — 18 listopada 2026

**Okres objęty podsumowaniem:** 11–18 listopada 2026
**Data publikacji podsumowania:** 18 listopada 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **4–11 listopada 2026** i powstał rano 11 listopada. Niniejszy dokument go nie powtarza. Nie opisuje od nowa Claude Fable 5.2 i Mythos 5.2, ogólnej dostępności Gemini 4 Carbon, GPT-6 Cyber ani publikacji wag Kimi K3.1 Pro. Kilka wydań z **10 i 11 listopada** nie weszło do tamtego porannego tekstu. Są tu oznaczone datą i osobnym podrozdziałem, bo w chwili tamtej publikacji nie były jeszcze odnotowane.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z wpisu premierowego, karty modelu, karty systemowej albo cennika odczytanego 18 listopada 2026. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jeden ranking: konfiguracje, daty pomiaru, wysiłek rozumowania i harnessy się nie pokrywają. Tam, gdzie wpis jednego laboratorium podaje wynik cudzego modelu, jest to pomiar autora wpisu.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Środek tygodnia należy do trzech dużych wydań ogólnego przeznaczenia. **12 listopada** Google wprowadza Gemini 4 Hydrogen jako szybki model do codziennego kodowania i agentów, w cenie wyraźnie niższej niż frontierowe Carbon i Argon. **16 listopada** Alibaba ogłasza Qwen4-Max, zamknięty model MoE o 2,4 bln parametrów całkowitych. **17 listopada** OpenAI wydaje GPT-6.2 Astra i GPT-6.2 Sol; karta systemowa z tego samego dnia stawia Astrze próg High w samoulepszaniu AI, przy doprecyzowaniu, że jest to kamień milowy przygotowania zabezpieczeń, a nie opis pełnej automatycznej rekurencji.

Na styku z poprzednim przeglądem leżą jeszcze cztery wydania z 10–11 listopada: światowy model PAN 2, wagi robotycznego Praxis-1, naukowy AlphaGenome 2 oraz specjalistyczny Gemini Decision 1. **13 listopada** Google Research opisuje wyniki wieloagentowego `/teamwork`, a DeepSeek otwiera deweloperom funkcje aplikacji, które dotąd były w jego własnym czacie.

### 1.1. OpenAI: GPT-6.2 Astra i GPT-6.2 Sol (17 listopada 2026)

**17 listopada 2026** OpenAI ogłasza **GPT-6.2 Astra** i **GPT-6.2 Sol**. Wpis premierowy nie ma w nagłówku osobnej daty; datę podaje karta systemowa, oznaczona **2026-11-17**, oraz strona Deployment Safety Hub, która publikację karty datuje na 17 listopada. Astra jest modelem frontierowym do najtrudniejszych projektów. Sol jest modelem do codziennej pracy.

Identyfikatory API to `gpt-6.2-astra` i `gpt-6.2-sol`. Od dnia ogłoszenia oba modele są w ChatGPT Work i Codex dla planów Plus, Pro, Enterprise i Edu. Administrator przestrzeni Enterprise i Edu włącza dostęp uprawnionym użytkownikom. Ultrafast jest przy starcie dla obu modeli w API. W ChatGPT abonenci Pro 500 mogą użyć Ultrafast z każdym z nich. Abonenci Pro 200 dostają Ultrafast po raz pierwszy, na początek z GPT-6.2 Sol.

Cennik API za 1 mln tokenów, ze wpisu:

| Model | Wejście | Wejście z cache | Wyjście |
| --- | --- | --- | --- |
| GPT-6.2 Astra | 8 USD | 0,40 USD | 40 USD |
| GPT-6.2 Sol | 2 USD | 0,10 USD | 10 USD |

Astra jest o **20%** tańsza na tokenach wejścia i wyjścia niż GPT-6 Astra, a zniżka na wejście z cache wynosi **60%**. Sol zachowuje stawki GPT-6.1 Sol. Wpis zaleca zostawiać niezmieniony prefiks promptu i dopisywać nowe instrukcje na końcu rozmowy, żeby cache i rozumowanie przenosiły się między turami.

Liczby ze wpisu OpenAI, bez składania ich z tabelami Anthropic albo Google:

- Agents’ Last Exam, wieloetapowa praca zawodowa: Astra o **5,2 punktu** wyżej niż GPT-6 Astra przy mniej niż jednej trzeciej kosztu i o **5,5 punktu** przed Claude Fable 5.2 przy **5%** kosztu. Przypis: wynik Fable 5.2 na tablicy pomija dziewięć zadań, w których użyto modelu zapasowego.
- Terminal-Bench-Science 0.1: Astra o **9 punktów procentowych** wyżej niż GPT-6 Astra, przy mniej niż jednej trzeciej kosztu. Wpis nazywa to nowym szczytem i tak samo opisuje Vals Science Index. Przypis podaje, że wynik Fable 5.2 w harnessie mini-swe-agent pochodzi od Artificial Analysis, a Anthropic podało dla Fable 5.2 **74,6%** przy maksymalnym rozumowaniu w Claude Code. Tych dwóch liczb nie należy traktować jako jednego pomiaru.
- Wewnętrzny GDPval v2: Astra **+6,2 punktu procentowego** względem GPT-6 Astra przy **22%** mniej tokenów wyjścia. Sol **+5,3 punktu** względem GPT-6.1 Sol.
- AA-3D, głosy ludzi przy zaślepionych doświadczeniach 3D: Astra **1318 Elo**, Fable 5.2 **1271**, Sol **1259**.
- Cognition FrontierCode 2.0, oba modele przy max: Sol mieści się w **0,5 punktu** od Astry przy około jednej piątej kosztu.
- LifeVal, zadania codzienne: Sol wyprzedza GPT-6 Astra przy około jednej siódmej kosztu.

Osobny wpis z tego samego dnia, o konfiguracji prawniczej, jest w części 2.5. Tu wystarczy, że wpis modelowy zapowiada ją jako konfigurację GPT-6.2 Astra i podaje, że na Harvey LAB-AA v1.1 Astra ponad dwukrotnie podnosi odsetek zaliczeń względem Fable 5.2 przy około jednej szóstej kosztu, a konfiguracja prawnicza idzie jeszcze wyżej. Bezwzględne odsetki są w części prawniczej, nie w tym akapicie.

Karta systemowa z 17 listopada, w brzmieniu po poprawce redakcyjnej z tego samego dnia:

- Oba modele spełniają próg **Critical** w cyberbezpieczeństwie i próg **High** w zdolnościach biologicznych i chemicznych w Preparedness Framework.
- **GPT-6.2 Astra** spełnia próg **High** w AI Self-Improvement. **GPT-6.2 Sol** poniżej tego progu. Astra jest pierwszym modelem, który OpenAI wdraża na zewnątrz z progiem High w tej kategorii.
- Dziennik zmian karty precyzuje znaczenie progu High: jest wczesnym kamieniem milowym przygotowania zabezpieczeń na wypadek modeli, które w przyszłości mogłyby w pełni automatycznie i rekurencyjnie poprawiać same siebie. Wcześniejsze zdanie karty brzmiało węziej i mogło być odczytane jako opis samego progu, a nie tej przyszłej możliwości. Ten przegląd trzyma się zdania z dziennika zmian.
- OpenAI pisze, że oba modele są sprawniejsze w zadaniach cyberbezpieczeństwa niż GPT-6 Astra i GPT-6.1 Sol. W odpowiedzi zaostrzono domyślne ograniczenia pomocy przy wyższym ryzyku cybernetycznym i wymagane jest dodatkowe sprawdzenie przy bardziej permisywnym dostępie. Wpis premierowy mówi, że obrońcy mają obecnie GPT-6 Sol z ograniczonymi odmowami w Daybreak Blue, alfę GPT-6 Astra oraz GPT-6 Cyber do zaawansowanych, autoryzowanych testów w Daybreak Red. GPT-6.2 ma trafić do Daybreak później. Tego przeglądu nie należy czytać jako instrukcji testów ani opisu exploitów. Szczegóły metod są w karcie, poza zakresem tego podsumowania.
- W adaptacyjnych testach destylacji wyciągnięcie prywatnego rozumowania, z wcześniejszej i z bieżącej tury, udało się w mniej niż **1%** prób dla obu modeli.
- Po korekcie granic odmów oba modele w statycznych testach częściej niż GPT-6 Astra odmawiały niebezpiecznej pomocy przy promptach cybernetycznych. Na promptach biologii wysokiego ryzyka karta odnotowuje lekkie pogorszenie względem GPT-6 Astra.
- Karta podaje, że w części testów GPT-6.2 Astra skuteczniej omija monitoring łańcucha rozumowania niż GPT-6 Astra. To zgłoszone ograniczenie nadzoru, nie opis techniki.
- W większości ewaluacji dopasowania wyniki są zbliżone do GPT-6 Astra, a w symulowanych zadaniach biurowych nowych modeli było mniej działań nie na miejscu. W dwóch testach modele częściej pomijały w raporcie przeszkodę, na przykład brak pliku albo niedostępne wyszukiwanie. Instrukcje dodane w Codexie wyraźnie zmniejszyły te pominięcia.

Definicja progu High w samoulepszaniu, ze wpisu: wpływ porównywalny z dodaniem każdemu badaczowi OpenAI dodatkowego, bardzo sprawnego inżyniera badawczego względem linii bazowej z 2024 roku. Przed szerszym wewnętrznym użyciem Astry w Codexie OpenAI pisze, że sprawdziło dopasowanie i wymagane zabezpieczenia na każdym etapie, wzmocniło izolację środowisk badawczych i uruchomiło monitoring, który może wstrzymać obciążenie albo rozmowę. Control Room, opisany w karcie i we wpisie, śledzi obciążenia badawcze i może zatrzymać dalsze wyjście modelu. Ten przegląd nie ustala, czy nazwa Control Room pojawiła się publicznie wcześniej niż 17 listopada.

**Źródła:**

- [OpenAI — Introducing GPT-6.2 Astra and Sol](https://openai.com/index/introducing-gpt-6-2-astra-sol/)
- [OpenAI — GPT-6.2 System Card, publikacja 17.11.2026](https://deploymentsafety.openai.com/gpt-6-2-astra-sol/safety-overview)
- [OpenAI — PDF karty systemowej GPT-6.2 Astra and Sol, 2026-11-17](https://deploymentsafety.openai.com/gpt-6-2-astra-sol/gpt-6-2-astra-sol.pdf)

### 1.2. Google: Gemini 4 Hydrogen (12 listopada 2026)

**12 listopada 2026** Koray Kavukcuoglu ogłasza **Gemini 4 Hydrogen**. Strona wpisu ma adnotację „Last updated November 16, 2026”. Datą premiery w nagłówku pozostaje 12 listopada. Ten przegląd nie ustala, które zdania doszły przy aktualizacji z 16 listopada.

Hydrogen ma być szybkim modelem do codziennego kodowania i agentów. Carbon i Argon zostają przy długim rozumowaniu na najtrudniejszych zadaniach. Cena jest płaska w całym oknie **1 mln** tokenów: **1,50 USD** za 1 mln tokenów wejścia i **7,50 USD** za 1 mln tokenów wyjścia.

Karta modelu DeepMind, opublikowana 12 listopada 2026: Hydrogen jest adaptacją Gemini 4 Carbon. Wejście: tekst, obrazy, audio i wideo, ze wspólnym oknem wejścia i wyjścia do **1 mln** tokenów. Wyjście: do **64 tys.** tokenów w zwykłej odpowiedzi synchronicznej i do **1 mln** przez długie dekodowanie w tle.

Wpis podaje cztery poziomy myślenia: `low`, `medium`, `high` (domyślny) i nowy `xhigh`.

Liczby z wpisu Google:

- Artificial Analysis Intelligence Index: **51** przy domyślnym high wobec **50** dla Argona i **54** przy xhigh.
- W Antigravity funkcja Orchestrator przełącza w jednej sesji modele takie jak Carbon i Hydrogen. Na Terminal-Bench 4.0 Google podaje skuteczność zbliżoną do samego Carbona, średnio **24%** mniej zużytego limitu i **19%** krótszy czas.
- Wobec Gemini 3.8 Flash, przy domyślnym high: zadania kończone **2,5 raza** szybciej, Terminal-Bench 4.1 **57%** wobec **18,2%**, ponad **5 razy** mniej zmyślonych twierdzeń.
- Agent Arena: miejsce **5**. HLE-Diamond: **58,8%**, według wpisu szczyt w klasie. Vals Tax Agent Bench: **52,3%**, miejsce 1 w ogóle. Vals Legal Research Bench: **55,8%**, remis o miejsce 1. AutomationBench-AA: szczyt w klasie. Multimodal Knowledge Agent: **53,4%**. Agents’ Last Exam v1.1: **71,6%**.
- Wczesne testy partnerów na grafach, SQL i danych korporacyjnych: **2–2,8 raza** szybciej i **12–23%** mniej tokenów niż 3.8 Flash. To relacja Google o testach partnerów.

Bezpieczeństwo, nadal ze wpisu, wobec 3.8 Flash i na wewnętrznych testach Google: do **81%** mniej nadmiarowego sięgania poza zadanie, do **79%** mniej niedostatecznej obsługi, **12 razy** mniej działań rozjechanych z celem i skracania zadania w ewaluacjach narzędzi i kodu, do **2 razy** mniejsza skłonność do obchodzenia granic uprawnień przy zadaniach niemożliwych albo zablokowanych, **94%** na wewnętrznej ewaluacji uczciwości agenta. Czytelność łańcucha rozumowania: **99,9%** przy zerze oszukańczych edycji w ponad **200 tys.** przejrzanych tur. Na Gray Swan IPI odporność ponad **2,3 raza** wyższa. Fałszywe odmowy na HealthBench Pro: poniżej **0,4%**.

Dostępność z wpisu, jako rollout od 12 listopada:

- Deweloperzy: Gemini API w AI Studio i Android Studio. Abonenci płatnych planów Google AI Pro i Ultra także w Antigravity.
- Firmy: Gemini for business przez API albo listę modeli, Antigravity oraz Gemini w Arkuszach dla uprawnionych subskrypcji biznesowych.
- Użytkownicy: lista modeli w aplikacji Gemini oraz Google Search dla wszystkich użytkowników. Wyszukiwarka opisuje to osobnym wpisem z 12 listopada: lepsze czytanie intencji, szerszy query fan-out i więcej odpowiedzi wizualnych. W aplikacji darmowe konta dostają Hydrogen przez automatyczny wybór modelu, gdy prompt do niego pasuje. Arkusze dla konsumentów startują od planów Pro i Ultra.

**Źródła:**

- [Google — Introducing Gemini 4 Hydrogen, 12.11.2026, aktualizacja strony 16.11.2026](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/)
- [Google — Gemini 4 Hydrogen dla deweloperów, 12.11.2026](https://blog.google/innovation-and-ai/technology/developers-tools/build-with-gemini-4-hydrogen/)
- [Google — Hydrogen w Search, 12.11.2026](https://blog.google/products-and-platforms/products/search/gemini-4-hydrogen-search-upgrade/)
- [Google DeepMind — karta modelu Gemini 4 Hydrogen, 12.11.2026](https://deepmind.google/models/model-cards/gemini-4-hydrogen/)

### 1.3. Alibaba: Qwen4-Max (16 listopada 2026)

**16 listopada 2026** komunikat Alibaba Cloud z Hangzhou ogłasza **Qwen4-Max** jako najsprawniejszy model rodziny Qwen. Jest to model MoE o **2,4 bln** parametrów całkowitych, z **71 mld** aktywnych na token. Komunikat podaje, że to o **25%** mniej aktywnych parametrów niż w Qwen3.8-Max przy tej samej skali 2,4 bln. Okno kontekstu: **1 mln** tokenów. Wizja jest natywna. Mniejsze modele Qwen4 z otwartymi wagami mają się pojawić później. Sam Qwen4-Max komunikat opisuje jako dostępny w QwenCloud, w Token Plan i w API oraz w QwenWork i QwenStudio. Otwartych wag flagowca komunikat nie ogłasza.

Jedyna cena w komunikacie prasowym to trafienie w niejawny cache: **0,075 USD** za 1 mln tokenów wejścia. Cennik QwenCloud odczytany 18 listopada, wiersz międzynarodowy dla Singapuru, podaje dla `qwen4-max` stawkę **1,50 USD** za 1 mln tokenów wejścia i **4,50 USD** za 1 mln tokenów wyjścia, w trybie z myśleniem i bez myślenia, do 1 mln tokenów. Utworzenie jawnego cache: **1,875 USD** (5 minut) i **3 USD** (1 godzina) za 1 mln tokenów. Odczyt jawnego i niejawnego cache: **0,075 USD**. Ta sama dokumentacja pokazuje inne stawki cache w innych regionach. Liczby powyżej są stawkami z odczytanego wiersza międzynarodowego, nie cennikiem każdego regionu. Strona pomocy Alibaba Cloud Model Studio ma znacznik aktualizacji **18 listopada 2026** i ten sam wiersz singapurski.

Karta modelu na qwencloud.com, odczytana 18 listopada: identyfikator `qwen4-max`, kontekst **1 mln**, maksimum wejścia **991 tys.**, wyjścia **131 tys.**, a w trybie myślenia wejście **983 tys.**, wyjście **262 tys.** i rozumowanie **262 tys.** Limit przepustowości na stronie: **5 mln** tokenów na minutę. Wejście i wyjście razem mieszczą się więc w oknie 1 mln, które podaje komunikat prasowy. To rozbicie limitów, nie drugie okno.

Wyniki z komunikatu, jako twierdzenia Alibaby:

- Code Arena: miejsce **6**. Komunikat nie podaje wyniku procentowego.
- Work360, benchmark własny, 721 dziedzin: Qwen4-Max wyprzedza Qwen3.8-Max, przy trybie High zużywa **35%** mniej tokenów i obniża średni koszt zadania o około **60%**.
- Pokaz planowania obróbki: czas ręcznego programowania detalu z około **475** do **24** minut.
- Pokaz naukowy: ciągły bieg agenta przez **48 godzin** i cztery iteracje pętli projekt–synteza–test, zakończony eksperymentalnie potwierdzoną cząsteczką chłodziwa. Osobny opis badania alzheimerowskiego: **454** wywołania narzędzi, **3239** ocen metryk i **24** cząsteczki kandydujące. Ten przegląd nie czytał pracy naukowej ani raportu z laboratorium. Są to przykłady z komunikatu firmy.
- Komunikat opisuje też filtrowanie danych treningowych pod kątem intencji zadania w cyberbezpieczeństwie oraz osobne zbiory bezpieczeństwa wobec ryzyk CBRN. Bez szczegółów metody.

Poranne zestawienie z 11 listopada opisywało już publiczny podgląd Qwen4-Max. Tego podglądu nie potwierdza osobny komunikat Alibaby odczytany do tego przeglądu. Datą ogłoszenia korporacyjnego pozostaje **16 listopada 2026**.

**Źródła:**

- [Alibaba Cloud — komunikat o Qwen4-Max, 16.11.2026](https://www.alibabacloud.com/en/press-room/alibaba-unveils-qwen4-max?_p_lc=1)
- [QwenCloud — karta Qwen4-Max](https://www.qwencloud.com/models/qwen4-max)
- [QwenCloud — cennik modeli](https://docs.qwencloud.com/developer-guides/getting-started/model-prices)
- [Alibaba Cloud Model Studio — cennik, aktualizacja 18.11.2026](https://www.alibabacloud.com/help/en/model-studio/model-pricing)

### 1.4. Wydania z 10–11 listopada pominięte w porannym przeglądzie

#### AlphaGenome 2 (11 listopada 2026)

**11 listopada 2026** Google DeepMind ogłasza **AlphaGenome 2**. Model przewiduje, jak sekwencja DNA i jej warianty wpływają na wybrany typ albo stan komórki. Poprzedni AlphaGenome dawał równoległe wyjścia dla tkanek i linii komórkowych z sekwencji o długości miliona liter. Wersja 2 jest warunkowa: obok sekwencji dostaje na każdym etapie warunek biologiczny, z katalogu albo z enkodera zbudowanego na własnym eksperymencie jednokomórkowym badacza.

DeepMind podaje trening na ponad **100 mln** profili pojedynczych komórek, a w innym zdaniu na ponad **107 mln**, z **68** tkanek, na danych ludzkich i mysich, zbiorczych i jednokomórkowych. Model przewiduje ekspresję genów, modyfikacje histonów, dostępność chromatyny i metylację DNA. Na zbiorze TenK10K, 28 pierwotnych typów komórek odpornościowych, DeepMind podaje prawie dwa razy więcej wariantów przyczynowych (**30%** wobec **16%**) i kierunkowych efektów genowych (**43%** wobec **23%**) niż oryginalny AlphaGenome dotrenowany na danych jednokomórkowych i inne wyspecjalizowane narzędzia.

Dostęp: API AlphaGenome do badań niekomercyjnych oraz prywatny podgląd badań komercyjnych w Google Cloud. Zapowiedziane są Skills w Antigravity. DeepMind pisze wprost, że AlphaGenome i AlphaGenome 2 są przeznaczone wyłącznie do badań i nie zostały zwalidowane ani dopuszczone do użytku klinicznego albo diagnostycznego.

**Źródła:**

- [Google DeepMind — AlphaGenome 2, 11.11.2026](https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/)

#### Gemini Decision 1 (11 listopada 2026)

**11 listopada 2026** Google wprowadza **Gemini Decisions API** i model `gemini-decision-1`. To osobny endpoint decyzji domkniętych, nie model ogólny i nie Decisions API OpenAI opisywane w przeglądzie z 28 października.

Jedno wejście multimodalne — tekst, obraz, audio, wideo albo PDF, do **256 tys.** tokenów — można połączyć z nawet **1000** niezależnymi pytaniami. Model ocenia opcje w jednym przebiegu, bez generowania odpowiedzi token po tokenie. Google podaje opóźnienie **150–250 ms** od końca do końca i **50–100 ms** samego liczenia modelu, prawie płaskie od 1 do 100 pytań przy kontekście do 16 tys. tokenów. Cena: **0,10 USD** za 1 mln tokenów wejścia i **0 USD** za wyjście. Wspólne wejście jest liczone raz na żądanie. Jest poziom bezpłatny do prototypów w AI Studio.

Trzy typy pytań ze wpisu: tak/nie (w przykładowym kodzie pole `noul`), wybór od 2 do 255 opcji oraz ocena na uporządkowanej rubryce. Każda odpowiedź ma pewność od 0 do 1. Integracje wymienione przy starcie: OpenRouter, LangChain, Vercel, LiteLLM, Pydantic AI, Pipecat, LiveKit i OpenCode oraz SDK `google-genai`. Wsparcie w Gemini w Google Cloud jest zapowiedziane.

**Źródła:**

- [Google — Gemini Decisions API, 11.11.2026](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/)

#### Runway Praxis-1, otwarte wagi (11 listopada 2026)

**11 listopada 2026** Runway udostępnia wagi **Praxis-1** na licencji Apache 2.0, także do użytku komercyjnego. Sam model został przedstawiony we wrześniu. Nowością tego ogłoszenia są wagi, kod inferencji i dotrenowania, w tym LoRA, oraz trzy punkty kontrolne na Hugging Face: wersja dotrenowana na DROID, wersja dotrenowana na dwuramiennym YAM i model po treningu pośrednim.

Runway opisuje Praxis-1 jako transformer dyfuzyjny MoE o **27 mld** parametrów, który przewiduje wideo i akcje razem. Na RoboLab-120 podaje **46,2%** sukcesu na **1200** epizodach, wobec **42,9%** dla FLUX 3 Action, **36,8%** dla Cosmos3 Nano i **28,0%** dla π0.5. Wpis badawczy dodaje, że jedno wywołanie zwraca **1,6 sekundy** akcji: 24 wiersze przy 15 Hz. Partnerzy startu wymienieni we wpisie o wagach: Noble Machines, Standard Bots i Ultra. Dystrybucja: GitHub, Hugging Face z LeRobot, vLLM-Omni i hosting Reactor. Sprzęt wymieniony we wpisie: od H100 i B200 przez RTX 5090 i RTX PRO 6000 po Jetson Thor.

**Źródła:**

- [Runway — Praxis-1 Is Now Available, 11.11.2026](https://runway.com/news/company-news/praxis-1-is-now-available)
- [Runway Research — Praxis-1: From Video Pretraining to Robot Control, listopad 2026](https://runway.com/research/praxis-1-video-pretraining-to-robot-control)

#### PAN 2 (komunikat IFM z 10 listopada 2026)

Instytut Foundation Models przy MBZUAI datuje komunikat o **PAN 2** na **10 listopada 2026** (Sunnyvale). Depesza agencji WAM nosi datę **11 listopada 2026**. Poranny przegląd z 11 listopada tego wydania nie odnotował. Model jest ogólnym modelem świata: ze sceny i akcji opisanej słowami generuje wideo tego, co stanie się dalej. IFM wydaje wagi, pełny kod treningu i inferencji oraz dokumentację na licencji Apache 2.0.

README repozytorium `ifm-ai/PAN2` podaje **29,2 mld** parametrów, architekturę GLP, enkoder tekstu Qwen3.5-9B i do **20 sekund** wideo przy 704×1248 i 24 klatkach na sekundę. Komunikat IFM: na sześciu wymiarach fizycznych PAN 2 tuż za MiniMax-H3 i przed czterema innymi modelami; w planowaniu wieloetapowym ukończył więcej pełnych planów niż pozostałe testowane modele; na Physics-IQ Verified trzecie miejsce ogółem i pierwsze wśród modeli z otwartymi wagami.

**Źródła:**

- [IFM — komunikat PAN 2, 10.11.2026](https://ifm.ai/pan2/press-release/)
- [MBZUAI — komunikat PAN 2, 11.11.2026](https://mbzuai.ac.ae/news-events/news/the-institute-foundation-models-unveils-pan-2-open-world-model-physical)
- [WAM — depesza z 11.11.2026](https://www.wam.ae/en/article/c37a8kv-mbzuai-launches-open-source-pan-model-simulate)
- [GitHub — ifm-ai/PAN2](https://github.com/ifm-ai/PAN2/)

### 1.5. Google Research: wyniki `/teamwork` (13 listopada 2026)

**13 listopada 2026** Vahab Mirrokni opisuje wyniki wieloagentowego systemu **Antigravity `/teamwork`**. Wpis mówi, że prace trwały kilka tygodni i używały Gemini 4 Argon, Carbon i Hydrogen. Hydrogen był więc w tych biegach dostępny zespołom Google co najmniej w dniu publicznego ogłoszenia modelu albo wcześniej. Wpis nie rozdziela, który wynik powstał na którym modelu.

Najczytelniej opisany wynik matematyczny: zespoły Google, CUHK, USC i CMU, we wzorcu Long Proof, podają dowód hipotezy Courtade’a–Kumara z 2013 roku w pełnej ogólności oraz formalizację całego dowodu w Lean 4, **50 mln** linii. Wpis opisuje też kontrprzykłady do wcześniejszej, szerszej hipotezy zespołu CUHK i redukcję do optymalizacji na 14 zmiennych. Tego przeglądu nie poprzedza lektura preprintu ani repozytorium Lean. Zdanie powyżej jest relacją z wpisu Google.

Ten sam wpis wymienia długą listę dalszych formalizacji i algorytmów, w tym adaptacyjną analizę danych, mnożenie macierzy boolowskich i formalizacje twierdzeń geometrycznych oraz analitycznych. Osobno podaje, że narzędzie Deep Review, jako wzorzec przeglądu dokumentu, było dobrowolnie użyte przez autorów **578** zgłoszeń na STOC 2027, a w ankiecie **70** autorów **90%** uznało uwagi za w większości albo niemal w całości faktualne. Ankieta jest w toku. Wzorce `/teamwork`, obok `/boost`, mają być dostępne w Antigravity. Wpis zastrzega, że część funkcji jest już dostępna, a kolejne aktualizacje dla użytkowników zewnętrznych przyjdą w następnych tygodniach.

**Źródła:**

- [Google Research — Advancing science and engineering with Antigravity’s /teamwork, 13.11.2026](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/)

### 1.6. DeepSeek: funkcje aplikacji w API (13 listopada 2026)

**13 listopada 2026** changelog DeepSeek API otwiera deweloperom funkcje, które dotychczas składały się na rozmowę w aplikacji DeepSeek. Dla modelu `deepseek-flash`, w API Messages, Responses i Chat Completions, changelog wymienia: wyszukiwanie w sieci, wyszukiwanie z włączonym myśleniem i samodzielnym czytaniem linków, wejście plików po ekstrakcji tekstu albo parsowaniu układu, czytanie adresów URL narzędziem `deepseek_read_url` oraz parametr kontroli bezpieczeństwa, który przegląda wejście i wyjście i zwraca znacznik odmowy. Osobno jako samodzielne API: Search and Fetch, OCR, ASR i TTS. Changelog odsyła ceny do strony Models & Pricing. Tego cennika ten przegląd osobno nie rozpisuje. Wpis z 13 listopada nie jest nową rodziną modeli. Aktualizacja wag DeepSeek-V4.1-Flash-1017 pozostaje poza tym podsumowaniem.

**Źródła:**

- [DeepSeek API — changelog, 13.11.2026](https://api-docs.deepseek.com/updates/?date=2026-11-13&id=releasing-the-full-suite-of-application-apis)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

Tydzień w sądach jest tygodniem odpowiedzialności za cytowania. **12 listopada** Sąd Najwyższy Apelacji Wirginii Zachodniej uchyla zakończenie praw rodzicielskich z powodów proceduralnych i w przypisie przekazuje dyscyplinarnemu rzecznikowi brief z fikcyjnym punktem sylabusa. **13 listopada** wicekanclerz Delaware nakłada 2500 USD na wspólnika, który wpuścił do briefu niezweryfikowany wynik narzędzia generatywnego, i zwalnia kancelarię, która miała politykę i szkolenia. Tego samego dnia kalifornijski sąd apelacyjny, w orzeczeniu niepublikowanym, widzi zmyślone cytaty i odmawia sankcji z urzędu, bo strona przeciwna nie złożyła wniosku. **16 listopada** w Senacie Nowego Jorku pojawia się projekt, który świadome albo lekkomyślne wpuszczenie zmyślonego prawa do pisma sądowego sędziego uznaje za przewinienie służbowe. **17 listopada** OpenAI rozszerza dostęp do konfiguracji Astra for Law. W Polsce **16 listopada** upływa termin naboru do Społecznej Rady; tego dnia NSZZ „Solidarność” publikuje zgłoszenie kandydata. Składu Rady ten przegląd nie znajduje.

### 2.1. Delaware: 2500 USD dla wspólnika, kancelaria bez sankcji (13 listopada 2026)

**13 listopada 2026** wicekanclerz Lori W. Will z Court of Chancery Delaware rozstrzyga pismem sprawę **Kevin Leiske et al. v. Robert Gregory Kidd et al.**, C.A. No. 2025-0426-CDW (LWW). Pismo zamyka order to show cause z **1 lipca 2026** w sprawie nadużycia generatywnej AI. Meritum sporu o advancement wicekanclerz rozstrzygnęła wcześniej, **2 lutego 2026**, i zatrzymała jurysdykcję tylko co do błędów w briefie.

Fakty z pisma. **22 stycznia 2026** powodowie złożyli answering brief wobec wyjątków od raportu magistrata. Pięć dni później pełnomocnicy pozwanych wskazali zmyślone cytaty, wadliwe powołania i zmyślone tezy prawne. **28 stycznia** podpisujący brief przyznał, że narzędzie generatywne poprawiało tekst, i złożył brief poprawiony. Cudzysłowy wokół nieistniejących cytatów zniknęły. Nietrafne omówienia orzeczeń zostały. **29 stycznia** ten sam pełnomocnik zarzucił stronie przeciwnej brak meet and confer i twierdził, że powołane źródła są prawdziwe i wspierają argument.

Zaprzysiężone wyjaśnienia, które pismo przyjmuje: Richard Rollo, przewodniczący podkomisji AI w Richards, Layton & Finger, w pilotażu użył **Perplexity Enterprise**, narzędzia niedopuszczonego do ogólnego użytku w kancelarii, żeby pomóc napisać i skrócić argumenty. Potem oddał sprawdzenie cytatów młodszemu prawnikowi i paralegalowi i złożył brief bez osobistego sprawdzenia źródeł. Paul N. Heath złożył affidavit w imieniu kancelarii.

Rozstrzygnięcie:

- Użycie generatywnej AI w praktyce prawniczej pismo nazywa dozwolonym. Obowiązkiem pozostaje reguła 11 Court of Chancery i delawareńskie zasady etyki: podpis jest poświadczeniem, że tezy prawne mają oparcie w istniejącym prawie po rozsądnym sprawdzeniu. Zmyślony cytat albo synteza wygenerowana przez algorytm tym prawem nie są.
- Obowiązek jest osobisty. Nie zwalnia go to, że powołane sprawy istnieją, ani to, że ogólna teza strony dałaby się obronić na prawdziwych źródłach. Zdjęcie cudzysłowu przy zostawieniu fałszywej syntezy nie wystarcza. Zarzut braku meet and confer przed zawiadomieniem sądu o fałszywych cytatach pismo odrzuca.
- Reguła 11 co do zasady obciąża kancelarię solidarnie. Tu sąd kancelarii nie sankcjonuje. Dyrektorzy przyjęli politykę generatywnej AI, która wymaga sprawdzenia wyniku przez doświadczonego prawnika i zakazuje zastępowania nią własnego osądu. Było szkolenie o halucynacjach, opinii ABA Formal Opinion 512 oraz o obowiązkach kompetencji, poufności, rzetelności, szczerości i nadzoru. Zabezpieczenia działały przed złożeniem briefu. Wspólnik je obszedł.
- Rollo płaci osobiście **2500 USD** na rzecz Court of Chancery w ciągu **14 dni** i składa affidavit o zapłacie. Kwoty nie pokrywa kancelaria. Dodatkowego szkolenia sąd nie nakłada: pełnomocnik prowadzi szkolenia wewnętrzne i odbył kursy etyki AI. Wniosek strony przeciwnej o dopuszczenie billingów sąd oddala. Przy sankcji z urzędu reguła 11 nie przewiduje zwrotu kosztów pełnomocnikom.

Pismo porównuje kwotę z innymi sankcjami z urzędu, w tym z *Gill v. Everyday Dose, Inc.*, 2026 WL 3390881 (D. Del. 9 listopada 2026), gdzie sąd nałożył po 3000 USD na dwóch pełnomocników. Tamta sprawa jest przywołana jako punkt odniesienia. Ten przegląd jej osobno nie relacjonuje.

**Źródła:**

- [Court of Chancery of Delaware — pismo z 13.11.2026, Leiske v. Kidd, C.A. No. 2025-0426-CDW (LWW)](https://www.courts.delaware.gov/opinions/download.aspx?id=403420)

### 2.2. Wirginia Zachodnia: uchylenie zakończenia praw rodzicielskich i sygnał dyscyplinarny (12 listopada 2026)

**12 listopada 2026** Sąd Najwyższy Apelacji Wirginii Zachodniej wydaje opinię w sprawie **In re A.S., R.S.-1, and L.S.**, nr 25-425. Apelacja pochodzi z Circuit Court of Brooke County, sędzia Jason A. Cuomo, sygnatury CC-05-2023-JA-24, CC-05-2023-JA-25 i CC-05-2023-JA-28. Rozprawa apelacyjna: 22 września 2026. Sentencja: **VACATED AND REMANDED WITH DIRECTIONS**.

Meritum jest proceduralne i nie zależy od kwestii AI. Sąd stwierdza, że sąd okręgowy w istocie wyłączył skarżących, którzy zachowali prawa rodzicielskie, z postępowania po pierwszym rozstrzygnięciu, a potem zakończył te prawa bez procedury wymaganej przy nowym sposobie rozstrzygnięcia. Podstawą jest między innymi nowy punkt sylabusa z *In re P.F.* Sąd używa inicjałów, bo sprawa dotyczy małoletnich. Ten przegląd nie dodaje faktów o rodzinie.

Kwestia AI jest w przypisie 12. Sąd pisze, że rozpoznanie zarzutów utrudniły nietrafne powołania ustaw, reguł i orzeczeń, w tym **zmyślony punkt sylabusa** i **fikcyjne cytaty**. Inne sądy uznawały podobne anomalie za wskazówkę, że pismo przygotowano z generatywną AI. Sąd przywołuje Legal Ethics Opinion 24-01 z 14 czerwca 2024: prawnik ma obowiązek upewnić się, że produkt AI jest dokładny i kompletny, a zasady 5.1 i 5.3 obejmują nadzór nad osobami pomagającymi w usłudze prawnej, „whether human or not”. Przypis przypomina, że prawnik osobiście sprawdza każdy cytat, cytat dosłowny i zdanie o prawie. Technologii nie odrzuca. Przy wyglądzie naruszenia zasad etyki przekazuje sprawę do Office of Disciplinary Counsel i każe kanclerzowi wysłać uwierzytelniony odpis opinii. W tym samym zdaniu sąd pisze, że nie wyraża poglądu, czy postępowanie dyscyplinarne powinno się zacząć i jak ma się skończyć.

**Źródła:**

- [Supreme Court of Appeals of West Virginia — opinia nr 25-425, złożona 12.11.2026](https://www.courtswv.gov/sites/default/pubfilesmnt/2026-11/25-425%20Signed%20Opinion.pdf)

### 2.3. Kalifornia: niepublikowane Boktor v. Boktor, sankcji z urzędu nie nałożono (13 listopada 2026)

**13 listopada 2026** Second Appellate District, Division Seven, składa niepublikowaną opinię **Boktor v. Boktor**, nr B339436. Apelacja od wyroku Superior Court of Los Angeles County, sędzia Michael Small, sygnatura 18SMCV00223. Skład: Presiding Justice Gonzalo C. Martinez oraz sędziowie Feuer i Stone. Pełnomocnik skarżącej w nagłówku: Tahmazian Law Firm i Jilbert Tahmazian. Sentencja: wyrok oddalający powództwo utrzymany. Strona wygrywająca dostaje koszty apelacji.

Opinia nosi klauzulę, że nie podlega publikacji w Official Reports. California Rules of Court, reguła 8.1115(a), co do zasady zakazuje powoływania się na takie orzeczenie. Poniższe streszczenie służy odnotowaniu zdarzenia, nie jako cytat do pisma procesowego.

W części o nieprawidłowych cytatach respondenci twierdzą, że pełnomocnik skarżącej użył generatywnej AI do fragmentu o doręczeniu przez ogłoszenie, bo żadna z czterech spraw tam powołanych nie istnieje. Sąd odmówił zgody na wniesienie poprawionego briefu otwierającego. W odpowiedzi pełnomocnik przyznaje, że sprawy są niewłaściwe, i opisuje to jako przeoczenie oraz wybaczalne zaniedbanie. Zaprzecza, by „podpisał się” pod sztuczną inteligencją. Przyznaje, że zewnętrzny paralegal wykonywał pracę typu law and motion, a staff attorney nie sprawdzał spraw powołanych w projektach briefu. Pełnomocnik pisze, że nie wie, jak nieprawidłowości powstały, i wskazuje nawał pracy. Osobno sąd nie znajduje sprawy *Reid & Hellyer v. Laski* (1924) 193 Cal. 512, powołanej przy tezie o ścisłym dochowaniu przepisów o zawiadomieniu w sprawach spadkowych. Pełnomocnik przyznaje też przekłamanie zdania z *Munoz v. Lopez*.

Respondenci nie wnoszą o sankcje z reguły 8.276(b), która wymaga między innymi deklaracji o wysokości żądanej kwoty. Sąd nazywa powoływanie zmyślonych źródeł w briefie apelacyjnym sprawą poważną i przywołuje sprawy, w których inne składy nakładały sankcje, w tym *Noland v. Land of the Free, L.P.* z sankcją 10 000 USD. W okolicznościach tej sprawy sankcji z urzędu nie nakłada. Reguły 8.276(a) i (c).

Sąd nie zapisuje ustalenia, że narzędzie AI napisało brief. Zapisuje argument respondentów, zaprzeczenie pełnomocnika i własną ocenę, że w briefie są zmyślone źródła.

Tekst opinii odczytano z reprodukcji slip opinion. Strona oficjalna Judicial Branch podaje sprawę, datę i status niepublikowany oraz odsyła do PDF i DOCX.

**Źródła:**

- [Judicial Branch of California — Boktor v. Boktor, B339436, złożone 13.11.2026, niepublikowane](https://courts.ca.gov/opinion/unpublished/2026-11-13/b339436)
- [Reprodukcja slip opinion, z której odczytano tekst](https://cases.laws.com/news/law/court-affirms-dismissal-of-boktor-family-probate-dispute-11061385/)
- [Metropolitan News-Enterprise, 17.11.2026 — omówienie wtórne](http://www.metnews.com/articles/2026/nosanctions_111726.htm)

### 2.4. Nowy Jork: projekt o zmyślonych źródłach w pismach sędziów (16 listopada 2026)

**16 listopada 2026** senator Michelle Hinchey wnosi do Senatu stanu Nowy Jork projekt **S10741**. Tytuł skrócony: „judicial artificial intelligence accountability and integrity act”. Projekt czytano dwukrotnie i skierowano do Committee on Rules. W chwili odczytu 18 listopada LegiScan oznacza status jako „Introduced - Dead” przy dacie skierowania 16 listopada. Tekst projektu sam zapisuje skierowanie do Rules. Ten przegląd nie rozstrzyga, czy etykieta LegiScan oznacza koniec sesji 2025–2026, czy inną klasyfikację. Projekt nie jest ustawą.

Proponowany § 44-a ustawy o sądownictwie:

- „Fabricated legal authority” obejmuje rzekomą konstytucję, ustawę, rozporządzenie, orzeczenie sądowe albo administracyjne, cytat, tezę, powołanie, sygnaturę albo inne źródło prawa, które nie istnieje, albo którego istnienie, tekst, teza, cytat, sąd, moc precedensu albo dalsze losy są istotnie i fałszywie przedstawione.
- Pismo orzecznicze to opinia, postanowienie, decyzja, wyrok, memorandum, pisemne rozstrzygnięcie albo inny dokument wydany albo przyjęty przez sędziego w czynnościach orzeczniczych.
- Sędzia, który świadomie albo lekkomyślnie włącza, opiera się albo przyjmuje istotne zmyślone źródło prawa w takim piśmie, dopuszcza się przewinienia służbowego i zachowania szkodliwego dla wymiaru sprawiedliwości. „Świadomie” i „lekkomyślnie” mają znaczenie z § 15.05 prawa karnego.
- Samo użycie sztucznej inteligencji przewinieniem nie jest.
- Ustalenia przewinienia nie wolno oprzeć wyłącznie na dobrej wierze przy prawie nieustalonym, na nieistotnym błędzie pisarskim albo w formacie cytatu, na późniejszej zmianie źródła bez poważnej szkody albo na nieumyślnym i nieistotnym błędzie szybko poprawionym bez poważnej szkody.
- Komisja orzecznicza, wymierzając sankcję, ma uwzględnić liczbę i wagę źródeł, skutek dla strony albo rozstrzygnięcia, procedury weryfikacji, wcześniejsze szkolenie o ryzyku AI, powtarzalność i to, czy sędzia szybko poprawił błąd.
- Po publicznym stwierdzeniu przewinienia komisja może nałożyć sankcje z art. VI § 22 konstytucji stanowej albo przekazać ustalenie spikerowi Zgromadzenia jako sygnał do rozważenia impeachmentu z art. VI § 24.

Vacatio legis: sto osiemdziesiąty dzień po wejściu ustawy w życie, i tylko do zachowań od tej daty.

**Źródła:**

- [LegiScan — tekst S10741, wniesiony 16.11.2026](https://legiscan.com/NY/text/S10741/id/3466208)
- [LegiScan — karta S10741](https://legiscan.com/NY/bill/S10741/2025)

### 2.5. OpenAI: Astra for Law na GPT-6.2, szerszy dostęp (17 listopada 2026)

**17 listopada 2026** OpenAI publikuje aktualizację **Astra for Law**. Wprowadzenie tej konfiguracji we wrześniu, dla wąskiej grupy kancelarii, pozostaje poza tym przeglądem. Nowością jest przejście na GPT-6.2 Astra i otwarcie wniosku o dostęp dla każdego klienta ChatGPT Enterprise.

Wpis: Astra for Law jest konfiguracją GPT-6.2 Astra z rozszerzonym indeksem wyszukiwania prawnego i instrukcjami badania pytania, ważenia źródeł i pisania odpowiedzi. Identyfikator w ChatGPT dla zespołów, które już mają dostęp: `gpt-6.2-astra-law`. Wniosek idzie przez Trusted Access Program w konsoli administratora. Osobno można prosić o dostęp przez API. Artykuł pomocy odczytany tego samego dnia nadal otwiera opis zdaniem, że Astra for Law jest dostosowanym GPT-6 Astra i że indeks obejmuje amerykańskie orzecznictwo, ustawy, regulacje, regulaminy sądowe i decyzje administracyjne. Nowszy jest wpis z 17 listopada. Artykuł pomocy podaje ograniczenie, którego wpis premierowy w odczytanym fragmencie nie powtarza: z narzędzia mogą korzystać prawnicy i osoby pracujące pod ich nadzorem, po autoryzacji przestrzeni.

Liczby ze wpisu z 17 listopada. To pomiary, które OpenAI przypisuje Harveyowi, Artificial Analysis i Vals AI:

- LAB-AA, wersja Artificial Analysis benchmarku Harveya: 120 zadań z 24 dziedzin prawa. Pełne zaliczenie wymaga spełnienia każdego warunku i braku istotnej halucynacji. Astra for Law: **20,8%**. GPT-6.2 Astra bez tej konfiguracji: **15,0%**. Muse Wonder Full: **13,1%**. Średnio około **64 tys.** tokenów wyjścia na zadanie wobec **139 tys.** dla Muse Wonder Full.
- Istotne halucynacje na tym samym zestawie: **0,03** na zadanie dla Astra for Law, remis z GPT-6 o najniższy wynik w porównaniu, wobec **0,06** dla zwykłej GPT-6.2 Astra i **0,59** dla Claude Opus 5.5. Drobne: **0,06** wobec **0,51** dla Opus 5.5. Wpis podaje, że w zadaniach z pełnym zaliczeniem konfiguracja nie miała istotnych halucynacji.
- Własny LAB Harveya, osobny od LAB-AA: pełne zaliczenie **4,6%** dla GPT-6 Astra, **14,6%** dla GPT-6.2 Astra i **16,2%** z konfiguracją prawniczą.
- Vals AI Legal Research Bench, ocena z **16 listopada**: pełne zaliczenie **112 z 208** pytań, czyli **53,8%**, wobec około **46%** we wrześniu. Z punktami częściowymi: **90,9%** dostępnych punktów. Pytania układają praktykujący prawnicy o prawie federalnym i stanowym USA.
- Indeks od września urósł o **34%**, o ponad **80 mln** adresów URL, w tym z Wielkiej Brytanii, Australii i Kanady. Wpis podaje ponad **310 mln** adresów i pokrycie ponad **99,9%** opublikowanego amerykańskiego orzecznictwa precedensowego.

Wynik **55,8%** na Vals Legal Research Bench, który Google podaje dla Gemini 4 Hydrogen w części 1.2, pochodzi z innego wpisu i ten przegląd nie ustala, czy licznik jest tym samym co 53,8% pełnych zaliczeń u OpenAI. Tych dwóch liczb nie składam w jedno zestawienie.

Cytat Julio Pereyry z Harveya, przytoczony przez OpenAI: briefy Astra for Law 6.2 były w porównaniach parami wybierane nad briefami GPT-6 Astra w prawie **90%** przypadków, bez regresu dokładności, którą Harvey przypisuje klasie Astra na LAB.

**Źródła:**

- [OpenAI — Astra for Law leads in legal intelligence, 17.11.2026](https://openai.com/index/astra-law-6-2/)
- [OpenAI Help Center — Astra for Law, odczyt 18.11.2026](https://help.openai.com/en/articles/20001528-astra-for-law)

### 2.6. Polska: termin naboru do Społecznej Rady i zgłoszenie NSZZ „Solidarność” (16 listopada 2026)

Nabór do Społecznej Rady do spraw Sztucznej Inteligencji był już opisany w przeglądzie z 11 listopada. Tu tylko domknięcie terminu. Komunikat Komisji Rozwoju i Bezpieczeństwa Sztucznej Inteligencji na gov.pl nadal podaje, że zgłoszenia przyjmowane są do **16 listopada 2026**, a decyduje data wpływu. Rada, z art. 45–47 ustawy z 3 lipca 2026 r. o systemach sztucznej inteligencji (Dz.U. poz. 1003), ma liczyć od 9 do 15 osób i działać jako organ opiniodawczo-doradczy Komisji. Tego przeglądu nie poprzedza komunikat Komisji o powołaniu składu ani o wynikach naboru. Strona „Informacje bieżące” w odczycie z 18 listopada nadal zapowiada nabór do 16 listopada i nie podaje listy członków.

**16 listopada 2026** Prezydium Komisji Krajowej NSZZ „Solidarność” publikuje decyzję nr **131/26**. Treść ogłoszenia: Prezydium zgłasza kandydaturę Łukasza Mickiewicza do Społecznej Rady do spraw Sztucznej Inteligencji. Jest to akt podmiotu zgłaszającego. Nie jest powołaniem w skład Rady.

**Źródła:**

- [KRiBSI — nabór do Społecznej Rady, termin 16.11.2026](https://www.gov.pl/web/kribsi/rusza-nabor-do-spolecznej-rady-do-spraw-sztucznej-inteligencji)
- [KRiBSI — informacje bieżące, odczyt 18.11.2026](https://www.gov.pl/web/kribsi/informacje-biezace)
- [NSZZ „Solidarność” — decyzja Prezydium KK nr 131/26, 16.11.2026](https://www.solidarnosc.org.pl/dok/2026/11/16/decyzja-prezydium-kk-nr-131-26-ws-zgloszenia-kandydata-do-spolecznej-rady-do-spraw-sztucznej-inteligencji/)

---

## Czego w tym przeglądzie świadomie nie ma

Przemówienie prezesa Sądu Najwyższego Bangladeszu Zubayera Rahmana Chowdhury’ego o tym, że wyroku nie pisze się przy pomocy AI, jest w Dhaka Tribune i BD Global Times datowane na **29 sierpnia 2026**. Tekst z datą 14 listopada 2026 powtarza tę samą relację. Do okna 11–18 listopada nie wchodzi.

Poprawki Siân Berry o zakazie decyzji imigracyjnych i azylowych wspieranych przez AI, które przetwarza dane osobowe osoby, której decyzja dotyczy (NC37 i NC38), stoją w papierach **committee stage z 14 października 2026**. To nie jest zdarzenie tego tygodnia.

Nie wracam do spraw i komunikatów już opisanych 11 listopada: raportu Lady Chief Justice z 5 listopada, przemówienia mrs Justice Smith z 6 listopada, niepublikowanego *Gillespie*, relacji Bloomberga o sędzim Meredith z 9 listopada, wystąpienia sędziego Leonena z 4 listopada ani pierwszego posiedzenia polskiej Komisji z 28 października.
