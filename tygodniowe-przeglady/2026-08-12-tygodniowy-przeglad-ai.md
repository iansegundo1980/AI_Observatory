# Tygodniowy przegląd AI — 12 sierpnia 2026

**Okres objęty podsumowaniem:** 5–12 sierpnia 2026  
**Data publikacji podsumowania:** 12 sierpnia 2026  
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach wdrażanych w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

### 1.1. Meta: Muse Spark 1.2 i terminalowy agent Muse Code (5 sierpnia 2026)

Meta wypuściła **Muse Spark 1.2** — aktualizację modelu frontierowego ukierunkowaną na kodowanie — oraz **Muse Code** (beta), terminalowego agenta kodującego napędzanego tym modelem. Według firmy model i harness były **współtrenowane**: trajektorie harnessu, kompaktowanie kontekstu, cele oraz subagenty zostały wplecione w trening, by poprawić generowanie kodu, debugowanie i zrozumienie dużych repozytoriów.

Muse Code ma prowadzić długie projekty (w tym generowanie całych repozytoriów), uruchamiać wiele subagentów równolegle i zachowywać dziennik działań, dzięki czemu po awarii może wznowić pracę zamiast zaczynać od zera. Muse Spark 1.2 jest dostępny w Muse Code oraz w Meta Model API (m.in. wariant z wyższą ceną bez użycia promptów do poprawy produktów). Niezależne źródła ostrzegają, że headline’owe wyniki na Terminal-Bench 2.1 pochodzą z harnessu Meta i nie mają jeszcze niezależnej weryfikacji na oficjalnej tablicy wyników.

**Źródła:**
- [Introducing Muse Code and Muse Spark 1.2 — Meta AI Research](https://research.meta.ai/blog/introducing-muse-code-and-muse-spark-1-2)
- [Reuters — Meta launches Muse Code powered by Muse Spark 1.2](https://www.reuters.com/technology/meta-launches-new-ai-coding-tool-powered-by-muse-spark-12-2026-08-05/)
- [VentureBeat — Meta enters the AI coding wars with Muse Spark 1.2 and Muse Code](https://venturebeat.com/orchestration/meta-enters-the-ai-coding-wars-with-muse-spark-1-2-and-muse-code-with-persistent-async-background-agents)
- [Kingy.ai — weryfikacja benchmarków Muse Spark 1.2](https://kingy.ai/blog/muse-code-muse-spark-1-2-benchmarks-verified/)

### 1.2. Meta open-sourcuje Muse Glimmer — lokalny model agentyczny 30B (10 sierpnia 2026)

**Meta Superintelligence Labs** opublikowało **Muse Glimmer**: otwarty, multimodalny model o ok. **30 mld parametrów**, destylowany z linii Muse Spark i wydany na licencji **Apache 2.0**. Model jest zaprojektowany pod **zawsze włączone lokalne agentów**: wywołania narzędzi, kodowanie lokalne, długie sesje oraz LLM-as-a-judge — z możliwością działania na pojedynczym konsumenckim GPU lub Macu, bez wymogu chmury.

Architektura obejmuje dedykowany enkoder percepcji (~1,8B ViT), kontekst **131k+**, wejście tekst+obraz i wyjście tekstowe. Meta dołącza kwantyzację (ok. 4-bit) oraz **DFlash** (spekulatywne dekodowanie), by osiągnąć płynną interakcję lokalną. Wagi są na Hugging Face; integracje z llama.cpp, MLX, ExecuTorch, Ollama, LM Studio i partnerami inference mają dojść w kolejnych dniach. To pierwsze otwarte wydanie wagowe Meta Superintelligence Labs po zamkniętej fazie Muse Spark.

**Źródła:**
- [Introducing Muse Glimmer — Meta AI Research](https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model)
- [Hugging Face Blog — Muse Glimmer](https://huggingface.co/blog/muse-glimmer)
- [meta-models/Muse-Glimmer-30B — Hugging Face](https://huggingface.co/meta-models/Muse-Glimmer-30B)
- [MarkTechPost — Muse Glimmer 30B na jednym GPU](https://www.marktechpost.com/2026/08/10/meta-ai-releases-muse-glimmer/)

### 1.3. Anthropic: Claude poprawia dolne ograniczenie związane z hipotezą Riemanna (10 sierpnia 2026)

Anthropic ogłosiło, że **nieopublikowana wersja badawcza Claude** — w toku nieudanej próby podejścia do hipotezy Riemanna — poprawiła długoletnie **dolne ograniczenie** na udział zer funkcji zeta Riemanna leżących na linii krytycznej: z **41,6%** do **67,2%**. Wynik nie dowodzi hipotezy Riemanna; wzmacnia gwarancję matematyczną dotyczącą odsetka zer spełniających warunek hipotezy.

Według Anthropic model pracował w Claude Code (m.in. dziesiątki milionów tokenów wyjściowych, subagenci, skrypty i przegląd literatury z arXiv). Matematycy Anthropic zweryfikowali argument; zewnętrzni teorio-liczbowcy **Brian Conrey** i **Dan Goldston** przejrzeli pracę; Claude przygotował też wersję formalną w **Lean**. Firma podkreśla, że nie oczekuje, by te techniki doprowadziły do pełnego dowodu hipotezy.

**Źródła:**
- [Learning more about Claude's mathematical capabilities — Anthropic](https://www.anthropic.com/research/riemann-zeta)
- [PDF — More than two thirds of the zeros… (Claude / Anthropic)](https://www-cdn.anthropic.com/564f962e60643842f5fcb4a17c9dbc8f608f1c37.pdf)
- [The AI Insider — Claude improved Riemann-related bound](https://theaiinsider.tech/2026/08/11/anthropic-says-claude-improved-a-longstanding-bound-tied-to-the-riemann-hypothesis/)

### 1.4. NVIDIA: Nemotron 3.5 Lightning i NeMo Switchyard (11 sierpnia 2026)

NVIDIA wypuściła **Nemotron 3.5 Lightning** — otwarty model MoE o ok. **30B** parametrach z **~3B aktywnymi**, zoptymalizowany pod **wysoką przepustowość i niskie opóźnienie** w długotrwałych agentach. Architektura hybrydowa łączy Mamba-2, MoE i attention; okno kontekstu sięga **1 mln tokenów**. Dostępne są checkpointy **BF16** i **NVFP4**, a także metody spekulatywnego dekodowania (m.in. MTP, DFlash, DSpark).

Równolegle firma przedstawia **NeMo Switchyard** — bibliotekę routującą zadania do modelu najlepiej dopasowanego do kroku workflow (lokalnie lub w chmurze). Lightning jest pozycjonowany jako warstwa wykonawcza agentów (nie „najinteligentniejszy” frontier), z naciskiem na lokalne i datacentrowe wdrożenia na sprzęcie NVIDIA. SGLang ogłosił Day-0 support. Licencja wag: OpenMDW 1.1.

**Źródła:**
- [NVIDIA Technical Blog — Nemotron 3.5 Lightning](https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/)
- [Hugging Face — NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4)
- [LMSYS / SGLang — Day-0 support (11.08.2026)](https://www.lmsys.org/blog/2026-08-11-nemotron-3-5-lightning)
- [The Decoder — Nemotron 3.5 Lightning prioritizes speed](https://the-decoder.com/nvidias-open-weight-nemotron-3-5-lightning-prioritizes-speed-over-maximum-intelligence/)

### 1.5. Luka w szyfrowanych śladach rozumowania API OpenAI, Anthropic i Google (ok. 11 sierpnia 2026)

Zespół badaczy (m.in. ELLIS Institute Tübingen, Max Planck Institute, MATS, Snyk) opublikował pracę **„Stealing Reasoning Traces from Proprietary LLM APIs”** (arXiv:2608.09867). Pokazuje ona, że zaszyfrowane bloki chain-of-thought zwracane klientom przez API Anthropic, OpenAI i Google były w praktyce **przenośne między sesjami, użytkownikami i modelami** tego samego dostawcy. Atak polegał na wstrzyknięciu śladu silniejszego modelu do słabszego „rodzeństwa” i zmuszeniu go — m.in. jailbreakiem — do wypisania ukrytego rozumowania w plaintextcie.

Konsekwencje obejmują obchodzenie zabezpieczeń anty-destylacyjnych, ekstrakcję PII i sekretów z publicznych logów sesji, ujawnianie informacji hazardowych ukrytych w myśleniu oraz wariant niewidocznego prompt injection wewnątrz zaszyfrowanych bloków. Po responsible disclosure dostawcy wdrożyli łaty po stronie serwera; oryginalne PoC przestały działać. Wydarzenie jest istotnym sygnałem dla bezpieczeństwa agentów i architektury „encrypted CoT”.

**Źródła:**
- [arXiv:2608.09867 — Stealing Reasoning Traces from Proprietary LLM APIs](https://arxiv.org/abs/2608.09867v1)
- [Simon Willison — Stealing Reasoning Traces (11.08.2026)](https://simonwillison.net/2026/Aug/11/stealing-reasoning-traces/)
- [The Decoder — leaked passwords in ChatGPT hidden reasoning](https://the-decoder.com/but-marinade-and-leaked-passwords-are-what-researchers-found-in-chatgpts-hidden-reasoning/)
- [Cyber Security News — vulnerability exposes hidden reasoning traces](https://cybersecuritynews.com/top-ai-models-apis-flaw-exposes-hidden-reasoning/)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

### 2.1. Chiny: sądy po stronie pracowników zwalnianych „z powodu AI” (relacja NPR, 10 sierpnia 2026)

**10 sierpnia 2026** NPR opublikowało reportaż o linii orzeczniczej chińskich sądów i komisji arbitrażowych w sprawach zwolnień związanych z automatyzacją AI. Przykład z **Guangzhou Intermediate People’s Court**: grafik „Wei”, którego obowiązki przejęło AI, został zwolniony z powołaniem na „istotną zmianę okoliczności obiektywnych”. Sąd utrzymał wyrok I instancji o **bezprawnym zwolnieniu** i nakazał dodatkowe odszkodowanie; sędzia **Chen Shiyuan** podkreśliła, że pracodawca nie może przerzucać ryzyka normalnych aktualizacji technologii na pracownika i powinien najpierw proponować inne stanowisko lub szkolenie.

Podobne rozstrzygnięcia pojawiały się wcześniej m.in. w Hangzhou i Pekinie: adopcja AI jest traktowana jako **strategiczny wybór biznesowy**, a nie nieprzewidywalna zmiana okoliczności uzasadniająca rozwiązanie umowy. Relacja podkreśla, że ochrona prawna jest silna na papierze, ale egzekucja pozostaje wyzwaniem; prawnicy z Europy śledzą chińskie precedensy w rostących lokalnych sporach o zwolnienia AI.

**Źródła:**
- [NPR / Iowa Public Radio — China's courts side with workers displaced by AI (10.08.2026)](https://www.iowapublicradio.org/news-from-npr/2026-08-10/chinas-courts-side-with-workers-displaced-by-ai-but-job-anxiety-persists)
- [The Next Web — China: firing workers to replace them with AI illegal](https://thenextweb.com/news/china-court-ai-layoffs-illegal-labor-law)
- [Caixin Global — Chinese courts on AI-related terminations (kontekst precedensów)](https://www.caixinglobal.com/2026-04-30/chinese-courts-rule-companies-cannot-fire-workers-simply-to-replace-them-with-ai-102439602.html)

### 2.2. Unia Europejska: od 2 sierpnia 2026 egzekwowalne obowiązki przejrzystości AI Act; high-risk (w tym wymiar sprawiedliwości) odroczony

**2 sierpnia 2026** wszedł w życie kluczowy etap stosowania unijnego **AI Act**, zmodyfikowany tuż wcześniej przez **Digital Omnibus on AI** (rozporządzenie UE 2026/1744). Od tej daty egzekwowalne są m.in. **obowiązki przejrzystości z art. 50** (ujawnianie interakcji z AI, etykietowanie deepfake’ów, informowanie o treściach AI w sprawach interesu publicznego) oraz mechanizmy sankcji i nadzoru rynkowego. Jednocześnie pełne obowiązki dla systemów **wysokiego ryzyka z Aneksu III** — obejmujących m.in. **egzekwowanie prawa i wymiar sprawiedliwości** — zostały **przesunięte na 2 grudnia 2027**.

Dla sądów i organów publicznych oznacza to: obowiązki „soft” przejrzystości i zakazy już działają, ale najbardziej wymagający reżim zgodności high-risk (dokumentacja, nadzór człowieka, oceny ryzyka/praw podstawowych itd.) daje dodatkowy czas — przy czym katalogi systemów AI i przygotowania compliance i tak są już przedmiotem zainteresowania organów. W Polsce kontekst uzupełnia krajowa ustawa o systemach AI oraz ostrożne stanowisko Ministerstwa Sprawiedliwości wobec nieskoordynowanych wdrożeń w sądach.

**Źródła:**
- [GamingTechLaw — EU AI Act from 2 August 2026: what applies / what was postponed](https://www.gamingtechlaw.com/2026/08/eu-ai-act-from-2-august-2026/)
- [Sourcing Speak — transparency & enforcement take effect; high-risk deferred (3.08.2026)](https://www.sourcingspeak.com/eu-ai-act-transparency-enforcement-rules-high-risk-regime-deferred/)
- [AIACT Blog — Article 50 enforcement and fines since 2 August 2026](https://www.aiactblog.nl/en/posts/article-50-enforcement-fines-ai-act-2026)
- [Gazeta Prawna — MS: AI w sądach tak, ale nie na własną rękę](https://edgp.gazetaprawna.pl/prawo/prawnik/artykuly/11282779,ai-w-sadach-ministerstwo-sprawiedliwosci-tak-ale-nie-na-wlasna-reke.html)

### 2.3. Indie: sędzia SN N. Kotiswar Singh — „algorytmy nie mogą udzielać kaucji” (AILGS-2026, zakończenie 8 sierpnia)

Na konferencji **AILGS-2026** (Bennett University / Indian Law Institute i partnerzy; zakończenie **8 sierpnia 2026** w New Delhi) sędzia Sądu Najwyższego Indii **N. Kotiswar Singh** podkreślił, że wymiar sprawiedliwości nie może zostać zredukowany do algorytmów i danych. W szczególności wskazał, że decyzje takie jak **udzielenie kaucji (bail)** wymagają empatii, uzasadnienia i wrażliwości na okoliczności sprawy, których maszyna nie jest w stanie adekwatnie uchwycić.

Powiązał wdrożenia AI z konstytucyjnymi gwarancjami równości, wolności osobistej i prywatności (m.in. orzecznictwo *Maneka Gandhi*, *Puttaswamy*). Ostrzegł też przed reprodukowaniem biasów treningowych. Dyrektor ILI przestrzegł przed „halucynacjami” AI w edukacji prawniczej. Konferencja wpisuje się w szerszą indyjską debatę o draftowych **Regulations for Use of AI in Courts, 2026** SN Indii (human primacy, zakaz samodzielnego orzekania/sentencingu przez AI).

**Źródła:**
- [Times Now — Algorithms Can’t Grant Bail (relacja 11.08.2026)](https://www.timesnownews.com/education/algorithms-cant-grant-bail-honourable-justice-n-kotiswar-singh-judge-supreme-court-of-india-urges-human-centred-ai-at-bennett-university-law-conference-article-155591402)
- [The Leaflet — Explained: Supreme Court of India Draft AI Regulations for Courts, 2026](https://theleaflet.in/law-and-technology/explained-the-supreme-court-of-indias-draft-regulations-for-use-of-artificial-intelligence-in-courts-2026)
- [The Print — SC draft regulations on AI use in courts](https://theprint.in/judiciary/supreme-court-releases-draft-regulations-on-ai-use-in-courts-invites-public-feedback/2950645/)

### 2.4. Indie: CJI Surya Kant o mediacji online i granicach AI (przełom lipca/sierpnia 2026)

**Chief Justice of India Surya Kant** na Commonwealth Peace Mediation Conference 2026 w Jaipurze ostrzegł przed pozostawieniem mediacji online wyłącznie oprogramowaniu AI: system może mieć „ludzki głos”, ale nie okazuje **empatii ani przeprosin**. Mediacja online powinna być prowadzona głównie przez wyszkolonych mediatorów, przy wsparciu technologii ODR sięgającej odległych regionów Wspólnoty.

W wystąpieniach z początku sierpnia CJI powtórzył, że AI może **wspierać** inteligencję sędziowską, lecz nie zastąpi **sumienia sędziowskiego**, odwołując się do draftowych regulacji SN Indii chroniących prywatność, dane i niezależność sądów. Przesłanie jest spójne z linią „human-centred AI” artykułowaną także przez innych sędziów SN w tym samym tygodniu.

**Źródła:**
- [Times Now — CJI Surya Kant cautions against leaving online mediation to AI](https://www.timesnownews.com/india/cji-surya-kant-cautions-against-leaving-online-mediation-to-artificial-intelligence-says-ai-has-human-voice-but-cannot-display-empathy-article-155225886)
- [New Kerala — CJI on AI augmenting judicial intelligence; draft AI regulations (6.08.2026)](https://www.newkerala.com/news/a/institutions-must-open-questioning-its-part-their-strength-931.htm)

### 2.5. Polska i UE: ostrożne wdrażanie AI w sądach przy rosnącym reżimie regulacyjnym

W Polsce Ministerstwo Sprawiedliwości — w odpowiedzi na interpelację poselską — podkreśla, że korzystanie przez sądy z AI wiąże się z istotnymi ryzykami (w tym danymi z akt i wymogami AI Act), dlatego zwłaszcza w orzekaniu potrzebne jest **spójne, kontrolowane** podejście, a nie samodzielne eksperymenty jednostek. Resort wskazuje m.in. nakłady na działający już system **transkrypcji** (ok. **8,7 mln zł** na funkcjonowanie i testy).

Eksperci i praktycy przypominają, że systemy AI w wymiarze sprawiedliwości są w unijnym AI Act klasyfikowane jako **wysokiego ryzyka**: AI może wspierać (transkrypcja, anonimizacja, wyszukiwanie orzeczeń, organizacja pracy), ale **nie może zastąpić** sędziego w ocenie dowodów, subsumpcji i wymierzaniu kary. W kontekście daty **2 sierpnia 2026** (przejrzystość art. 50) oraz odroczenia pełnych obowiązków high-risk, polski wymiar sprawiedliwości pozostaje na etapie narzędzi pomocniczych i centralnego sterowania ryzykiem.

**Źródła:**
- [Gazeta Prawna — AI w sądach? MS: tak, ale nie na własną rękę](https://edgp.gazetaprawna.pl/prawo/prawnik/artykuly/11282779,ai-w-sadach-ministerstwo-sprawiedliwosci-tak-ale-nie-na-wlasna-reke.html)
- [Prawo.pl — sztuczna inteligencja a orzekanie przez sędziów](https://www.prawo.pl/prawnicy-sady/sztuczna-inteligencja-a-orzekanie-przez-sedziow,533830.html)
- [Porady.pl — AI w postępowaniu karnym: kiedy można, a kiedy nie](https://porady.pl/sztuczna-inteligencja-w-postepowaniu-karnym-kiedy-mozna-ja-wykorzystac-a-kiedy-nie/)
- [Gov.pl — MS: nowoczesne podejście do sądownictwa oparte na AI (kontekst strategii)](https://www.gov.pl/web/sprawiedliwosc/nowoczesne-podejscie-do-sadownictwa-oparte-na-sztucznej-inteligencji-i-innowacjach-technologicznych)

---

## Uwagi metodologiczne

- Okres: wydarzenia i publikacje z ok. **5–12 sierpnia 2026**, z niezbędnym kontekstem wcześniejszym (np. draft regulacji SN Indii, wcześniejsze wyroki chińskie), gdy jest bezpośrednio powiązany z relacjami z tego tygodnia.
- Priorytet mają źródła pierwotne (blogi laboratoriów, arXiv, komunikaty sądów/mediów wiarygodnych) oraz niezależne relacje weryfikujące claimy produktowe.
- Tam, gdzie status wydania jest niejednoznaczny w źródłach wtórnych, pominięto wpis lub zaznaczono brak niezależnej weryfikacji (np. benchmarki Muse Spark 1.2).
