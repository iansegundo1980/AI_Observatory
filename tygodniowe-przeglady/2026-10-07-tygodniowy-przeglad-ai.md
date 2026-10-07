# Tygodniowy przegląd AI — 7 października 2026

**Okres objęty podsumowaniem:** 30 września – 7 października 2026  
**Data publikacji podsumowania:** 7 października 2026  
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach wdrażanych w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd w tym repozytorium zamyka okno **23–30 września 2026**. Niniejszy dokument go nie powtarza: nie wraca do Claude Sonnet 5.5, GPT-6.1 Sol, agentów Dots, odwołania październikowej premiery GPT-6.1 Astra, ani do spraw sądowych opisanych tam (Idaho, Floryda, USPTO, personalny start KRiBSI). W źródłach przejrzanych do 7 października nie widać publicznego wydania Claude Haiku 5.5 ani wznowienia premiery GPT-6.1 Astra.

Wyjątek na progu okna: **Gemini 4 Argon** jest datowany na 30 września i nie wszedł do przeglądu z tego dnia. W części drugiej jest drugi, węższy wyjątek: przemówienie Lorda Pentlanda z **28 września**, również nieodnotowane w tamtym pliku, bo 1 października weszły do obiegu dalsze omówienia, a treść dotyczy sądów.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora albo z jego odczytu cudzej tablicy. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru i harnessy się nie pokrywają.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

### 1.1. Google: Gemini 4 Argon wchodzi najpierw do obrońców cybernetycznych, nie do otwartego API (30 września 2026)

**30 września 2026** Koray Kavukcuoglu ogłosił **Gemini 4 Argon**, frontierowy model Google DeepMind do długich zadań w inżynierii oprogramowania, pracy wiedzy (prawo, finanse) i obrony cybernetycznej. To nie jest ogólna premiera. Argon idzie najpierw do wąskiej grupy zaufanych obrońców w programie **Fairwind**. Google pisze, że uczestniczy w dobrowolnej amerykańskiej procedurze dostępu do modelu przed szerokim wydaniem i że dostęp dla deweloperów, firm i konsumentów — zaczynając od płatnego API i subskrybentów Google AI Ultra — ma przyjść „tak szybko, jak to możliwe”, po dalszym zacieśnianiu zabezpieczeń.

Cena wprowadzająca: **2 USD / 10 USD** za 1 mln tokenów wejścia / wyjścia, a tokeny wejścia z cache mają być o **95%** tańsze od stawki wejścia. Po okresie wprowadzającym: **4 USD / 20 USD**. Limit wyjścia Google podnosi do **1 mln tokenów**, z wcześniejszych 64 tysięcy. To jest głowa do długiej trajektorii w jednym przebiegu, nie skrót marketingowy „dłuższego kontekstu”.

Wybrane liczby z ogłoszenia, wszystkie vendorskie:

- DeepSWE v1.1: **77,9%** (długie zadania inżynierii oprogramowania).
- AutomationBench (Zapier): **51,3%**, miejsce 1 w odczycie Google.
- LVBench (długie wideo): **91,7%**.
- CWE-bench v1 (łatanie podatności): **68%**, remis o pierwsze miejsce; Google porównuje to z wynikami 3.8 Flash Cyber na starszej wersji CWE-bench.
- Vals Index (finanse, kod, prawo, podatki, wagi według udziału w PKB USA) oraz Harvey’s Legal Agent Benchmark: Google nazywa Argona modelem prowadzącym. Sześć dni później Mistral zgłasza na zachodzących benchmarkach prawnych i finansowych własny prymat (punkt 1.2). To dwa komunikaty vendora, nie rozstrzygnięty pojedynek.

Wewnątrz Google Argon jest już używany przez tysiące pracowników. Firma podaje anegdoty operacyjne, nie audyt osoby trzeciej: optymalizacja podprogramu kwantowego o **40%** względem opublikowanej bazy w kilka minut; agenci, którzy na telemetrii floty zwolnili ponad **300 TiB** pamięci, z szacunkiem **500 TiB–1 PiB** po pełnym wdrożeniu; migracje C/C++ do Rusta, od dziesiątek tysięcy linii (re2, libgav1) do ponad **800 tys.** linii jądra Fuchsia Zircon. Przy libgav1 agenci mieli zastąpić 32 tys. linii SIMD tak, by kompilator wektoryzował bezpieczny Rust, z wynikiem **2,7×** szybszym niż istniejący port Rusta i z identycznym wyjściem wideo. Google zastrzega, że tak duże przepisy krytycznych systemów przechodzą audyt automatyczny i ręczny, testy emulacji i recenzję, zanim wejdą na produkcję.

W cyberobronie Argon ma sam znajdować, potwierdzać i łatać podatności. Dla zaufanych obrońców i zespołów wewnętrznych Google model idzie **bez** cybernetycznych guardrailów. Wiz, w programie Scan for Good, miał dzięki niemu znaleźć krytyczną podatność w oprogramowaniu szpitalnym, której wcześniejsze modele frontierowe nie wychwyciły. Ogłoszenie nie podaje identyfikatora CVE.

Zabezpieczenia przed szerokim dostępem Google opisuje w czterech warstwach: odmowa nadużyć cybernetycznych i CBRN przy zachowaniu legalnych badań dual-use, w tym monitoring aktywacji wewnętrznych; odporność na pośredni prompt injection (prowadzenie na benchmarku Gray Swan IPI, bez liczby w tekście ogłoszenia); monitoring łańcucha myśli i działań, który zatrzymuje wykonanie przy wyjściu poza intencję użytkownika, z zastrzeżeniem, że wnioski z monitoringu treningu nie wracają do treningu; utwardzone, izolowane sandboxy przed ryzykownym treningiem i ewaluacją. Google wprost prosi resztę branży, by w tym momencie nie zaciemniać śladów rozumowania modelu.

**Źródła:**
- [Google — Introducing Gemini 4 Argon (30.09.2026)](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/)

### 1.2. Mistral Large 4: publiczny podgląd modelu o bilionie parametrów, wagi pod koniec miesiąca (6 października 2026)

**6 października 2026** Mistral uruchomił publiczny podgląd **Mistral Large 4** (ML4, w komunikacie: „le Chonk”). To model natywnie multimodalny: **1 bilion** parametrów ogółem, **49 miliardów** aktywnych. API podglądu działa w Mistral Studio. Wagi mają spaść **do końca października**. Do tego czasu ten sam model, z obniżoną moderacją i rozszerzonymi zdolnościami cybernetycznymi, dostają liderzy cyberbezpieczeństwa, sprawdzeni partnerzy i organy państwowe, którzy red-teamują go w warunkach operacyjnych.

Trening od zera szedł na **3 800** GPU NVIDIA Grace Blackwell w centrach danych Mistrala w Europie. Ten sam sprzęt serwuje podgląd. Mistral mówi o wdrożeniu europejskim prowadzonym od końca do końca, niezależnie od innych dostawców usług cyfrowych i pod prawem europejskim. Istotna część danych treningowych była wielojęzyczna: ponad **160** języków, w tym wszystkie urzędowe języki UE. ML4 jest pierwszym kamieniem milowym po rundzie **Series D na 3 mld euro**, którą firma nazywa największą rundą equity europejskiej spółki technologicznej. Bieg reinforcement learning za tym podglądem wciąż trwa; przy obecnej skali około 3 tys. GPU jeden bieg ma dawać około **33 mld** tokenów dziennie, z czego około **16 mld** to trenowalne tokeny uzupełnień po filtracji.

Wybrane wyniki z ogłoszenia (harness vendora, o ile nie napisano inaczej):

| Zadanie | Wynik podany przez Mistral |
| --- | --- |
| DeepSWE v1.1 | 61,7% |
| SWE-Atlas-QnA | 59,4% |
| Terminal-Bench 4 | 28,3% |
| Coding Agent Index | 49,8% (przed DeepSeek V4 Pro 0813 i Qwen3.8 Max, według Mistrala) |
| AutomationBench (657 workflow) | 59,9% |
| AA-Briefcase | 1 393 Elo |
| Dense 200 (visual grounding) | 42% wobec 41% dla GPT-6 Astra |
| Cybench (40 zadań z zawodów) | 93% |
| jeden test indeksu AA Cyber (odtworzenie i łatanie realnej podatności w OSS) | 82%, najwyższy wynik spośród modeli w tym teście |
| Lakera B3 (odporność na ataki) | 93,3% |
| KORA (maks. 2) | 1,691 |

Terminal-Bench 4 na poziomie 28,3% trzeba czytać obok Coding Agent Index, nie zamiast niego: na jednych osiach kodu ML4 jest, według własnej tabeli, przed dużymi modelami otwartymi, na innych zostaje daleko od tego, co Anthropic podawało dla Sonnet 5.5 pod koniec września. Ślepa ocena ludzka Surge AI (tożsamość modelu ukryta, skala 1–5, jakość kodu) dała podglądowi ML4 **3,74** i drugie miejsce z pięciu: przed Kimi K3 (3,59), GLM-5.3 (3,60) i GLM-5.2 (3,40), za Claude Opus 5 (4,22). To Opus 5, nie Opus 5.5.

Na Artificial Analysis Cyber Index Mistral stawia ML4 w pierwszej piątce globalnie i na czele modeli otwartych spoza Chin. Zdanie, które waży więcej niż procent: kilka zamkniętych modeli, w tym Claude Opus 5.5 i GPT-6 Astra, ma na tym samym teście odtwarzania podatności wynik bliski zera, **bo odmawia zadania**. Mistral przedstawia to jako przewagę obrońcy, który musi udowodnić, że luka jest prawdziwa. Jednocześnie pisze, że średni odsetek odmów ML4 na promptach cybernetycznych z JailbreakBench, StrongREJECT i AgentHarm jest wyższy niż u porównywanych modeli open-source. Zdolność i odmowa idą tu w jednej notce vendora; niezależnego rozdzielenia tych dwóch osi ten przegląd nie ma.

Dla części drugiej liczy się wiersz prawa. Mistral pisze, że ewaluator trzeci (vals.ai) na zadaniach prawnych i finansowych stawia ML4 powyżej GPT-6 Astra, a na Harvey’s Legal Agent Benchmark model bije wszystkie modele open-source. Google sześć dni wcześniej nazwał Argona prowadzącym na Vals Index i na benchmarku Harvey. Oba zdania zostają twierdzeniami laboratoriów o własnych przebiegach.

**Źródła:**
- [Mistral — Introducing Mistral Large 4 (06.10.2026)](https://mistral.ai/news/mistral-large-4/)

### 1.3. Reflection Beam: 501 mld parametrów, 23 mld aktywnych, wagi dopiero „w tym miesiącu” (5 października 2026)

**5 października 2026** Reflection ogłosiło **Beam**, pierwszy model open-weight tej firmy. To rzadki Mixture-of-Experts: **501 miliardów** parametrów ogółem, **23 miliardy** aktywnych na token, pod kod, rozumowanie i pracę agentową. Pretrening: **23,8 biliona** tokenów. Bieg RL: ponad **100 milionów** rolloutów na **10,5 tys.** GPU NVIDIA GB300 przez cztery tygodnie, budżet kontekstu do 256 tys. tokenów, około **1,3 miliarda** sandboxów do treningu i oceniania, pula blisko **1 miliona** środowisk. Reflection nazywa to jednym z największych biegów RL w otwartym laboratorium. Wagi, raport techniczny, karta modelu i artefakty deweloperskie mają wyjść **później w październiku** na licencji Apache 2.0. Dziś jest zapis na wczesny dostęp; model jest w końcowym red-teamingu. To zapowiedź wag, nie ich publikacja.

Własna tabela Reflection nie uprawnia do nagłówka „najmocniejszy model otwarty spoza Chin”. Na DeepSWE v1.1 Beam ma **44,4%**, obok GLM 5.2 (**44,0%**), ale za GLM 5.3 (61,0%), Kimi K3 (68,0%), Qwen 3.8 Max (51,0%) i DeepSeek V4.1 Flash (74,2%) — wszystkie liczby z tej samej tabeli, część komórek to „NR”. Teza firmy jest węższa i dotyczy kosztu: na rozumowaniu Beam ma być porównywalny z GLM 5.2 przy **3–4×** mniejszym koszcie inferencji, liczonym szacunkiem FLOPs z aktywnych parametrów i średniej liczby wygenerowanych tokenów, bez prefillu i narzutu serwowania. Szacunek jest Reflection, nie pomiarem rachunku na fakturze.

Inne komórki z tej samej tabeli, żeby nie cytować tylko osi, na której model wygląda równo z GLM 5.2: Terminal Bench v2.1 **80,1%** (DeepSeek V4.1 Flash w tej tabeli: 90,6%); HLE bez narzędzi **36,2%** (Kimi K3: 46,9%); GPQA Diamond **90,5%**; AutomationBench public **37,0%**. Beam jest modelem tekstowym. Może pracować z innymi modalnościami tylko wtedy, gdy da się je zapisać jako tekst.

**Źródła:**
- [Reflection — Introducing Beam (05.10.2026)](https://reflection.ai/blog/introducing-beam)
- [The Decoder — omówienie z 06.10.2026; nagłówek o „najmocniejszym modelu spoza Chin” jest szerszy niż tabela Reflection](https://the-decoder.com/reflections-beam-becomes-the-most-capable-open-weight-model-built-outside-china/)

### 1.4. Aleph Alpha Kolibri: wagi Apache 2.0, model niemiecko-angielski pod administrację i przemysł (3 października 2026)

**3 października 2026**, w Dniu Jedności Niemiec, Aleph Alpha opublikowało wagi **Kolibri**. Komunikat prasowy z Heidelbergu jest z **5 października** i potwierdza, że model jest dostępny od 3 października. To Mixture-of-Experts angielsko-niemiecki: w tabeli porównawczej **78,1 mld** parametrów ogółem i **3,46 mld** aktywnych (blog zaokrągla do 78 mld / 3 mld). Licencja **Apache 2.0**, wagi na Hugging Face. Strona produktu podaje kontekst **1 048 576** tokenów i rekomenduje **262 144** do efektywnego serwowania i zadań złożonych. Raport techniczny mówi o treningu na **24 bilionach** tokenów łącznie (pretrening, mid-training, wydłużenie kontekstu); tabela na blogu podaje **20 bilionów** samych tokenów pretreningu. Niemiecki ma stanowić **21,3%** tokenów pretreningu, tłumaczenie tylko około 6%.

Kolibri jest pozycjonowany pod pracę suwerenną w administracji publicznej, przemyśle i lotnictwie, z możliwością uruchomienia on-premise. Karta produktu: ślad pamięci około **78 GB** przy wagach FP8; minimum m.in. 2× A100 80 GB albo 1× H200 / B200 / B300. Pretrening Kolibri skończył się **11 września 2026**; poprzednik Kolibri Origin (30,6 mld / 3,27 mld aktywnych, bez publicznej premiery) skończył pretrening 11 czerwca. Odcięcie wiedzy: 18 czerwca 2026, po angielsku i niemiecku.

Benchmarki w ogłoszeniu są z harnessów Aleph Alpha, przy najwyższym wysiłku rozumowania porównywanych modeli. Firma mówi, że na matematyce, kodzie, ugruntowaniu i długim kontekście Kolibri dorównuje modelom o nawet czterokrotnie większej liczbie aktywnych parametrów, takim jak Nemotron 3 Super. Z tabeli, nie z nagłówka: AIME 2025 **96,9** (po niemiecku 87,5); GPQA Diamond **84,3** (DE 81,3); LiveCodeBench v6 **85,9**; BFCL v4 **61,4**, czyli **poniżej** Qwen3.6-35B-A3B (67,2); LongBench Pro **64,5** wobec 70,8 u tego samego Qwena; AA-Omniscience Index **−32,8**. Ujemny indeks wiedzy jest w tabeli obok wysokiego AIME. Wewnętrzne proxy klientów (nie publiczne benchmarki) firma rysuje jako wzrost od Kolibri Origin do Kolibri, m.in. niemiecki sektor publiczny 0,54 → 0,75 i lotnictwo 0,14 → 0,59.

Dla prawa istotne jest zdanie projektowe, nie wynik egzaminu. Aleph Alpha pisze, że Kolibri budowano z myślą o AI Act, Kodeksie praktyk dla modeli ogólnego przeznaczenia i RODO, z prawem autorskim jako osobną osią, oraz że protokół Merlin-Arthur ma wymuszać wstrzymanie odpowiedzi, gdy kontekst jej nie niesie. Komunikat z 5 października dodaje, że firma ogłosiła wcześniej porozumienie z Cohere w sprawie transatlantyckiej spółki suwerennego AI; transakcja czeka na zgodę regulatora, a do zamknięcia Aleph Alpha działa samodzielnie. Daty samego porozumienia ten przegląd nie przesuwa na ten tydzień: w tekście jest „recently”.

**Źródła:**
- [Aleph Alpha — Kolibri Has Landed (03.10.2026)](https://aleph-alpha.com/en/blog/kolibri-has-landed-a-sovereign-open-weight-model/)
- [Aleph Alpha — karta produktu Kolibri](https://aleph-alpha.com/en/kolibri/)
- [Aleph Alpha — komunikat prasowy (05.10.2026)](https://aleph-alpha.com/en/news/kolibri-sovereign-ai-made-in-germany/)
- [Aleph Alpha — raport techniczny (PDF)](https://aleph-alpha.com/downloads/tech-report.pdf)

### 1.5. Google tego samego dnia co Mistral: EmbeddingGemma 2 na urządzeniu i Nano Banana 2.1 do obrazu (6 października 2026)

**EmbeddingGemma 2**, ogłoszony **6 października 2026**, nie jest modelem frontierowym do pisania pism. Jest otwartym modelem embeddingów multimodalnych: **740 milionów** parametrów, architektura Gemma 4, licencja Apache 2.0. Mapuje tekst, kod, obraz, wideo i audio w jedną przestrzeń. Poprzednik tekstowy miał, według Google, ponad **20 milionów** pobrań.

Liczby z ogłoszenia: MTEB Code **68,76 → 78,68**. Wariant tekstowy może zejść do około **270 mln** parametrów, enkoder wizji to około **170 mln**, audio około **300 mln**. Matryoshka Representation Learning skraca wektor z 768 wymiarów do 512, 256 albo 128, co Google szacuje na nawet **6×** mniej miejsca w lokalnej bazie wektorów. Kontekst **8 tys.** tokenów, cztery razy tyle co EmbeddingGemma 1: do około 5,5 minuty audio, 29 obrazów albo 58 klatek. Na Pixelu 11 Pro, po kwantyzacji, Google podaje około **191 MB** aktywnego RAM dla samych wag tekstowych i około **567 MB** dla pełnego modelu. Wagi są na Hugging Face i Kaggle. To narzędzie do lokalnego wyszukiwania i RAG, w tym po kodeksie, bez wysyłania zbioru do API.

**Nano Banana 2.1** ma kartę modelu z tą samą datą publikacji, **6 października 2026**. To model obrazu oparty na **Gemini 3.6 Flash**, nie nowa rodzina Gemini 4. Wejście: tekst i obrazy, okno do 1 mln tokenów. Wyjście: obraz (4 tys. tokenów wyjścia) i tekst (64 tys.). Kanały z karty: aplikacja Gemini, AI Studio, Gemini API, AI Mode w wyszukiwarce, Google Ads, Flow, Stitch. Osobnego wpisu na blog.google w momencie publikacji karty nie było; Android Authority opisuje ogłoszenie z 6 października jako wdrożenie poprawy projektu wizualnego, edycji maską i spójności obiektu, z wyjściem 1K/2K/4K i do 14 obrazów referencyjnych.

Tabela na karcie to własny side-by-side Google (Elo preferencji, stan na październik 2026), nie zewnętrzna arena. Ogólna preferencja text-to-image, wariant z myśleniem: **1050 ± 14**, bez myślenia 1015 ± 13, wobec 990 ± 7 dla Gemini 3.1 Flash Image („Nano Banana 2”) i 935 ± 8 dla Gemini 3 Pro Image. Faktualność infografiki: **0,521** z myśleniem wobec 0,179 u Nano Banana 2. Edycja wielu postaci: 1106 ± 14 wobec 978 ± 10. Karta sama zapisuje ograniczenia: halucynacje, słaby drobny tekst, niedoskonałą spójność postaci, mylenie lewo/prawo. Odcięcie wiedzy bazy Gemini 3.6 Flash: marzec 2026, a w części dziedzin styczeń 2025, zgodnie z rodziną Gemini 3. Ocena bezpieczeństwa frontierowego jest pochodna od Gemini 3.1 Pro i 3.7 Flash, które według Google nie weszły na progi Tracked/Critical; Nano Banana 2.1 nie ma, według tej karty, nowych zdolności, które by ten wniosek zmieniały.

**Źródła:**
- [Google — EmbeddingGemma 2 (06.10.2026)](https://blog.google/innovation-and-ai/technology/developers-tools/embeddinggemma-2/)
- [Google DeepMind — karta modelu Nano Banana 2.1 (opublikowana 06.10.2026)](https://deepmind.google/models/model-cards/nano-banana-2-1/)
- [Android Authority — relacja z 06.10.2026](https://www.androidauthority.com/google-launches-nano-banana-2-1-3719823/)
- [Search Engine Roundtable — Nano Banana 2.1 w AI Mode (06.10.2026)](https://www.seroundtable.com/nano-banana-21-google-ai-mode-42246.html)

### 1.6. Microsoft: strumieniowa transkrypcja i dwa modele głosu (1 października 2026)

**1 października 2026** Microsoft AI wydał **MAI-Transcribe-2-Streaming** oraz **MAI-Voice-2.1** i **MAI-Voice-2.1-Flash**. To nie jest model ogólny. To pętla agenta głosowego: słuchanie w trakcie wypowiedzi i mowa z niskim opóźnieniem.

Transkrypcja strumieniowa obejmuje **60** języków z ciągłym wykrywaniem języka. Microsoft pisze, że na Artificial Analysis model jest pierwszy w dokładności transkryptu końcowego i częściowego oraz na granicy Pareto dokładność–opóźnienie. Pierwsze hipotezy („partials”) mają wracać po niewiele ponad **100 ms** audio. Wewnętrzne testy dyktowania i napisów: słowa pojawiają się **2×** szybciej niż u najbliższego konkurenta, którego post nie nazywa. Cena wprowadzająca: **0,54 USD za godzinę** audio do końca 2026 roku.

MAI-Voice-2.1: **23** języki i **26** locale, jedna tożsamość głosu przez języki, **22 USD** za 1 mln znaków. Karta modelu wymienia wśród locale także polski. Wariant Flash: te same języki, **45 sekund** audio przy opóźnieniu end-to-end **150 ms**, według Microsoftu **55%** szybsza inferencja i około **60%** taniej niż „porównywalne modele”, **15 USD** za 1 mln znaków. Oba modele klonują głos z kilku sekund próbki i mają mieć zapory zgody. Dystrybucja: Microsoft Foundry, a głosy także przez OpenRouter; na liście są też Vercel, Azure Voice Live i MAI Playground. LiveKit: „wkrótce”.

**Źródła:**
- [Microsoft AI — ogłoszenie z 01.10.2026](https://microsoft.ai/news/our-first-streaming-transcription-model/)
- [Microsoft — karta modelu MAI-Voice-2.1 (PDF, aktualizacja 1 października 2026)](https://microsoft.ai/pdf/MAI-Voice-2.1-Model-Card-Memo.pdf)

### 1.7. Reka Rho-1: jeden model na tekst, obraz, wideo i akcję, na razie podgląd badawczy (5 października 2026)

**5 października 2026** Reka pokazała podgląd badawczy **Rho-1**, modelu **19 mld** parametrów trenowanego od zera. Teza architektoniczna: tekst, wizja i akcja robotyczna są tokenami w jednym oknie, bez przekazywania zadania do osobnego modelu obrazu, wideo i polityki ruchu. Tokeny dyskretne niosą tekst i polecenia, ciągłe — latenty obrazu, klatki, akcje i propriocepcję. Generacja ciągła idzie przez flow matching, tekst przez predykcję następnego tokenu, a oba strumienie dzielą uwagę.

Liczby z posta są wewnętrzne. Bazowy model generuje wideo w **0,79×** czasu rzeczywistego (mediana), z oglądalnym strumieniem po około 6 sekundach. Wariant destylowany skraca trajektorię odszumiania ze **99** kroków do **8**. Reka pisze, że klip 5,3 s wrócił w około sekundę i że w jej pomiarach był to najszybszy model wideo, jaki zestopowała. Checkpoint, z którego pochodzą wyniki posta, trenował **3 miesiące na 320 GPU H100**. Firma sama nazywa to ułamkiem kosztu frontierowych modeli języka i wideo oraz „funkcjonalnym dowodem koncepcji, nie gotowym produktem”.

Ograniczenia zapisane w tym samym poście: po około 30 sekundach strumień może trzymać teksturę, a zgubić układ pomieszczenia; wykrywanie obiektów działa na klatce, nie w czasie wideo; edycja jest krucha; natywne wideo jest ograniczone do **672×384**. Rho-1 jest dostępny jako podgląd badawczy, nie jako wagi publiczne.

**Źródła:**
- [Reka — Rho-1: Collapsing the multimodal stack (05.10.2026)](https://reka.ai/news/rho-1-collapsing-the-multimodal-stack)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

### 2.1. Argentyna, Morón: apelacja honorariów upadła, bo precedens Sądu Najwyższego prowincji nie daje się odnaleźć (1 października 2026)

**1 października 2026** Sala II Cámara de Apelación en lo Civil y Comercial de Morón (sędziowie Gabriel Hernán Quadri i Laura Andrea Moro) w sprawie **P. M. M. c/ G. A., F. M. d. S.H. s/ cobro ordinario de sumas de dinero**, causa MO-14691-2021, RS-722-2026, uznała za bezprzedmiotowy (desierto) środek odwoławczy mediatora od podstawy wymiaru honorarium. Diario Judicial opisał rozstrzygnięcie **2 października**.

Pismo opierało się prawie w całości na orzeczeniu, które skarżący nazwał „Colegio de Abogados de La Plata c/ Provincia de Buenos Aires” (sprawa „Barrio”) z 5 maja 2021 roku i któremu przypisywał zakaz stosowania stóp pasywnych, gdy zaniżają wierzytelność zawodową. Sąd sprawdził system akt: causa C-121.461 to incydent upadłościowy z ostatnim ruchem w 2017 roku, więc nie mieści wyroku z 2021. W bazie Juba nie ma ani takiej caratuli, ani przywołanego sumariusza. Znane orzeczenie „Barrios” dotyczy czego innego (następcza niekonstytucyjność art. 7 i 10 ustawy 23.928) i nie niesie tezy, na której mediator zbudował zarzut. Brak konkretnej i uzasadnionej krytyki wyroku pierwszej instancji sąd oparł na art. 260 i 246 kodeksu postępowania cywilnego prowincji Buenos Aires. Koszty ponosi apelujący.

Sąd wpisuje epizod w debatę o halucynacjach generatywnej AI i przypomina sprawę *Mata v. Avianca* oraz wcześniejszą, podobną pomyłkę własnej Cámara, semantycznie zlepioną ze sprawą „Barrios”. Jednocześnie pisze wprost, że **nie może stwierdzić z pewnością**, iż cytaty wzięły się z AI; źródło może być inne. Mocniejsza teza procesowa jest inna: caratula znanego orzeczenia z cudzą treścią jest trudniejsza do wyłapania niż całkowicie zmyślona sygnatura, bo znajoma nazwa usypia obowiązek otwarcia tekstu.

Sankcji pieniężnej nie ma. Sąd poleca zawiadomić adwokata i przesłać decyzję do Colegio de Abogados departamentu, żeby izba — **jeśli uzna to za stosowne** — przypomniała członkom o weryfikacji cytatów przy narzędziach generatywnych. Baza Damiena Charlotina (aktualizacja 5 października) oznacza wynik jako „Bar Referral”. To szersza etykieta niż opis Diario Judicial i Nino Legal: nie ma tu skierowania dyscyplinarnego, jest prośba o okólnik. Regulayer cytuje z sentencji osobne zdanie o kontroli wyników narzędzi AI, „incluso la ‘Visión general creada por IA’ del buscador de Google”, gdy odpowiedź podpina znaną caratulę pod tezę. Tego zdania o przeglądzie Google nie ma w relacji Diario Judicial; przywołujemy je jako cytat z omówienia, które podaje się za wyciąg z orzeczenia.

**Źródła:**
- [Diario Judicial — „Sin cita real, no hay recurso” (02.10.2026)](https://www.diariojudicial.com/news-104568-sin-cita-real-no-hay-recurso)
- [Nino Legal — omówienie RS-722-2026](https://ninolegal.com/novedad/camara-moron-civil-declara-desierto-recurso-cita-inexistente-inteligencia-artificial)
- [Regulayer — omówienie z cytatem sentencji, w tym o przeglądzie AI Google](https://regulayer.com/sanctions/pmm-c-ga-moron-argentina)
- [Damien Charlotin — baza halucynacji, wpis z 1 października 2026; etykieta „Bar Referral” jest szersza niż relacje prasowe](https://www.damiencharlotin.com/hallucinations/)

### 2.2. USA: Board of Immigration Appeals nadaje moc precedensu zawieszeniu za halucynacje i brak szczerości (1 października 2026)

**1 października 2026** Board of Immigration Appeals opublikował jako precedens sprawę **Matter of Mike Singh Sethi**, 30 I&N Dec. 112 (BIA 2026). Przypis 1 mówi wprost, że decyzja wyszła najpierw niepublikowana **15 września 2026**, a oznaczenie precedensu wiąże się z poprawkami redakcyjnymi. Wydarzeniem tego tygodnia jest więc precedens, nie pierwszy dzień zawieszenia.

Sentencja: zawieszenie w występowaniu przed BIA, sądami imigracyjnymi i Department of Homeland Security na **6 miesięcy, ze skutkiem od 13 czerwca 2026**. To dyscyplina wzajemna. 3 czerwca 2026 Sąd Apelacyjny dla Dziewiątego Okręgu zawiesił tego samego pełnomocnika na sześć miesięcy w *Malkeet Lnu v. Blanche*, 177 F.4th 1014, ze skutkiem 13 czerwca. BIA 1 lipca 2026 wydał natychmiastowe zawieszenie na wniosek dyscyplinarny. Wniosek o uchylenie tego wstrzymania został oddalony. Panel: sędziowie apelacyjni Mullane i Creppy oraz tymczasowy sędzia White; opinię napisał Mullane.

Pełnomocnik chciał rozprawy, bo kwestionował wiedzę o tym, że błędy w piśmie pochodzą z AI, i nazywał wzajemną sankcję za AI „karą odstającą”, której inne okręgi federalne nie stosują. BIA odmawia ponownego ustalania faktów Dziewiątego Okręgu. Sąd okręgowy wywiódł wiedzę z okoliczności: niewiarygodne tłumaczenie nieistniejącej sprawy literówką, praktyka niesprawdzania cytatów pisanych przez brief writerów przed złożeniem, trwanie przy tej wersji po wezwaniu do wyjaśnień oraz „Notice of Errata” w innej sprawie, gdzie dwie błędne cytacje podmieniono na prawdziwe bez ujawnienia, że były halucynacjami. BIA nie ma kompetencji do ataku ubocznego na te ustalenia.

Zdanie, które zostaje regułą precedensu, jest szersze niż imigracja. Cytowanie spraw, których nie ma, przypisywanie cytatów opiniom, w których tych słów nie ma, przeinaczanie realnego orzeczenia, brak wskazania prawa, na które powód się powołuje, świadomie fałszywe stwierdzenia prawa i brak ich sprostowania podlegają dyscyplinie **z AI albo bez AI**. Stosowanie reguł zawodowych do nadużycia AI nie jest, w języku BIA, „outlier penalty”. Ciężar obalenia domniemania z 8 C.F.R. § 1003.103(b)(2) — brak due process, ułomność dowodu albo „grave injustice” — nie został udźwignięty. Trudności finansowe praktyki nie są „grave injustice”; inaczej prawie każde zawieszenie dałoby się uchylić.

**Źródła:**
- [Departament Sprawiedliwości USA — Matter of Sethi, 30 I&N Dec. 112 (PDF, decided October 1, 2026)](https://www.justice.gov/eoir/media/1463666/dl?inline=)

### 2.3. Dania: wytyczne dla arbitrów przy AI Act, start w Copenhagen Arbitration Days (1 października 2026)

**1 października 2026**, w sesji AI in ADR otwierającej Copenhagen Arbitration Days, Duński Instytut Arbitrażowy (DIA) ogłosił wytyczne o regulacji użycia AI przez arbitrów. LexisNexis odnotował publikację **5 października**. Wytyczne są adresowane do arbitrów wyznaczonych w sprawach DIA, nie do pełnomocników, biegłych ani stron. Sekretarz generalny Steffen Pihlblad mówi, że reguły wysokiego ryzyka mogą już dotykać spraw wszczętych w DIA, jeśli nie skończą się przed wejściem tych przepisów.

Na stronie instytutu, w zapowiedzi sesji, data wejścia przepisów wysokiego ryzyka AI Act to **2 sierpnia 2027**. Tego samego 1 października Niels Chr. Ellegaard, jeden z autorów wytycznych, napisał publicznie, że reguły wysokiego ryzyka dla rozstrzygania oraz researchu prawnego sądów i trybunałów arbitrażowych stosuje się od **2 grudnia 2027**. Ten przegląd **nie rozstrzyga**, która data jest właściwa po pakiecie Digital Omnibus. Poprzedni przegląd w tym repozytorium przyjmował 2 grudnia 2027 dla obowiązków załącznika III, w tym określonych zastosowań w wymiarze sprawiedliwości. Rozjazd jest w źródłach z tego tygodnia i warto go widzieć, zanim kancelaria wpisze jedną datę do regulaminu zespołu orzekającego.

Treść, co do której źródła są zgodne: decyzja co do istoty wyroku arbitrażowego ma zostać przy człowieku. Ellegaard: strony płacą za osąd i wiedzę prawniczą arbitrów, nie za decyzję robota. Wytyczne dotyczą użycia, które wpływa na substancję orzeczenia, nie korekty językowej. W takim użyciu autor mówi o modelu certyfikowanym na podobieństwo wyrobu medycznego, którego wyjście wchodzi do decyzji klinicznej, i o odpowiedzialności arbitra za wyjście, z którego skorzystał. Osobne ryzyko: model, który chwali projekt wyroku i „podrzuca” cztery nieuwzględnione aspekty sprawy, może wpłynąć na osąd nawet wtedy, gdy arbiter sądzi, że tylko korzysta z podpowiedzi. LexisNexis streszcza obowiązek osobnego przejrzenia akt i przygotowania rozstrzygnięcia oraz wczesną kwalifikację: czy planowane użycie jest wysokiego ryzyka i czy trybunał jest dostawcą, czy podmiotem stosującym system.

Ellegaard odsyła też do „niedawnej sprawy kanadyjskiej”, w której użycie AI przekroczyło granicę i wyrok arbitrażowy uchylono. Strona DIA nie podaje sygnatury. Nie dopisujemy jej z pamięci.

**Źródła:**
- [DIA — AI in arbitration, zapowiedź wytycznych i sesji 1 października, ze zdaniem o 2 sierpnia 2027](https://voldgiftsinstituttet.dk/en/ai-in-arbitration-innovation-challenges-and-opportunities/)
- [LexisNexis — notatka z 05.10.2026 o opublikowanych wytycznych](https://www.lexisnexis.co.uk/legal/news/danish-institute-of-arbitration-publishes-guidelines-on-regulation-of-arbitrators-use-of-ai)
- [Niels Chr. Ellegaard — nota z 01.10.2026 o starcie wytycznych i dacie 2 grudnia 2027](https://www.linkedin.com/posts/ncellegaard_guidelines-on-the-regulation-of-arbitrators-use-of-aipdf-activity-7511521295277273088-_jiN)

### 2.4. Szkocja, próg okna: Lord President mówi, że pogarda sądu jest „niebezpiecznie blisko” (przemówienie 28 września 2026)

Przemówienie jest z **28 września 2026**, czyli z ostatniego pełnego tygodnia objętego poprzednim przeglądem, który go nie zapisał. Komunikat sądownictwa wyszedł tego samego dnia, Scottish Legal News **29 września**, a omówienie Resultsense **1 października**. Wchodzi tutaj jako zaległość jednego dnia, nie jako orzeczenie z października.

Lord Pentland, Lord President i najwyższy sędzia Szkocji, otwierał rok sądowy 2026–27 w Parliament House w Edynburgu. O ławie: asystenci generatywnej AI będą narzędziem wspierającym pracę sędziów, nie jej zastępstwem; rozstrzyganie zostaje wyłącznie przy sędziach; sędzia ma znać ryzyka i korzyści narzędzia przed użyciem, a szkolenie ma chronić integralność sądu. O stronach, zwłaszcza bez pełnomocnika: AI może ułatwiać dostęp do sądu i jednocześnie niesie ryzyko dla kogoś, kto ufa jej bezkrytycznie.

Zdanie operacyjne: ani sąd, ani pozostałe strony nie chcą tracić czasu na zacytowane halucynacje spraw, twierdzenia o przekonaniu podane jako fakt albo ustawy, których nie ma. „All of these have happened in our courts and the bar for contempt of court is perilously close to being met.” Prace nad tym, co z tym zrobić, trwają. Scottish Civil Justice Council ma w tym roku powołać grupę ds. innowacji cyfrowej i AI po stronie spraw cywilnych. To nie jest grzywna i nie jest pierwszy szkocki wyrok za cytat z modelu. Jest to zapowiedź, z ust osoby kierującej sądownictwem, że próg pogardy sądu został już prawie osiągnięty w realnych pismach.

**Źródła:**
- [Judiciary of Scotland — komunikat z 28.09.2026](https://judiciary.scot/home/media-information/media-hub-news/2026/09/28/courts-and-tribunals-are-facing-unprecedented-demand---the-lord-president)
- [Judiciary of Scotland — tekst przemówienia (PDF, 28.09.2026)](https://judiciary.scot/docs/librariesprovider3/judiciarydocuments/speeches/opening-of-the-legal-year-2026-final-(003).pdf?sfvrsn=d5ac0566_1)
- [Scottish Legal News — relacja z 29.09.2026](https://www.scottishlegal.com/articles/courts-and-tribunals-facing-unprecedented-demand-warns-lord-pentland)
- [Resultsense — omówienie z 01.10.2026](https://www.resultsense.com/news/2026-10-01-lord-pentland-ai-hallucinated-law-scottish-courts/)

### 2.5. Porównanie: benchmark „agenta prawnego” w laboratorium, podpis i człowiek w sali

Tydzień 30 września – 7 października ustawia obok siebie dwie prędkości, które nadal się nie spotykają w jednym produkcie.

Po stronie modeli Google trzyma Argona przy obrońcach cybernetycznych i nazywa go prowadzącym na Vals Index oraz benchmarku Harvey. Sześć dni później Mistral, w publicznym podglądzie bez wag, mówi, że na zadaniach vals.ai w prawie i finansach oraz na Harvey’s Legal Agent jest wyżej, także od GPT-6 Astra, i że część testów cybernetycznych zamknięte modele oblewają odmową, nie brakiem umiejętności. Aleph Alpha oddaje wagi modelu zbudowanego pod niemiecką administrację i wprost wpisuje AI Act w założenia projektowe. Żadne z tych ogłoszeń nie twierdzi, że model może podpisać pismo albo wydać wyrok. Terminal-Bench ML4 na 28,3% i DeepSWE Beama na 44,4%, w ich własnych tabelach, są przypomnieniem, że „stan techniki w prawie” w slajdzie vendora nie jest tym samym co stan techniki w kodzie.

Po stronie instytucji ten tydzień jest o człowieku, który zostaje przy dokumencie. W Morón apelacja upada, bo nie ma orzeczenia, na którym stoi pismo, a sąd nie musi dowieść, że winne jest AI, żeby uznać brak krytyki wyroku. BIA, już jako precedens, mówi, że dyscyplina za fałszywe prawo nie staje się karą odstającą tylko dlatego, że narzędziem był model. W Kopenhadze arbitrzy dostają wytyczne pod AI Act: istota wyroku zostaje przy człowieku, a data wejścia obowiązków wysokiego ryzyka jest w źródłach z tego tygodnia rozjechana między 2 sierpnia a 2 grudnia 2027. W Szkocji, dzień przed zamknięciem poprzedniego przeglądu, najwyższy sędzia mówi, że pogarda sądu jest niebezpiecznie blisko, i jednocześnie że asystent AI na ławie nie przejmuje rozstrzygnięcia.

W Polsce w tym oknie nie ma nowego orzeczenia sądowego o AI ani nowego aktu wokół KRiBSI. Najbliższa data instytucjonalna pozostaje ta z przeglądu z 30 września: przepisy o kontrolach, postępowaniach, opiniach indywidualnych i karach wchodzą **28 października 2026**. Systemy wysokiego ryzyka w samym wymiarze sprawiedliwości, według harmonogramu przyjmowanego w tamtym przeglądzie, czekają do grudnia 2027. Luka praktyczna tygodnia jest więc ta sama, tylko z nowymi nazwami modeli: agent prawny w benchmarku vendora jest już „lepszy od Astry”, a sąd w Morón, Board of Immigration Appeals i Lord President nadal czytają zdanie, nie slajd.

**Źródła:** jak w punktach 1.1, 1.2, 1.4 oraz 2.1–2.4. Termin 28 października 2026 dla egzekucji polskiej ustawy o systemach AI jest przypomnieniem z [przeglądu z 30 września](https://github.com/iansegundo1980/AI_Observatory/blob/cursor/tygodniowy-przegl-d-ai-0da6/tygodniowe-przeglady/2026-09-30-tygodniowy-przeglad-ai.md), nie nowym wydarzeniem.
