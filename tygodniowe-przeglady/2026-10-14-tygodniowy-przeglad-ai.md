# Tygodniowy przegląd AI — 14 października 2026

**Okres objęty podsumowaniem:** 7–14 października 2026  
**Data publikacji podsumowania:** 14 października 2026  
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach wdrażanych w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd w tym repozytorium zamyka okno **30 września – 7 października 2026**. Niniejszy dokument go nie powtarza: nie wraca do samej zapowiedzi Gemini 4 Argon z 30 września, do publicznego podglądu Mistral Large 4 z 6 października, do zapowiedzi Reflection Beam z 5 października, ani do spraw już tam opisanych (Argentyna, Board of Immigration Appeals, wytyczne DIA, przemówienie Lorda Pentlanda). Wagi Beama i Mistral Large 4 w tym oknie nadal nie spadły. Repozytorium Hugging Face modelu Mistral pokazuje oczekiwane wydanie **31 października 2026** i status oczekiwania, nie pliki wag. Strona Reflection z 5 października wciąż mówi o wagach „później w tym miesiącu”.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora albo z odczytu tablicy, którą vendor lub serwis ewaluacyjny sam publikuje. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru i harnessy się nie pokrywają.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

### 1.1. OpenAI: GPT-6 w ChatGPT dla wszystkich, z interfejsem składanym w locie (7 października 2026)

**7 października 2026** OpenAI zaczęło wprowadzać GPT-6 do karty czatu ChatGPT dla ponad **1,2 miliarda** osób, które według firmy korzystają z produktu co tydzień. To nie jest premiera GPT-6.1 Sol ani agentów Dots z 29 września i nie zmienia modeli stojących za Work i Codex. Karta systemowa rozdziela wersje miesiącem: **październikowe** Sol i Luna wchodzą do czatu i zastępują tam GPT-5.6 Sol oraz GPT-5.6 Luna; **wrześniowe** Sol i Luna zostają w Codex i w ChatGPT Work.

W czacie płatne plany Plus, Pro, Business i Enterprise dostają **GPT-6 Sol**. Plany Free i Go, od **8 października**, dostają **GPT-6 Luna**. Oba warianty są dostrojone do zwykłej rozmowy. Dostępność w planach Enterprise zależy od ustawień administratora. Wdrożenie płatnych planów ruszyło 7 października; darmowe i Go — dzień później.

Nowością produktową jest **Intelligent UI**. Model składa odpowiedź z tekstu, grafiki i elementów interaktywnych: przycisków, formularzy, wykresów, diagramów. OpenAI opisuje bibliotekę natywnych, strumieniowanych komponentów oraz kompilator, który rysuje interfejs w trakcie generacji, bez czekania na całą odpowiedź. Model ma sam decydować, kiedy porównanie jest tabelą, kiedy wyjaśnienie jest diagramem, a kiedy wystarczy zdanie. Firma wprost pisze, że ocena projektowa modelu nadal wymaga pracy.

Druga zmiana dotyczy czasu oczekiwania. Zamiast dokończyć całe rozumowanie i dopiero potem odpowiedzieć, GPT-6 ma przeplatać myślenie z odpowiedzią. W wewnętrznej ewaluacji codziennych zadań agentowych **GPT-6 Extra High** zaczyna odpowiadać w czasie porównywalnym z **GPT-5.6 Medium**, a końcowy wynik OpenAI stawia wyżej niż u **GPT-5.6 Extra High**. Przy pytaniach wymagających wyszukiwania w sieci **GPT-6 Instant** zaczyna odpowiedź średnio o **44%** wcześniej niż GPT-5.6 Instant. To pomiary wewnętrzne, nie publiczny benchmark.

Karta z 7 października traktuje październikowe Sol i Luna jako **High** w cyberbezpieczeństwie oraz w domenie biologicznej i chemicznej w ramach Preparedness Framework i jako poniżej progu High w samodoskonaleniu AI. Zabezpieczenia mają być tym samym zestawem, który opisano dla GPT-5.6 Sol i Luny. OpenAI zgłasza mocniejszą odporność na jailbreaki, w tym wieloturowych, oraz spadek nieuczciwości i obchodzenia guardrailów względem GPT-5.6 w czacie. Jednocześnie karta odnotowuje regresje na trudnych ewaluacjach: Sol na standardowym zbiorze dotyczącym samookaleczenia, Luna także na przemocy graficznej i treściach seksualnych, a oba modele na części testów dla użytkowników poniżej 18. roku życia. Firma pisze, że ręczny przegląd uznał te odpowiedzi za niskiej wagi, że model nie realizuje próśb o ułatwienie samookaleczenia i że część zabezpieczeń systemowych (klasyfikatory, linie kryzysowe, kontrola rodzicielska) nie wchodzi do tych liczb. Na hierarchii instrukcji, bez zabezpieczeń systemowych, Sol ma **99,99%**, a Luna **99,79%** odporności w ewaluacji GPT-Red. Te procenty mierzą jedną warstwę stosu, nie cały produkt.

**Źródła:**
- [OpenAI — GPT-6 and Intelligent UI for everyone (07.10.2026)](https://openai.com/index/gpt-6-for-everyone/)
- [OpenAI — GPT-6 Sol and GPT-6 Luna: October 2026 update (karta, 07.10.2026)](https://deploymentsafety.openai.com/gpt-6-october)

### 1.2. Anthropic: Claude Haiku 5.5, tańszy model do podzadań, i cięcie cache Sonneta (7 października 2026)

**7 października 2026** Anthropic wydał **Claude Haiku 5.5**, najtańszy i — przy standardowej prędkości — najszybszy model, jaki firma dotąd opublikowała. Identyfikator na Claude Platform: `claude-haiku-5-5`. Model jest od razu na AWS, Google Cloud i Microsoft Azure oraz w GitHub Copilot. Przegląd z 7 października, zamykany tego samego dnia rano, jeszcze tej premiery nie miał.

Haiku 5.5 jest modelem do dużej liczby tanich wywołań: streszczeń, kompresji kontekstu, zapytań do baz, klasyfikacji, podagentów przy Opus 5.5 i Sonnet 5.5, wsparcia na żywo i obsługi przeglądarki. To pierwszy Haiku z regulowanym poziomem wysiłku. Przypis Anthropic: przy standardowej prędkości jest najszybszy w rodzinie, ale wolniejszy niż Opus w trybie Fast.

Cena za 1 mln tokenów, próg **100 tys.** tokenów promptu:

| | Haiku 5.5 do / ponad 100 tys. | Haiku 4.5 | Sonnet 5.5 |
| --- | --- | --- | --- |
| Odczyt cache | 0,01 / 0,05 USD | 0,10 USD | 0,10 USD |
| Zapis cache | 0,125 / 0,625 USD | 1,25 USD | 2,50 USD |
| Wejście | 0,10 / 0,50 USD | 1,00 USD | 2,00 USD |
| Wyjście | 0,50 / 2,50 USD | 5,00 USD | 10,00 USD |

Anthropic liczy, że względem Haiku 4.5 nowy model jest o **90%** tańszy na promptach do 100 tys. tokenów i o **50%** tańszy powyżej, a średnio około **75%** tańszy, bo około 90% zapytań do poprzedniego Haiku mieściło się w niższym progu. Nowy tokenizer, zbliżony do Sonneta 5.5 i Opusa 5.5, zużywa nieco więcej tokenów na to samo zadanie; średnia to już uwzględnia.

Tego samego dnia odczyt cache **Sonneta 5.5** spada o połowę, z 0,20 do **0,10 USD** za 1 mln tokenów. Firma szacuje, że na większości pracy agentowej Sonnet 5.5 staje się przez to około **20%** tańszy. W tym tygodniu mają też wejść miesięczne kredyty API: **100 USD** dla Max 5x, **200 USD** dla Max 20x i do **500 USD** łącznie dla planu Team. SDK Pythona i TypeScript dostają w becie obsługę komputera i przeglądarki.

Wybrane liczby z tabeli Anthropic. Kolumna Sonnet 5.5 jest odniesieniem, nie twierdzeniem, że Haiku go dogania:

| Zadanie | Haiku 5.5 | Haiku 4.5 | GPT-6 Luna | Sonnet 5.5 |
| --- | --- | --- | --- | --- |
| GDPval-AA v2.1 | 1620 | 735 | 1437 | 1840 |
| AA-Briefcase v1.1 | 1578 | 614 | 1336 | 1824 |
| OSWorld 2.1, podzbiór offline | 72,4% | 15,7% | 48,9% | 83,9% |
| Humanity’s Last Exam, bez narzędzi | 45,9% | 10,2% | — | 56,9% |
| Humanity’s Last Exam, z narzędziami | 57,4% | 18,7% | — | 64,5% |
| Terminal-Bench 4.0 | 39,2% | 0,0% | 16,4% | 70,6% |
| FrontierCode 1.1 (Main) | 46,4% | — | 42,4% | 52,1% (Xhigh) |
| Chartography, bez narzędzi | 46,4% | 6,4% | 29,1% | 61,6% |

Terminal-Bench 4.0 na poziomie 39,2% trzeba czytać obok 70,6% Sonneta 5.5 w tej samej tabeli. Anthropic samo pisze, że do złożonego kodu agentowego zostają Sonnet 5.5 i Opus 5.5, a Haiku jest do węższych zadań, które przy poprzedniej cenie były zbyt drogie. Wczesne liczby klientów, też z ogłoszenia, nie z niezależnego audytu: Asana — ponad 30% mniej opóźnienia i do 2,5× szybsza inferencja na turę agenta; HubSpot — 92,8% na własnym zestawie CRM, średnia z trzech biegów; AlphaSense — 0,84 wobec 0,76 dla Haiku 4.5 na 400 zapytaniach; Box — 11 punktów wyżej niż Haiku 4.5 przy około połowie opóźnienia; Devin Fusion z Haiku 5.5 jako modelem pomocniczym i Opusem 5.5 jako prowadzącym — FrontierCode **66,2**.

Zabezpieczenia cybernetyczne Haiku 5.5 są ciaśniejsze niż u Haiku 4.5 i luźniejsze niż u Sonneta 5.5: firma pisze, że dopuszczają szerszy zakres zadań obronnych, ale blokują testy penetracyjne i techniki bliższe atakującemu. Zabezpieczenia biologiczne mają być takie jak u Sonneta 5, Sonneta 5.5 i Opusa 5. Szersza praca biologiczna i cybernetyczna idzie przez programy weryfikacji Anthropic.

**Źródła:**
- [Anthropic — Introducing Claude Haiku 5.5 (07.10.2026)](https://www.anthropic.com/claude-haiku-5-5)
- [AWS — Claude Haiku 5.5 na Amazon Bedrock (07.10.2026)](https://aws.amazon.com/blogs/machine-learning/introducing-claude-haiku-5-5-on-aws/)
- [GitHub Changelog — Claude Haiku 5.5 w GitHub Copilot (07.10.2026)](https://github.blog/changelog/2026-10-07-claude-haiku-5-5-in-github-copilot/)

### 1.3. Google: Gemini 4 Argon wychodzi z wąskiego programu obrońców (13 października 2026)

**13 października 2026** Google otworzył **Gemini 4 Argon** szerzej. Przegląd z 7 października opisywał ogłoszenie z **30 września**, w którym model szedł najpierw do zaufanych obrońców w programie Fairwind, a publiczne API było zapowiedzią. Tydzień później API płatne w AI Studio i na platformie Gemini, Google AI Ultra w Antigravity oraz subskrybenci Ultra i Pro w aplikacji Gemini i w AI Mode w wyszukiwarce dostają model globalnie. Osobna ścieżka bez cybernetycznych guardrailów zostaje przy Fairwind; Google pisze, że od 13 października rozszerza ten program o kolejne setki partnerów.

Cena wprowadzająca, już podana 30 września, dostaje datę końca: **2 USD / 10 USD** za 1 mln tokenów wejścia / wyjścia, cache wejścia o 95% taniej, do **30 listopada 2026**. Potem **4 USD / 20 USD**. Przypis dotyczy modelu przeznaczonego do dostępu publicznego. Limit **1 mln** tokenów wejścia i wyjścia łącznie oraz protokół kontynuacji zostały w dokumentacji API.

Ogłoszenie z 13 października ponownie nazywa Argona modelem nr 1 na Vals Index (finanse, kod, prawo, podatki). To wciąż twierdzenie Google o własnym odczycie, nie nowe rozstrzygnięcie sporu z Mistralem z 6 października. Nowych, niezależnych liczb na DeepSWE ten wpis nie dodaje. Dodaje anegdoty operacyjne, wszystkie vendorskie i bez audytu osoby trzeciej:

- w Chromium, w folderze rzędu **6 mln** linii wewnątrz bazy rzędu **40 mln**, agenci mieli rozplątać kod funkcji przeglądarki w setkach plików; Google mówi o miesiącach pracy zrobionych w tygodniach;
- w otwartym Agent Development Kit cięcie narzutu frameworka: **40%** krótsze przygotowanie sesji w pamięci przy długich sesjach i **21%** szybszy zimny import;
- pakiet chemii kwantowej xTB: do **2,3×** szybsze przewidywanie struktur i **1,8×** szybsze przeszukiwanie konformerów, zmiany oddane do oficjalnego repozytorium;
- inferencja Gemma 4 E2B na A100 przez vLLM: **2,85×**, z około 37 900 do ponad 108 000 tokenów na sekundę, przy deklarowanej zgodności tokenów.

W bezpieczeństwie wpis podaje liczby, których nie było w tekście z 30 września. Zewnętrzny red team biologiczny miał odblokować mniej niż **1%** testowanych podzadań. Na zbiorze przeciwstawnym naruszenia przy niebezpiecznych prośbach spadły prawie dwukrotnie względem wcześniejszych modeli Google. Próby skrótów na benchmarkach kodu, tam gdzie model nie ma motywacji, by się powstrzymać, Google stawia na **2%**. Na Gray Swan Indirect Prompt Injection skuteczność ataku po 15 próbach adaptacyjnych ma wynosić **0,7%**. Monitor niezgodności czyta kroki agenta i nie jest używany do karania śladu rozumowania w treningu — to ta sama zasada, którą Google prosiło branżę zachować 30 września.

Dla badaczy: **10 tysięcy** naukowców może dostać najwyższy próg użycia Antigravity za darmo przez sześć miesięcy, nabór stopniowy, z limitem miejsc. Na benchmarku Embodied Reasoning (ERQA) Google podaje **87%** i pierwsze miejsce wśród modeli frontierowych w swoim odczycie. Osobne akapity o enzymach, genomach noworodków i fuzji są anegdotami laboratorium, nie zrecenzowaną publikacją; ten przegląd ich nie rozwija.

**Źródła:**
- [Google — Gemini 4 Argon is now available for everyone (13.10.2026)](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-argon/)
- [Google — Introducing Gemini 4 Argon, dostęp Fairwind (30.09.2026)](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/)

### 1.4. Meta: Muse Wonder i Muse Wonder Full do agentów osobistych i zawodowych (12 października 2026)

**12 października 2026** Meta Superintelligence Labs wydało **Muse Wonder** i większy **Muse Wonder Full**. Wejście: tekst, obraz, wideo, dźwięk. Wyjście: tekst. Kontekst: **1 mln** tokenów. Wonder jest w Meta Model API i w Muse Code. Wonder Full w dniu premiery jest tylko dla subskrybentów Muse Code, bez ceny za token. Cena Wonder, według Artificial Analysis: **4 USD** za 1 mln tokenów wejścia, **0,20 USD** za wejście z cache, **20 USD** za wyjście. To ten sam rząd co Claude Opus 5.5 i wyraźnie więcej niż Muse Spark 1.3 (1,25 / 0,15 / 4,25 USD w tym samym artykule).

Firma opisuje dwa mechanizmy produktu, nie nowe warstwy architektury opublikowane jako wagi: **Active Memory** (kontekst o użytkowniku między rozmowami i dobieranie tego, co jest potrzebne do zadania) oraz **Active Focus** (dłuższa praca nad celem, z dopytywaniem i zatrzymaniem przed ważnymi działaniami). Pełniejszy raport bezpieczeństwa zapowiedziano jako „wkrótce”. Karta modelu z tego samego dnia już jest.

Artificial Analysis, niezależnie od wpisu Meta, stawia Wonder Full (max) na **56** i Wonder (max) na **52** w Intelligence Index v4.3, wobec 48 dla Muse Spark 1.3 (max). Największy skok Full wobec Sparka na Terminal-Bench 4.0: z **33%** do **57%**, na poziomie, który AA przypisuje Argonowi w ustawieniu high. Coding Agents Index: Full **68**, Wonder **63**, Spark 1.3 **54**; Full remisuje w tej tabeli z Claude Code i Sonnetem 5.5 (max, 68) i jest obok Opusa 5.5 (max, 66). AA liczy koszt zadania indeksu dla Wonder (max) na **4,52 USD**, przy 7,69 mln tokenów wejścia na zadanie. Full nie ma ceny za token, więc nie ma tej pozycji. Na AA-Omniscience wiedza zostaje słabszą osią (Full 30, Wonder 25), a spadek halucynacji Full z 33% do **23%** jest w artykule AA osobną liczbą, nie tym samym co wynik wiedzy.

Karta Meta mówi wprost, że część porównań kodu nie jest wspólnym harnessem: wyniki SWE-Marathon biorą od Abundant AI, a wyniki konkurentów na tej osi używają Codex albo Claude Code. Wonder Full na tej osi karta opisuje przy wysiłku xhigh. Proza karty nie podaje procentu pass@1, a publiczna strona benchmarku 14 października zapowiada świeżą tablicę zamiast wystawiać liczby w HTML. Tego procentu ten przegląd więc nie przepisuje i nie skleja go z 57% Terminal-Bench z AA.

W ryzyku karta ocenia Wonder Full, jako mocniejszy wariant, dla całej rodziny. Bez mitigacji Meta **nie wyklucza** progu wysokiego ryzyka w domenie chemicznej i biologicznej. Z mitigacjami i zabezpieczeniami systemowymi ryzyko rezydualne we wszystkich ocenianych domenach, także w cyberbezpieczeństwie i utracie kontroli, karta stawia na „umiarkowane lub niższe” i na tej podstawie pisze o decyzji o wdrożeniu. Szczegółowych wyników testów dotyczących patogenów ten przegląd nie przepisuje. Na MASK (uczciwość pod presją) karta podaje **87,3%**. Na Agentic Misalignment — **0%** szkodliwych działań w tym teście.

**Źródła:**
- [Meta — Muse Wonder (12.10.2026)](https://research.meta.ai/blog/muse-wonder)
- [Meta — karta modelu Muse Wonder (12.10.2026)](https://research.meta.ai/static/muse-wonder-model-card)
- [Artificial Analysis — Muse Wonder (12.10.2026)](https://artificialanalysis.ai/articles/muse-wonder)
- [SWE-Marathon — strona benchmarku (14.10.2026 bez liczb pass@1 w HTML)](https://www.swe-marathon.org/)

### 1.5. JetBrains: Mellum2.1, ten sam mały model, inny trening agentowy (8 października 2026)

**8 października 2026** JetBrains wydał **Mellum2.1**. Architektura względem Mellum2 z czerwca się nie zmienia: mieszanka ekspertów, **12 mld** parametrów ogółem, **2,5 mld** aktywnych, licencja **Apache 2.0**. Zmienia się post-trening. Reinforcement learning, wcześniej krótki etap na końcu, stał się główną częścią treningu. Firma pisze o milionach sandboxów w tysiącach środowisk i o filtrowaniu otwartych zbiorów RL, w których testy bywają zepsute albo zadania są zbyt łatwe lub nierozwiązywalne.

Wagi są na Hugging Face. Kwantyzacje GGUF pod llama.cpp, Ollamę i LM Studio oraz głowa multi-token prediction pod spekulatywne dekodowanie w vLLM mają przyjść później. Wykresy benchmarków na blogu nie mają w tekście tabeli procentów, więc ten przegląd ich nie odtwarza. Zdania, które są w tekście: największy zysk względem Mellum2 jest w kodowaniu agentowym; pod dużym obciążeniem model serwuje prawie dwa razy więcej tokenów niż Qwen3.5-9B w tym samym porównaniu JetBrains; przy jednym żądaniu MTP daje około **1,6×**. To pomiar vendora na własnej grupie modeli (Mellum2, Qwen3.5-9B, Gemma 4 E4B), nie ranking frontierowy.

Sens premiery jest węższy niż u Haiku czy Wonder: mały model, który da się postawić u siebie i włożyć jako worker albo podagent do systemu agentowego, bez wysyłania repozytorium do cudzego API.

**Źródła:**
- [JetBrains — Mellum2.1 (08.10.2026)](https://blog.jetbrains.com/ai/2026/10/mellum2-1-gets-to-work-a-fast-open-model-for-coding-agents/)

### 1.6. Hugging Face Bio: Carbon-A i baza adnotacji genów (8 października 2026)

**8 października 2026** Hugging Face Bio opublikował **Carbon-A** (Carbon-Annotator), model o **1,2 mld** parametrów, oraz **Carbon Annotation Database**. Model przewiduje regiony kodujące białka wprost z DNA, jednym checkpointem dla ssaków, pozostałych kręgowców, bezkręgowców, roślin, grzybów i protistów. Okno kontekstu: **98 304** pary zasad. Predykcja jest w rozdzielczości nukleotydu, na obu niciach.

Na 42 genomach benchmarkowych laboratorium podaje makro-uśrednione F1 nukleotydowe **0,944** i wynik wyższy niż u porównywanych narzędzi (AUGUSTUS, Helixer, Tiberius, ANNEVO, OrionGeno, SegmentNT, NTv3) na poziomie nukleotydu, eksonu i genu. To porównanie autorów. Bieżące wydanie bazy: **48 167** złożonych genomów, **22 617** taksonów, około **27 bilionów** par zasad i **566 milionów** przewidywanych loci kodujących białka. Wobec korpusu treningowego z RefSeq autorzy liczą około 11 razy więcej taksonów i 9 razy więcej sekwencji. Pokryta jest mniej więcej połowa docelowego zbioru GenBank; kolejna partia ma wyjść za około trzy tygodnie. Adnotacje mają trafić także do EMBL.

Walidacja mokrego laboratorium, z ActiveSite i UCSD, używa PacBio Iso-Seq na kocie, chomiku syryjskim, kurczaku i rzodkiewniku. Autorzy piszą, że część regionów przewidywanych przez Carbon-A, a nieobecnych w RefSeq, ma wsparcie w odczytach transkryptów, oraz że zagregowane wsparcie kompletnego CDS jest około **0,62** i bliskie referencji. W tym samym wpisie jest granica, której nie należy zgubić: eksperyment wspiera transkrypcję i strukturę eksonów. Nie pokazuje jeszcze, że RNA jest tłumaczone na białko, ani jaką to białko pełni funkcję. Wynik F1 **0,960** na *Tetrahymena thermophila*, przy niestandardowym kodzie genetycznym, też jest liczbą autorów.

Model i eksplorator bazy są publiczne na Hugging Face. To narzędzie do stawiania hipotez o adnotacji istniejących, publicznie złożonych genomów, nie zamiennik eksperymentu.

**Źródła:**
- [Hugging Face Bio — Carbon-A (08.10.2026)](https://huggingface.co/blog/HuggingFaceBio/carbon-annotator-genbank-genome-annotation)
- [Hugging Face — Carbon-A-1.2B](https://huggingface.co/HuggingFaceBio/Carbon-A-1.2B)

### 1.7. Qwen: ten sam generator obrazu, osiem kroków zamiast czterdziestu (9 października 2026)

**9 października 2026** na Hugging Face pojawił się **Qwen-Image-2.1-Turbo**, przyspieszony checkpoint **Qwen-Image-2.1**. Architektura zostaje przy około **7 mld** parametrów. Zadanie: tekst na obraz i edycja, w tym obrazy z przezroczystością i kompozycje z wielu referencji. Harmonogram próbkowania zapisany w checkpointcie ma **8** kroków odszumiania zamiast 40 w modelu bazowym. Domyślne CFG wynosi 1. Prefiksowy cache KV ma przenosić kontekst tekstu i obrazu referencyjnego między krokami. Samo ustawienie liczby kroków w wywołaniu nie nadpisuje zapisanego harmonogramu; inne harmonogramy karta oznacza jako nieewaluowane.

To nie jest nowa rodzina modeli, tylko tańsza inferencja istniejącej. „Otwarte wagi” nie znaczą tu Apache 2.0. Przed użyciem komercyjnym trzeba przeczytać plik licencji w repozytorium; opisy wtórne wskazują licencję badawczą Qwen.

**Źródła:**
- [Hugging Face — Qwen/Qwen-Image-2.1-Turbo](https://huggingface.co/Qwen/Qwen-Image-2.1-Turbo)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie nie ma nowego orzeczenia polskiego sądu o AI ani nowego aktu wokół KRiBSI. Daty z poprzednich przeglądów zostają: przepisy o kontrolach, postępowaniach, opiniach indywidualnych i karach wchodzą **28 października 2026**, pierwsze posiedzenie komisji ustawa wiąże z **11 listopada 2026**. Poniżej są zdarzenia, które w tym tygodniu naprawdę zapadły albo zostały opublikowane: dwa sądy amerykańskie, jeden sądowy porządek ochronny o danych w odkryciu dowodowym, stanowisko sądownictwa Anglii i Walii oraz decyzja brazylijskiej rady sądownictwa. Osobno, z jawną datą wrześniową, jest komentarz prasowy do sankcji, której poprzednie przeglądy nie odnotowały.

### 2.1. Floryda: IV District Court of Appeal przerzuca koszt ścigania zmyślonych cytowań na stronę i jej pełnomocnika (7 października 2026)

**7 października 2026** Sąd Apelacyjny IV Okręgu Florydy w sprawie *Kid International, LLC v. City National Bank of Florida*, nr **4D2025-2599**, utrzymał wyrok sądu okręgowego w Broward (sędzia Jeffrey R. Levenson) co do przedawnienia, bez omawiania meritum, i osobno uwzględnił wniosek pozwanych o sankcje.

Skład (Shaw, J., przy zgodzie Gerbera, C.J., i Lotta, J.) ograniczył wywód do briefu apelacyjnego, nie do wcześniejszego postępowania, w którym strona działała sama. W skardze pro se sąd naliczył 32 cytowane sprawy: 15 nie istniało, dwie były zacytowane trafnie, ale z fałszywą tezą, czternaście było zacytowanych nietrafnie i z fałszywą tezą, jedna była trafna. Pozew wniesiony już przez adwokata tych halucynacji nie powtórzył. Brief apelacyjny tak.

Sąd wymienia pięć grup błędów: oparcie wywodu na prawdziwej sprawie federalnej *City National Bank of Florida v. Louisiana Apple, LLC* z fikcyjnymi cytatami i tezami o przyznaniu faktów; siedmiokrotne powołanie nieistniejącej sprawy *Ogilvie v. Sebring Airport Authority*, 841 So. 2d 529 (Fla. 2d DCA 2003), razem z fikcyjnym cytatem; *Mansolillo v. Parties by Lynn, Inc.* z obcą sygnaturą, obcym sądem, obcym rokiem, obcą tezą i obcym cytatem; cytat przypisany *Seaboard Air Line Railroad Co. v. Holt*, którego w opinii nie ma; oraz *Silvestrone v. Edell* użyte do tez, których opinia nie stawia.

Pełnomocnik w odpowiedzi na wezwanie do wyjaśnień przyjął odpowiedzialność. Napisał, że przyjął od klienta materiały badawcze, nie wiedząc wtedy o błędach w pierwszej skardze, oraz że kancelaria używała generatywnej AI jako jednego z elementów researchu i pisania. Poprawiony brief, o którego złożenie prosił, sam przyznał, że nie usuwał wszystkich błędów. Sąd briefu nie skreślił: poszedł dalej w meritum, pomijając zmyślone cytaty i fałszywe tezy, powołując *Friend v. Serpa*.

Nowe względem wcześniejszych spraw tego samego sądu (*Francois v. Vive Financial*, *Eclectic Synergy v. Seredin*) jest podstawa kosztowa. Tamte szły z własnej władzy sądu na podstawie Florida Rule of Appellate Procedure **9.410(a)**. Tu sąd pisze, że to samo uzasadnienie niesie wniosek strony o honorarium na podstawie **9.410(b)**. Powodowie i ich pełnomocnik odpowiadają **solidarnie** za rozsądne koszty apelacji strony przeciwnej. Kwotę ustali sąd okręgowy po zwrocie sprawy. Jeśli wpłynie wniosek o rehearing, praca nad nim też wchodzi do rachunku. Opinia nie jest prawomocna do czasu rozstrzygnięcia ewentualnego, terminowego wniosku o rehearing.

**Źródła:**
- [Opinia IV DCA, Opinion_2025-2599.pdf (07.10.2026)](https://flcourts-media.flcourts.gov/content/download/2496382/opinion/Opinion_2025-2599.pdf)
- [Leagle — Kid International, LLC v. City National Bank of Florida](https://www.leagle.com/decision/inflco20261007143)

### 2.2. Georgia: każdy pozew cywilny u sędziego Browna ma zaświadczyć albo o braku AI, albo o osobistym sprawdzeniu (8 października 2026)

**8 października 2026** sędzia Michael L. Brown z Sądu Okręgowego USA dla Północnego Okręgu Georgii (Atlanta) podpisał nowy *Standing Order Regarding Civil Litigation* dla spraw do niego przydzielonych. Porządek, razem z przepisami lokalnymi i Federal Rules of Civil Procedure, zastępuje wcześniejsze standing orders tego sędziego.

Punkt o generatywnej AI dotyczy każdej strony, przez pełnomocnika albo samodzielnie, i każdego pisma. Na końcu pisma trzeba poświadczyć jedno z dwojga:

1. przy sporządzaniu pisma, **w tym w researchu do niego**, nie użyto generatywnej AI; albo
2. jeśli użyto, autor pisma osobiście sprawdził każdą część, na którą AI wpłynęła, a wszystkie cytaty wskazują prawdziwe, nie fikcyjne orzeczenia albo inne źródła i wiernie oddają ich treść.

Zaświadczenie nie wlicza się do limitu stron. Pismo bez niego **nie spełnia porządku i może zostać skreślone bez merytorycznego rozpoznania i bez prawa do poprawki**. To jest surowsze niż typowa groźba sankcji uznaniowej: stawką jest samo pismo, a gałąź „nie użyłem AI” obejmuje też narzędzia researchu, nie tylko edytor tekstu. W praktyce kancelarii, w której wyszukiwarka prawnicza ma wbudowaną generację, zdanie przeczące trzeba umieć obronić.

Tekst jest na stronie sądu. Omówienie z 8 października (AI News Today) dodaje, że egzemplarz, który autor czytał, wszedł do sprawy już toczącej się od 2025 roku (dokument 54 w sprawie 1:25-cv-05356-MLB), oraz że z publicznego archiwum RECAP nie da się policzyć, do ilu wokand porządek faktycznie wszedł. Liczby wokand ten przegląd więc nie podaje.

**Źródła:**
- [N.D. Ga. — Standing Order sędziego Michaela L. Browna (PDF, 08.10.2026)](https://www.gand.uscourts.gov/sites/gand/files/Judge_Brown_Standing_Order.pdf)
- [AI News Today — omówienie porządku (08.10.2026)](https://agenccy.ai/news/a-judge-now-wants-an-ai-certification-on-filings-that-used-no-ai/)

### 2.3. Kalifornia: materiał objęty protective order nie idzie do publicznego modelu, który się na nim doucza (8 października 2026)

**8 października 2026** w *United States v. Peplow*, 2026 WL 3026474 (E.D. Cal.), sąd wszedł w uzgodniony protective order, który osobno reguluje AI. Cytat poniżej jest z omówienia Michaela Bermana z 9 października, który przytacza Westlaw; samego płatnego oryginału Westlaw ten przegląd nie otwierał.

Kto ma dostęp do materiału chronionego, nie wprowadza go do narzędzia AI — także po anonimizacji — bez pisemnej zgody rządu albo postanowienia sądu po wniosku, chyba że narzędzie spełnia trzy warunki naraz: jest platformą klasy enterprise, którą licencjonuje obrońca; wiążąca umowa każe dostawcy trzymać dane użytkownika w poufności i zakazuje użycia ich do treningu, dostrajania, ulepszania produktu i jakiegokolwiek celu poza świadczeniem usługi; są zabezpieczenia techniczne i organizacyjne rozsądnie liczone na to, by materiału nie ujawnić. „Narzędzie AI” jest zdefiniowane szeroko: system automatyczny używający modelowania statystycznego, uczenia maszynowego albo podobnych technik, w tym duże modele językowe i usługi generatywne, w chmurze i poza nią. Obrońca poświadcza, że materiał da się z narzędzia usunąć po zakończeniu sprawy. Publiczny system, który zatrzymuje dane i uczy na nich model, jest wyłączony wprost, z uzasadnieniem, że danych wbudowanych w model nie da się praktycznie odzyskać.

Ten sam wpis z 9 października zbiera też uzgodnione porządki z 1, 2 i 6 października (*Hoffman*, *ANR Pipeline*, *Amanuel*, *White*, *Lockhart* i inne). Te daty leżą w poprzednim oknie albo na jego krawędzi i nie są nowymi wydarzeniami tego przeglądu. *Peplow* jest przykładem z 8 października: sądy federalne dopisują AI do protective orders jako warunek przetwarzania cudzego materiału, a linia cięcia biegnie między publicznym modelem a usługą objętą umową o zakazie treningu, nie między „wolno używać AI” a „nie wolno”.

**Źródła:**
- [E-Discovery LLC — Three More A.I. Protective Orders (09.10.2026), cytat z *United States v. Peplow*, 2026 WL 3026474 (E.D. Cal. 08.10.2026)](https://www.ediscoveryllc.com/three-more-a-i-protective-orders/)

### 2.4. Anglia i Walia: stanowisko sądownictwa „ostrożne, ale pozytywne”, bez listy dopuszczonych narzędzi (9 października 2026)

**9 października 2026** Courts and Tribunals Judiciary opublikowało *Position Statement on the Judicial use of Artificial Intelligence (AI)*. Podpis: Sir Colin Birss, President of the Business and Property Division, Lead Judge for Artificial Intelligence. Dokument uzupełnia, i sam tak pisze, przewodnik dla sędziów z października 2025. Go nie zastępuje.

Zakres jest instytucjonalny, nie indywidualny. Stanowisko prowadzi starszy skład sądownictwa we współpracy z Judicial Office, HM Courts and Tribunals Service i Ministerstwem Sprawiedliwości przy wdrażaniu: szkolenia, pilotaże, nadzór, komunikacja, przejrzystość. To nie jest nowy regulamin pisma dla strony.

Zasady, które da się zacytować bez skrótu myślowego: decyzję wydaje piastun urzędu sędziowskiego; AI może pomagać, ale nie zastępuje rozumowania, oceny dowodów ani uznania sędziowskiego; każde wyjście AI użyte w pracy sądowej sprawdza, weryfikuje i zatwierdza odpowiedzialny sędzia, który zostaje w pełni rozliczalny; narzędzie AI nie rozstrzyga sprawy. Ton, w pierwszym punkcie: „ostrożny, ale pozytywny”.

Do celów sądowych wolno używać tylko zatwierdzonych narzędzi. Listy nie ma, „ze względu na tempo zmian”. Cechy, które narzędzie musi mieć, w brzmieniu stanowiska: rezydencja danych w Zjednoczonym Królestwie, ochrona danych klasy enterprise oraz „Disabled web access”, czyli wyłączony dostęp narzędzia do sieci. Nowe zastosowania, produkty i pilotaże idą przez jedną scentralizowaną grupę sterującą, której przewodniczy Lead AI Judge. Grupa jest jedyną ścieżką nadzoru nad rozwojem, pilotażem i wdrożeniem oraz ścieżką eskalacji. Szkolenie prowadzi Judicial College. Grupa ma zmieniać zatwierdzone użycia, zabezpieczenia i nadzór, gdy pojawią się nowe pilotaże, incydenty albo ryzyka.

Pilotaże opisane w dokumencie dotyczyły funkcji niższego ryzyka: streszczeń, transkrypcji, anonimizacji, pisania prostszym językiem, zadań administracyjnych, chronologii i analizy dokumentów. Oceniano niezawodność, ile sprawdzenia człowiek musi dołożyć i jak obchodzić się z materiałem wrażliwym. Dokument nie podaje, które produkty pilotaże zaliczyły.

**Źródła:**
- [Courts and Tribunals Judiciary — Position Statement on the Judicial use of AI (09.10.2026)](https://www.judiciary.uk/guidance-and-resources/position-statement-on-the-judicial-use-of-artificial-intelligence-ai/)
- [Courts and Tribunals Judiciary — AI Judicial Guidance (31.10.2025), dokument uzupełniany, nie zastępowany](https://www.judiciary.uk/guidance-and-resources/artificial-intelligence-ai-judicial-guidance-october-2025/)

### 2.5. Brazylia: Corregedoria CNJ zawiesza skutki orzeczenia sądu wyborczego do wyjaśnienia, czy w tekście zostały ślady generacji (9 października 2026)

**9 października 2026**, o 22:05, minister Benedito Gonçalves, corregedor nacional de Justiça, podpisał decyzję w postępowaniu **0008562-17.2026.2.00.0000** przed Conselho Nacional de Justiça. Wnioskodawczyni: Aava Santiago Aguiar. Zobowiązany: Tribunal Regional Eleitoral de Goiás. To postanowienie tymczasowe w procedurze administracyjnej rady, nie wyrok kasacyjny w sprawie mandatu.

Wniosek dotyczy acórdão o identyfikatorze 38509590 w sprawie wyborczej **0600124-65.2026.6.09.0000**, w której uznano przyczynę utraty mandatu elektowego i polecono zawiadomić Câmara Municipal de Goiânia. Wnioskodawczyni twierdzi, że w podpisanym tekście zostały polecenia, instrukcje i zapisy konferencji niespójne ze zwykłą redakcją orzeczenia, i że to wskazuje na użycie generatywnej AI bez nadzoru człowieka wymaganego przez **Resolução CNJ nº 615/2025**. Prosi o zawieszenie skutków orzeczenia i aktów, które z niego wynikły, w tym zawiadomienia rady miejskiej.

Gonçalves pisze, że w poznaniu wstępnym zarzut jest dostatecznie prawdopodobny, żeby nie czekać na wyjaśnienia sądu. Przywołane fragmenty „w teorii” wyglądają na wewnętrzne instrukcje rewizji, służące sprawdzeniu przesłanek faktycznych i prawnych. Podkreśla granice: Corregedoria nie kontroluje treści jurysdykcyjnej i nie przegląda meritum orzeczenia wyborczego. Sprawdza regularność administracyjną sporządzenia aktu i zgodność z własnymi normami rady o nadzorze człowieka, przejrzystości i możliwości prześledzenia użycia AI. Niebezpieczeństwo zwłoki wiąże z tym, że ofício do rady miasta już wyszło i skutki mandatu mogą się skonsumować, zanim rada ustali fakty.

Liminar zawiesza skutki wskazanego acórdão i aktów administracyjnych wprost z niego wynikających, w tym Ofício nº 126/2026, do późniejszego rozstrzygnięcia w tym postępowaniu. TRE-GO ma **15 dni** na informacje. Sąd wyborczy i radę miasta należy zawiadomić natychmiast. Postanowienie samo mówi, że nie stwierdza nieważności orzeczenia i nie wkracza definitywnie w orzekanie Justiça Eleitoral.

Kontekst polityczny — zmiana partii, głosowanie 6 do 1 jeszcze latem, zaprzysiężenie zastępcy na godziny przed liminarem — pochodzi z doniesień prasowych, nie z sentencji CNJ. Ten przegląd go nie przenosi do opisu samego postanowienia.

**Źródła:**
- [CNJ, dokument 26100922050513700000006219673, decyzja z 09.10.2026, 22:05](https://www.cnj.jus.br/pjecnj/Processo/ConsultaDocumento/listView.seam?x=26100922050513700000006219673)
- [Kopia tej samej decyzji (JuriNews)](https://jurinews.com.br/storage/uploads/0008562-1720262000000-1791658246.pdf)
- [Jornal Opção — doniesienie o zawieszeniu skutków (kontekst, nie sentencja)](https://www.jornalopcao.com.br/ultimas-noticias/reviravolta-na-camara-de-goiania-cnj-suspende-cassacao-de-aava-santiago-apos-posse-de-michel-magul-877741/)

### 2.6. Massachusetts, z datą wrześniową: komentarz z 13 października do cofnięcia pro hac vice (orzeczenie 25 września 2026)

To nie jest orzeczenie z tygodnia 7–14 października. Memorandum sędzi Angel Kelley w *Aguilar v. The Crawford Group, Inc.* (D. Mass.) jest z **25 września 2026** i nie weszło do przeglądu z 30 września ani z 7 października. **13 października 2026** Massachusetts Lawyers Weekly opisało sankcję, więc data trafia tu jawnie, żeby nie czytać jej jako październikowego wyroku.

Według Leagle, The Expert Record i MLW sąd nałożył sankcje z Rule 11, także z własnej inicjatywy. W sprzeciwie wobec wniosku o skreślenie około połowa cytowań miała błąd. *Rodriguez v. Doral Mortgage Corp.*, prawdziwy wyrok I Circuit z 1995 roku, był powołany sześciokrotnie na tezę, której nie stawia, i był jedyną sprawą pod jednym z argumentów. Były cytaty przypisane sprawom, które ich nie zawierają, oraz cytowanie z fikcyjną sygnaturą Westlaw. Pełnomocnik Blake Lindemann, dopuszczony pro hac vice z Kalifornii, przyznał, że przy tym sprzeciwie użył AI, bo sądził, że wersja enterprise jego oprogramowania nie halucynuje spraw. Sąd uznał to przekonanie za nieistotne dla obowiązku sprawdzenia. Napisał, że nie ma zakazu używania AI do researchu i pisania, ale trzeba z niego korzystać odpowiedzialnie, i że użycie AI nie zmniejsza obowiązków z Rule 11. Błędy były w trzech pismach na przestrzeni miesięcy; sąd nie uzależnił sankcji od tego, czy w dwóch późniejszych pismach AI została przyznana.

Sankcje: kancelaria Lindemanna płaci rozsądne koszty i honoraria pozwanych Enterprise za trzy pisma, nie więcej niż **10 000 USD**, oraz **cofnięcie dopuszczenia pro hac vice**. Lokalny pełnomocnik w sprawie zostaje. Sąd nie nałożył sankcji za błędy w pismach wobec innych pozwanych, opisane jako mniej poważne i nieobjęte ich wnioskiem. MLW podkreśla osobno obowiązek lokalnego pełnomocnika nadzorowania pism kolegi dopuszczonego pro hac vice. Kwota i cofnięcie dopuszczenia są w omówieniach; pełnego PDF memorandum w tym przeglądzie nie ma, jest wpis Leagle i artykuł z 13 października.

**Źródła:**
- [Leagle — Aguilar v. Crawford Group, memorandum z 25.09.2026](https://www.leagle.com/decision/infdco20260928c33)
- [Massachusetts Lawyers Weekly (13.10.2026)](https://masslawyersweekly.com/2026/10/13/lawyer-ai-citations-pro-hac-vice-sanctions/)
- [The Expert Record — omówienie sankcji](https://www.theexpertrecord.com/ai-in-court/aguilar-v-crawford-group-pro-hac-vice-revoked/)

---

Tydzień po stronie modeli jest tygodniem dostępu, nie tygodniem pierwszych wag. GPT-6 Sol i Luna, w wersji, którą karta nazywa październikową, wchodzą do zwykłego czatu, także darmowego, i zaczynają składać interfejs zamiast samej wstęgi tekstu. Haiku 5.5 wypełnia lukę, którą przegląd z 7 października jeszcze odnotował jako otwartą, i jednocześnie obniża odczyt cache Sonneta 5.5. Argon, dwa tygodnie po starcie tylko dla obrońców, dostaje płatne API i subskrybentów, z guardrailami zdjętymi nadal tylko w Fairwind. Muse Wonder jest nową rodziną agentową Mety, z ceną Wonder na poziomie Opusa i z kartą, która bez mitigacji nie wyklucza wysokiego progu w domenie chemicznej i biologicznej. Obok tego stoją rzeczy, które da się pobrać od razu: Mellum2.1 na Apache 2.0 i Carbon-A do adnotacji genomów. Wagi Beama i Mistral Large 4 nadal są zapowiedzią.

Po stronie sądów linia jest zbieżna w czterech krajach i nie jest zakazem narzędzia. Floryda przerzuca koszt weryfikacji zmyślonych cytowań na tego, kto je wniósł, solidarnie ze stroną. Georgia każe poświadczyć albo brak AI w całym researchu, albo osobiste sprawdzenie, pod rygorem skreślenia pisma. Kalifornia w sprawie karnej nie puszcza materiału chronionego do modelu, który się na nim uczy. Anglia i Walia mówią sędziom-instytucji, że AI może pomagać i nie może rozstrzygać, oraz że nowe narzędzie ma jedną ścieżkę zatwierdzenia. Brazylia, na razie w zabezpieczeniu i bez stwierdzenia, że model na pewno pisał wyrok, zawiesza skutki orzeczenia sądu wyborczego, dopóki sąd nie wyjaśni, czemu w podpisanym tekście zostały zapisy wyglądające na instrukcję rewizji. Żadne z tych rozstrzygnięć nie twierdzi, że model z części pierwszej może podpisać pismo albo wydać wyrok.
