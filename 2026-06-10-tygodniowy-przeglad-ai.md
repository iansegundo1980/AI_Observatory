# Tygodniowy przeglad wydarzen AI - 2026-06-10

Zakres: najwazniejsze wydarzenia z okresu ok. 3-10 czerwca 2026 r. Zestawienie dzieli sie na dwie czesci: ogolne przelomy i nowe modele AI oraz zastosowania AI w prawie i wymiarze sprawiedliwosci, ze szczegolnym uwzglednieniem sadow.

## 1. Ogolne przelomy i nowe modele AI o istotnym znaczeniu

### Anthropic: Claude Fable 5 i Claude Mythos 5 - model klasy "Mythos" udostepniony szerzej, ale z nowymi zabezpieczeniami

9 czerwca Anthropic oglosil dwa modele: Claude Fable 5, czyli pierwszy szeroko dostepny model klasy Mythos, oraz Claude Mythos 5, wersje o zdjetych wybranych zabezpieczeniach, udostepniana ograniczonej grupie partnerow w programie Project Glasswing i przyszlym programie trusted access. To jedno z najwazniejszych ogloszen tygodnia, bo Anthropic opisuje Fable 5 jako model przewyzszajacy wszystkie dotychczas publicznie dostepne modele firmy w obszarach takich jak programowanie, praca wiedzy, wizja, badania naukowe i dlugie zadania agentowe.

Kluczowe znaczenie ma nie tylko sama wydajnosc, ale model dystrybucji. Anthropic wprost przyznaje, ze zdolnosci klasy Mythos moga zwiekszac ryzyko naduzyc w cyberbezpieczenstwie, biologii i chemii, dlatego Fable 5 korzysta z dodatkowych klasyfikatorow bezpieczenstwa. Gdy system uzna zapytanie za ryzykowne, odpowiedz ma byc obslugiwana przez Claude Opus 4.8 zamiast Fable 5. Wedlug firmy dotyczy to srednio mniej niz 5% sesji, a uzytkownik ma byc informowany o takim przekierowaniu.

Wersja Mythos 5 ma byc tym samym modelem bazowym co Fable 5, ale z podniesionymi ograniczeniami w okreslonych dziedzinach dla zaufanych cyberobroncow, operatorow infrastruktury oraz - w przyszlosci - wybranych badaczy biologii. Anthropic podaje cene 10 USD za milion tokenow wejscia i 50 USD za milion tokenow wyjscia oraz identyfikator API `claude-fable-5`.

Znaczenie: to przyklad coraz wyrazniejszego rozdzialu miedzy modelem publicznym a modelem zaufanego dostepu. Laboratoria probuja udostepniac bardzo silne zdolnosci agentowe, ale jednoczesnie segmentuja dostep wedlug ryzyka dziedzinowego.

Zrodla:

- [Anthropic - "Claude Fable 5 and Claude Mythos 5", 9 czerwca 2026](http://anthropic.com/news/claude-fable-5-mythos-5)
- [IBM Think - omowienie premiery Anthropic, 9 czerwca 2026](https://www.ibm.com/think/news/anthropic-launches-powerful-ai-model-fable-5-mythos-5-safety-guardrails)

### NVIDIA: Nemotron 3 Ultra - otwarty model MoE dla dlugotrwalych agentow

4 czerwca NVIDIA zaprezentowala Nemotron 3 Ultra, otwarty model Mixture-of-Experts o 550 mld parametrow, z 55 mld aktywnych parametrow. Model zostal zaprojektowany przede wszystkim do orkiestracji dlugich przeplywow agentowych, w ktorych system wielokrotnie planuje, wywoluje narzedzia, deleguje zadania, odbiera obserwacje i koryguje kurs.

Najwazniejsze elementy techniczne:

- architektura hybrydowa Mamba-Transformer dla lepszego dlugiego kontekstu;
- NVFP4, umozliwiajace wedlug NVIDIA do 5x wyzsza przepustowosc na GPU Blackwell w porownaniu z BF16;
- LatentMoE do bardziej efektywnego routingu ekspertow;
- multi-token prediction dla szybszego generowania dlugich odpowiedzi;
- Multi-Teacher On-Policy Distillation, czyli uczenie z wielu wyspecjalizowanych modeli-nauczycieli;
- deklarowana otwartosc wag, danych, receptur i licencji OpenMDW-1.1.

NVIDIA podaje, ze Nemotron 3 Ultra ma obnizac koszt wykonania zadan agentowych nawet o 30% oraz osiagac 5x wyzsza przepustowosc niz porownywalne otwarte modele w swojej klasie. Wazne jest tez to, ze firma wskazuje na legal data jako jedna z domen wzmacnianych w dodatkowym pretrainingu: 4 mld tokenow syntetycznych danych prawnych mialy poprawic wynik proxy LegalBench z 64,6% do 74,7%.

Znaczenie: rynek otwartych modeli przesuwa sie z samego "chatowania" ku modelom zoptymalizowanym pod koszt, narzedzia i wieloetapowe autonomiczne wykonanie. Nemotron 3 Ultra jest szczegolnie istotny dla firm budujacych wlasne, kontrolowane stosy agentowe.

Zrodlo:

- [NVIDIA Technical Blog - "NVIDIA Nemotron 3 Ultra Powers Faster, More Efficient Reasoning for Long-Running Agents", 4 czerwca 2026](https://developer.nvidia.com/blog/nvidia-nemotron-3-ultra-powers-faster-more-efficient-reasoning-for-long-running-agents/)

### Google DeepMind: Gemma 4 12B - multimodalny model lokalny bez osobnych enkoderow

3 czerwca Google DeepMind oglosil Gemma 4 12B, sredniej wielkosci model multimodalny projektowany do pracy lokalnej na laptopach z ok. 16 GB VRAM lub pamieci wspoldzielonej. Najciekawsza cecha jest unified, encoder-free architecture: obraz i audio nie sa przetwarzane przez osobne multimodalne enkodery, lecz trafiaja bezposrednio do rdzenia LLM po lekkiej projekcji.

Wedlug DeepMind model ma:

- laczyc wizje, audio i tekst w jednej architekturze;
- dzialac lokalnie przy znacznie nizszym sladzie pamieciowym niz wiekszy model Gemma 4 26B MoE;
- osiagac wyniki zblizone do wiekszego wariantu 26B w standardowych benchmarkach;
- korzystac z Multi-Token Prediction dla nizszej latencji;
- byc wydany na licencji Apache 2.0 i wspierany w narzedziach takich jak Hugging Face Transformers, llama.cpp, MLX, SGLang, vLLM, Ollama i LM Studio.

Znaczenie: Gemma 4 12B wzmacnia trend "frontier-like on-device", czyli przenoszenia coraz bardziej zlozonej multimodalnosci na sprzet konsumencki. To moze miec znaczenie dla prywatnosci, kosztow i wdrozen edge AI.

Zrodlo:

- [Google DeepMind - "Introducing Gemma 4 12B: a unified, encoder-free multimodal model", 3 czerwca 2026](https://deepmind.google/blog/introducing-gemma-4-12b-a-unified-encoder-free-multimodal-model/)

### Microsoft AI: siedem modeli MAI i strategia uniezalezniania sie od zewnetrznych dostawcow

Microsoft AI oglosil rodzine siedmiu modeli MAI, zaktualizowana 8 czerwca. W sklad rodziny wchodza m.in.:

- MAI-Thinking-1 - flagowy model rozumujacy Microsoft AI;
- MAI-Code-1-Flash - efektywny inference'owo model agentic coding, zintegrowany z GitHub Copilot, VS Code i stosem Microsoftu;
- MAI-Image-2.5 i MAI-Image-2.5 Flash - generowanie oraz edycja obrazow;
- MAI Transcribe-1.5 - model transkrypcyjny z obsluga terminologii dziedzinowej w 43 jezykach;
- MAI-Voice-2 i zapowiadany MAI-Voice-2-Flash - generowanie mowy w 15 jezykach.

Najwazniejsza informacja strategiczna: Microsoft przedstawia modele jako trenowane od podstaw na czystych, sledzalnych danych, bez destylacji z modeli innych laboratoriow. Firma zapowiada tez "Microsoft Frontier Tuning", czyli dopasowywanie modeli poprzez reinforcement learning w srodowiskach odzwierciedlajacych realne przeplywy pracy klienta. W obszarze zdrowia Microsoft oglosil wspolprace z Mayo Clinic nad wyspecjalizowanym modelem klinicznym, ktory ma byc najpierw wdrozony w srodowisku Mayo Clinic.

Znaczenie: Microsoft wzmacnia wlasna warstwe modelowa, nie tylko infrastrukture i dystrybucje. To moze zmieniac uklad sil na rynku enterprise AI, zwlaszcza tam, gdzie klienci chca strojenia wag i kontroli nad danymi.

Zrodlo:

- [Microsoft AI - "Building a hill-climbing machine: Launching seven new MAI models", 2 czerwca 2026, aktualizacja 8 czerwca](https://microsoft.ai/news/building-a-hillclimbing-machine-launching-seven-new-mai-models/)

### OpenAI: nowe mozliwosci GPT-Rosalind i rozszerzona pamiec ChatGPT

OpenAI mial w tym tygodniu dwa istotne ogloszenia produktowo-badawcze.

Pierwsze, z 3 czerwca, dotyczy GPT-Rosalind, modelu wyspecjalizowanego dla life sciences. Aktualizacja laczy zdolnosci agentowego kodowania i uzycia narzedzi z GPT-5.5 z mocniejszym rozumowaniem w medycynie translacyjnej, medicinal chemistry, genomice, analizie danych biologicznych i workflow laboratoryjnych. OpenAI opisuje GPT-Rosalind jako research preview dla uprawnionych organizacji w modelu trusted access. Rownolegle udostepniono w Codex wtyczki Life Sciences Research i Life Sciences NGS Analysis, laczace wyszukiwanie dowodow naukowych, interpretacje biologiczna i bioinformatyczne wykonanie workflow.

Drugie, z 4 czerwca, dotyczy "Dreaming", nowej architektury pamieci ChatGPT. OpenAI opisuje ja jako bardziej skalowalny system syntezy pamieci, ktory ma rozwiazywac problemy starzenia sie, poprawnosci i skalowania kontekstu u setek milionow uzytkownikow. Pamiec ma byc syntetyzowana w tle z wielu rozmow, a uzytkownik ma widziec podsumowanie tego, co ChatGPT o nim zapamietal. Firma twierdzi, ze postep w wydajnosci obliczeniowej pozwolil obnizyc koszt obslugi tej funkcji ok. 5x, co otwiera droge do szerszego rollout'u poza Plus i Pro.

Znaczenie: OpenAI nie zaprezentowal w tym tygodniu nowego modelu ogolnego porownywalnego z premiera Claude Fable 5, ale przesunal granice w dwoch kierunkach: wyspecjalizowane modele naukowe o kontrolowanym dostepie oraz dlugoterminowa personalizacja modeli konsumenckich.

Zrodla:

- [OpenAI - "Introducing new capabilities to GPT-Rosalind", 3 czerwca 2026](https://openai.com/index/introducing-new-capabilities-to-gpt-rosalind/)
- [OpenAI - "Dreaming: Better memory for a more helpful ChatGPT", 4 czerwca 2026](https://openai.com/index/chatgpt-memory-dreaming/)
- [OpenAI - strona GPT-Rosalind](https://openai.com/gpt-rosalind/)

### Unisound: U2 - model agentowy nastawiony na 100+ krokow wykonawczych

7 czerwca Unisound oglosil U2, nowy general-purpose large language model opisywany jako "native agentic large model" nastawiony nie na pojedyncza odpowiedz, ale na domkniecie dlugiego przeplywu pracy. Firma deklaruje, ze U2 potrafi autonomicznie dekomponowac i wykonywac workflow liczace ponad 100 krokow, obejmujace planowanie, interakcje ze srodowiskiem, uzycie narzedzi, korekte procesu i walidacje wyniku.

Wedlug komunikatu model osiaga m.in. 87,9 na GPQA Diamond, 75 na SWE-Bench Verified, 76,9 na Claw-Eval pass@3 i 72,9 na GDPval. Unisound akcentuje "Hybrid Thinking", czyli dynamiczne przelaczanie miedzy niejawnym rozumowaniem latentnym a jawnym reasoningiem w momentach wymagajacych weryfikacji, oraz wspolne trenowanie modelu i harnessu agentowego.

Znaczenie: U2 pokazuje, ze coraz wiecej firm opisuje modele nie jako chatboty, ale jako systemy do dostarczania rezultatow biznesowych: raportow, aplikacji, analiz, dashboardow czy interaktywnych prezentacji. Dane pochodza z komunikatu prasowego, wiec wyniki benchmarkowe wymagaja niezaleznej weryfikacji.

Zrodlo:

- [PR Newswire / Unisound - "Unisound Releases U2...", 7 czerwca 2026](https://www.prnewswire.com/news-releases/unisound-releases-u2-a-native-agentic-large-model-built-for-execution-capable-of-autonomously-decomposing-and-completing-100-steps-in-complex-real-world-workflows-302793560.html)

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwosci

### Wielka Brytania: pilotaż AI w Crown Court, asystenci prawni i transkrypcja dla probacji oraz trybunalow

9 czerwca brytyjskie Ministerstwo Sprawiedliwosci oglosilo zestaw projektow AI majacych skracac zaleglosci w wymiarze sprawiedliwosci, szczegolnie w Crown Court. Najwazniejsze elementy:

- AI legal assistants dla prawnikow i pracownikow sadowych, przeznaczone do rutynowej pracy nad sprawami, researchu i analizy akt;
- narzedzie dla sedziow pomagajace identyfikowac sprawy gotowe do rozprawy i grupowac podobne posiedzenia;
- Justice Transcribe, czyli narzedzie AI do automatycznego nagrywania i transkrypcji rozmow kuratorow/probation officers z osobami skazanymi lub nadzorowanymi;
- test podobnej technologii transkrypcji w Immigration and Asylum Tribunals, aby sedziowie mogli szybciej sporzadzac notatki;
- AI Growth Labs jako kontrolowane srodowiska testowe dla lawtechu.

Rzad podkresla, ze asystenci AI maja byc najpierw testowani w wysoce kontrolowanych warunkach, ze standardami bezpiecznego i etycznego uzycia. Oficjalne uzasadnienie to zmniejszenie backlogu, odciazenie pracownikow administracyjnych i szybszy dostep ofiar do rozstrzygniecia.

Znaczenie dla sadow: Wielka Brytania przesuwa AI z eksperymentow back-office w kierunku narzedzi bezposrednio zwiazanych z zarzadzaniem lista spraw i przygotowaniem pracy prawnej. Jednoczesnie na razie mowi o wsparciu ludzi, a nie o automatycznym rozstrzyganiu.

Zrodla:

- [GOV.UK - "AI tech ambition to deliver smarter justice for victims", 9 czerwca 2026](https://www.gov.uk/government/news/ai-tech-ambition-to-deliver-smarter-justice-for-victims)
- [Legal Futures - "AI legal assistants to help speed up work of Crown Court"](https://www.legalfutures.co.uk/latest-news/ai-legal-assistants-to-help-speed-up-work-of-crown-court)

### Indie: projekt kompleksowych regulacji AI dla sadow - human primacy, zakaz risk scoringu i obowiazkowe audyty

3 czerwca Komitet ds. AI przy Sadzie Najwyzszym Indii opublikowal projekt "Regulations for Use of Artificial Intelligence in Courts, 2026" i zaprosil interesariuszy do skladania uwag do 20 czerwca. To jeden z najbardziej szczegolowych dokumentow tygodnia dotyczacych AI w sadownictwie.

Projekt obejmuje wszystkie funkcje sadow: adjudykacyjne, quasi-adjudykacyjne i administracyjne. Najwazniejsze zasady:

- prymat czlowieka i niezaleznosc sedziowska: AI ma byc zawsze podporzadkowana ludzkiej ocenie i wladzy sadowniczej;
- odpowiedzialnosc czlowieka: nie mozna uchylac sie od odpowiedzialnosci za blad, powolujac sie na "black box" lub halucynacje systemu;
- transparentnosc, wyjasnialnosc, audytowalnosc i ciagly nadzor;
- ochrona danych, minimalizacja danych, cyberbezpieczenstwo;
- domniemanie odpowiedzialnego wdrazania AI tam, gdzie poprawia dostep do sprawiedliwosci lub zmniejsza opoznienia.

Projekt wymienia przyklady dozwolonych zastosowan: zarzadzanie sprawami, przygotowanie wokand, transkrypcje, tlumaczenia, research prawny, weryfikacja cytowan, streszczanie dokumentow, chatboty informacyjne dla stron, dostepnosc dla osob z niepelnosprawnosciami, anonimizacja orzeczen i analityka backlogu.

Jednoczesnie dokument wprowadza bezwzgledne zakazy, m.in.:

- brak rozstrzygniecia wylacznie na podstawie AI;
- brak samodzielnego orzekania i skazywania przez AI;
- zakaz risk scoringu w procesie sadowym, w tym oceny ryzyka ucieczki, recydywy, kwalifikacji do kaucji lub wiarygodnosci stron i swiadkow;
- zakaz nieujawnionych, nieprzejrzystych systemow, ktore moga materialnie wplywac na prawa lub wolnosc osobista;
- zakaz wykorzystywania AI do nadzoru lub ciaglego monitorowania sedziow, adwokatow, stron i innych osob w zwiazku z sadem;
- zakaz skladania outputu AI jako samodzielnego dowodu bez pelnego ujawnienia jego charakteru.

Znaczenie dla sadow: Indie proponuja pelna architekture zarzadzania AI w sadach: Apex Body, komitety AI, sekretariat, rejestr AI, audyty, baze incydentow, controlled environment testing i roczne raporty transparentnosci. To model bardziej instytucjonalny niz same wytyczne etyczne.

Zrodla:

- [Supreme Court of India - projekt "Regulations for Use of Artificial Intelligence in Courts, 2026", 3 czerwca 2026](https://hcraj.nic.in/hcraj/hcraj_admin/uploadfile/latestupdates/Final_draft_with_Notice_v178072027287.pdf)
- [Indian Express - "Supreme Court AI draft rules: No AI in verdicts, bail eligibility"](https://indianexpress.com/article/legal-news/supreme-court-ai-regulations-2026-draft-rules-courts-ban-ai-decisions-10723503/)
- [Bar & Bench - informacja o projekcie regulacji](https://www.barandbench.com/news/lawyers-can-use-ai-ifsupreme-court-releases-draft-regulations-for-use-of-ai-in-courts-invites-inputs)

### Brazylia: prompt injection w pismach procesowych i odpowiedz sadow na manipulowanie systemami AI

W Brazylii najwazniejszym tematem tygodnia byly proby ukrytego manipulowania systemami AI wykorzystywanymi lub potencjalnie wykorzystywanymi przez sady. Chodzi o prompt injection w dokumentach procesowych, np. tekst pisany biala czcionka na bialym tle, niewidoczny dla czlowieka, ale czytelny dla systemu przetwarzajacego dokument.

Folha/BBC News Brasil opisaly przypadek z TJ-SP, w ktorym ukryty tekst mial instruowac agenta AI, aby przyznal bezplatna pomoc sadowa, udzielil zabezpieczenia i zarzadzil cytacje pozwanego. W innych stanach ujawniono podobne przypadki:

- w Para prawniczki zostaly ukarane grzywna ok. 84,2 tys. reali po wykryciu ukrytego polecenia skierowanego do AI;
- w Minas Gerais sedzia nalozyl grzywne 8,1 tys. reali za ukryty prompt w sprawie przeciwko bankowi;
- STJ wszczal wewnetrzne dochodzenie dotyczace prob oszustwa wobec systemow sadu;
- eksperci wskazuja, ze problem moze dotyczyc nie tylko bialego tekstu, ale tez metadanych PDF, ukrytych warstw dokumentu, linkow, zalacznikow i baz orzeczen.

ConJur opisuje te praktyke jako potencjalny akt naruszajacy godnosc wymiaru sprawiedliwosci i integralnosc infrastruktury technologicznej procesu. Odwoluje sie tez do brazylijskiej regulacji CNJ nr 615/2025, zmienionej rezolucja 674 z 25 marca 2026 r., zgodnie z ktora AI w sadownictwie ma miec charakter pomocniczy i komplementarny, a sedzia pozostaje odpowiedzialny za decyzje.

Znaczenie dla sadow: brazylijskie przypadki sa praktycznym ostrzezeniem dla kazdego sadu, ktory wpuszcza modele jezykowe do analizy akt. Oprocz halucynacji pojawia sie ryzyko aktywnego ataku na przeplyw pracy sadu przez sam dokument procesowy. Minimalny zestaw zabezpieczen powinien obejmowac sanitizacje dokumentow, wykrywanie warstw ukrytych, konwersje do kontrolowanego tekstu, blokowanie instrukcji od stron jako polecen dla modelu oraz obowiazkowa weryfikacje ludzka.

Zrodla:

- [Folha / BBC News Brasil - "A tentativa 'invisivel' de manipular a Justica com IA...", 9 czerwca 2026](https://www1.folha.uol.com.br/tec/2026/06/a-tentativa-invisivel-de-manipular-a-justica-com-ia-que-preocupa-tribunais-pelo-brasil-e-so-a-ponta-do-iceberg.shtml)
- [ConJur - "Justica hackeada: prompt injection e a fraude processual na era da IA", 5 czerwca 2026](https://www.conjur.com.br/2026-jun-05/justica-hackeada-prompt-injection-e-a-fraude-processual-na-era-da-ia/)

### Stany Zjednoczone: fala pozwow i pism tworzonych z pomoca AI, spory o poufnosc rozmow z chatbotami

4 czerwca MIT Technology Review opisal, jak sady federalne w USA mierza sie ze wzrostem liczby pism i pozwow przygotowywanych przez osoby niereprezentowane przez prawnikow z pomoca AI. Wedlug przywolanej analizy 4,5 mln federalnych spraw cywilnych z lat 2005-2026 udzial pozwow skladanych przez self-represented litigants wzrosl z 11% w 2022 r. do 16,8% w 2025 r., a liczba pism w tych sprawach ponad dwukrotnie wzrosla wzgledem poziomow sprzed 2023 r. W probie 1600 dokumentow udzial tekstow oznaczonych jako zawierajace tresc wygenerowana przez AI wzrosl z 1% w 2023 r. do 18% w 2026 r.

Sedziowie widza dwa skutki jednoczesnie:

- pozytywny: pisma osob bez adwokata bywaja czytelniejsze i lepiej uporzadkowane;
- negatywny: pojawiaja sie halucynowane sprawy, zle cytaty i nieadekwatne porady prawne.

Artykul wskazuje tez na spor o status rozmow z chatbotami. W jednych sprawach sady uznawaly rozmowy z ChatGPT za work product chroniony przed ujawnieniem, w innych odmawialy ochrony rozmow z Claude, argumentujac, ze chatbot nie jest prawnikiem i uzytkownik nie ma uzasadnionego oczekiwania poufnosci. Pojawiaja sie tez pytania o odpowiedzialnosc za zla porade prawna. Przykladem jest sprawa Nippon Life Insurance przeciw OpenAI, w ktorej zarzucono, ze ChatGPT mial pomagac w ponownym otwieraniu juz rozstrzygnietej sprawy; OpenAI wnosi o oddalenie, twierdzac, ze ChatGPT nie wykonuje zawodu prawnika.

W tle warto odnotowac stanowa reakcje regulacyjna: Sad Najwyzszy Florydy 28 maja zmienil regule 2.515(d)(2), z data wejscia w zycie 15 czerwca 2026 r., wymagajac od podpisujacego pismo oswiadczenia, ze przywolane podstawy prawne istnieja i sa poprawnie cytowane. Regula przewiduje sankcje za naruszenie.

Znaczenie dla sadow: USA pokazuja, ze AI moze realnie zwiekszac dostep do sadu, ale niekoniecznie poprawia wynik procesowy. Najwieksze pytania dotycza poufnosci, odpowiedzialnosci za porade prawnicza, sankcji za halucynowane cytowania oraz obciazenia sedziow dodatkowymi pismami.

Zrodla:

- [MIT Technology Review - "How courts are coping with a flood of AI-generated lawsuits", 4 czerwca 2026](https://www.technologyreview.com/2026/06/04/1138391/courts-coping-ai-lawsuits/)
- [Supreme Court of Florida - In re Amendments to Rule 2.515, 28 maja 2026, skuteczne od 15 czerwca 2026](https://www.workplaceprivacyreport.com/wp-content/uploads/sites/938/2026/05/FL-Supreme-Court-opinion-sc2026-0673-2.pdf)

### Unia Europejska: AI Act klasyfikuje narzedzia dla wymiaru sprawiedliwosci jako wysokiego ryzyka

W tygodniu 3-10 czerwca aktualne pozostaly przygotowania do stosowania AI Act, w tym komunikaty Komisji Europejskiej o wdrazaniu pakietu cyfrowego i harmonogramie stosowania przepisow. Dla sadow najwazniejsze jest to, ze AI Act traktuje systemy uzywane przez organ sadowy lub w jego imieniu do badania i interpretacji faktow oraz prawa oraz stosowania prawa do konkretnego stanu faktycznego jako systemy wysokiego ryzyka.

To oznacza obowiazki dotyczace m.in. zarzadzania ryzykiem, jakosci danych, logowania aktywnosci, dokumentacji technicznej, informacji dla wdrazajacego, nadzoru ludzkiego, odpornosci, cyberbezpieczenstwa i dokladnosci. Jednoczesnie prawo odroznia takie zastosowania od czysto pomocniczych czynnosci administracyjnych, np. anonimizacji dokumentow, komunikacji miedzy personelem czy zadan administracyjnych, ktore nie wplywaja na rozstrzygniecie konkretnej sprawy.

Znaczenie dla sadow: europejski model nie zakazuje AI w sadownictwie, ale podnosi prog zgodnosci dla systemow, ktore realnie wspieraja interpretacje faktow i prawa. To bedzie wazne dla dostawcow legaltechu, administracji sadowej i jednostek publicznych kupujacych narzedzia AI.

Zrodla:

- [Komisja Europejska - AI Act, harmonogram i podejscie risk-based](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [AI Act, Recital 61 - wysokie ryzyko w administracji sprawiedliwosci](https://ai-act-law.eu/recital/61/)
- [AI Act, Annex III - high-risk systems in administration of justice](https://artificialintelligenceact.eu/annex/3/)

### Japonia: Sad Najwyzszy widzi potencjal AI w streszczaniu akt, ale nie w orzekaniu

Choc publikacja Mainichi/Kyodo ukazala sie 31 maja, pozostaje istotnym kontekstem dla ostatniego tygodnia debaty o AI w sadach. Japonski Sad Najwyzszy podsumowal projekt, w ktorym szesciu sedziow sadow dystryktowych testowalo przydatnosc AI do porzadkowania argumentow stron w sprawach cywilnych i streszczania dokumentow procesowych. Testy obejmowaly fikcyjne akta i uslugi AI takie jak Gemini 3 Pro.

Wnioski byly umiarkowane:

- AI moze pomoc w streszczaniu duzych wolumenow dokumentow i dowodow;
- moze wspierac sedziow dolaczajacych do sprawy w trakcie postepowania;
- nie ma zamiaru uzywac AI do wydawania rozstrzygniec zamiast sedziow;
- AI moze pomijac istotne fakty, blednie identyfikowac kwestie sporne i tworzyc pozornie uporzadkowane, ale mylace wyniki;
- sedziowie musza samodzielnie weryfikowac i korygowac output.

Znaczenie dla sadow: Japonia reprezentuje ostrozny model "AI do organizacji akt, nie do decyzji". To podejscie jest zgodne z kierunkiem widocznym w Indiach, UE, Wielkiej Brytanii i Brazylii: AI ma odciazac administracje i research, ale odpowiedzialnosc oraz ocena prawna maja zostac po stronie czlowieka.

Zrodlo:

- [The Mainichi / Kyodo - "Japan top court study sees AI useful in summarizing documents, risks remain", 31 maja 2026](https://mainichi.jp/english/articles/20260531/p2g/00m/0na/006000c)

## Wnioski przekrojowe

1. Najwiekszy trend modelowy tygodnia to przejscie od "najmocniejszego chatbota" do "systemu wykonawczego": Fable 5, Nemotron 3 Ultra, U2, MAI-Code-1-Flash i GPT-Rosalind sa opisywane przez pryzmat dlugich workflow, narzedzi, agentow, pamieci i walidacji.
2. Drugi trend to kontrolowany dostep do najbardziej ryzykownych zdolnosci: Anthropic ogranicza Mythos 5, OpenAI udostepnia GPT-Rosalind przez trusted access, a sady w wielu krajach chca kontrolowanych srodowisk testowych.
3. W prawie i sadownictwie dominujacy konsensus brzmi: AI moze pomagac w researchu, streszczeniach, transkrypcji, tlumaczeniach, zarzadzaniu sprawami i dostepnosci, ale nie powinna samodzielnie orzekac, oceniac winy, ustalac kary, przewidywac recydywy ani oceniac wiarygodnosci stron.
4. Najbardziej praktyczne ryzyko tygodnia to prompt injection w aktach sadowych. Brazylia pokazuje, ze problem nie jest teoretyczny: dokument procesowy moze stac sie wektorem ataku na system AI sadu.
5. Dla instytucji publicznych kluczowe staja sie procedury: rejestry systemow AI, audyty, logi, bazy incydentow, sanitizacja dokumentow, jawne zasady odpowiedzialnosci i szkolenie sedziow oraz pracownikow.
