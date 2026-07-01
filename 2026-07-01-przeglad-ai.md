# Tygodniowy przegląd AI — 2026-07-01

**Okres objęty przeglądem:** przede wszystkim 24 czerwca - 1 lipca 2026 r.  
**Zakres:** najważniejsze wydarzenia ogólne w AI oraz zastosowania AI w prawie i wymiarze sprawiedliwości, ze szczególnym uwzględnieniem sądów.

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

### 1.1. OpenAI pokazało rodzinę GPT-5.6: Sol, Terra i Luna

26 czerwca OpenAI rozpoczęło ograniczony preview rodziny GPT-5.6. W skład serii wchodzą: **Sol** jako model flagowy, **Terra** jako model zbalansowany kosztowo oraz **Luna** jako wariant szybki i tańszy. Najważniejsze znaczenie tej premiery polega nie tylko na wzroście możliwości, lecz także na modelu dystrybucji: dostęp jest początkowo ograniczony do wybranych, zaufanych partnerów, w związku z procesem uzgodnionym z administracją USA w obszarze cyberbezpieczeństwa.

OpenAI podkreśla wzrost kompetencji w zadaniach agentowych, kodowaniu, biologii i cyberbezpieczeństwie. Sol otrzymał nowe poziomy pracy: `max` dla głębszego rozumowania oraz `ultra`, który ma wykorzystywać subagentów do zadań złożonych. To ważny sygnał rynkowy: frontierowe modele coraz częściej są projektowane nie jako chatboty, ale jako systemy długiego działania, koordynujące narzędzia, podzadania i procesy bezpieczeństwa.

**Dlaczego to istotne:**

- preview GPT-5.6 pokazuje dalsze przesunięcie rynku w stronę modeli agentowych;
- premiera została powiązana z warstwowym stackiem zabezpieczeń i kontrolowaną dystrybucją;
- OpenAI wyraźnie komunikuje napięcie między szerokim dostępem do modeli a oczekiwaniami państwa wobec cyberbezpieczeństwa.

**Źródła:**

- OpenAI, „Previewing GPT-5.6 Sol: a next-generation model” — https://openai.com/index/previewing-gpt-5-6-sol/
- Axios o ograniczeniu premiery na prośbę administracji USA — https://www.axios.com/2026/06/25/trump-administration-openai-gpt-model-release
- The Verge o premierze GPT-5.6 i kontekście regulacyjnym — https://www.theverge.com/ai-artificial-intelligence/957845/openai-gpt-5-6-trump-administration-ai-preview

### 1.2. Anthropic wydało Claude Sonnet 5 jako tańszy model agentowy

30 czerwca Anthropic ogłosiło **Claude Sonnet 5**, opisując go jako najbardziej agentowy model z linii Sonnet. Model ma lepiej planować, używać narzędzi, obsługiwać kod i wykonywać dłuższe zadania autonomiczne. Anthropic pozycjonuje go jako model bliski wydajnością droższym modelom Opus, ale dostępny w niższej cenie.

Model jest dostępny w planach Claude, w Claude Code oraz przez API pod nazwą `claude-sonnet-5`. Cena promocyjna do 31 sierpnia 2026 r. wynosi 2 USD za milion tokenów wejściowych i 10 USD za milion tokenów wyjściowych, później 3/15 USD. To ważna premiera dla rynku narzędzi programistycznych i agentów, bo obniża koszt wieloetapowych przepływów pracy, w których zużycie tokenów jest wysokie.

**Dlaczego to istotne:**

- Sonnet 5 wzmacnia segment „średnich” modeli agentowych, które mają być używane produkcyjnie na dużą skalę;
- Anthropic wskazuje poprawę w rozumowaniu, tool use, kodowaniu i knowledge work;
- konkurencja przesuwa się z samej jakości odpowiedzi na relację koszt/wykonanie w długich zadaniach autonomicznych.

**Źródła:**

- Anthropic, „Introducing Claude Sonnet 5” — https://www.anthropic.com/news/claude-sonnet-5
- TechCrunch o premierze i pozycjonowaniu kosztowym Sonnet 5 — https://techcrunch.com/2026/06/30/anthropic-launches-claude-sonnet-5-as-a-cheaper-way-to-run-agents/

### 1.3. Google udostępniło Nano Banana 2 Lite i Gemini Omni Flash dla twórców

30 czerwca Google ogłosiło dwie premiery w obszarze generatywnych mediów: **Nano Banana 2 Lite** oraz **Gemini Omni Flash**. Nano Banana 2 Lite to szybki i tańszy model obrazu w rodzinie Gemini Image, przeznaczony do wysokoprzepustowych procesów generowania i iterowania grafik. Google deklaruje generowanie obrazu w około 4 sekundy oraz cenę 0,034 USD za obraz 1K.

Gemini Omni Flash został udostępniony deweloperom w Google AI Studio i Gemini API jako model do generowania i konwersacyjnej edycji wideo. Obsługuje wejścia tekstowe, obrazowe i wideo oraz ma służyć do wieloetapowej edycji, zachowania kontekstu i łączenia workflow obraz-wideo. Cena podana przez Google to 0,10 USD za sekundę wyjściowego wideo.

**Dlaczego to istotne:**

- Google wzmacnia pozycję w generatywnych mediach, nie tylko w modelach tekstowych;
- oba modele są projektowane pod skalowanie i szybkie prototypowanie;
- nacisk na SynthID i narzędzia weryfikacji wskazuje, że transparentność treści syntetycznych pozostaje centralnym elementem wdrożeń medialnych.

**Źródła:**

- Google, „Start building with Nano Banana 2 Lite and Gemini Omni Flash” — https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-flash-nano-banana-2-lite/
- Google Cloud Blog, „Bringing speed and strong cost performance to the market with Gemini Omni Flash and Nano Banana 2 Lite” — https://cloud.google.com/blog/products/ai-machine-learning/nano-banana-2-lite-and-gemini-omni-flash-available

### 1.4. Meituan zaprezentował LongCat-2.0, duży model MoE trenowany na chińskich chipach

30 czerwca Meituan/LongCat zaprezentował **LongCat-2.0**, model Mixture-of-Experts o 1,6 bln parametrów, z deklarowanym kontekstem 1 mln tokenów i aktywacją rzędu ok. 33-56 mld parametrów na token. Według materiałów LongCat model jest przeznaczony głównie do agentowego kodowania i zadań software engineering. Szczególnie ważny jest aspekt infrastrukturalny: Meituan twierdzi, że trening i inferencja modelu odbyły się na klastrze 50 tys. krajowych chińskich akceleratorów.

Trzeba odnotować niuans dostępności: repozytorium GitHub ma licencję MIT, ale w momencie publikacji materiały wskazują, że pełne wagi są „coming soon”. Oznacza to, że komunikat o „open-source” należy weryfikować przez faktyczną dostępność wag, nie tylko przez zapowiedź i repozytorium.

**Dlaczego to istotne:**

- LongCat-2.0 jest istotnym sygnałem chińskiej niezależności infrastrukturalnej w AI;
- model celuje w obszar agentowego kodowania, jeden z najważniejszych komercyjnych use case'ów LLM;
- przypadek pokazuje, że rynek open-weight/open-source wymaga dokładnego rozróżniania licencji, kodu, kart modeli i rzeczywistej dostępności wag.

**Źródła:**

- Oficjalna strona LongCat Models — https://www.longcatai.org/models/
- Repozytorium GitHub `meituan-longcat/LongCat-2.0` — https://github.com/meituan-longcat/LongCat-2.0
- VentureBeat o LongCat-2.0 i statusie wag — https://venturebeat.com/technology/meituan-open-sources-longcat-2-0-the-1-6t-near-frontier-agentic-coding-model-thats-been-leading-openrouter-trained-entirely-on-chinese-chips
- Reuters, przez WTBX, o treningu na krajowych chipach — https://wtbx.com/2026/06/30/chinas-meituan-says-new-ai-model-trained-on-domestic-chips/

### 1.5. Google Gemini 3.5 Pro: oczekiwana premiera przesunięta na lipiec

W tygodniu objętym przeglądem ważnym wydarzeniem była również informacja o przesunięciu publicznej premiery **Gemini 3.5 Pro**. Business Insider podał, że Google przesuwa dostępność z czerwca na lipiec, aby zebrać więcej feedbacku od wczesnych testerów i dopracować model. To nie jest premiera modelu, ale istotny sygnał rynkowy: największe laboratoria coraz częściej opóźniają szerokie wydania, jeśli modele mają działać w długich, agentowych zadaniach i środowiskach enterprise.

**Dlaczego to istotne:**

- opóźnienie pokazuje, że gotowość frontierowego modelu jest oceniana nie tylko benchmarkami, ale także zachowaniem w realnych workflow;
- Google pozostaje pod presją konkurencji w kodowaniu i agentach, gdzie OpenAI i Anthropic komunikują mocne wzrosty;
- rynek przechodzi z „premier demonstracyjnych” do kontrolowanych, etapowych wdrożeń.

**Źródła:**

- Business Insider o przesunięciu Gemini 3.5 Pro — https://www.businessinsider.com/google-3-5-pro-july-release-tokens-ai-agents-model-2026-6
- Times of India o doniesieniach dotyczących opóźnienia — https://timesofindia.indiatimes.com/technology/tech-news/google-delays-launch-of-gemini-3-5-pro-that-ceo-sundar-pichai-said-coming-in-june-says-it-needs-to-spend-extra-time-for-/articleshow/131993789.cms

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

### 2.1. USA: sądy zaostrzają odpowiedzialność za halucynacje AI w pismach procesowych

W USA utrwalił się trend nakładania sankcji za pisma procesowe zawierające fałszywe cytowania, nieistniejące orzeczenia lub zmyślone fragmenty wygenerowane z udziałem AI. 24 czerwca opisano sprawę z Nowego Jorku, w której Appellate Division, Second Department, nałożył sankcje pieniężne na prawnika i kancelarię za brief zawierający fikcyjne cytowania i błędne przedstawienia orzeczeń. Sankcja wobec samej kancelarii jest szczególnie ważna, bo sąd uznał, że odpowiedzialność może objąć nie tylko autora błędu, ale także podmiot firmujący dokument.

Równolegle komentowana była nowa nowojorska reguła **22 NYCRR Part 161**, obowiązująca od 1 czerwca 2026 r. Reguła nie zakazuje użycia AI i zasadniczo nie wymaga odrębnego ujawnienia użycia AI w każdym piśmie. Przenosi jednak ciężar na odpowiedzialność za produkt końcowy: prawnik lub strona muszą samodzielnie zweryfikować, czy dokument nie zawiera fikcyjnych spraw, przepisów, faktów ani innych materiałów.

**Znaczenie dla sądów i praktyki:**

- sądy nie karzą za samo użycie AI, lecz za podpisanie i złożenie niezweryfikowanego materiału;
- model „accountability over disclosure” z Nowego Jorku może być alternatywą dla obowiązkowych certyfikatów użycia AI;
- kancelarie muszą wdrażać procedury kontroli cytowań, a nie tylko polityki zakazujące nieautoryzowanego użycia AI.

**Źródła:**

- Law.com o sankcjach w Appellate Division, Second Department — https://www.law.com/newyorklawjournal/2026/06/24/brooklyn-based-appeals-court-orders-law-firm-to-pay-2500-over-ai-hallucinations/
- Above the Law o sankcjach 10,5 tys. USD — https://abovethelaw.com/2026/06/appeals-court-orders-10k-in-sanctions-over-ai-related-filing-mistakes/
- Legal AI Governance Tracker, New York Part 161 — https://legalaigovernance.com/tracker/court-orders/ny-part-161-ai-policy/
- Institute for AI Policy & Governance o regule nowojorskiej — https://aipg.institute/2026/06/26/disclosure-is-not-accountability-new-yorks-ai-court-rule-and-the-future-of-legal-responsibility/

### 2.2. USA: mozaika lokalnych nakazów sądowych zamiast jednolitego standardu federalnego

W Stanach Zjednoczonych nadal nie ma jednolitej federalnej reguły dla AI w pismach procesowych. Zamiast tego funkcjonuje mozaika lokalnych nakazów, standing orders i polityk sędziowskich. Część sądów wymaga ujawnienia użycia AI, część certyfikacji weryfikacji, część tylko przypomina o obowiązkach wynikających z Rule 11 i zasad etyki zawodowej.

To tworzy praktyczne ryzyko dla pełnomocników: zgodność z zasadami AI w sądzie trzeba sprawdzać per jurysdykcja, per sąd, a często per konkretny sędzia. Trend jest jednak spójny: niezależnie od różnic formalnych, sądy wymagają, aby człowiek zweryfikował fakty, cytowania i podstawy prawne.

**Znaczenie dla sądów i praktyki:**

- brak jednego standardu zwiększa koszty compliance;
- lokalne orders stają się realnym źródłem prawa procesowego w obszarze AI;
- rośnie znaczenie wewnętrznych checklist i narzędzi walidacji cytowań.

**Źródła:**

- Federal and State Court Orders on AI, Legal AI Governance — https://legalaigovernance.com/tracker/court-orders/
- Chambers, „Artificial Intelligence 2026 - USA” — https://practiceguides.chambers.com/practice-guides/artificial-intelligence-2026/usa/trends-and-developments
- ABA Journal o sankcjach 9th Circuit za halucynacje AI — https://www.abajournal.com/news/article/attorneys-lack-of-candor-over-ai-errors-leads-to-stricter-sanctions

### 2.3. Turcja: sąd handlowy jawnie ujawnił użycie AI przy sporządzaniu uzasadnienia

W analizie opublikowanej 25 czerwca opisano orzeczenie Istanbul 14th Commercial Court of First Instance, w którym sąd wprost ujawnił użycie AI jako narzędzia pomocniczego przy przygotowaniu uzasadnienia. Sprawa dotyczyła uznania i wykonania zagranicznego orzeczenia. Według opisu AI zostało użyte do przeglądu zagranicznych źródeł prawa, weryfikacji zagranicznych orzeczeń oraz tłumaczenia tekstów prawnych na turecki.

Najważniejsze jest to, że sąd nie przedstawił AI jako podmiotu współdecydującego. Narzędzie miało wspierać research i tłumaczenie, a nie ocenę dowodów, wykładnię prawa czy wydanie rozstrzygnięcia. Jawne ujawnienie użycia AI może być ważnym wzorcem transparentności: zamiast udawać, że narzędzi nie ma, sąd określa zakres ich zastosowania i granice odpowiedzialności sędziego.

**Znaczenie dla sądów i praktyki:**

- przykład pokazuje możliwy model dopuszczalnego użycia AI przez sąd: research, tłumaczenie, weryfikacja źródeł;
- transparentne ujawnienie ogranicza ryzyko „czarnej skrzynki”;
- sąd podkreśla, że odpowiedzialność za rozstrzygnięcie pozostaje po stronie sędziego.

**Źródła:**

- Paksoy, „Turkish courts and artificial intelligence — Part I” — https://paksoy.av.tr/en/2026/06/turkish-courts-and-artificial-intelligence-part-i-istanbul-commercial-court-expressly-discloses-use-of-ai-in-drafting-reasoned-judgment/
- Mondaq, ta sama analiza z datą 25 czerwca 2026 r. — https://www.mondaq.com/turkey/new-technology/1806778/turkish-courts-and-artificial-intelligence-part-i-istanbul-commercial-court-expressly-discloses-use-of-ai-in-drafting-reasoned-judgment
- GSI Brief o decyzji Istanbul 14th Commercial Court — https://www.goksusafiisik.av.tr/en/briefs/gsi-brief-189

### 2.4. Ghana: ogólnokrajowy asystent AI dla 445 sędziów i magistrates

W czerwcu ogłoszono wdrożenie **Eskwai Clerk**, asystenta AI dla wszystkich 445 sędziów i magistrates w Ghanie. Narzędzie, rozwijane przez Kwame AI we współpracy z Judicial Service of Ghana, ma wspierać research prawny, analizę dokumentów oraz przygotowywanie projektów orzeczeń i uzasadnień. Według komunikatów narzędzie ma być wdrażane wraz ze szkoleniem i z zachowaniem pełnego nadzoru człowieka.

To jeden z najciekawszych przykładów z Afryki, bo nie chodzi o pilotaż w pojedynczym sądzie, ale o ogólnokrajowe narzędzie dla całej grupy sędziów. Wdrożenie jest odpowiedzią na przeciążenie sądów i ograniczoną liczbę orzeczników w stosunku do populacji.

**Znaczenie dla sądów i praktyki:**

- Ghana testuje AI jako narzędzie zwiększania przepustowości wymiaru sprawiedliwości;
- kluczowe będą szkolenia, standardy weryfikacji i kontrola nad treścią projektów orzeczeń;
- przykład pokazuje, że AI w sądownictwie może być wdrażane szybciej w jurysdykcjach z silną potrzebą redukcji opóźnień.

**Źródła:**

- MyJoyOnline o wdrożeniu AI dla 445 sędziów — https://www.myjoyonline.com/judicial-service-to-deploy-ai-assistant-for-all-445-judges-nationwide/
- Eskwai/Kwame AI o partnerstwie z Judicial Service of Ghana — https://eskwai.kwame.ai/resources/blogs/introducing-eskwai-clerk-and-partnership-with-the-judicial-service-of-ghana
- Tech Labari o Eskwai Clerk — https://techlabari.com/kwame-ai-releases-ai-assistant-eskwai-clerk-to-improve-judicial-service-in-ghana/

### 2.5. Indie: projekt ogólnokrajowych regulacji AI w sądach, z zakazem risk scoringu

Choć projekt indyjskich regulacji został opublikowany 3 czerwca, wciąż był jednym z najważniejszych punktów odniesienia dla debat w ostatnich tygodniach. Supreme Court of India AI Committee opublikował projekt **Regulations for Use of Artificial Intelligence (AI) in Courts, 2026**, obejmujący Supreme Court, High Courts, sądy niższe, trybunały i organy adjudykacyjne.

Projekt opiera się na zasadach human primacy, transparentności, odpowiedzialności, ochrony danych i niezależności sądownictwa. Najmocniejszym elementem jest zakaz użycia AI do risk scoringu w procesach sądowych, w tym oceny ryzyka ucieczki, recydywy, kwalifikacji do kaucji czy wiarygodności stron i świadków. Projekt zakazuje też samodzielnego rozstrzygania przez AI oraz używania nieujawnionych lub niewyjaśnialnych systemów w sprawach wpływających na prawa i wolność osobistą.

**Znaczenie dla sądów i praktyki:**

- Indie proponują jeden z najbardziej szczegółowych sądowych frameworków AI;
- zakaz risk scoringu jest wyraźną odpowiedzią na krytykę systemów predykcyjnych w wymiarze sprawiedliwości;
- projekt łączy przyzwolenie na AI w administracji i researchu z bardzo twardymi granicami dla decyzji sądowych.

**Źródła:**

- Oficjalny projekt regulacji, Supreme Court of India AI Committee — https://cdnbbsr.s3waas.gov.in/s3ec0490f1f4972d133619a60c30f3559e/uploads/2026/06/2026060342.pdf
- Indian Express o zakazie AI w werdyktach i kaucji — https://indianexpress.com/article/legal-news/supreme-court-ai-regulations-2026-draft-rules-courts-ban-ai-decisions-10723503/
- Frontline o zakazie risk scoringu — https://frontline.thehindu.com/incoming/india-ai-risk-scoring-ban/article71108518.ece
- The Leaflet, szczegółowe omówienie projektu — https://theleaflet.in/law-and-technology/explained-the-supreme-court-of-indias-draft-regulations-for-use-of-artificial-intelligence-in-courts-2026

### 2.6. Unia Europejska: AI w wymiarze sprawiedliwości jako system wysokiego ryzyka

W Europie kluczowym punktem odniesienia pozostaje AI Act. Załącznik III klasyfikuje jako wysokiego ryzyka systemy AI używane przez organy sądowe lub w ich imieniu do badania i interpretacji faktów oraz prawa albo do stosowania prawa do konkretnego stanu faktycznego. W praktyce oznacza to, że sądowe narzędzia AI do researchu, analizy spraw czy wspierania decyzji będą podlegać wymaganiom dotyczącym dokumentacji, jakości danych, nadzoru człowieka, odporności, transparentności i zarządzania ryzykiem.

W porównaniu z podejściem amerykańskim, które jest rozproszone i oparte na lokalnych orders, UE przyjmuje model systemowy: klasyfikacja ryzyka jest wbudowana w horyzontalne prawo o AI. Wymiar sprawiedliwości znajduje się w katalogu zastosowań szczególnie wrażliwych, bo ryzyko dotyczy praw podstawowych, rzetelnego procesu i niezależności sądów.

**Znaczenie dla sądów i praktyki:**

- narzędzia AI dla sądów w UE będą oceniane przez pryzmat high-risk compliance;
- dostawcy legal tech muszą projektować systemy z myślą o audytowalności, jakości danych i nadzorze człowieka;
- sądy będą musiały odróżniać narzędzia czysto administracyjne od systemów realnie wspierających analizę prawną lub faktyczną.

**Źródła:**

- EU AI Act, Annex III, pkt 8 — https://artificialintelligenceact.eu/annex/3/
- eucrim o AI i digitalizacji współpracy sądowej — https://eucrim.eu/articles/artificial-intelligence-and-digitalisation-of-judicial-cooperation/
- OECD, „AI in justice administration and access to justice” — https://www.oecd.org/en/publications/2025/06/governing-with-artificial-intelligence_398fa287/full-report/ai-in-justice-administration-and-access-to-justice_f0cbe651.html

### 2.7. ECOWAS Court: cyfrowy system zarządzania sprawami jako fundament dalszej automatyzacji

30 czerwca ECOWAS Court of Justice uruchomił **Electronic Case Management System (ECMS)**. To nie jest system AI sensu stricto, ale jest ważny dla przyszłych zastosowań AI w wymiarze sprawiedliwości, ponieważ cyfryzacja akt, e-filing, śledzenie spraw w czasie rzeczywistym i elektroniczne repozytoria są warunkiem sensownych wdrożeń analityki i automatyzacji.

System ma działać w językach angielskim, francuskim i portugalskim, umożliwiać elektroniczne składanie pism, zarządzanie dokumentami, powiadomienia, monitoring spraw i wirtualne rozprawy. Sąd deklaruje cel pełnej cyfryzacji do 2030 r.

**Znaczenie dla sądów i praktyki:**

- bez elektronicznych akt i metadanych nie da się bezpiecznie wdrażać bardziej zaawansowanej AI;
- ECOWAS tworzy regionalną infrastrukturę cyfrowej sprawiedliwości dla państw Afryki Zachodniej;
- wielojęzyczność systemu może w przyszłości ułatwiać narzędzia tłumaczeniowe i wyszukiwawcze.

**Źródła:**

- Voice of Nigeria o uruchomieniu ECMS — https://von.gov.ng/ecowas-court-launches-electronic-case-management-system/
- allAfrica o cyfryzacji ECOWAS Court — https://allafrica.com/stories/202606300395.html
- Arise News o ECMS i cyfrowej sprawiedliwości — https://www.arise.tv/ecowas-court-launches-electronic-case-management-system-to-expand-digital-justice/

### 2.8. Brazylia, Chiny i Singapur: trzy różne modele sądowej AI

W tle wydarzeń tygodnia warto odnotować porównawcze badania nad AI w sądownictwie Brazylii, Chin i Singapuru. Brazylia rozwija scentralizowany model governance, oparty m.in. na Resolution CNJ No. 615/2025, rejestracji systemów, ocenach wpływu i nadzorze człowieka. Chiny reprezentują model efektywnościowy, w którym automatyzacja i AI są głęboko integrowane z infrastrukturą „smart courts”. Singapur zajmuje pozycję pośrednią: dopuszcza pragmatyczne wdrożenia, ale mocno akcentuje profesjonalną odpowiedzialność użytkowników.

**Znaczenie dla sądów i praktyki:**

- nie ma jednego globalnego modelu AI w sądownictwie;
- Brazylia pokazuje ścieżkę centralnej regulacji i audytowalności;
- Chiny pokazują skalę integracji AI z infrastrukturą sądową;
- Singapur pokazuje model pragmatyczny, oparty na odpowiedzialności i stopniowym wdrażaniu.

**Źródła:**

- Oxford Institute of Technology and Justice o Brazylii — https://www.techandjustice.bsg.ox.ac.uk/research/brazil
- Regulations.AI o Resolution CNJ No. 615/2025 — https://regulations.ai/regulations/RAI-BR-NA-RCN6CXX-2025
- „JudgeGPT: When Progress Meets Precedent” — https://btlj.org/wp-content/uploads/2026/04/40.4_Ferrari.pdf
- Stimson Center, „AI in Global Majority Judicial Systems” — https://www.stimson.org/2026/ai-in-global-majority-judicial-systems/

## Najważniejsze wnioski tygodnia

1. **Modele frontierowe przechodzą w fazę agentową.** OpenAI, Anthropic, Google i Meituan komunikują nie tylko lepsze odpowiedzi, ale dłuższe zadania, narzędzia, subagentów, kodowanie, multimedia i workflow.
2. **Dostęp do najmocniejszych modeli staje się bardziej kontrolowany.** GPT-5.6 pokazuje, że bezpieczeństwo narodowe i cyberbezpieczeństwo mogą wpływać na tempo oraz zakres premier.
3. **Koszt i szybkość stają się równie ważne jak benchmarki.** Sonnet 5 i Nano Banana 2 Lite są pozycjonowane przez pryzmat kosztu produkcyjnego, nie tylko jakości.
4. **Sądy odróżniają użycie AI od odpowiedzialności za wynik.** W USA i Turcji widać rosnące znaczenie weryfikacji, transparentności i odpowiedzialności człowieka.
5. **Najbardziej wrażliwe zastosowania sądowe są ograniczane.** Indie i UE wyraźnie wskazują, że AI może wspierać administrację i research, ale decyzje o wolności, winie, wiarygodności czy ryzyku wymagają twardych ograniczeń.
6. **Cyfryzacja sądów jest warunkiem AI.** ECOWAS Court pokazuje, że e-filing, elektroniczne akta i case management są fundamentem przyszłej automatyzacji.
