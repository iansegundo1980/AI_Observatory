# Tygodniowy przegląd AI — 28 października 2026

**Okres objęty podsumowaniem:** 21–28 października 2026
**Data publikacji podsumowania:** 28 października 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach wdrażanych w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **14–21 października 2026** i powstał rano 21 października. Niniejszy dokument go nie powtarza: nie wraca do wag Muse Spark Open, Nemotron 3.5 Super VL i Bolt 74B-A9B, wag Beam 1.0, DeepSeek-V4.1-Flash-1017 i DeepInfer, wpisu w Federal Register o produktach DeepSeek, MiniMax M3.1 Flash, Voxtral 3, listu intencyjnego NSA i Ministerstwa Cyfryzacji, materiałów Canadian Judicial Council, raportu sądów Idaho, obowiązków Fair Work Commission, studium NAO o Justice Transcribe, pozwów ośmiu stanów przeciwko OpenAI, orzeczenia *Stacia Davis v. Robert York* ani oddalenia wisconsińskiej petycji 26-02. Wydarzenie z 21 października, którego tamten przegląd nie ujął, jest tu opisane z jawną datą.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z wpisu premierowego, karty modelu albo dokumentacji API. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru i harnessy się nie pokrywają.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Tydzień przynosi szybszy model do pracy przy komputerze od OpenAI, flagowy model Moonshot zapowiedziany jako otwartowagowy, ale jeszcze bez wag, badawczy model świata DeepMind oraz mały model brzegowy NVIDIA, który poprzedni przegląd odnotował tylko jako zapowiedź na 23 października. Wagi Mistral Large 4 w dniu tego przeglądu nadal nie leżą w repozytorium.

### 1.1. OpenAI: GPT-6.1 Terra (26 października 2026)

**26 października 2026** OpenAI udostępniło **GPT-6.1 Terra**. Changelog API z tego dnia opisuje wydanie modelu `gpt-6.1-terra` w `v1/responses` i `v1/chat/completions`. Dodatek do karty systemu GPT-6 Astra nosi datę publikacji **26 października 2026**. Strona premierowa samego wpisu nie drukuje daty dziennej; datę dnia bierze się z changelogu i z karty.

Terra jest modelem do rozumowania wizualnego, obsługi komputera i pisania. Wejście: tekst i obraz. Wyjście: tekst. Okno kontekstu **1 050 000** tokenów, maksymalnie **922 000** tokenów wejścia i **128 000** tokenów wyjścia. Odcięcie wiedzy: **1 czerwca 2026**. Wysiłek rozumowania: `none`, `low`, `medium` (domyślnie), `high`, `xhigh` i `max`. Wywołania narzędzi wymagają Responses API. To model zamknięty, dostępny w produktach i w API, bez publikacji wag.

Cennik standardowego API: **1 USD** za 1 mln tokenów wejściowych, **0,05 USD** za 1 mln tokenów wejściowych z cache i **5 USD** za 1 mln tokenów wyjściowych. OpenAI pisze, że te stawki są o **50%** niższe niż u GPT-5.6 Terra i GPT-6.1 Sol. Od dnia premiery model jest dla użytkowników Plus, Pro, Enterprise i Edu w ChatGPT Work i w Codex oraz dla deweloperów w API.

Liczby z wpisu premierowego, wszystkie vendorskie:

| Zadanie | Co podaje OpenAI |
| --- | --- |
| Agents’ Last Exam, średni wysiłek | 15 punktów procentowych powyżej GPT-5.6 Terra, przy około jednej trzeciej kosztu; na poziomie GPT-6 Astra przy jednej dziesiątej ceny za token |
| Ten sam benchmark, maksymalny wysiłek | ponad trzykrotnie wyższa efektywność tokenowa niż Claude Opus 5.5 i jedna czwarta ceny za token; około 9× niższy koszt zadania; zadania kończone ponad trzykrotnie szybciej niż GPT-6 Astra i GPT-6.1 Sol |
| Wewnętrzny zbiór promptów wywołujących błędy | przy niskim wysiłku wskaźnik błędu spada z 53,6% (GPT-5.6 Terra) do 16,7%; przy maksymalnym wysiłku spadek o 18 punktów procentowych, do 4,3% |
| Terminal-Bench 4.0, maksymalny wysiłek | 50,3% zadań; opublikowany wynik GPT-5.6 Terra to 21,5% |

OpenAI samo pisze, że przy najtrudniejszym kodzie lepszym wyborem pozostają GPT-6.1 Sol i GPT-6 Astra. Terminal-Bench-Science 0.1, według wpisu, stawia Terrę przy maksymalnym rozumowaniu powyżej GPT-6.1 Sol i w odległości pięciu punktów od Opus 5.5, przy mniej niż jednej piątej szacowanego kosztu. Procentów MMMU-Pro i OSWorld 2.1 wpis nie podaje w tekście; są tam tylko porównania jakości i kosztu.

Bezpieczeństwo, z dodatku do karty: w Preparedness Framework Terra jest traktowana jako **Critical** w cyberbezpieczeństwie oraz **High** w zdolnościach biologicznych i chemicznych. Stos chroniący jest ten sam co przy GPT-6.1 Sol i GPT-6 Astra, z sondami dostosowanymi do modelu. Szczegóły metod ewaluacji siedzą w karcie GPT-6 Astra i w dodatku. Ten przegląd nie streszcza scenariuszy tych testów.

Tego samego tygodnia, **22 października 2026**, changelog API zapisuje osobną zmianę produktową: **Decisions API** przechodzi z publicznej bety do ogólnej dostępności z modelem `gpt-6-luna`. Jedno żądanie obsługuje do **400** pytań, wcześniej w becie 200. Cache współdzielonego wejścia, obrazy w instrukcjach poszczególnych pytań i dane strukturalne przez `input_json` są w opisie tej zmiany. Sam model Luna pochodzi ze wcześniejszego okna i nie jest tu opisywany jako nowa premiera.

**Źródła:**

- [OpenAI — Introducing GPT-6.1 Terra](https://openai.com/index/introducing-gpt-6-1-terra)
- [OpenAI API changelog, wpis z 26.10.2026 i z 22.10.2026](https://developers.openai.com/api/docs/changelog)
- [Dokumentacja modelu gpt-6.1-terra](https://developers.openai.com/api/docs/models/gpt-6.1-terra)
- [Dodatek do karty systemu GPT-6 Astra: GPT-6.1 Terra, publikacja 26.10.2026](https://deploymentsafety.openai.com/gpt-6-1-terra)

### 1.2. Moonshot: Kimi K3.1 Pro i Highspeed (wpis zaktualizowany 24 października 2026)

Moonshot wypuściło **Kimi K3.1 Pro** i szybszy wariant **Kimi K3.1 Pro Highspeed**. Chiński wpis produktowy ma stopkę **„更新于：2026-10-24”** (zaktualizowano 24 października 2026). Artificial Analysis datuje swój pomiar na **23 października 2026**. Angielski wpis techniczny na `kimi.ai/blog` w tekście odczytanym do tego przeglądu nie niesie osobnej daty dziennej. Okno premiery to 23–24 października. Wagi w dniu startu nie wyszły.

Oba oficjalne wpisy nazywają K3.1 Pro najsilniejszym modelem firmy w klasie **3 bln** parametrów, z oknem **1 mln** tokenów. To post-trening Kimi K3, z większym nakładem obliczeń na uczenie ze wzmocnieniem. Strona główna platformy API dodaje, że model natywnie obsługuje rozumienie obrazu. Rozbicia na parametry aktywne Moonshot w tych wpisach nie podaje. Artificial Analysis zapisuje **2,8 bln** parametrów łącznie i **104 mld** aktywnych oraz wejście tekstowe i obrazowe. To opis strony pomiarowej, nie zdanie z wpisu Moonshot. Pełne wagi mają się ukazać **do 4 listopada 2026**. Do tego przeglądu zapowiedź pozostaje zapowiedzią.

Highspeed, według wpisu produktowego i technicznego, ma tę samą inteligencję przy prędkości wyjścia około **2–3×**. Strona platformy API pisze o prędkości około **3×**. To dwie formuły tej samej firmy; przegląd ich nie uśrednia.

Kanały od dnia startu: kimi.com, aplikacja (iOS, Android, HarmonyOS), Kimi Work (desktop **3.1.0** lub nowszy, Windows i Apple silicon), Kimi Code oraz API pod identyfikatorami `kimi-k3.1-pro` i `kimi-k3.1-pro-highspeed`. Dla kont Enterprise dostęp jest na starcie wyłączony, dopóki administrator go nie włączy. Dokumentacja API serii K3 podaje okno **1 048 576** tokenów.

Cennik odczytany ze strony głównej platformy API, w juanach za 1 mln tokenów, bez podatków:

| Model | Wejście | Wyjście | Zapis cache | Trafienie cache |
| --- | --- | --- | --- | --- |
| K3.1 Pro | 13,00 | 68,00 | 13,00 | 1,30 |
| K3.1 Pro Highspeed | 26,00 | 136,00 | 26,00 | 1,30 |

Dokumentacja rozliczeń dodaje, że zapis cache serii K3 jest rozliczany osobno według TTL (5 minut i 1 godzina), a trafienie w cache nie dolicza drugi raz opłaty za zapis. Tabela na stronie głównej nie rozbija zapisu na dwa TTL. Artificial Analysis podaje ceny pierwszej strony jako **2 / 10 / 0,20 USD** za 1 mln tokenów wejścia, wyjścia i trafienia w cache. To przeliczenie strony pomiarowej, nie tabela juanowa powyżej.

Wyniki z wpisu Moonshot. Przypis bloga technicznego: wysiłek `max`, temperatura **1,0**, top-p **0,95**, o ile nie zaznaczono inaczej. Terminal-Bench 4.0 jest liczony harnessem Claude Code. Porównania z innymi laboratoriami w tej tabeli są liczbami, które Moonshot samo przytacza.

| Zadanie | K3.1 Pro według Moonshot |
| --- | --- |
| Terminal-Bench 4.0 | 65,7%; we wpisie powyżej GPT-6 Astra (58,2%) i tuż za Claude Opus 5.5 (66,4%) |
| Kimi Code Bench 3.0 Long-horizon (wewnętrzny) | 61,2%; K3: 55,95% |
| BenchCAD z narzędziami | 92,7%; we wpisie obok Opus 5.5 (96,2%) i GPT-6 Astra (95,9%) |
| OfficeQA Pro v2 | 64,4; wpis nazywa to wynikiem najlepszym |
| Kimi Hallu Bench Hard, błąd na poziomie twierdzenia | z 23,4% u K3 do 8,3% |
| Udział odpowiedzi z co najmniej jednym błędem faktu | 42,4% poziomu poprzednika |

Wewnętrzne delty finansowe w angielskim blogu: Financial Modeling **+7,2 punktu**, Financial Research **+11,6 punktu**, Business Operation około **4,2×** wyniku K3. Chiński wpis produktowy dla dwóch pierwszych wewnętrznych testów podaje wzrosty względne **14%** i **20%**. To inne wyrażenie tej samej pary testów. Nie wolno ich dodawać ani podstawiać jednego pod drugie. Moonshot zastrzega, że Hallu Bench Hard jest testem stresowym i nie opisuje zwykłego dziennego błędu.

Szybki start w dokumentacji API wciąż zawiera placeholdery w rodzaju `[xx.x%]` i inną parę wskaźników halucynacji niż blog. Liczby w tym podrozdziale biorą się z wpisu produktowego i z bloga technicznego, nie z tej strony szybkiego startu.

Osobny pomiar Artificial Analysis z 23 października, indeks własny tej firmy, stawia K3.1 Pro na **4.** miejscu z wynikiem **55**, o **11** punktów powyżej K3 (44). Przed nim są Claude Opus 5.5 (58), Claude Sonnet 5.5 (56) i Muse Wonder Full (56). Na Terminal-Bench 4.0 ta sama strona podaje **67%**, powyżej Sonnet 5.5 (64%) i powyżej 13% u K3. To inny harness niż 65,7% z bloga Moonshot. AA pisze też, że po publikacji wag K3.1 Pro byłby najwyżej notowanym modelem otwartowagowym na tym indeksie, a luka do czołowego modelu zamkniętego spadłaby z 12 do 3 punktów. To prognoza strony pomiarowej na dzień 23 października, przy wagach wtedy nieopublikowanych.

Moonshot pisze, że przed wydaniem wag usunęło materiał cybernetyczny z mid-treningu i ze środowisk RL oraz że checkpoint przeznaczony do otwartych wag ma ofensywną zdolność cybernetyczną poniżej tego, co ten sam potok wytworzyłby bez tego cięcia, i poniżej czołowych modeli zamkniętych dostępnych publicznie od co najmniej trzech miesięcy. Szczegółów zadań z tego rozdziału ten przegląd nie powtarza.

**Źródła:**

- [Kimi — wpis produktowy, aktualizacja 24.10.2026](https://www.kimi.com/news/kimi-k3-1-pro)
- [Kimi — blog techniczny](https://www.kimi.ai/blog/kimi-k3-1-pro)
- [Platforma API Kimi — opis i ceny juanowe na stronie głównej](https://platform.kimi.com/)
- [Dokumentacja rozliczeń API](https://platform.kimi.ai/docs/pricing/chat)
- [Artificial Analysis — pomiar z 23.10.2026](https://artificialanalysis.ai/articles/kimi-k3-1-pro-launch-benchmarks)

### 1.3. Google DeepMind: Genie 4 (27 października 2026)

**27 października 2026** Google DeepMind ogłosiło **Genie 4**, model świata do interaktywnej symulacji w czasie rzeczywistym. To zapowiedź badawcza, nie ogólny model językowy do czatu i nie publikacja wag.

Model jest natywnie multimodalny: razem ze sceną generuje dźwięk otoczenia, muzykę i dialog. Gemini Omni ma kotwiczyć wygląd i zachowanie w świecie rzeczywistym. Inne modele Gemini mają utrzymywać spójność i ciągłość. Użytkownik uruchamia zdarzenie i steruje sceną językiem naturalnym: kamera, pogoda, nowa postać. Między poleceniami Gemini, według wpisu, obserwuje scenę i koryguje jej bieg. W pętli czasu rzeczywistego rolę agenta prowadzącego pełni **Gemini 3.8 Flash**: rozbija cel na kroki, czyta klatki i sprawdza, czy krok się udał. Osobny przykład badawczy łączy **Gemini 4 Argon** z Genie 4 przy planie wielokrokowym dla robotyki; podpis pod materiałem pokazuje humanoida Apollo firmy Apptronik przy warcabach. To demonstracja kierunkowa, nie wdrożony system sterowania robotem.

DeepMind wymienia cztery kierunki: sterowanie symulacją w czasie rzeczywistym, fizykę i ruch ludzi, natywny dźwięk (pierwszy taki model świata firmy w czasie rzeczywistym, w tym dialog) oraz zdarzenia wielokrokowe prowadzone przez Gemini. Zastosowania, o których pisze firma, to środowiska treningowe dla robotów i agentów oraz narzędzia dla filmu, dziennikarstwa, gier i produkcji.

Dystrybucja: podgląd badawczy dla ograniczonej grupy zaufanych testerów. Dalej model ma trafić do subskrybentów Google AI Ultra w Project Genie oraz do partnerów wczesnego dostępu w Gemini API i AI Studio. Każde wideo i audio ma nieść **SynthID**, niewidoczny znak wodny.

Ograniczenia zapisane na stronie modelu: spójność wizualna i trwałość obiektów rozjeżdżają się z czasem, po wielu edycjach promptu i przy ruchu po scenie; model utrzymuje kilka minut ciągłej interakcji, nie długie sesje; tekst bywa czytelny głównie wtedy, gdy był w opisie wejściowym; rzeczywiste lokalizacje nie są odtwarzane z pełną dokładnością; złożone interakcje wielu agentów pozostają otwartym problemem. Wpis nazywa Genie 4 wczesną technologią i opisuje wewnętrzne ewaluacje bezpieczeństwa przed podglądem. Niezależnego pomiaru realizmu w tym przeglądzie nie ma.

**Źródła:**

- [Google DeepMind — Genie 4, 27.10.2026](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/)
- [Google DeepMind — strona modelu, w tym ograniczenia](https://deepmind.google/models/genie/)
- [Blog Google — zapowiedź z 27.10.2026](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/introducing-genie-4/)

### 1.4. NVIDIA: Nemotron 3.5 Bolt E4B jest już wagą (23 października 2026)

Przegląd z 21 października zapisał **Bolt E4B** jako zapowiedź na **23 października 2026**, obok wydanych tego samego 15 października Super VL i Bolt 74B-A9B. Zapowiedź doszła do skutku. Karty na Hugging Face podają datę wydania **10/23/2026** dla wariantu BF16 i dla wariantu 4 GB. Strona badawcza NVIDIA jest datowana **23 października 2026**.

**NVIDIA-Nemotron-3.5-Bolt-E4B** to mały model językowy, dalszy post-trening **Gemma-4-E4B-it**. Karta: **8 mld** parametrów łącznie, **4 mld** efektywnych, architektura Gemma-4-E4B, tekst na tekst, kontekst do **64 tys.** tokenów na wejściu i do **64 tys.** na wyjściu. Licencja użycia: **OpenMDW-1.1**. Model bazowy Gemma 4 pozostaje na Apache 2.0. Są przełączniki szablonu czatu dla trybu rozumowania i trybu konwersacyjnego. Rekomendowane próbkowanie z karty: temperatura **1,0**, top-p **0,95**.

Dwa artefakty pełnią różne role. **BF16** karta przeznacza do dopasowania, post-treningu i ewaluacji, nie do bezpośredniej inferencji produkcyjnej. Języki, które karta wymienia jako główne, to angielski i języki programowania; obok nich hiszpański, francuski, niemiecki, włoski i japoński. **Wariant 4 GB** (kwantyzacja pod lokalne uruchomienie, towarzyszy mu drafter DFlash) jest tym, co strona badawcza opisuje jako model asystenta na GeForce RTX, Jetson, RTX Spark i DGX Spark. Ta strona podaje obsługę **35** języków na bazie modelu wstępnie trenowanego na ponad 140 językach oraz twierdzenia vendorskie: około **40%** wyższa średnia jakość względem poprzedniego modelu NVIDIA na kluczowych testach agenta konwersacyjnego i do około **80%** mniej tokenów wyjściowych względem porównywanych modeli. Tych dwóch procentów karta BF16 w tekście odczytanym tutaj nie powtarza. Są zdaniem strony produktowej.

Identyfikatory: `nvidia/NVIDIA-Nemotron-3.5-Bolt-E4B-BF16` i `nvidia/NVIDIA-Nemotron-3.5-Bolt-E4B-4GB`. Endpoint na build.nvidia.com: `nemotron-3-5-bolt-e4b`.

**Źródła:**

- [Hugging Face — Bolt E4B BF16, data wydania 23.10.2026](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Bolt-E4B-BF16)
- [Hugging Face — Bolt E4B 4 GB](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Bolt-E4B-4GB)
- [NVIDIA Research — Bolt E4B 4 GB, 23.10.2026](https://research.nvidia.com/labs/nemotron/NVIDIA-Nemotron-3.5-Bolt-E4B-4GB/)

### 1.5. Mistral Large 4: wagi 28 października nadal są zapowiedzią

Zapowiedź wag **Mistral Large 4** na koniec października pochodzi z wpisu z **6 października 2026**. W tym przeglądzie sprawdzono kartę Hugging Face `mistralai/Mistral-Large-4-1T-A52B` w dniu **28 października 2026**. Strona nadal ma status **Upcoming release**. Bieżące ETA na karcie: **31 października 2026**. Licznik oczekujących w momencie odczytu: **975**. Planowany artefakt jest jeden. Plików wag na tej stronie nie ma.

Tekst karty powtarza opis z zapowiedzi: model multimodalny, **1 bln** parametrów, **49 mld** aktywnych na token i **52 mld** razem z embeddingami oraz warstwą wyjściową. To opis miejsca, w którym wagi mają się znaleźć, nie potwierdzenie, że już się tam znalazły. Jedyna data, którą sam wpis Mistrala z 6 października stawia przy wagach, to koniec miesiąca. ETA 31 października jest polem karty na Hugging Face.

**Źródła:**

- [Hugging Face — Mistral-Large-4-1T-A52B, odczyt 28.10.2026](https://huggingface.co/mistralai/Mistral-Large-4-1T-A52B)
- [Mistral — Introducing Mistral Large 4, 6.10.2026](https://mistral.ai/news/mistral-large-4/)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie sąd apelacyjny w USA uchyla zabezpieczenie i nakazuje zmianę sędziego po orzeczeniach, w których sam opisuje halucynacje i przyznanie się sądu pierwszej instancji do użycia AI. Australia publikuje dwie nowe regulacje dla użytkowników trybunału i sądu. W Polsce zaczynają obowiązywać przepisy ustawy o systemach sztucznej inteligencji o kontroli, karach i możliwości przedstawienia sądowi poglądu. W Nowym Jorku prasa opisuje praktyczny przewodnik dla pełnomocników; pliku tego przewodnika na stronie sądów w tym przeglądzie nie otwarto.

### 2.1. Stany Zjednoczone: Piąty Okręg w sprawie *Jackson Federation of Teachers v. Fitch* (22 października 2026)

**22 października 2026** Sąd Apelacyjny Stanów Zjednoczonych dla Piątego Okręgu złożył opinię w sprawie **nr 25-60496**, *Jackson Federation of Teachers i in. przeciwko Lynn Fitch i in.* Apelacja pochodzi z Sądu Okręgowego dla Południowego Dystryktu Missisipi, sygnatura **3:25-CV-417**. Skład: sędziowie Smith, Haynes i Engelhardt. Opinię napisał sędzia Jerry E. Smith. Sędzia Haynes dołączyła się wyłącznie do ostatniego akapitu.

Sentencja, w tym ostatnim akapicie: wstępne zabezpieczenie zostaje uchylone, sprawa wraca do sądu okręgowego, a prezes tego sądu ma przydzielić ją innemu sędziemu okręgowemu na dalszy bieg. Zabezpieczenie dotyczyło egzekucji stanowej ustawy H.B. 1193. Ten przegląd nie streszcza sporu o treść tej ustawy. Dla tematu AI liczy się to, co opinia ustala o materiale, na którym zabezpieczenie stało.

Opinia opisuje tymczasowy zakaz sędziego Henry’ego Wingate’a z **20 lipca 2025 r.** jako zawierający twierdzenia faktów nieobecne w aktach: strony spoza pozwu, „oświadczenia” osób nieistniejących albo nieobecnych, fałszywe cytaty przedstawiane jako tekst ustawy oraz programy, których ustawa miała już zlikwidować. Po ujawnieniu sędzia podmienił zakaz bez wyjaśnienia. Opinia zapisuje, że po publicznych zarzutach użycia AI sędzia Wingate przyznał, iż AI posłużyło do przygotowania zakazu, i złożył błąd na aplikanta, który użył AI przy projekcie. „Poprawiony” zakaz, włączony przez odesłanie do postanowienia o zabezpieczeniu, nadal cytował sprawę Czwartego Okręgu **„Cousins v. School Bd. of City of Norfolk”, 503 F.2d 422, 426–27 (4th Cir. 1974)**. Opinia stwierdza, że taka sprawa nie istnieje, i nazywa cytat halucynacją. Wykryto go na rozprawie przed Piątym Okręgiem.

Sąd nazywa przeniesienie sprawy do innego sędziego środkiem nadzwyczajnym i rzadko używanym. Uzasadnienie przeniesienia w opinii Smitha obejmuje zarówno materiał opisany jako halucynacje, jak i ocenę analizy prawnej sądu pierwszej instancji. Sędzia Haynes, dołączając się tylko do akapitu o uchyleniu i przeniesieniu, pisze, że na powrocie sprawy trzeba pełniej spojrzeć na H.B. 1193 i że nauczyciele nie powinni być ograniczeni w nauczaniu niedyskryminacji w zakresie Title VII. Osobnego zdania sędziego Engelhardta w opinii nie ma.

Źródłem powyższego jest tekst opinii, nie relacja prasowa. Relacje z 22–26 października (Courthouse News, Law.com, ABA Journal) powtarzają ten sam rdzeń: uchylenie, przeniesienie, nieistniejąca sprawa, przyznanie dotyczące aplikanta.

**Źródła:**

- [Opinia Piątego Okręgu, nr 25-60496, złożona 22.10.2026 (PDF)](https://www.ca5.uscourts.gov/opinions/pub/25/25-60496-CV0.pdf)
- [Courthouse News Service, 22.10.2026](https://www.courthousenews.com/fifth-circuit-castigates-ai-rulings-in-school-diversity-policy-case/)
- [ABA Journal, 26.10.2026](https://www.abajournal.com/news/article/5th-circuit-blasts-federal-judge-for-ai-errors-in-rulings)

### 2.2. Australia, Australijskie Terytorium Stołeczne: Practice Note 2 of 2026 (26 października 2026)

**26 października 2026** Civil and Administrative Tribunal Australijskiego Terytorium Stołecznego wydał **Practice Note 2 of 2026** o użyciu sztucznej inteligencji w postępowaniach trybunału. Notę podpisała rejestratorka K. Carter. Obowiązuje od **26 października 2026** we wszystkich jurysdykcjach trybunału. Podstawa: reguła 7 regulaminu postępowań z 2024 r. Trybunał może zwolnić osobę ze stosowania noty albo wydać kierunek, który notę zastępuje.

Generatywne AI w tej nocie tworzy treść z promptu. Korekta pisowni, gramatyki i formatowanie, które nie wytwarza treści merytorycznej, poza definicję wychodzą. Użycie przy dokumentach sprawy jest dozwolone tylko zgodnie z notą albo z zarządzeniami trybunału.

Osoba, która używa GenAI, ma: polecić narzędziu opieranie się na prawie Terytorium; sprawdzić, że wynik nie powołuje prawa z innej jurysdykcji albo prawa nieistotnego oraz że nie powołuje fałszywego orzecznictwa lub ustawodawstwa; nie wgrywać materiału otrzymanego od drugiej strony; nie wgrywać danych osobowych, wrażliwych ani objętych zakazem ujawnienia, niepublikacji albo poufności; napisać w dokumencie, że GenAI użyto, jak go użyto i jak sprawdzono; użyć aktualnego formularza trybunału. Oświadczenia świadka GenAI przygotowywać nie wolno. Załącznik do oświadczenia wolno przygotować z GenAI, jeżeli świadek upewni się, że treść jest prawdziwa i oddaje jego wiedzę. Biegły może użyć GenAI przy opinii tylko wtedy, gdy ujawni narzędzie i cel oraz potwierdzi, że opinia jest jego własnym poglądem. Tłumaczenie jest dozwolone, gdy do trybunału trafia oryginał, przekład i opis użycia.

Sprawdzenia ma dokonać człowiek. GenAI nie służy do weryfikowania, czy dokument jest prawdziwy i istotny. Przy niespełnieniu noty trybunał może odmówić przyjęcia materiału, nadać mu mniejszą wagę, powziąć wątpliwość co do jego wiarygodności albo opóźnić sprawę.

**Źródła:**

- [ACAT — Practice Note 2 of 2026 (PDF, 26.10.2026)](https://www.acat.act.gov.au/__data/assets/pdf_file/0005/3146279/Practice-Note-2-of-2026-Use-of-AI-in-ACAT-proceedings-.pdf)

### 2.3. Australia, Tasmania: wytyczne Sądu Najwyższego dla użytkowników sądu (21 października 2026)

**21 października 2026** Sąd Najwyższy Tasmanii ogłosił wytyczne o generatywnej AI dla użytkowników sądu. Poprzedni przegląd, zamykany rano tego dnia, tego dokumentu nie opisywał.

Tekst odczytany tutaj pochodzi z PDF-u opublikowanego przez Law Society of Tasmania. Nazwa pliku zawiera słowo „Draft”. Treść jest okólnikiem **nr 14 z 2026 r.**, datowanym **21 października 2026**, podpisanym przez rejestratorkę Penelope Ikedife. Okólnik stwierdza, że sędziowie zgodzili się opublikować wytyczne, że obowiązują one od tego dnia do odwołania, we wszystkich postępowaniach, wobec prawników, stron, świadków i innych osób składających dokumenty, oraz że będą dostępne na stronie sądu w dziale publikacji. Kopii osadzonej na domenie `supremecourt.tas.gov.au` w tym przeglądzie nie otwarto. Poniższe zdania są z tekstu okólnika w pliku palestry.

Użytkownik, który używa GenAI do tworzenia, pisania, redagcji albo innego przygotowania dokumentu, weryfikuje całą treść przed złożeniem. Weryfikacji dokonuje człowiek, nie samo narzędzie. Sprawdzenie obejmuje istnienie faktów i dowodów, istnienie spraw, ustaw, podręczników i artykułów oraz to, że popierają one stawianą tezę, autentyczność obrazu, wideo i dźwięku oraz zwięzłość. Certyfikatu użycia GenAI wytyczne nie wymagają. Użytkownik ujawnia użycie, gdy sąd zapyta. Biegły ujawnia je według kodeksu biegłego. Osoba używająca GenAI ma umieć wyjaśnić, którego narzędzia użyła, w jaki sposób i jak sprawdziła treść.

Szczególna ostrożność dotyczy przysiąg, oświadczeń świadków i innych dowodów: mają oddawać własną wiedzę, doświadczenie i słowa osoby oraz być prawdziwe według jej najlepszej wiedzy. Opinia biegłego ma zawierać jego własny pogląd i tok rozumowania. Informacji poufnych, objętych przywilejem, tajemnicą, zakazem publikacji albo prywatnych nie wolno wprowadzać do narzędzia, które nie jest narzędziem zamkniętym.

Skutki użycia sprzecznego z wytycznymi albo z zarządzeniami sądu mogą obejmować mniejszą wagę dokumentu albo jego pominięcie, odroczenie, koszty i oddalenie sprawy. Wobec prawnika dochodzi możliwość skierowania do Legal Profession Board of Tasmania oraz kosztów osobistych. Dodatek B przypomina, że narzędzie przewiduje prawdopodobny ciąg słów i że przekonująco brzmiący tekst może być fałszywy, nieaktualny, z innej jurysdykcji albo obciążony danymi treningowymi.

**Źródła:**

- [Law Society of Tasmania — PDF okólnika nr 14/2026 i wytycznych z 21.10.2026](https://lst.org.au/wp-content/uploads/2026/10/14-of-2026-Draft-Circular-on-AI-Guidelines-for-Court-Users.pdf)

### 2.4. Polska: 28 października 2026 r. wchodzą w życie przepisy nadzorcze ustawy o systemach sztucznej inteligencji

Ustawa z **3 lipca 2026 r.** o systemach sztucznej inteligencji została ogłoszona w Dzienniku Ustaw **27 lipca 2026 r.**, poz. **1003**. To nie jest akt uchwalony w tym tygodniu. W tym tygodniu dochodzi data, od której obowiązuje jego odłożona część.

Art. 127 stanowi, że ustawa wchodzi w życie po upływie 14 dni od ogłoszenia, z dwoma wyjątkami. Art. 125 ust. 4 — obowiązek ministra cyfryzacji, by utworzyć komórkę obsługującą Komisję — wszedł w życie następnego dnia po ogłoszeniu. **Art. 8–18 oraz rozdziały 3–5, 8 i 9 wchodzą w życie po upływie 3 miesięcy od dnia ogłoszenia.** Baza ELI Sejmu przekłada ten przepis na datę **28 października 2026 r.** Tego dnia zaczynają obowiązywać m.in. indywidualne opinie i wyjaśnienia Komisji Rozwoju i Bezpieczeństwa Sztucznej Inteligencji, kontrola, postępowanie przed organem nadzoru rynku, układ o nadzwyczajnym złagodzeniu sankcji, administracyjne kary pieniężne i przepisy karne oraz zmiany w innych ustawach.

Dla sądów bezpośrednio czyta się **art. 18**, objęty tą samą datą: Komisja może przedstawić sądowi istotny dla sprawy pogląd w sprawach z zakresu sztucznej inteligencji, jeżeli przemawia za tym interes publiczny. Odwołania od decyzji Komisji ustawa kieruje do Sądu Okręgowego w Warszawie — sądu ochrony konkurencji i konsumentów. Wysokość kar administracyjnych ustawa wiąże z przypadkami, wysokością i warunkami z rozdziału XII rozporządzenia 2024/1689; kwot w złotych ustawa w przepisie o wejściu w życie nie wpisuje.

Art. 125 ust. 3 każe przewodniczącemu zwołać pierwsze posiedzenie Komisji w terminie 3 miesięcy od dnia wejścia w życie ustawy. Wejście w życie co do zasady, według ELI, to **11 sierpnia 2026 r.** Ostatnim dniem tak liczonego terminu jest **11 listopada 2026 r.** To termin z ustawy, nie osobne ogłoszenie z tego tygodnia. Wejście w życie przepisów nadzorczych 28 października nie jest tym samym co odbycie pierwszego posiedzenia.

**Źródła:**

- [Dziennik Ustaw 2026, poz. 1003](https://dziennikustaw.gov.pl/DU/2026/1003)
- [ELI Sejmu — ustawa, w tym data 28.10.2026 dla art. 8–18 i rozdziałów 3–5, 8 i 9](https://eli.gov.pl/eli/DU/2026/1003)
- Tekst ustawy odczytany z PDF-u Dziennika Ustaw (art. 18 i art. 127); plik pobrany przy przygotowaniu tego przeglądu odpowiada ogłoszeniu z 27.07.2026, poz. 1003

### 2.5. Stany Zjednoczone, Nowy Jork: relacje o przewodniku dla pełnomocników (artykuł z 27 października 2026)

**27 października 2026** amNewYork opisał nowy materiał systemu sądów stanu Nowy Jork dla pełnomocników używających generatywnej AI. Tego samego dnia New York Law Journal podał, że administratorzy sądowi wydali przewodnik, i określił go jako siedmiostronicowy. Pliku przewodnika na `nycourts.gov` w tym przeglądzie nie odnaleziono i nie odczytano. Zdania poniżej są z artykułu amNewYork, nie z urzędowego PDF-u. Artykuł, opublikowany we wtorek 27 października, pisze o materiale „wydanym w poniedziałek”. Daty wydrukowanej na samym przewodniku tu nie potwierdzono.

Według artykułu przewodnik przygotował komitet doradczy ds. AI powołany przez głównego sędziego administracyjnego Josepha A. Zayasa. Pełnomocnik może używać generatywnej AI w pismach i co do zasady nie musi ujawniać tego sądowi. Ma rozumieć ograniczenia narzędzia, sam przeczytać i sprawdzić cytowania oraz upewnić się, że pismo nie zawiera zmyślonej sprawy, przepisu ani innej treści. Artykuł cytuje przewodnik: model jest zbudowany tak, by generować tekst, który brzmi właściwie, a nie tekst, który jest właściwy; publicznie dostępne modele w rodzaju ChatGPT, Claude, Gemini i Grok nie sięgają do bazy zweryfikowanych faktów, nie potwierdzają, że cytat odpowiada prawdziwej sprawie, i nie wiedzą, czy ich własny wynik jest prawdziwy. Podpis pod pismem nadal certyfikuje brak fałszywej treści, z dotychczasową sankcją. Jeżeli sędzia ma własną regułę stojącą, ona ma pierwszeństwo przed tym materiałem.

Zayas w cytacie z artykułu mówi, że narzędzia mogą zwiększać wydajność i niosą ryzyka wymagające ostrożności, oraz że pełnomocnik pozostaje w pełni odpowiedzialny za dokładność pism. Artykuł przytacza też uwagę przewodnika o luce wiedzy po dacie treningu oraz o stronniczości danych treningowych.

Sam **Part 161** regulaminu głównego administratora — polityka, że użycie AI przy pismach nie jest zakazane i że ujawnianie nie jest wymagane, plus modelowa reguła weryfikacji dla sądów, które zechcą ją przyjąć — obowiązywał wcześniej. Nie jest wydarzeniem tego tygodnia. Nowością opisywaną 27 października jest warstwa praktycznego wyjaśnienia dla palestry. Dopóki PDF sądowy nie zostanie odczytany, siedem stron z New York Law Journal i cytaty z amNewYork pozostają relacją prasową.

**Źródła:**

- [amNewYork, 27.10.2026](https://www.amny.com/law/nys-court-system-ai-attorney-guide/)
- [New York Law Journal, 27.10.2026](https://www.law.com/newyorklawjournal/2026/10/27/ny-courts-issue-ai-guide-for-attorneys-stressing-verification-of-court-filings/)
- [Part 161, stan wcześniejszy wobec tego tygodnia](https://www.nycourts.gov/rules/part-161-use-artificial-intelligence-technology)
