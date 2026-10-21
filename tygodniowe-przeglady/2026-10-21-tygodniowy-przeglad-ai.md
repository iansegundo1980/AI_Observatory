# Tygodniowy przegląd AI — 21 października 2026

**Okres objęty podsumowaniem:** 14–21 października 2026
**Data publikacji podsumowania:** 21 października 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach wdrażanych w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **7–14 października 2026** i powstał rano 14 października. Niniejszy dokument go nie powtarza: nie wraca do GPT-6 w czacie ChatGPT, Claude Haiku 5.5, publicznego dostępu do Gemini 4 Argon, Muse Wonder, Mellum2.1, Carbon-A, Qwen-Image-2.1-Turbo, sankcji IV DCA Florydy, standing order sędziego Browna, sprawy *United States v. Peplow*, stanowiska sądownictwa Anglii i Walii z 9 października ani liminaru CNJ wobec TRE-GO. Wydarzenia z wieczora 14 października, których tamten przegląd nie zdążył ująć, są tu opisane z jawną datą.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z karty modelu albo z wpisu premierowego. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru i harnessy się nie pokrywają.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Tydzień jest tygodniem wag i stosu inferencyjnego, nie tygodniem nowego zamkniętego modelu czołowego. Meta, NVIDIA, Reflection i DeepSeek wypuściły wagi, które da się pobrać. Mistral złożył osobny stos głosowy. MiniMax obniżył cenę pracy agentowej w API, bez wag. W tym samym oknie Federal Register opublikował — z datą rozkazu z lipca — wyłączenie produktów DeepSeek z cywilnych systemów IT władzy wykonawczej USA.

### 1.1. Meta: wagi Muse Spark Open (15 października 2026)

**15 października 2026** Meta Superintelligence Labs opublikowało wagi **Muse Spark Open**. To natywnie multimodalny model mieszanki ekspertów: **816 mld** parametrów łącznie, **42 mld** aktywnych na token, okno kontekstu **1 mln** tokenów. Wejście obejmuje tekst, obraz, dźwięk i wideo. Wyjście to tekst. Meta opisuje go jako model do kodu i pracy agentowej: długiego horyzontu, inżynierii oprogramowania i rozumowania wielokrokowego. Firma nazywa go najbardziej zdolnym amerykańskim modelem z otwartymi wagami do tej daty. To inne wydanie niż Muse Wonder i Muse Wonder Full z 12 października, które zostały przy API i Muse Code.

Wagi są na Hugging Face (`meta-models`, zbiór Muse Spark Open), w Amazon SageMaker, Google Cloud Model Garden i Microsoft Foundry. Hostowane endpointy w dniu premiery: Baseten, Fireworks AI, Groq, Modal, Nebius, OpenRouter i Together AI. Silniki: SGLang, vLLM, TensorRT-LLM, Transformers, Apple MLX, llama.cpp i Unsloth. Meta pisze, że model tej klasy po raz pierwszy da się uruchomić na biurku: dwa Mac Studio z M5 Ultra i MLX, po **512 GB** zunifikowanej pamięci na maszynę. To konfiguracja podana przez firmę, nie pomiar niezależnego laboratorium.

Licencja to **Muse Model License** z ograniczonymi warunkami komercyjnymi. Meta pisze, że wielu deweloperów może używać modelu bezpłatnie. To nie jest licencja OSI w rodzaju Apache 2.0. Szczegółowe progi przychodu trzeba czytać w pliku licencji, nie w skrócie bloga. W SGLang dołączono jądro Helion; Meta podaje przyspieszenie jąder **1,03–3,95×** na GPU NVIDIA i AMD oraz **3%** przyspieszenia end-to-end na AMD MI350. To liczby vendorskie.

Bezpieczeństwo: Meta oceniała model według własnego Superintelligence Scaling Framework i pisze, że spełnił progi wymagane do wydania. Pełny raport ewaluacji w dniu premiery był zapowiedziany jako „wkrótce”. Karta modelu ma zawierać wyniki szczegółowe. Nie ma tu publicznego progu w stylu kart Preparedness OpenAI.

**Źródła:**

- [Meta AI Research — Introducing Muse Spark Open (15.10.2026)](https://research.meta.ai/blog/muse-spark-open)
- [Hugging Face — Welcome Muse Spark Open (15.10.2026)](https://huggingface.co/blog/meta-muse-spark-open)
- [Hugging Face — kolekcja wag](https://huggingface.co/collections/meta-models/muse-spark-open)

### 1.2. NVIDIA: Nemotron 3.5 Super VL i Bolt (15 października 2026)

**15 października 2026** NVIDIA wydało **Nemotron 3.5 Super VL** oraz **Nemotron 3.5 Bolt 74B-A9B**. Super VL ma **120 mld** parametrów łącznie i **12 mld** aktywnych. Architektura z karty: hybryda Mamba-2, warstw uwagi i mieszanki ekspertów, enkoder wizyjny C-RADIO, natywne spekulatywne dekodowanie przez Multi-Token Prediction. Wejście: tekst, obrazy i wideo. Wyjście: tekst. Kontekst do **1 mln** tokenów. Licencja: **OpenMDW-1.1**. Wagi BF16 karta przeznacza do dopasowania i pełnej precyzji; wariant NVFP4 — do wdrożenia. Data wydania na karcie Build.NVIDIA.com i Hugging Face: **10/15/2026**. Repozytorium BF16: `nvidia/NVIDIA-Nemotron-3.5-Super-VL-120B-A12B-BF16`.

Blog NVIDIA stawia obok Super VL dwa modele brzegowe. **Bolt 74B-A9B** w wariancie 24 GB jest dostępny od razu (llama.cpp, Ollama, LM Studio, Unsloth, vLLM). **Bolt E4B** w wariancie 4 GB NVIDIA zapowiada na **23 października 2026** — w tym przeglądzie to zapowiedź, nie wydanie. Twierdzenia o „5× wyższej przepustowości” i „najszybszym otwartym modelu agentowym w klasie” są z wpisu NVIDIA, bez niezależnego potwierdzenia w tym dokumencie.

Razem z modelem NVIDIA publikuje otwarte zbiory do dotrenowania (narzędzia, finanse, instrukcje, długi kontekst, fairness, język-wizja) oraz środowiska uczenia ze wzmocnieniem w NeMo Gym. Karta mówi o ok. **26 bln** tokenów pretreningu i dalszego pretreningu oraz ok. **3,8 mln** próbek post-treningu. To skala podana przez producenta.

**Źródła:**

- [NVIDIA Blog — Nemotron 3.5 Super VL i Bolt (15.10.2026)](https://blogs.nvidia.com/blog/nemotron-3-5-super-vl/)
- [NVIDIA Developer — opis architektury (15.10.2026)](https://developer.nvidia.com/blog/nvidia-nemotron-3-5-super-vl-powers-specialized-agents-with-multimodal-reasoning/)
- [Karta modelu NVFP4 na build.nvidia.com](https://build.nvidia.com/nvidia/nemotron-3-5-super-vl-120b-a12b/modelcard)
- [Hugging Face — NVIDIA-Nemotron-3.5-Super-VL-120B-A12B-BF16](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Super-VL-120B-A12B-BF16)

### 1.3. Reflection: wagi Beam 1.0 na Apache 2.0 (16 października 2026)

Przegląd z 14 października odnotował zapowiedź **Beam** z **5 października** i brak wag. **16 października 2026** Reflection opublikowało wagi na Hugging Face na licencji **Apache 2.0**. To pierwszy otwartowagowy model firmy. Architektura: rzadka mieszanka ekspertów, **501 mld** parametrów łącznie (**501,3 mld** w tabeli karty), **23 mld** aktywnych (**23,4 mld**), **52** warstwy (3 gęste i 49 MoE), **256** ekspertów, kontekst **1 mln** tokenów, słownik **152 tys.**, odcięcie wiedzy **30 czerwca 2026**. Modalność: tekst na tekst. Formaty: BF16, FP8 i NVFP4 oraz model szkicujący do spekulatywnego dekodowania. Identyfikator: `Beam-1.0-501B-A23B`. Repozytorium Hugging Face ma datę ostatniej modyfikacji **16 października 2026**.

Reflection nazywa wydanie „otwartym systemem operacyjnym dla agentów”: wagi, kontenery, integracje inferencji i ścieżki dopasowania. W dniu premiery model jest m.in. w AWS, Google Cloud, Microsoft Foundry, Cloudflare, CoreWeave, Databricks, Fireworks, Together, OpenRouter, NVIDIA NIM, Ollama i LM Studio oraz, za zaporą, u Della i HPE. Harness **Mirror CLI** jest otwierany razem z modelem; Beam był też sprawdzany z Pi, OpenCode i Hermes. Licencja, według karty, nie zabrania destylacji, dotrenowania ani dobrowolnej ewaluacji odpornościowej systemów, do których ma się uprawnienie.

Liczby z karty, wszystkie vendorskie, temperatura **0,7**, top_p **0,99**, kolumna BF16:

| Zadanie | Beam BF16 |
| --- | --- |
| SWE-bench Verified | 81,6% |
| SWE-bench Pro v1 | 66,1% |
| Terminal Bench v2.1 | 80,1% |
| DeepSWE v1.1 | 43,3% |
| HLE bez narzędzi | 36,0% |
| HLE z narzędziami | 51,1% |
| GPQA Diamond | 90,6% |
| MCP Atlas | 80,8% |

Te procenty nie są porównywalne jeden do jednego z tabelą DeepSeek poniżej: inne harnessy i inne daty. W ewaluacji bezpieczeństwa Iris (vendorska) wskaźnik odmowy na żądaniach szkodliwych dla BF16 wynosi **88,9%**, a zgodność na żądaniach nieszkodliwych **81,5%**. Szczegóły metodologii: raport bezpieczeństwa Beam.

**Źródła:**

- [Reflection — Beam is now available (16.10.2026)](https://reflection.ai/blog/beam-is-available)
- [Reflection — karta modelu](https://reflection.ai/beam-model-card)
- [Hugging Face — reflection/Beam-1.0-501B-A23B](https://huggingface.co/reflection/Beam-1.0-501B-A23B)
- [Dokumentacja wag](https://developers.reflection.ai/serving-weights)

### 1.4. DeepSeek: V4.1-Flash-1017, DeepInfer i amerykański rozkaz, który dopiero teraz wszedł do rejestru

**17 października 2026** DeepSeek wydało **DeepSeek-V4.1-Flash-1017**. Karta na Hugging Face nazywa to mniejszą aktualizacją V4.1-Flash z września: krótsze odpowiedzi, szybsze domknięcie zadania i wyższe wyniki na własnych testach. Wagi są na Hugging Face i ModelScope na licencji **MIT**. Repozytorium `deepseek-ai/DeepSeek-V4.1-Flash-1017` powstało **17 października 2026**. Nazwa API `deepseek-flash` wskazuje teraz na tę wersję; sposób wywołania, według wpisu, się nie zmienia. Jest też referencyjna implementacja kodowania promptu. Osobno firma otworzyła API Search i Fetch: **0,75 USD za 1000 wywołań**. Wywołania tych narzędzi po stronie serwera w DeepSeek Harness, Claude Code i Codex są do **31 października 2026, 16:00 UTC** bezpłatne dla użytkowników API DeepSeek; potem wchodzi cennik.

Tabela z README modelu. Harness: Claude Code dla Terminal-Bench 4.0, Mini-SWE-V2 dla DeepSWE v1.1. Krzyżyk przy HLE oznacza podzbiór tekstowy. Kolumny porównawcze są z tej samej tabeli DeepSeek, nie z niezależnego rankingu.

| Benchmark | 1017 | V4.1-Flash (poprzedni) |
| --- | --- | --- |
| HLE bez narzędzi | 42,6 (44,0†) | 36,8 (39,1†) |
| Terminal-Bench 4.0 | 42,3 | 31,2 |
| DeepSWE v1.1 | 77,0 | 74,2 |
| ProgramBench | 29,1 | 20,3 |
| NL2Repo-Bench | 68,2 | 65,4 |
| Automation-Bench v1.0.6 | 60,5 | 54,8 |

**20 października 2026** DeepSeek opublikowało **DeepInfer**, własny silnik inferencji używany w produkcji, oraz komponent **deepseek-recipe**. Repozytorium `deepseek-ai/DeepInfer` jest na **Apache 2.0**. README mówi, że wydanie obejmuje inferencję offline dla DeepSeek-V4.1-Flash: jądra, równoległość uwagi i ekspertów, spekulatywne dekodowanie (DSpark), SWA bounded replay, szeregowanie asynchroniczne, wyjścia strukturalne oraz — na NVIDIA — inferencję niezmienniczą względem batcha i deterministyczne próbkowanie. Sprzęt w tym wydaniu: GPU NVIDIA **SM100** i NPU Huawei **Ascend 950**. README wprost wylicza, czego nie ma: systemu cache KV, rozdzielenia prefill/decode jako gotowej usługi oraz równoważenia obciążenia między replikami. To nie jest kompletny serwis, tylko rdzeń, na którym DeepSeek mówi, że sam serwuje V4.1-Flash. Kod wyrósł głównie z vLLM, z inspiracji SGLang i TensorRT-LLM.

Tego samego tygodnia Departament Bezpieczeństwa Krajowego USA opublikował w **Federal Register** z **20 października 2026** (dokument **2026-21447**, **91 FR 66346**, złożony **19 października**) zawiadomienie o rozkazie wydanym na podstawie Federal Acquisition Supply Chain Security Act z 2018 r. (41 U.S.C. 1321–1328). Rozkaz (1) wyłącza z zamówień cywilnych agencji federalnych produkty i usługi IT spółki Hangzhou DeepSeek Artificial Intelligence Co., Ltd. i podmiotów powiązanych w rozumieniu 48 CFR 2.101 oraz (2) nakazuje usunięcie z cywilnych systemów IT produktów DeepSeek i podmiotów powiązanych, a także produktów i usług stron trzecich wytworzonych z użyciem implementacji DeepSeek. Skan podpisanego rozkazu w załączniku do ogłoszenia nosi datę **24 lipca 2026**. HTML zawiadomienia sam tej daty nie powtarza; data lipcowa jest na reprodukcji podpisu. To publikacja rozkazu sprzed kwartału, nie nowy rozkaz z 20 października. Zakres tekstu rejestru to cywilna władza wykonawcza, nie Departament Obrony. Dla zespołów, które w tym tygodniu dostały wagi MIT i kod DeepInfer, rozkaz dotyczy zakupów i systemów agencji cywilnych oraz produktów zbudowanych na implementacjach DeepSeek, nie samego faktu, że wagi leżą na Hugging Face.

**Źródła:**

- [DeepSeek API Docs — DeepSeek-V4.1-Flash-1017 (17.10.2026)](https://api-docs.deepseek.com/news/news261017)
- [Hugging Face — DeepSeek-V4.1-Flash-1017](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017)
- [GitHub — deepseek-ai/DeepInfer](https://github.com/deepseek-ai/DeepInfer)
- [GitHub — deepseek-ai/deepseek-recipe](https://github.com/deepseek-ai/deepseek-recipe)
- [Federal Register — zawiadomienie DHS, 20.10.2026, 91 FR 66346](https://www.federalregister.gov/documents/2026/10/20/2026-21447/notice-of-order-regarding-exclusion-and-removal-of-deepseek-products-from-federal-civilian-executive)
- [API JSON tego samego dokumentu](https://www.federalregister.gov/api/v1/documents/2026-21447.json)

### 1.5. MiniMax: M3.1 Flash w API (19 października 2026)

**19 października 2026** MiniMax wprowadziło **MiniMax M3.1 Flash** do API, planu M i MiniMax Code. Firma pisze, że wcześniejsza anonimowa usługa „Space Bunny”, która przetworzyła ponad **200 bln** tokenów, była wczesną wersją tego modelu. Cena płaska za 1 mln tokenów: **0,15 USD** wejścia, **0,60 USD** wyjścia, **0,015 USD** wejścia z cache. MiniMax podaje niemal trzykrotnie szybszą inferencję online wobec poprzednika, ponad **200** tokenów na sekundę w typowym użyciu (mediana ponad **170**) oraz **70%** niższy koszt zadań agentowych. Wagi w wpisie z 19 października nie spadły; firma pisze, że ukażą się później.

Liczby z wpisu MiniMax, vendorskie: DeepSWE v1.1 **73,7%**, OSWorld V2 **61,7**, Agents’ Last Exam **29,6**, BankerToolBench **76,2**, CyberGym **82%**. Dokumentacja platformy z tego samego dnia zapowiada wycofanie rodzin M2.5 i M2.7: od 19 października niedostępne dla nowych użytkowników, koniec życia **18 listopada 2026**. W planach M i Token Plan stare nazwy od 19 października są kierowane na M3.1 Flash.

**Źródła:**

- [MiniMax — M3.1 Flash (19.10.2026)](https://www.minimax.io/blog/minimax-m31f)
- [MiniMax IR — ta sama premiera](https://ir.minimax.io/news-events/new-releases)
- [Dokumentacja modeli i harmonogram wycofania M2.5/M2.7](https://platform.minimax.io/docs/faq/models)

### 1.6. Mistral: Voxtral 3, stos głosowy (20 października 2026)

**20 października 2026** Mistral wydało **Voxtral 3**: modele mowy i SDK agenta głosowego, który w jednym strumieniu słucha, rozumuje, woła narzędzia i mówi. Transkrypcja **Voxtral Small Transcribe 3** obejmuje ponad **50** języków, w tym 24 języki urzędowe UE, z diaryzacją, context biasing i detekcją końca wypowiedzi. **Voxtral Mini Transcribe 3** ma **4 mld** parametrów. TTS **Voxtral Mini TTS 3** / **Voxtral Speech 3** obejmuje ponad **35** języków i ponad **50** dialektów. Osobno jest tryb realtime. **Pro Voice** dopasowuje głos mówcy z około **30 minut** próbek. SDK stoi na LiveKit: osobny model słucha, model ogólny (w cenniku przykładowo Mistral Small) rozumuje, model mowy odpowiada. Mistral pisze, że tura mieści się poniżej sekundy i że agenta można postawić na API hostowanym w UE albo na własnej infrastrukturze.

Cennik z tabeli na stronie premiery:

| Element | Cena |
| --- | --- |
| Voxtral Mini Transcribe 3, batch | 0,0035 USD / min |
| Voxtral Mini Transcribe Realtime 3 | 0,008 USD / min |
| Voxtral Small Transcribe 3 | 0,0040 USD / min |
| Voxtral Speech 3 | 13 USD / 1 mln znaków |
| Agent głosowy z Mistral Small 4 | 0,04 USD / min |
| Agent głosowy z innym modelem rozumującym | 0,08 USD / min |

Twierdzenia o wygranej z Whisperem, Scribe v2 i Gemini 3.5 Transcribe są z wykresów Mistrala. Ten przegląd nie przepisuje z nich procentów błędu słów, bo wartości siedzą w grafikach, nie w tabeli tekstowej.

**Źródła:**

- [Mistral — Voxtral 3 (20.10.2026)](https://mistral.ai/news/voxtral-3/)
- [Dokumentacja — Voxtral Small Transcribe 3, data wydania 2026-10-20](https://docs.mistral.ai/models/voxtral-small-transcribe-3-0.md)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie nie ma jednego wyroku, który zmienia standard dla pełnomocników na kilku kontynentach. Jest za to wdrożeniowy list intencyjny w Polsce, nowe materiały dla sędziów w Kanadzie, raport zarządczy sądów Idaho, wejście w życie australijskich obowiązków stron, studium brytyjskiego urzędu kontroli o transkrypcji w probation oraz pozwy ośmiu stanów USA przeciwko OpenAI. Obok nich stoi orzeczenie apelacyjne w Indianie o sfabrykowanych cytatach — bez ustalenia, że powstały w generatorze — oraz krótkie oddalenie wisconsińskiej petycji o rozdział regulaminu poświęcony AI.

### 2.1. Polska: list intencyjny NSA i Ministerstwa Cyfryzacji (20 października 2026)

**20 października 2026** Naczelny Sąd Administracyjny i Ministerstwo Cyfryzacji podpisały list intencyjny o współpracy przy AI w sądownictwie administracyjnym. To nie jest uruchomienie systemu orzeczniczego. Komunikat NSA opisuje dwa kroki.

Najpierw pilotaż **Asystenta Urzędniczego AI**, narzędzia Ministerstwa Cyfryzacji dla administracji. **30** pracowników NSA, nazwanych ambasadorami, ma sprawdzić streszczanie i porównywanie dokumentów, projekty pism, wyszukiwanie przepisów i anonimizację. Każdy dokument wytworzony przez AI ma być sprawdzony i zatwierdzony przez sędziego. Na podstawie pilotażu ma powstać **Asystent AI Sędziego Sądu Administracyjnego**, pod pracę sędziego i asystenta oraz pod akta spraw. Ministerstwo ma udostępniać NSA i pozostałym sądom administracyjnym kolejne wersje asystenta urzędniczego przy wsparciu modelu **PLLuM**. NSA udostępni NASK orzeczenia z Centralnej Bazy Orzeczeń Sądów Administracyjnych wyłącznie po to, by doskonalić narzędzia. Komunikat mówi o dobrowolności i przejrzystości.

Prezes NSA Jacek Chlebny w cytacie na stronie sądu odróżnia test „AI Urzędnika” od docelowego asystenta sędziego. Wicepremier i minister cyfryzacji Krzysztof Gawkowski mówi o przejściu z papieru na cyfrę bez odbierania roli człowieka na końcu procesu. W tym oknie nie opublikowano nowego orzeczenia polskiego sądu o halucynacjach ani nowego aktu wokół KRiBSI.

**Źródła:**

- [NSA — Asystent AI dla sędziów, PLLuM (20.10.2026)](https://www.nsa.gov.pl/aktualnosci/wydarzenia/sztuczna-inteligencja-wesprze-sadownictwo-administracyjne-asystent-ai-dla-sedziow-pllum-w-naczelnym-sadzie-administracyjnym/)

### 2.2. Kanada: wytyczne Rady Sądownictwa i dowód cyfrowy (ogłoszenie 20 października 2026)

**20 października 2026** Canadian Judicial Council opublikowało dwa materiały przygotowane przez komitet technologiczny rady. Przewodniczący, prezes Sądu Najwyższego Richard Wagner, mówi w komunikacie, że sędziowie mają używać AI zgodnie z obowiązkami zawodowymi i rozumieć skutki dla postępowania oraz dowodów.

Pierwszy materiał to drugie wydanie *Guidelines for the Use of Artificial Intelligence in Canadian Courts*. Komunikat — i tylko on, bo osobny PDF drugiego wydania w dniu tego przeglądu nie został odczytany z trwałego adresu publikacji z 2024 r. — zapowiada jaśniejszy podział użyć dozwolonych, granicznych i niedozwolonych, mocniejszy nadzór sędziego oraz zarządzanie AI w administracji sądowej. Starszy PDF z września 2024 r. nadal wisiał pod dotychczasowym adresem publikacji. Nie należy czytać tamtego pliku jako tekstu drugiego wydania.

Drugi materiał udało się otworzyć: *Guidance for Canadian Judges on Evaluating Digital Media Evidence*, **26** stron, data na okładce **wrzesień 2026**, ogłoszony 20 października. Cel: pomoc sędziemu, gdy dowód w postaci mediów cyfrowych mógł zostać wytworzony albo istotnie zmieniony narzędziami generatywnymi, także gdy strony tego nie podnoszą, a dowód i tak wymaga uwierzytelnienia. Spis obejmuje „deepfake defence” i „liar’s dividend”, rozróżnienie dowodu, przy którym użycie AI jest przyznane, sporne albo tylko pośrednie, oraz listy kontrolne: cel dowodu, proces, dane wejściowe, waga wyniku, uprzedzenie, biegły, pochodzenie i łańcuch custody. To materiał edukacyjny rady, nie wyrok w konkretnej sprawie.

**Źródła:**

- [CJC — komunikat, 20.10.2026](https://cjc-ccm.ca/en/news/canadian-judicial-council-publishes-new-guidance-judges-artificial-intelligence)
- [CJC — Guidance for Canadian Judges on Evaluating Digital Media Evidence (PDF, okładka: wrzesień 2026)](https://cjc-ccm.ca/en/resources-center/publications/guidance-canadian-judges-evaluating-digital-media-evidence)

### 2.3. Stany Zjednoczone, Idaho: raport o zarządzaniu AI w sądach stanowych (19 października 2026)

**19 października 2026** Sąd Najwyższy Idaho opublikował komunikat o raporcie **AI Governance Implementation**. Grupa sędziów, adwokatów, informatyków i administratorów przez rok, z udziałem National Center for State Courts, opisywała, kiedy sądy stanowe mogą używać AI do pracy urzędu. Raport niczego nie wdraża i żadnego narzędzia nie wskazuje. Zasady — etyka, przejrzystość, rozliczalność, nadzór człowieka, prowadzenie narzędzia przez osoby, które wykonują daną pracę — sąd przyjął wcześniej w tym roku. Nowością 19 października jest sam raport i propozycja stałego komitetu doradzającego Sądowi Najwyższemu, a na prośbę stanowej palestry także przy regułach dla adwokatów. Decyzje zostają przy sądzie, który administruje władzą sądowniczą. Zespół zwołał były prezes G. Richard Bevan. W cytacie z komunikatu mówi, że sądy mają być sądami zasad, nie algorytmów.

**Źródła:**

- [Idaho Supreme Court — Report Examines AI Use by Idaho Courts (19.10.2026)](https://isc.idaho.gov/news-article/report-examines-ai-use-by-idaho-courts)

### 2.4. Australia: obowiązki Fair Work Commission wchodzą w życie (20 października 2026)

Wytyczne Fair Work Commission o generatywnej AI w sprawach przed komisją zostały ogłoszone **24 sierpnia 2026** i od **20 października 2026** obowiązują. To nie jest nowy dokument z tego tygodnia. To data, od której strony mają je stosować. Poprzednie przeglądy odnotowały zapowiedź i nie traktowały jej jako wydarzenia z 7–14 października. Tu liczy się skutek.

Gdy GenAI tworzy, pisze, redaguje albo inaczej przygotowuje dokument, strona musi: powiedzieć, że i jak użyła GenAI; sama sprawdzić, że treść jest prawdziwa, istotna i oparta na rzeczywistych dowodach oraz autoritetach; napisać w dokumencie, że te sprawdzenia zrobiła. Przy zeznaniu lub oświadczeniu świadek albo składający oświadczenie ma dodatkowo upewnić się, że tekst wynika z jego wiedzy, oddaje jego słowa i jest prawdziwy według jego najlepszej wiedzy. Pełnomocnicy zawodowi w dokumentach przygotowanych z GenAI mają podawać hiperłącza do przywołanego orzecznictwa. Formularze wniosku i odpowiedzi miały zostać zaktualizowane do 20 października.

**Źródła:**

- [Fair Work Commission — Use of AI in Commission cases (ogłoszenie 24.08.2026, skutek 20.10.2026)](https://www.fwc.gov.au/about-us/news-and-media/news/use-ai-commission-cases)
- [Fair Work Commission — Using AI to help you with your case](https://www.fwc.gov.au/genai)

### 2.5. Wielka Brytania: NAO o Justice Transcribe w probation (sesja 14 października 2026)

National Audit Office złożyło studium przypadku **HC 615**, sesja 2026–27, data na okładce **14 października 2026**. Kontroler podpisał raport **6 października**, Izba Gmin zleciła druk **13 października**. Poprzedni przegląd, zamykany rano 14 października, tego dokumentu nie opisywał. Narzędzie nie startuje w tym tygodniu. Studium dotyczy już przeprowadzonego wdrożenia.

**Justice Transcribe** transkrybuje i streszcza spotkania dozoru probacyjnego. Pomysł wyszedł od funkcjonariuszy pierwszej linii. Ministerstwo Sprawiedliwości i HM Prison and Probation Service nie budowały modelu od zera: jednostka Justice AI dostosowała **Minute**, narzędzie transkrypcji ze służby i.AI w Government Digital Service. W pilotażu wzięło udział **40** funkcjonariuszy. Potem, między lutym a marcem 2026, narzędzie dostało około **11 000** osób personelu probation. Między **7 października 2025** a **14 września 2026** narzędzie obsłużyło ponad **1,6 mln** spotkań. HMPPS szacuje około **266 667** zaoszczędzonych godzin i prognozuje około **450 000** godzin rocznie. Służba prowadzi około **3,7 mln** spotkań dozoru rocznie. NAO zapisuje też ryzyko z pilotażu: poleganie na streszczeniu bez wystarczającego sprawdzenia. We wdrożeniu są przypomnienia, żeby funkcjonariusz przejrzał i poprawił streszczenie, zanim trafi do krajowego systemu spraw. Dalszy krok, już po rolloutcie, to wpięcie narzędzia w kontrolę jakości, w tym dokładność wyjścia modelu i zmianę zachowania ludzi w czasie.

**Źródła:**

- [NAO — strona studium](https://www.nao.org.uk/insights/productivity-improvement-the-justice-transcribe-ai-enabled-transcription-tool/)
- [NAO — PDF, HC 615 (14.10.2026)](https://www.nao.org.uk/wp-content/uploads/2026/10/Productivity-improvement-the-Justice-Transcribe-AIenabled-transcription-tool.pdf)

### 2.6. Stany Zjednoczone: pozwy ośmiu stanów przeciwko OpenAI (14 października 2026)

**14 października 2026** prokurator generalna Iowy Brenna Bird złożyła w Sądzie Okręgowym hrabstwa Polk pozew *State of Iowa ex rel. Brenna Bird v. OpenAI Global, LLC* i innych spółek grupy. Petycja jest datowana tego dnia. Podstawa: Iowa Consumer Fraud Act, Iowa Code § 714.16. To zarzuty stanu, nie ustalenia sądu. Żaden wyrok w tej sprawie w tym oknie nie zapadł.

Żądania z sentencji petycji, skrót: stwierdzenie wprowadzających w błąd praktyk; kara cywilna do **40 000 USD** za każde naruszenie i dodatkowo do **5 000 USD**, gdy naruszenie dotyczy osoby starszej; usunięcie danych mieszkańców Iowy pozyskanych przed wyrokiem; zwrot świadczeń konsumentom; wydanie przychodu z zakwestionowanych praktyk; zakaz dalszego wprowadzania w błąd co do cech ChatGPT; zakaz zbierania i sprzedaży wrażliwych danych bez weryfikacji wieku, jasnej informacji i wyraźnej zgody; oraz zakaz dalszych testów zaawansowanych modeli, dopóki zabezpieczenia nie zostaną wdrożone i potwierdzone przez niezależnych kontrolerów. Ostatni punkt jest wnioskiem o zabezpieczenie, nie obowiązującym zakazem.

Tego samego dnia własne pozwy zapowiedzieli lub złożyli prokuratorzy generalni Kansas (Kris Kobach), Nebraski (Mike Hilgers) i Wirginii Zachodniej (JB McCuskey). Iowa Capital Dispatch, relacjonując konferencję w kapitolu stanu, wymienia także Arkansas, Arizonę, Idaho i Montanę jako stany pozywające OpenAI we własnych sądach stanowych za wprowadzające w błąd twierdzenia o bezpieczeństwie ChatGPT. Petycja Iowy przywołuje cudze sprawy i doniesienia o szkodach, w tym wobec dzieci. Ten przegląd nie streszcza opisów tych szkód. Do czasu wyroku pozostają twierdzeniami pozwu.

**Źródła:**

- [Petycja Iowy, PDF, 14.10.2026](https://www.iowaattorneygeneral.gov/media/cms/261014_Petition_EC459B522F957.pdf)
- [Iowa Capital Dispatch — konferencja prokuratorów, 14.10.2026](https://iowacapitaldispatch.com/2026/10/14/iowa-attorney-general-brenna-bird-other-ags-move-to-sue-openai-in-state-courts/)

### 2.7. Indiana: sfabrykowane cytaty i koszty apelacyjne, bez ustalenia co do AI (14 października 2026)

**14 października 2026** Court of Appeals of Indiana wydał opinię w sprawie *Stacia Davis v. Robert York i in.*, sygn. **25A-PL-1882**. Strona skarżąca działała sama. Sąd utrzymał wyrok o ważności testamentu i zasądzone w pierwszej instancji **22 208,18 USD** kosztów pełnomocnika specjalnego administratora, płatnych przez Davis. Ta kwota dotyczy ustalenia złej wiary w sporze spadkowym, nie cytatów.

Osobno, na wniosek przeciwnika z Appellate Rule **66(E)**, sąd zasądził koszty apelacyjne i przekazał sądowi pierwszej instancji ustalenie ich wysokości. Uzasadnienie: apelacja jest przeniknięta bezzasadnością oraz złą wiarą proceduralną i materialną. Materialnie sąd pisze, że przywołane autorytety są albo sfabrykowane, albo nie potwierdzają tez. Przykład nieistniejącego cytatu z uzasadnienia: „T.R. v. G.T., 82 N.E.3d 319 (Ind. Ct. App. 2017)”. W odpowiedzi na apelację sąd wymienia sześć dalszych cytatów, przy których sprawa podana przez skarżącą nie istnieje, w tym „Estate of Rickert v. Robinson, 871 N.E.2d 1039 (Ind. Ct. App. 2007)”.

Opinia nie nazywa narzędzia i nie stwierdza, że cytaty powstały w modelu generatywnym. Bazy spraw o halucynacjach klasyfikują ją jako użycie domniemane. Ten przegląd zostawia przy tekście sądu: sfabrykowane i nietrafione cytaty, koszty apelacyjne w wysokości do ustalenia, brak imiennego ustalenia co do AI.

**Źródła:**

- [Court of Appeals of Indiana — opinia 25A-PL-1882 (14.10.2026)](https://public.courts.in.gov/Decisions/api/Document/Opinion?Id=Jot9nW-v1EdqggqqctGHB0ij5t2yuPoi8flVdram4Gw3GeCrPeISske6-EHQ3qE40)

### 2.8. Wisconsin: oddalenie wycofanej petycji o rozdział regulaminu (15 października 2026)

**15 października 2026** Sąd Najwyższy Wisconsin oddalił petycję regulaminową **26-02**, *In re Creation of SCR Ch. 76, Use of Generative Artificial Intelligence in Court Proceedings*. Jay Stone wniósł ją **19 lutego 2026** i **30 września 2026** wniósł o jej cofnięcie. Postanowienie z 15 października wniosek uwzględnia i petycję oddala. Żaden nowy rozdział 76 z tej petycji nie powstaje. Osobna petycja **26-06**, o regułach 76.20–76.24 i równym dostępie do narzędzi AI, została złożona **28 września 2026** i w tym oknie pozostaje w toku. To nie jest nowe prawo z 15 października.

**Źródła:**

- [Postanowienie, petycja 26-02 (15.10.2026, PDF)](https://www.wicourts.gov/sc/rulhear/DisplayDocument.pdf?content=pdf&seqNo=1192324)
- [Wykaz postanowień Sądu Najwyższego Wisconsin](https://www.wicourts.gov/scrules/orders.htm)
- [Petycje w toku, w tym 26-06 z 28.09.2026](https://www.wicourts.gov/scrules/pending.htm)

---

## Jak czytać ten tydzień

Po stronie modeli ciężar przesunął się na wagi, które da się postawić u siebie: Muse Spark Open na licencji Mety, Nemotron 3.5 Super VL na OpenMDW, Beam na Apache 2.0 i poprawka DeepSeek na MIT, razem z niepełnym, ale produkcyjnym silnikiem DeepInfer. Obok nich stoją tańszy Flash MiniMax bez wag i europejski stos głosowy Mistrala. Ten sam tydzień pokazuje granicę polityczną: lipcowy rozkaz DHS wobec DeepSeek został ogłoszony w rejestrze federalnym dopiero 20 października i obejmuje także produkty stron trzecich zbudowane na implementacjach tej firmy w cywilnych systemach federalnych.

Po stronie sądów powtarza się ten sam podział ról. NSA, Idaho, Kanada, Australia i brytyjski probation biorą AI do streszczeń, dowodu i administracji pod warunkiem, że człowiek zatwierdza wynik albo przynajmniej odpowiada za akt. Pozwy stanowe przeciwko OpenAI są na razie żądaniami prokuratorów, nie standardem orzeczniczym. Opinia z Indiany podnosi koszt sfabrykowanego cytatu, nie nazywając generatora.
