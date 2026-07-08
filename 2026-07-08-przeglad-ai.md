# Tygodniowy przeglad AI - 2026-07-08

**Zakres:** najwazniejsze wydarzenia i sygnaly z okresu ok. 1-8 lipca 2026 r.  
**Cel:** krotko wyjasnic znaczenie nowych modeli i produktow AI oraz pokazac, jak w tym samym czasie sady i instytucje wymiaru sprawiedliwosci porzadkuja praktyczne uzycie AI.

## 1. Ogolne przelomy i nowe modele AI o istotnym znaczeniu

### 1.1. Meta uruchomila Muse Image i zapowiedziala Muse Video

Meta oglosila **Muse Image**, pierwszy model generowania obrazow rozwijany przez Meta Superintelligence Labs, oraz pokazala wczesny podglad **Muse Video**. Muse Image ma obslugiwac precyzyjna edycje, kompozycje z wielu referencji, generowanie obrazow w Meta AI, Instagram Stories i WhatsApp, a takze niewidoczne znakowanie pochodzenia tresci poprzez system **Content Seal**. Meta podaje, ze Muse Video korzysta z tej samej bazy pretrainingowej i ma oferowac natywne audio, choc firma sama wskazuje jeszcze obszary do poprawy, m.in. synchronizacje audio-wideo i szybki ruch.  
**Znaczenie:** Meta przesuwa generatywne media glebiej do masowych kanalow spolecznosciowych, co zwieksza skale zastosowan kreatywnych, ale rownoczesnie nasila pytania o zgode, prawa do danych treningowych i identyfikowalnosc tresci syntetycznych.  
**Zrodla:** [Meta AI - Introducing Muse Image and Muse Video](https://ai.meta.com/blog/introducing-muse-image-muse-video-msl/), [TechCrunch - Meta rolls out Muse Image](https://techcrunch.com/2026/07/07/meta-rolls-out-muse-a-new-ai-image-generator/).

### 1.2. OpenAI wydalo GPT-Realtime-2.1 i GPT-Realtime-2.1-mini dla agentow glosowych

OpenAI udostepnilo w API modele **gpt-realtime-2.1** i **gpt-realtime-2.1-mini** do niskolatencyjnych interakcji glosowych i multimodalnych. Wedlug changelogu i komunikatu deweloperskiego aktualizacja poprawia rozpoznawanie ciagow alfanumerycznych, obsluge ciszy i szumu, zachowanie przy przerywaniu wypowiedzi oraz zmniejsza opoznienia p95 w modelach Realtime voice o co najmniej 25% dzieki lepszemu cache'owaniu. Wariant mini ma byc szybsza i tansza opcja dla aplikacji glosowych.  
**Znaczenie:** rynek agentow glosowych przechodzi od prostych chatbotow do systemow dzialajacych w czasie rzeczywistym, z narzedziami, barge-in i konfigurowalnym wysilkiem rozumowania. To istotne dla obslugi klienta, edukacji, dostepnosci i aplikacji mobilnych.  
**Zrodla:** [OpenAI Developer Community - New Realtime models](https://community.openai.com/t/new-realtime-models-on-the-api-gpt-realtime-2-1-and-gpt-realtime-2-1-mini/1385896), [OpenAI API Changelog](https://developers.openai.com/api/docs/changelog), [OpenAI API - GPT-Realtime-2.1 model](https://developers.openai.com/api/docs/models/gpt-realtime-2.1), [OpenAI API - Voice agents](https://developers.openai.com/api/docs/guides/voice-agents).

### 1.3. Anthropic udostepnil Claude Sonnet 5 i przywrocil dostep do Claude Fable 5

Anthropic poinformowal, ze **Claude Sonnet 5** jest dostepny dla wszystkich planow, jako model domyslny dla uzytkownikow Free i Pro oraz przez API pod identyfikatorem `claude-sonnet-5`. Firma pozycjonuje go jako model do kodowania, agentow i pracy profesjonalnej na duza skale. Rownolegle Anthropic przywrocil globalny dostep do **Claude Fable 5** i **Claude Mythos 5** po zniesieniu ograniczen eksportowych; Fable 5 ma byc dostepny dla uzytkownikow Claude Platform, Claude.ai, Claude Code i Claude Cowork, natomiast Mythos 5 pozostaje modelem o scisle ograniczonym dostepie dla zaufanych partnerow, szczegolnie w cyberbezpieczenstwie defensywnym.  
**Znaczenie:** tydzien pokazal dwutorowa strategie Anthropic: szeroko dostepny model klasy produkcyjnej oraz bardziej kontrolowane modele o wyzszej zdolnosci w domenach wrazliwych. To wazny sygnal dla governance modeli frontierowych.  
**Zrodla:** [Anthropic - Introducing Claude Sonnet 5](https://www.anthropic.com/news/claude-sonnet-5), [Anthropic - Redeploying Claude Fable 5](https://www.anthropic.com/news/redeploying-fable-5), [Anthropic - Claude Fable 5 and Claude Mythos 5](https://www.anthropic.com/news/claude-fable-5-mythos-5).

### 1.4. Tencent oficjalnie wydal Hy3: otwarty model MoE 295B z kontekstem 256K

Tencent Hunyuan oglosil oficjalne wydanie **Hy3**, modelu Mixture-of-Experts o 295 mld parametrow lacznie, 21 mld aktywnych parametrow, warstwie Multi-Token Prediction 3,8 mld oraz oknie kontekstowym do 256K tokenow. Model jest udostepniany na platformach takich jak Hugging Face i ModelScope, a Tencent podkresla jego zastosowania w agentach, rozumowaniu, kodowaniu i integracji produktowej.  
**Znaczenie:** Hy3 wzmacnia konkurencje w segmencie duzych modeli otwartych/otwartowagowych, szczegolnie dla organizacji zainteresowanych dlugim kontekstem i samodzielnym lub partnerskim hostowaniem modeli agentowych.  
**Zrodla:** [Tencent - Hunyuan officially releases Hy3](https://www.tencent.com/en-us/articles/2202386.html), [Tencent-Hunyuan/Hy3 on GitHub](https://github.com/Tencent-Hunyuan/Hy3), [tencent/Hy3 on Hugging Face](https://huggingface.co/tencent/Hy3), [VentureBeat - Hy3 analysis](https://venturebeat.com/technology/tencents-apache-licensed-hy3-takes-on-glm-5-2-at-half-the-size-and-wins-everywhere-except-coding).

### 1.5. GitHub wprowadzil Kimi K2.7 Code do Copilota, takze dla Business i Enterprise

GitHub oglosil, ze **Kimi K2.7 Code** jest ogolnie dostepny w GitHub Copilot, poczatkowo dla planow Pro, Pro+ i Max, a od 7 lipca rowniez dla Copilot Business i Copilot Enterprise. To pierwszy model open-weight widoczny jako opcja w wyborze modeli Copilota; w organizacjach Business i Enterprise jest domyslnie wylaczony i wymaga wlaczenia przez administratora polityki.  
**Znaczenie:** dostawcy narzedzi programistycznych zaczynaja laczyc modele zamkniete z open-weight w jednym interfejsie, a administratorzy enterprise dostaja wiecej decyzji dotyczacych kosztow, bezpieczenstwa i zgodnosci.  
**Zrodla:** [GitHub Changelog - Kimi K2.7 Code generally available](https://github.blog/changelog/2026-07-01-kimi-k2-7-is-now-available-in-github-copilot/), [GitHub Changelog - Kimi K2.7 for Business and Enterprise](https://github.blog/changelog/2026-07-07-kimi-k2-7-now-available-for-copilot-business-and-enterprise/).

### 1.6. NVIDIA pokazala Audex: zunifikowany model audio-tekst bez duzej regresji tekstowej

NVIDIA opublikowala **Nemotron-Labs-Audex-30B-A3B**, model audio-tekst zbudowany na bazie Nemotron-Cascade-2-30B-A3B. Model ma obslugiwac rozumienie audio, rozpoznawanie i tlumaczenie mowy, text-to-speech, generowanie audio i speech-to-speech, przy zachowaniu zdolnosci tekstowych modelu bazowego. Artykul badawczy opisuje architekture, w ktorej audio wejscia trafiaja do przestrzeni embeddingow tekstowych, a wyjscia audio sa generowane jako dyskretne tokeny obok tokenow tekstu.  
**Znaczenie:** multimodalnosc audio przestaje byc dodatkiem do LLM, a staje sie elementem jednej architektury. To wazne dla asystentow glosowych, dubbingu, tworzenia tresci audio i narzedzi dostepnosci.  
**Zrodla:** [NVIDIA Audex on Hugging Face](https://huggingface.co/nvidia/Nemotron-Labs-Audex-30B-A3B), [arXiv - Unified Audio Intelligence Without Regressing on Text Intelligence](https://arxiv.org/pdf/2607.05196), [Hugging Face Papers - Audex](https://huggingface.co/papers/2607.05196).

### 1.7. Sakana AI uruchomila Sakana Translate oparte na modelach Namazu

Sakana AI dodala do Sakana Chat narzedzie **Sakana Translate**, darmowa aplikacje webowa do tlumaczen dwukierunkowych miedzy japonskim, angielskim i chinskim. System opiera sie na serii modeli **Namazu**, dostrojonych do realiow jezyka japonskiego, i oferuje trzy tryby: tlumaczenie, korekte oraz pytania o niuanse. Firma akcentuje obsluge kontekstu kulturowego, jezyka grzecznosciowego, nazw wlasnych i slangu.  
**Znaczenie:** to przyklad regionalizacji modeli frontierowych: zamiast jednego uniwersalnego modelu, pojawiaja sie wyspecjalizowane warstwy produktowe zoptymalizowane pod jezyk i kulture.  
**Zrodla:** [Sakana AI - Sakana Translate release](https://sakana.ai/translate-release/), [ITmedia NEWS - Sakana Translate](https://www.itmedia.co.jp/news/articles/2607/06/news089.html).

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwosci

### 2.1. Najwazniejsze wydarzenie tygodnia: Sad Najwyzszy Indii uchylil orzeczenia oparte na fikcyjnych precedensach

Najmocniejszym sygnalem z ostatniego tygodnia byl wyrok Sadu Najwyzszego Indii dotyczacy uzycia nieistniejacych, prawdopodobnie wygenerowanych przez AI, precedensow. Sad uchylil rozstrzygniecia National Company Law Tribunal i National Company Law Appellate Tribunal, wskazujac, ze material oparty na halucynowanych precedensach jest "katastrofalny" dla procesu sadowego i nie moze stanowic decyzji w sensie prawnym. Sad zwrocil tez uwage, ze sedziowie i trybunaly nie moga automatycznie ufac cytowaniom podawanym przez strony lub odnalezionym w niezweryfikowanych narzedziach.  
**Wniosek praktyczny:** generatywna AI jest uzyteczna w researchu, ale kazdy cytat, teza i fragment orzecznictwa musi byc sprawdzony w autorytatywnym zrodle; inaczej ryzyko obejmuje uchylenie orzeczenia, odpowiedzialnosc zawodowa i utrate zaufania do procesu.  
**Zrodla:** [The Hindu - Supreme Court says AI-generated hallucinated precedents catastrophic](https://www.thehindu.com/news/national/methyl-isocyanate-of-law-supreme-court-quashes-verdict-based-on-ai-generated-precedents/article71173725.ece), [The Indian Express - Supreme Court cautions on AI use](https://indianexpress.com/article/legal-news/supreme-court-ai-in-courts-fake-judgments-bar-council-guidelines-10768011/), [ThePrint - SC quashes tribunal orders](https://theprint.in/judiciary/ai-in-courts-sc-quashes-two-tribunal-orders-for-citing-hallucinated-judicial-precedents/2975888/).

### 2.2. Indie: projekt przepisow dla AI w sadach stawia na "human primacy"

Orzeczenie wpisuje sie w szerszy proces regulacyjny w Indiach. Komitet AI Sadu Najwyzszego opublikowal projekt **Regulations for Use of Artificial Intelligence in Courts, 2026**, obejmujacy Sad Najwyzszy, sady wyzsze, sady nizsze, trybunaly i organy adjudykacyjne. Projekt zaklada, ze AI moze miec charakter wylacznie pomocniczy, wymaga ujawniania AI w pismach, zakazuje wykorzystania AI do rozstrzygania spraw, ustalania kary, decyzji o kaucji, oceny wiarygodnosci swiadkow i scoringu ryzyka. Przewiduje tez struktury nadzoru, audyty, rejestry systemow AI i zarzadzanie incydentami.  
**Znaczenie:** Indie probuja polaczyc bardzo aktywne uzycie technologii w sadach, takich jak transkrypcja, tlumaczenie i research, z twarda granica: AI nie moze zastapic sedziego ani rozstrzygac o prawach i wolnosci.  
**Zrodla:** [Draft Regulations for Use of AI in Courts, 2026 - PDF](https://cdnbbsr.s3waas.gov.in/s3ec0490f1f4972d133619a60c30f3559e/uploads/2026/06/2026060342.pdf), [The Indian Express - draft rules: no AI in verdicts, bail eligibility](https://indianexpress.com/article/legal-news/supreme-court-ai-regulations-2026-draft-rules-courts-ban-ai-decisions-10723503/), [LawBeat - draft AI rules for courts](https://lawbeat.in/top-stories/supreme-court-releases-draft-ai-rules-for-courts-lawyers-must-disclose-use-of-ai-in-pleadings-1598628), [Government of India/PIB - AI enhancing access to justice in India](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2026/feb/doc2026211785401.pdf).

### 2.3. USA / Nowy Jork: systemowa regulacja dopuszcza AI bez obowiazkowego ujawniania, ale wymaga weryfikacji

W stanie Nowy Jork od 1 czerwca 2026 r. obowiazuje **22 NYCRR Part 161**, regulujacy uzycie AI w papierach skladanych w sadach Unified Court System. Regula stanowa nie zakazuje AI i nie wymaga automatycznego ujawniania jej uzycia przy kazdym pismie, ale przypomina, ze podpisujacy dokument odpowiada za brak fikcyjnych spraw, przepisow i materialnych nieprawdziwosci. Poszczegolne sady moga przyjac dodatkowy modelowy wymog certyfikacji.  
**Znaczenie:** to model oparty na istniejacych obowiazkach zawodowych, a nie na powszechnym formularzu "AI disclosure". Jest kontrastem wobec podejsc wymagajacych ujawniania AI przy kazdym uzyciu.  
**Zrodla:** [New York Courts - Part 161 Use of Artificial Intelligence Technology](https://www.nycourts.gov/rules/part-161-use-artificial-intelligence-technology), [New York State Bar Association - Part 161 effective June 1, 2026](https://nysba.org/effective-june-1-2026-the-new-york-state-unified-court-system-has-adopted-a-new-rule-regarding-the-use-of-artificial-intelligence/), [Legal AI Governance tracker - NY Part 161](https://legalaigovernance.com/tracker/court-orders/ny-part-161-ai-policy/).

### 2.4. Australia: Federal Court opublikowal praktyczna note GPN-AI

Federal Court of Australia opublikowal **Use of Generative Artificial Intelligence Practice Note (GPN-AI)**. Dokument nie traktuje GenAI jako technologii zakazanej, ale wymaga odpowiedzialnego uzycia, ochrony informacji poufnych, mozliwosci wyjasnienia, jak narzedzie zostalo uzyte, oraz ujawnienia w okreslonych sytuacjach, m.in. gdy AI pomaga przy materialach dowodowych, raportach ekspertow lub oswiadczeniach.  
**Znaczenie:** Australia przyjmuje podejscie operacyjne: dopuszcza AI w pracy procesowej, ale wzmacnia transparentnosc tam, gdzie AI moglaby wplywac na dowody lub fakty.  
**Zrodla:** [Federal Court of Australia - Notice to the Profession, 16 April 2026](https://www.fedcourt.gov.au/law-and-practice/practice-documents/notice-to-profession/16-april-2026), [Federal Court of Australia - GPN-AI Practice Note](https://www.fedcourt.gov.au/law-and-practice/practice-documents/practice-notes/gpn-ai).

### 2.5. Singapur: AI jako narzedzie dostepu do spraw drobnych i dla stron bez pelnomocnika

Singapore Judiciary rozwija narzedzia GenAI w **Small Claims Tribunals**. Oficjalny przewodnik opisuje funkcje generowania streszczen spraw w systemie Community Justice and Tribunals System, gdzie strony moga uzyskac streszczenie stanowiska powoda lub pozwanego wraz z argumentami, dowodami i chronologia. Jednoczesnie singapurski przewodnik dla uzytkownikow sadow stanowi, ze sad ma neutralne podejscie do GenAI, ale uzytkownik pozostaje w pelni odpowiedzialny za tresci wykorzystane w dokumentach.  
**Znaczenie:** Singapur pokazuje praktyczny przypadek AI nastawionej na dostep do wymiaru sprawiedliwosci, a nie na rozstrzyganie: streszczenia, tlumaczenia i przygotowanie stron do postepowan o niskiej wartosci sporu.  
**Zrodla:** [Singapore Judiciary - AI-generated summaries guide](https://www.judiciary.gov.sg/docs/default-source/civil-docs/guide-to-sct-ai-generated-summaries.pdf?sfvrsn=bc53fa8d_1), [Singapore Judiciary - Guide on the Use of Generative AI Tools by Court Users](https://www.judiciary.gov.sg/docs/default-source/news-and-resources-docs/guide-on-the-use-of-generative-ai-tools-by-court-users.pdf?sfvrsn=3900c814_1), [Singapore Courts Annual Report 2024](https://www.judiciary.gov.sg/docs/default-source/publication-docs/sg_courts_annual_report_2024.pdf%3Fsfvrsn%3D61059197_3).

### 2.6. Wielka Brytania: sedziowie moga uzywac AI pomocniczo, ale odpowiadaja osobiscie za wynik

W Anglii i Walii aktualne wytyczne dla judicial office holders podkreslaja, ze AI musi byc zgodna z obowiazkiem ochrony integralnosci wymiaru sprawiedliwosci. Wskazuja ryzyka halucynacji, stronniczosci, poufnosci i bezpieczenstwa, a sedziowie pozostaja osobiscie odpowiedzialni za material powstaly w ich imieniu. Wytyczne dopuszczaja zastosowania pomocnicze, takie jak streszczanie lub prace administracyjne, ale ostrzegaja przed traktowaniem publicznych chatbotow jako autorytatywnych baz prawa.  
**Znaczenie:** brytyjski model jest ostrozny i zawodowo-etyczny: nie buduje jednej szczegolowej regulacji procesowej, lecz wzmacnia odpowiedzialnosc sedziego i prawnika za weryfikacje oraz ochrone poufnosci.  
**Zrodla:** [Courts and Tribunals Judiciary - AI Judicial Guidance, October 2025](https://www.judiciary.uk/guidance-and-resources/artificial-intelligence-ai-judicial-guidance-october-2025/), [Bar Standards Board - Artificial Intelligence Guidance, May 2026](https://www.barstandardsboard.org.uk/static/5e1baa5c-614c-4105-afae9a9ccdf8d97b/c0d1ed62-fcad-4a68-8ab810de5fa9b116/Artificial-Intelligence-Guidance-May-2026.pdf).

### 2.7. Brazylia: risk-based governance AI w sadownictwie

Brazylijska Krajowa Rada Sprawiedliwosci (**CNJ**) przyjela **Resolution No. 615/2025**, ktora tworzy ramy projektowania, wdrazania, audytu i zarzadzania AI w sadownictwie. Rozwiazania sa klasyfikowane wedlug ryzyka; systemy nadmiernego ryzyka sa zakazane, a wysokiego ryzyka wymagaja m.in. oceny wplywu algorytmicznego, monitoringu i nadzoru. Brazylijskie sady wykorzystuja AI m.in. do klasyfikacji spraw, wykrywania podobienstw i spraw masowych, wspierania researchu i prac redakcyjnych, a kraj rozwija tez platforme Sinapses jako rejestr i repozytorium rozwiazan.  
**Znaczenie:** Brazylia jest jednym z najwazniejszych przykladow systemowego podejscia do AI w sadach: zamiast samego ostrzegania przed halucynacjami tworzy infrastrukture governance i audytu dla wielu narzedzi sadowych.  
**Zrodla:** [Oxford Institute of Technology and Justice - Brazil](https://www.techandjustice.bsg.ox.ac.uk/research/brazil), [Regulations.AI - CNJ Resolution No. 615/2025](https://regulations.ai/regulations/RAI-BR-NA-RCN6CXX-2025), [Portulans Institute - Artificial Intelligence in Brazilian Courts](https://portulansinstitute.org/wp-content/uploads/2025/11/Final-ARTIFICIAL-INTELLIGENCE-IN-BRAZILIAN-COURTS-171125-1.pdf).

### 2.8. Chiny: "smart courts" i AI jako asystent, formalnie nie jako sedzia

Chinskie sady od lat rozwijaja koncepcje **smart courts**. W 2026 r. Najwyzszy Sad Ludowy ponownie podkreslal, ze systemy AI dla sadownictwa maja miec pozycje pomocnicza, a podmiotem odpowiedzialnosci sadowej moze byc tylko sedzia. Jednoczesnie Chiny rozwijaja krajowa infrastrukture prawnego AI, w tym platformy do wyszukiwania materialu prawnego, analizy akt, rekomendacji spraw i wsparcia uslug publicznych.  
**Znaczenie:** Chiny sa najbardziej rozwinietym przykladem szerokiej integracji AI w administracji sadowej i obsludze spraw, ale pozostaja tez przypadkiem wymagajacym krytycznej obserwacji ze wzgledu na skale automatyzacji, nadzor i ryzyka dla niezaleznosci sadownictwa.  
**Zrodla:** [Supreme People's Court of China - use technology to empower justice](https://www.court.gov.cn/zixun/xiangqing/492941.html), [China Court - AI platform to boost judicial efficiency](https://english.court.gov.cn/2024-12/05/c_1050751.htm), [Oxford Institute of Technology and Justice - China](https://www.techandjustice.bsg.ox.ac.uk/research/china), [European Chinese Law Research Hub - AI for China's Courts](https://blog.uni-koeln.de/eclrhub/2026/04/27/ai-for-chinas-courts-training-and-testing-for-the-socialist-rule-of-law/).

### 2.9. Wspolny mianownik dla sadow

Z porownania wynika piec wspolnych trendow:

1. **AI jest traktowana jako narzedzie pomocnicze**, nie jako samodzielny decydent. Indie, Chiny, Australia, Wielka Brytania i Singapur wprost podkreslaja role czlowieka jako ostatecznego odpowiedzialnego podmiotu.  
   **Zrodla:** [India draft AI Regulations](https://cdnbbsr.s3waas.gov.in/s3ec0490f1f4972d133619a60c30f3559e/uploads/2026/06/2026060342.pdf), [China SPC statement](https://www.court.gov.cn/zixun/xiangqing/492941.html), [Federal Court of Australia GPN-AI](https://www.fedcourt.gov.au/law-and-practice/practice-documents/practice-notes/gpn-ai), [UK Judicial Guidance](https://www.judiciary.uk/guidance-and-resources/artificial-intelligence-ai-judicial-guidance-october-2025/), [Singapore GenAI guide](https://www.judiciary.gov.sg/docs/default-source/news-and-resources-docs/guide-on-the-use-of-generative-ai-tools-by-court-users.pdf?sfvrsn=3900c814_1).

2. **Najwiekszym praktycznym ryzykiem generatywnej AI w procesie jest fikcyjne prawo**: nieistniejace sprawy, zmyslone cytaty, bledne streszczenia orzecznictwa. Indyjski wyrok z tego tygodnia jest najbardziej wyrazistym ostrzezeniem.  
   **Zrodla:** [The Hindu](https://www.thehindu.com/news/national/methyl-isocyanate-of-law-supreme-court-quashes-verdict-based-on-ai-generated-precedents/article71173725.ece), [The Indian Express](https://indianexpress.com/article/legal-news/supreme-court-ai-in-courts-fake-judgments-bar-council-guidelines-10768011/), [New York Courts Part 161](https://www.nycourts.gov/rules/part-161-use-artificial-intelligence-technology).

3. **Ujawnianie AI nie jest jednolite**: Indie proponuja obowiazek ujawniania w pismach, Australia wymaga ujawnienia w okreslonych kontekstach, Nowy Jork rezygnuje z powszechnego disclosure, a Singapur nie wymaga prewencyjnej deklaracji, chyba ze sad o to poprosi.  
   **Zrodla:** [India draft AI Regulations](https://cdnbbsr.s3waas.gov.in/s3ec0490f1f4972d133619a60c30f3559e/uploads/2026/06/2026060342.pdf), [Federal Court of Australia GPN-AI](https://www.fedcourt.gov.au/law-and-practice/practice-documents/practice-notes/gpn-ai), [New York Courts Part 161](https://www.nycourts.gov/rules/part-161-use-artificial-intelligence-technology), [Singapore GenAI guide](https://www.judiciary.gov.sg/docs/default-source/news-and-resources-docs/guide-on-the-use-of-generative-ai-tools-by-court-users.pdf?sfvrsn=3900c814_1).

4. **Najbezpieczniejsze wdrozenia dotycza administracji i dostepnosci**: transkrypcja, tlumaczenia, streszczenia, klasyfikacja spraw, wykrywanie brakow w e-filingu, wyszukiwanie materialow i obsluga stron bez pelnomocnika.  
   **Zrodla:** [OECD - AI in justice administration and access to justice](https://www.oecd.org/en/publications/2025/06/governing-with-artificial-intelligence_398fa287/full-report/ai-in-justice-administration-and-access-to-justice_f0cbe651.html), [Singapore AI-generated summaries](https://www.judiciary.gov.sg/docs/default-source/civil-docs/guide-to-sct-ai-generated-summaries.pdf?sfvrsn=bc53fa8d_1), [Government of India/PIB](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2026/feb/doc2026211785401.pdf).

5. **Globalne wytyczne przesuwaja sie w strone audytu i governance**, nie tylko etycznych apeli. UNESCO rekomenduje ramy oparte na transparentnosci, odpowiedzialnosci, nadzorze czlowieka i prawach czlowieka; Brazylia i Indie probuja przekladac te zasady na konkretne struktury instytucjonalne.  
   **Zrodla:** [UNESCO - Guidelines for the use of AI systems in courts and tribunals](https://www.unesco.org/en/articles/guidelines-use-ai-systems-courts-and-tribunals), [Brazil CNJ Resolution 615/2025 summary](https://regulations.ai/regulations/RAI-BR-NA-RCN6CXX-2025), [India draft AI Regulations](https://cdnbbsr.s3waas.gov.in/s3ec0490f1f4972d133619a60c30f3559e/uploads/2026/06/2026060342.pdf).

## Najkrotsza synteza

W czesci modelowej tydzien nalezal do multimodalnosci i agentow: Meta weszla mocniej w generowanie obrazow i wideo, OpenAI poprawilo modele realtime voice, Anthropic uporzadkowal dostep do nowych modeli Claude, Tencent wzmocnil segment otwartych modeli MoE, GitHub dopuscil open-weight model do Copilota, NVIDIA pokazala audio-tekstowy Audex, a Sakana AI zaprezentowala regionalnie dostrojone tlumaczenia.

W czesci prawno-sadowej najwazniejsza lekcja jest bardziej dyscyplinujaca: sady coraz chetniej wykorzystuja AI do tlumaczen, streszczen, transkrypcji i zarzadzania sprawami, ale coraz ostrzej oddzielaja to od rozstrzygania. Wyrok Sadu Najwyzszego Indii o halucynowanych precedensach pokazuje, ze brak weryfikacji AI w prawie przestaje byc tylko problemem technicznym, a staje sie bezposrednim zagrozeniem dla waznosci orzeczen i odpowiedzialnosci zawodowej.
