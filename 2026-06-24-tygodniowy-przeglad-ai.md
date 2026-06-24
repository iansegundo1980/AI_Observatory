# Tygodniowy przeglad AI - 2026-06-24

**Zakres raportu:** wydarzenia i komunikaty z okresu ok. 17-24 czerwca 2026 r. (UTC), z krotkim kontekstem dla inicjatyw, ktore weszly w zycie lub byly istotnie komentowane w tym tygodniu.
**Tematy przewodnie:** szybkie przesuniecie od chatbotow do agentow zdolnych do dlugich zadan, coraz bardziej specjalistyczne modele dla cyberbezpieczenstwa i dokumentow, oraz wyrazne zaciesnianie zasad uzywania AI w sadach.

## 1. Ogolne przelomy i nowe modele AI o istotnym znaczeniu

### 1.1. OpenAI: Daybreak i pelna wersja GPT-5.5-Cyber do obronnego cyberbezpieczenstwa

OpenAI oglosilo 22 czerwca rozszerzenie programu **Daybreak**, obejmujace aktualizacje **GPT-5.5-Cyber**, nowe przeplywy pracy w Codex Security oraz inicjatywe **Patch the Planet** wspierajaca projekty open source w przechodzeniu od wykrycia luk do realnych poprawek. Wazne jest przesuniecie akcentu: wedlug OpenAI bottleneckiem nie jest juz samo znajdowanie podatnosci, ale ich walidacja, priorytetyzacja i bezpieczne wdrazanie patchy.

Najwazniejsze elementy:

- **GPT-5.5-Cyber** ma byc bardziej zdolny i bardziej "permisywny" dla zweryfikowanych obroncow, przy zachowaniu silniejszych mechanizmow dostepu, monitorowania i przegladu.
- OpenAI podaje wyniki benchmarkow: **85,6% na CyberGym** wobec 81,8% dla GPT-5.5, **39,5% na ExploitGym** wobec 25,95% dla GPT-5.5 oraz **69,8% na SEC-bench Pro** wobec 63,1% dla GPT-5.5.
- Codex Security ma wspierac skanowanie repozytoriow, modelowanie zagrozen, sledzenie sciezek ataku, generowanie dowodow i propozycji poprawek; OpenAI twierdzi, ze od marcowego preview przeskanowano ponad **30 mln commitow** w ponad **30 tys. codebase'ow**.
- **Patch the Planet**, zalozony z Trail of Bits we wspolpracy m.in. z HackerOne, ma finansowac ekspertow i dawac maintainerom wsparcie modeli oraz narzedzi, aby redukowac obciazenie wynikajace z lawiny zgloszen.

**Znaczenie:** to jeden z najwazniejszych sygnalow, ze frontierowe modele cyber sa wprowadzane w modelu kontrolowanego dostepu, z naciskiem na "defense-first" i procesy dowodowe. Rownoczesnie pokazuje narastajace napiecie regulacyjne: modele zdolne pomagac obroncom moga tez obnizac koszty dzialan ofensywnych.

**Zrodla:** [OpenAI - Daybreak: Tools for securing every organization in the world](https://openai.com/index/daybreak-securing-the-world)

### 1.2. Mistral AI: Mistral OCR 4 jako wyspecjalizowany model Document Intelligence

Mistral AI wydal 23 czerwca **Mistral OCR 4**, model do rozumienia dokumentow. Nie jest to ogolny LLM, ale wyspecjalizowany komponent dla wyszukiwania, RAG, ekstrakcji danych i automatyzacji pracy na dokumentach.

Najwazniejsze elementy:

- OCR 4 zwraca nie tylko tekst, lecz takze **bounding boxy**, klasy blokow (np. tytuly, tabele, rownania, podpisy) i **confidence scores**.
- Model obsluguje **170 jezykow** w 10 grupach jezykowych i ma poprawiac wyniki dla jezykow specjalistycznych oraz niskozasobowych.
- Mistral podaje **85,20 na OlmOCRBench** oraz srednia przewage w ocenach preferencji ludzkich; firma zastrzega, ze benchmarki OCR maja istotne ograniczenia.
- Model moze byc uruchamiany jako pojedynczy kontener, co ma znaczenie dla organizacji z wymaganiami rezydencji danych, tajemnicy zawodowej lub compliance.
- Dostep: API w Mistral Studio, Amazon SageMaker i Microsoft Foundry; self-hosting dla klientow enterprise.

**Znaczenie:** dla rynku prawniczego, finansowego i zdrowotnego to praktycznie wazniejszy komunikat niz wiele premier chatbotow. Strukturyzacja dokumentow z lokalizacja fragmentow i pewnoscia odczytu jest kluczowa dla cytowalnego RAG, redakcji, due diligence, e-discovery i przetwarzania akt.

**Zrodla:** [Mistral AI - Introducing OCR 4](https://mistral.ai/news/ocr-4/)

### 1.3. Anthropic: Claude Tag - agent zespolowy w Slacku z pamiecia kanalu

Anthropic oglosil 23 czerwca **Claude Tag**, bete dla klientow Claude Enterprise i Team. Produkt pozwala dodac Claude'a do kanalow Slacka jako wspolnego "czlonka zespolu": uzytkownicy oznaczaja `@Claude`, deleguja zadanie, a model dziala z dostepem do narzedzi i danych przydzielonych przez administratora.

Najwazniejsze elementy:

- Claude Tag dziala w trybie zespolowym: jeden agent moze byc wspoldzielony przez kanal, a praca odbywa sie publicznie w watkach Slacka.
- Model buduje kontekst na podstawie kanalow i zrodel, do ktorych ma uprawnienia; pamiec jest ograniczana zakresem administracyjnym.
- W trybie "ambient" Claude moze proaktywnie sygnalizowac informacje, przypominac o watkach i planowac zadania.
- Anthropic podaje, ze wewnetrzna wersja Claude Tag tworzy obecnie **65% kodu zespolu produktowego** firmy.
- Produkt dziala z **Claude Opus 4.8** i zastepuje dotychczasowa aplikacje Claude in Slack.

**Znaczenie:** to wazny krok w strone "multiplayer AI" - agentow nie jako prywatnych chatbotow, ale widocznych, audytowalnych uczestnikow pracy zespolowej. Dla organizacji kluczowe beda logi, kontrola uprawnien, limity kosztow i separacja pamieci miedzy zespolami.

**Zrodla:** [Anthropic - Introducing Claude Tag](https://www.anthropic.com/news/introducing-claude-tag)

### 1.4. Google DeepMind: AI Control Roadmap dla coraz bardziej autonomicznych agentow

18 czerwca Google DeepMind opublikowal **AI Control Roadmap** - framework zabezpieczania agentow AI wdrazanych w systemach wewnetrznych Google. Nie jest to premiera modelu, lecz istotny dokument systemowy, bo opisuje obrone przed agentami traktowanymi jak potencjalne "insider threats".

Najwazniejsze elementy:

- Roadmapa idzie poza klasyczne alignment: zaklada, ze agent moze byc niedoskonale zestrojony i trzeba ograniczac jego realne mozliwosci szkodzenia.
- Google opisuje monitorowanie trajektorii agentow, klasyfikacje zachowan wedlug taksonomii zagrozen i eskalacje do ludzi.
- DeepMind twierdzi, ze przeanalizowal **milion zadan agentow kodujacych**, co pomoglo budowac monitor dla agenta Gemini Spark.
- Framework skaluje srodki kontroli wedlug dwoch osi: zdolnosci agenta do unikania detekcji oraz potencjalnej szkody.

**Znaczenie:** to sygnal, ze najwieksze laboratoria AI przygotowuja sie do swiata, w ktorym glownym ryzykiem nie jest pojedyncza odpowiedz modelu, ale dlugotrwale dzialanie agenta z uprawnieniami do systemow, kodu, danych i narzedzi.

**Zrodla:** [Google DeepMind - Securing the future of AI agents](https://deepmind.google/blog/securing-the-future-of-ai-agents/)

### 1.5. Perplexity: Brain - samodoskonalaca sie pamiec dla agentow

Perplexity oglosilo 18 czerwca **Brain**, system pamieci dla Perplexity Computer. W odroznieniu od typowej pamieci "o uzytkowniku", Brain ma pamietac, **co agent zrobil**, co zadzialalo, co zawiodlo i jak poprawiono wynik.

Najwazniejsze elementy:

- Brain buduje graf kontekstu pracy wykonywanej przez Computer i okresowo analizuje go, aby poprawiac przyszle wykonanie zadan.
- Perplexity podaje wczesne wyniki: **+25% poprawnosci odpowiedzi** dla zadan widzianych wczesniej, **+16% recall** i **-13% kosztu** zadan wymagajacych kontekstu historycznego.
- Dostep: Research Preview dla subskrybentow Max i Enterprise Max.

**Znaczenie:** to kolejny dowod, ze konkurencja przenosi sie z "najlepszej odpowiedzi w jednej sesji" na infrastrukture pracy ciaglej: pamiec, slady wykonania, uczenie sie z poprzednich trajektorii i powtarzalnosc zadan.

**Zrodla:** [Perplexity - Self-improving Memory for Agents](https://www.perplexity.ai/hub/blog/self-improving-memory-for-agents)

### 1.6. Meta: AI Mode i narzedzia kreatywne na Facebooku, zasilane przez Muse Spark

Meta oglosila nowe funkcje AI na Facebooku, w tym **AI Mode** w wyszukiwaniu oraz kreatywne narzedzia do edycji zdjec i wideo. AI Mode ma odpowiadac z wykorzystaniem publicznych sygnalow z ekosystemu Meta, m.in. Groups i Reels, a nie tylko zwracac liste linkow.

Najwazniejsze elementy:

- AI Mode ma dawac odpowiedzi oparte na tym, co ludzie publicznie publikuja i rekomenduja w aplikacjach Meta.
- Narzedzia kreatywne obejmuja m.in. sugestie montazy z rolki aparatu, szablony kolaży, przejscia oraz presety AI do zmiany ubioru, wlosow i akcesoriow.
- Meta wskazuje, ze funkcje sa zasilane przez **Muse Spark**, model ogloszony wczesniej jako fundament nowego Meta AI.

**Znaczenie:** to mniej "frontier model release", a bardziej masowa dystrybucja AI w produkcie konsumenckim. W praktyce moze miec duzy wplyw na to, jak setki milionow uzytkownikow zaczna traktowac wyszukiwanie spolecznosciowe, generowanie tresci i rekomendacje.

**Zrodla:** [Meta - New AI Tools to Help You Make Things Happen on Facebook](https://about.fb.com/news/2026/06/new-ai-tools-to-help-you-make-things-happen-on-facebook/), [Meta - Introducing Muse Spark](https://about.fb.com/news/2026/04/introducing-muse-spark-meta-superintelligence-labs/)

### 1.7. Kimi K2.7 Code: mocny model kodujacy na granicy tygodnia raportowego

Moonshot AI opublikowal 16 czerwca **Kimi K2.7 Code**. Data jest tuz przed glownym oknem raportu, ale model byl szeroko omawiany w analizowanym tygodniu i jest istotny dla trendu agentow programistycznych.

Najwazniejsze elementy:

- Kimi K2.7 Code deklaruje wyzsze wyniki niz K2.6 w benchmarkach narzedziowych, m.in. **62,0 na Kimi Code Bench V2** wobec 50,9 dla K2.6.
- Model ma lepiej obslugiwac dlugie zadania kodowania, sekwencje ponad 4000 wywolan narzedzi i ponad 12 godzin ciaglej egzekucji.
- Moonshot wskazuje ok. **30% redukcji tokenow "thinking"** wzgledem K2.6 oraz wersje HighSpeed osiagajaca do 260 tokenow/s w krotkich kontekstach.
- Model wspiera multimodalne uzycie narzedzi, w tym wideo i obrazy.

**Znaczenie:** premiera wzmacnia konkurencje w segmencie modeli do dlugohoryzontowego kodowania i agentow narzedziowych. W tym obszarze liczy sie juz nie tylko jakosc pojedynczej odpowiedzi, ale stabilnosc przez tysiace krokow, koszt rozumowania i predkosc.

**Zrodla:** [Moonshot AI Forum - Kimi K2.7 Code](https://forum.moonshot.ai/t/here-comes-kimi-k2-7-code-better-coding-with-more-efficiency/441)

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwosci

### 2.1. Indie: projekt regulacji AI w sadach - "human primacy" i zakaz AI w rozstrzyganiu

Najwazniejszym watkiem regulacyjnym dla sadow w czerwcu pozostaje indyjski projekt **Regulations for Use of Artificial Intelligence (AI) in Courts, 2026**, opublikowany przez Komitet AI Sadu Najwyzszego Indii. Termin konsultacji uplynal **20 czerwca 2026 r.**, czyli w tygodniu raportu.

Najwazniejsze elementy:

- Projekt obejmuje Sad Najwyzszy, High Courts, sady nizsze, trybunaly i organy adjudykacyjne.
- Zasady przewodnie obejmuja **human primacy**, niezaleznosc sedziowska, praworzadnosc, niedyskryminacje, transparentnosc, wyjasnialnosc, audytowalnosc, ochrone danych, proporcjonalnosc, cyberbezpieczenstwo i dostepnosc.
- AI ma pozostac narzedziem wspierajacym, a nie zastepowac sedziego w ustalaniu faktow, prawa lub sprawiedliwego wyniku.
- Projekt przewiduje system instytucjonalny: apex body, komitety techniczne i sedziowskie, rejestr AI, audyty, baze incydentow i roczne raporty transparentnosci.
- Komentarze prawnicze podkreslaly szczegolnie zakaz uzywania AI do rozstrzygania wynikow, wymierzania kary, oceny wiarygodnosci swiadkow, ryzyka recydywy lub kwalifikacji do kaucji.

**Znaczenie:** Indie probuja zbudowac scentralizowany, sadowniczy model governance AI, bardziej formalny niz amerykanski patchwork, ale wyraznie ostrozniejszy niz chinski program "smart courts". To moze stac sie wzorcem dla panstw, ktore chca dopuscic automatyzacje administracyjna i badawcza, ale zamknac droge do automatycznego orzekania.

**Zrodla:** [Supreme Court of India - Draft Regulations for Use of AI in Courts, 2026 (PDF)](https://hcraj.nic.in/hcraj/hcraj_admin/uploadfile/latestupdates/Final_draft_with_Notice_v178072027287.pdf), [ThePrint - AI in courts: how India's draft rules stack up](https://theprint.in/judiciary/ai-in-courts-how-indias-draft-rules-stack-up-against-the-eu-us-and-china/2951484/), [Indian Express - No AI in verdicts, bail eligibility](https://indianexpress.com/article/legal-news/supreme-court-ai-regulations-2026-draft-rules-courts-ban-ai-decisions-10723503/)

### 2.2. Stany Zjednoczone: od patchworku sedziowskiego do stanowowych standardow w Nowym Jorku i na Florydzie

W USA nadal nie ma jednolitej ogolnokrajowej zasady dotyczacej generatywnej AI w pismach procesowych. Najwazniejsze sa reguly stanowe, lokalne i zarzadzenia poszczegolnych sedziow.

**Nowy Jork.** Od 1 czerwca obowiazuje **22 NYCRR Part 161** dla New York State Unified Court System. Regula dopuszcza AI w przygotowywaniu pism i nie naklada ogolnego obowiazku ujawniania, ale wymaga, aby adwokaci samodzielnie sprawdzali, ze materialy AI-assisted nie zawieraja fikcyjnych spraw, ustaw ani innych tresci.

**Floryda.** Supreme Court of Florida zmienil Rule 2.515(d)(2), a zmiana weszla w zycie **15 czerwca 2026 r.** Podpisujacy pismo - adwokat lub osoba bez pelnomocnika - reprezentuje, ze wskazane autorytety prawne istnieja i sa prawidlowo cytowane. Naruszenie moze skutkowac sankcjami, m.in. upomnieniem, contempt, skresleniem pisma, kosztami czy oddaleniem postepowania.

**Znaczenie:** USA przesuwaja sie od prostego pytania "czy ujawnic uzycie AI?" do standardu odpowiedzialnosci za wynik. Nowy Jork stawia na accountability bez obowiazkowego ujawnienia, Floryda na jednolita certyfikacje prawdziwosci autorytetow, zastepujaca rozne lokalne zarzadzenia.

**Zrodla:** [NYSBA - Part 161 effective June 1, 2026](https://nysba.org/effective-june-1-2026-the-new-york-state-unified-court-system-has-adopted-a-new-rule-regarding-the-use-of-artificial-intelligence/), [Supreme Court of Florida - Opinion SC2026-0673 (PDF)](https://flcourts-media.flcourts.gov/content/download/2489374/opinion/Opinion_SC2026-0673.pdf), [Jones Day - Florida statewide AI certification standard](https://www.jonesday.com/en/insights/2026/06/supreme-court-of-florida-creates-statewide-standard-for-artificial-intelligence-certification-in-court-filings)

### 2.3. Unia Europejska: AI Act, wysokie ryzyko i administracja wymiaru sprawiedliwosci

16 czerwca Parlament Europejski zatwierdzil zmiany w AI Act w ramach pakietu digital omnibus. Z perspektywy sadow wazne jest przesuniecie terminow dla systemow wysokiego ryzyka, w tym systemow z obszaru administracji wymiaru sprawiedliwosci i procesow demokratycznych.

Najwazniejsze elementy:

- Obowiazki dla samodzielnych systemow wysokiego ryzyka maja stosowac sie od **2 grudnia 2027 r.**
- Systemy AI w produktach objetych regulacjami bezpieczenstwa sektorowego maja termin **2 sierpnia 2028 r.**
- Parlament jednoczesnie zaakceptowal zakaz systemow generujacych materialy CSAM lub tzw. "nudifier apps" bez zgody osoby identyfikowalnej.
- Draft guidance Komisji Europejskiej wskazuje, ze AI wspierajaca organy sadowe w badaniu, interpretacji lub stosowaniu prawa do faktow moze byc kwalifikowana jako high-risk.

**Znaczenie:** UE nie zakazuje AI w sadownictwie, ale klasyfikuje czesc zastosowan jako wysokiego ryzyka. W praktyce oznacza to wymogi zarzadzania ryzykiem, danych, dokumentacji, nadzoru ludzkiego i transparentnosci. Dla sadow oraz dostawcow legaltech to sygnal, ze wdrozenia wspierajace orzekanie beda wymagala rygorystycznego compliance.

**Zrodla:** [European Parliament - AI Act simplification measures](https://www.europarl.europa.eu/news/en/press-room/20260611IPR45207/ai-act-ep-approves-simplification-measures-and-nudifier-app-ban), [Osborne Clarke - draft high-risk classification guidelines](https://www.osborneclarke.com/insights/european-commission-publishes-draft-ai-act-guidelines-high-risk-classification-and), [EU AI Act - Regulation 2024/1689](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng)

### 2.4. Brazylia: AI jako narzedzie odciazania sadow, ale z granica etyczna

19 czerwca prezes brazylijskiego Supremo Tribunal Federal, **Edson Fachin**, poparl wykorzystanie AI do przyspieszenia pracy wymiaru sprawiedliwosci, ale mocno zaznaczyl granice etyczne. Wskazal, ze brazylijski system ma ponad **80 mln spraw w toku**, a AI moze pomagac w automatyzacji powtarzalnych zadan, identyfikacji precedensow i pracy administracyjnej.

Najwazniejsze elementy:

- Fachin podkreslil, ze AI moze organizowac i korelowac dane w skali niedostepnej czlowiekowi, ale nie rozumie cierpienia, podatnosci na krzywde ani emocjonalnego wymiaru spraw.
- Jako przyklad granicy etycznej przywolal sprawe Mari Ferrer i znaczenie ludzkiej wrazliwosci w sprawach osob pokrzywdzonych.
- Tlo regulacyjne tworzy **Resolution CNJ No. 615/2025**, ktora wymaga nadzoru ludzkiego, zasad governance i ogranicza zastapienie czlowieka w funkcjach orzeczniczych.

**Znaczenie:** Brazylia jest jednym z najciekawszych laboratoriow AI w sadownictwie, bo laczy ogromne obciazenie sprawami z centralna rola Conselho Nacional de Justica. Przekaz Fachina pokazuje dominujacy kompromis: AI do skali, administracji i precedensow; czlowiek do oceny godnosci, wiarygodnosci, krzywdy i sprawiedliwosci.

**Zrodla:** [CBN Globo - Fachin apoia uso de IA e cita caso Mari Ferrer](https://cbn.globo.com/politica/noticia/2026/06/19/fachin-apoia-uso-de-ia-e-cita-caso-mari-ferrer-para-defender-limites-eticos-no-judiciario.ghtml), [CNJ Resolution 615/2025 (PDF)](https://atos.cnj.jus.br/files/original1555302025031467d4517244566.pdf), [CNJ - IAJus 2026](https://www.cnj.jus.br/agendas/iajus-2026-brazilian-judiciary-ai-integration-forum/)

### 2.5. Kanada: certyfikacja i "human in the loop" w Supreme Court of Yukon

2 czerwca Supreme Court of Yukon wydal Practice Direction **General-35** dotyczaca uzywania generatywnej AI w pisemnych i ustnych wystapieniach. W tygodniu raportu temat byl ujmowany w szerszych przegladach kanadyjskich zasad sadowych.

Najwazniejsze elementy:

- Prawnicy i strony musza opierac sie na autorytatywnych zrodlach, takich jak oficjalne strony sadow, strony rzadowe, uznani wydawcy lub CanLII.
- Uzycie AI wymaga sprawdzenia i potwierdzenia poprawnosci informacji; sad wprost opisuje zasade **"Human in the Loop"**.
- Wszystkie pleadings, notices of application, responses i outlines musza zawierac certyfikat potwierdzajacy autentycznosc powolanych przepisow, zasad prawnych i - dla outlines - spraw.
- Naruszenie moze skutkowac kosztami, w tym kosztami osobistymi.

**Znaczenie:** Kanada pozostaje zdecentralizowana, ale widoczny jest trend praktycznych certyfikatow i wymogu weryfikacji, nie tylko ogolnych ostrzezen o halucynacjach.

**Zrodla:** [Supreme Court of Yukon - Practice Direction General-35 (PDF)](https://www.yukoncourts.ca/sites/default/files/2026-06/35.%20General%2035%20-Conditions%20on%20use%20of%20generative%20AI%20in%20written%20and%20oral%20representations_1.pdf), [Canadian Judicial Council - Guidelines for the Use of AI in Canadian Courts](https://cjc-ccm.ca/en/resources-center/publications/guidelines-use-artificial-intelligence-canadian-courts), [Canadian Lawyer - survey of Canadian courts](https://www.canadianlawyermag.com/news/general/canadian-lawyer-survey-how-canadas-courts-are-regulating-using-and-evaluating-generative-ai/394199)

### 2.6. Singapur: neutralne dopuszczenie GenAI, ale pelna odpowiedzialnosc uzytkownika sadu

Singapurskie sady maja od 1 pazdziernika 2024 r. przewodnik dla uzytkownikow sadow dotyczacy generatywnej AI, a w marcu 2026 r. Ministerstwo Prawa opublikowalo szerszy przewodnik dla sektora prawnego. To wazny punkt odniesienia porownawczy dla jurysdykcji, ktore nie chca zakazywac AI, ale chca utrzymac odpowiedzialnosc i dowodowa integralnosc postepowan.

Najwazniejsze elementy:

- Sad nie zakazuje uzycia GenAI do przygotowania dokumentow, ale uzytkownik sadu ponosi pelna odpowiedzialnosc za tresc.
- Nie ma prewencyjnego obowiazku deklarowania AI, chyba ze sad o to poprosi.
- Uzytkownicy musza weryfikowac sprawy, przepisy, cytaty i komentarze prawnicze w wiarygodnych zrodlach; nie wolno potwierdzac jednego outputu AI drugim narzedziem AI.
- GenAI nie moze sluzyc do fabrykowania, wzmacniania, oslabiania lub manipulowania dowodami.
- Sad moze zadac wskazania fragmentow wygenerowanych przez AI i wyjasnienia sposobu weryfikacji.

**Znaczenie:** Singapur pokazuje model "neutral stance + strict accountability": technologia jest dozwolona, ale ryzyko procesowe i dyscyplinarne zostaje przy stronie lub prawniku.

**Zrodla:** [Singapore Judiciary - Guide on the Use of Generative AI Tools by Court Users (PDF)](https://www.judiciary.gov.sg/docs/default-source/news-and-resources-docs/guide-on-the-use-of-generative-ai-tools-by-court-users.pdf), [Singapore Ministry of Law - Guide for Using Generative AI in the Legal Sector (PDF)](https://www.mlaw.gov.sg/files/Guide_for_using_Generative_AI_in_the_Legal_Sector__Published_on_6_Mar_2026_.pdf), [Singapore High Court judgment [2026] SGHC 49 (PDF)](https://www.elitigation.sg/gd/gd/2026_SGHC_49/pdf)

### 2.7. Australia: praktyczne noty dla AI w postepowaniach federalnych i stanowych

Australia rozwija jeden z bardziej szczegolowych zestawow praktycznych zasad dla AI w postepowaniach. Federal Court of Australia opublikowal 16 kwietnia **Generative Artificial Intelligence Practice Note (GPN-AI)**, a w 2025-2026 podobne dokumenty i wytyczne rozwijaly m.in. sady Nowej Poludniowej Walii i Queensland.

Najwazniejsze elementy:

- Federal Court wskazuje na potencjalne korzysci GenAI dla efektywnosci, kosztow i dostepu do wymiaru sprawiedliwosci, ale wymaga odpowiedzialnego uzycia zgodnego z dotychczasowymi obowiazkami.
- Szczegolna ostroznosc dotyczy pleadings, submissions, evidence oraz informacji poufnych lub chronionych.
- Australijskie wytyczne klada nacisk na ujawnienie uzycia AI, weryfikacje zrodel, zakaz wprowadzania poufnych danych do publicznych narzedzi oraz zakaz zastapienia profesjonalnego osadu.

**Znaczenie:** Australia jest przykladem podejscia proceduralnego: zamiast abstrakcyjnego prawa o AI, sady wydaja praktyczne noty operacyjne, ktore prawnicy musza uwzgledniac przy kazdym pismie i materiale dowodowym.

**Zrodla:** [Federal Court of Australia - GPN-AI](https://www.fedcourt.gov.au/law-and-practice/practice-documents/notice-to-profession/16-april-2026), [Supreme Court of New South Wales - Practice Note SC Gen 23 (PDF)](https://supremecourt.nsw.gov.au/documents/Practice-and-Procedure/Practice-Notes/general/current/PN_SC_Gen_23.pdf), [Queensland Courts - Guidelines for judicial officers (PDF)](https://www.courts.qld.gov.au/__data/assets/pdf_file/0009/879714/the-use-of-generative-ai-guidelines-for-judicial-officers.pdf)

### 2.8. Chiny: "smart courts" i Faxin LLM jako kontrastowy model integracji AI

Chiny pozostaja najbardziej zaawansowanym przykładem szerokiej integracji AI z sadownictwem, choc najwazniejsze podstawy programu pochodza z poprzednich lat. W czerwcu 2026 r. temat jest istotny porownawczo, zwlaszcza wobec indyjskiego projektu, ktory wyraznie dystansuje sie od AI jako narzedzia merytorycznego orzekania.

Najwazniejsze elementy:

- Strategia "smart courts" zaklada gleboka integracje AI z obsluga postepowan, administracja sadow, egzekucja i uslugami dla obywateli.
- Supreme People's Court w dokumentach z 2022 r. deklarowal cel wysokiego poziomu wsparcia AI do 2030 r., przy jednoczesnym formalnym zastrzezeniu, ze AI nie moze zastapic sedziego.
- Faxin Legal Foundation LLM, przedstawiony w 2024 r., jest modelem prawniczym budowanym dla chinskiego systemu sadowniczego.
- Analizy akademickie wskazuja na bardzo szerokie uzycie systemow automatycznego kierowania spraw, generatywnej AI i narzedzi wspierajacych wymiar kary, przy ryzykach zwiazanych z kontrola polityczna, przejrzystoscia i danymi treningowymi.

**Znaczenie:** Chinski model pokazuje najbardziej zintegrowana, panstwowa wizje AI w sadach. Jest zarazem punktem ostrzegawczym dla jurysdykcji demokratycznych: formalna zasada "AI nie zastapi sedziego" moze byc niewystarczajaca, jesli narzedzia AI sa w praktyce gleboko wbudowane w workflow i rekomendacje.

**Zrodla:** [Supreme People's Court Opinions via China Justice Observer](https://www.chinajusticeobserver.com/law/x/the-supreme-people-s-court-the-opinions-on-regulating-and-strengthening-the-applications-of-artificial-intelligence-in-the-judicial-field-20221208), [European Chinese Law Research Hub - AI for China's Courts](https://blog.uni-koeln.de/eclrhub/2026/04/27/ai-for-chinas-courts-training-and-testing-for-the-socialist-rule-of-law/), [Oxford Institute of Technology and Justice - China](https://www.techandjustice.bsg.ox.ac.uk/research/china)

## Najwazniejsze wnioski tygodnia

1. **Agentowosc staje sie glownym polem rywalizacji.** OpenAI, Anthropic, Perplexity i Google DeepMind koncentruja sie nie tylko na modelach, ale na pamieci, kontroli, pracy asynchronicznej, monitoringu i wykonywaniu dlugich zadan.
2. **Specjalizacja modeli przyspiesza.** GPT-5.5-Cyber i Mistral OCR 4 pokazuja, ze rynek bedzie dzielil sie na modele ogolne oraz silne, wyspecjalizowane komponenty dla cyberbezpieczenstwa, dokumentow, prawa, finansow i RAG.
3. **Sady akceptuja AI jako pomoc, nie jako sedziego.** Indie, Singapur, Kanada, Australia, USA i Brazylia roznia sie szczegolami, ale wspolny mianownik to: czlowiek odpowiada za wynik, AI wymaga weryfikacji, a automatyczne orzekanie pozostaje poza granica.
4. **Regulacja przechodzi z poziomu etyki na poziom procedury.** Certyfikaty autentycznosci cytatow, obowiazki weryfikacji, rejestry AI, audyty, logi i sankcje procesowe staja sie bardziej konkretne niz ogolne deklaracje "odpowiedzialnego AI".
5. **Najwieksze ryzyko dla wymiaru sprawiedliwosci to nie samo uzycie AI, lecz niewidzialne uzycie bez kontroli.** Wlasnie dlatego jurysdykcje eksperymentuja z ujawnianiem, certyfikacja, prawem sedziego do zadania wyjasnien i zakazem wprowadzania danych poufnych do publicznych narzedzi.
