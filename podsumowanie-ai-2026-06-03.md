# Tygodniowy przeglad AI - 2026-06-03

**Data sporządzenia:** 3 czerwca 2026 r.  
**Zakres:** najważniejsze wydarzenia z okresu ok. 27 maja - 3 czerwca 2026 r.  
**Uwaga metodologiczna:** priorytetowo potraktowano źródła pierwotne (komunikaty firm, sądów, ustawodawców i instytucji publicznych), a przy doniesieniach medialnych wskazano, czy opisują one pilotaż, propozycję regulacyjną czy obowiązującą zmianę.

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

### 1.1. Anthropic udostępnił Claude Opus 4.8 i przesunął akcent na agentów wieloetapowych

28 maja Anthropic ogłosił Claude Opus 4.8, nową wersję swojego najmocniejszego publicznie dostępnego modelu. Firma opisuje ją jako „modest but tangible improvement” względem Opus 4.7, ale znaczenie premiery polega przede wszystkim na poprawie niezawodności w zadaniach agentowych, kodowaniu i pracy długokontekstowej. Anthropic podkreśla, że Opus 4.8 lepiej sygnalizuje niepewność i rzadziej przepuszcza błędy we własnym kodzie bez komentarza; według firmy w ewaluacjach był ok. czterokrotnie mniej skłonny niż poprzednik do pozostawienia wad w kodzie bez ostrzeżenia.

Najważniejsze elementy premiery:

- **Dynamic Workflows w Claude Code** - funkcja w research preview pozwalająca modelowi planować duże zadania i uruchamiać setki równoległych subagentów w jednej sesji, np. przy migracjach całych codebase'ów.
- **Kontrola wysiłku modelu** w claude.ai i Cowork - użytkownicy mogą regulować kompromis między głębszym rozumowaniem a szybkością/zużyciem limitów.
- **Fast mode** - wariant działania z deklarowaną szybkością 2,5x i niższym kosztem niż wcześniejsze tryby szybkie.
- **API** - model dostępny jako `claude-opus-4-8`, przy standardowej cenie bez zmian względem Opus 4.7.

Znaczenie: to kolejny sygnał, że rynek frontier AI przesuwa się od pojedynczej odpowiedzi chatbota do długotrwałych, kontrolowanych przebiegów agentowych z walidacją wyniku. Warto zwrócić uwagę, że w komunikacie Anthropic cytuje także wynik na „Legal Agent Benchmark”, co łączy tę premierę z rynkiem profesjonalnych narzędzi prawniczych.

Źródła:

- Anthropic, „Introducing Claude Opus 4.8”, 28.05.2026: <https://www.anthropic.com/news/claude-opus-4-8>
- TechCrunch, omówienie premiery i Dynamic Workflows: <https://techcrunch.com/2026/05/28/anthropic-releases-opus-4-8-with-new-dynamic-workflow-tool/>

### 1.2. Anthropic rozszerzył Project Glasswing i kontrolowany dostęp do Claude Mythos Preview

2 czerwca Anthropic poinformował o rozszerzeniu Project Glasswing - programu wykorzystującego Claude Mythos Preview do defensywnego wyszukiwania podatności w krytycznym oprogramowaniu. Po początkowej grupie ok. 50 partnerów dostęp ma zostać rozszerzony o ok. 150 nowych organizacji z ponad 15 krajów, po spełnieniu wymagań bezpieczeństwa. Firma wskazuje, że dotychczas partnerzy znaleźli ponad 10 tys. podatności o wysokiej lub krytycznej wadze.

Znaczenie: Anthropic nie wypuszcza Mythos publicznie, bo model tej klasy może ułatwiać zarówno obronę, jak i atak. Jest to ważny przykład „kontrolowanej dyfuzji” najbardziej ryzykownych możliwości: najpierw infrastruktura krytyczna, maintainerzy open source i testerzy bezpieczeństwa, a dopiero później ewentualne szersze udostępnienie po wzmocnieniu zabezpieczeń.

Źródła:

- Anthropic, „Expanding Project Glasswing”, 2.06.2026: <https://www.anthropic.com/news/expanding-project-glasswing>
- Cybersecurity Dive, omówienie rozszerzenia na operatorów infrastruktury krytycznej: <https://www.cybersecuritydive.com/news/ai-anthropic-claude-mythos-project-glasswing-expand/821714/>

### 1.3. Microsoft AI zaprezentował siedem modeli MAI, w tym MAI-Thinking-1 i MAI-Code-1-Flash

2 czerwca Microsoft AI ogłosił rodzinę siedmiu modeli MAI obejmującą rozumowanie, kodowanie, obraz, transkrypcję i głos. Najważniejszy jest **MAI-Thinking-1**, określany jako flagowy model reasoningowy Microsoftu. Microsoft opisuje go jako model trenowany od podstaw na „clean data”, bez destylacji z modeli zewnętrznych. W osobnym opisie modelu firma podaje architekturę MoE: 35 mld aktywnych parametrów i ok. 1 bln parametrów łącznie, 256 tys. tokenów kontekstu, kompatybilność z Chat Completions API oraz dostęp w private preview przez Microsoft Foundry.

Pozostałe elementy rodziny:

- **MAI-Code-1-Flash** - szybki, 5-miliardowy model kodujący zintegrowany z GitHub Copilot, VS Code i stosem Microsoftu.
- **MAI-Image-2.5** i wariant Flash - generowanie/edycja obrazów.
- **MAI Transcribe-1.5** - transkrypcja z obsługą terminologii domenowej w 43 językach.
- **MAI-Voice-2** i zapowiedziany wariant Flash - generowanie mowy w 15 językach.
- **Frontier Tuning** - koncepcja dostrajania modeli poprzez uczenie ze śladów realnych workflow w środowisku klienta.
- **Model dla Mayo Clinic** - wspólny projekt frontier AI dla zastosowań klinicznych, najpierw w środowisku Mayo Clinic, później przez Azure Foundry.

Znaczenie: Microsoft coraz wyraźniej buduje własny stos modeli, danych, benchmarków, dostrajania i dystrybucji, a nie tylko integruje modele partnerów. To istotne dla konkurencji w enterprise AI, bo firma akcentuje licencjonowane dane, brak destylacji oraz możliwość tuningu pod konkretne organizacje.

Źródła:

- Microsoft AI, „Building a hill-climbing machine: Launching seven new MAI models”, 2.06.2026: <https://microsoft.ai/news/building-a-hillclimbing-machine-launching-seven-new-mai-models/>
- Microsoft AI, „Introducing MAI-Thinking-1”, 2.06.2026: <https://microsoft.ai/news/introducing-mai-thinking-1/>
- Microsoft AI, „Introducing MAI-Code-1-Flash”, 2.06.2026: <https://microsoft.ai/news/introducingmai-code-1-flash/>

### 1.4. OpenAI rozszerzył Codex poza programowanie i udostępnił modele frontier oraz Codex na AWS

1 czerwca OpenAI ogłosił ogólną dostępność modeli frontier i Codex na AWS, w tym przez Amazon Bedrock. Z punktu widzenia dużych organizacji kluczowe jest to, że modele OpenAI można wdrażać w istniejących procesach bezpieczeństwa, zgodności, rozliczeń i governance AWS, także w regionach Commercial i GovCloud.

2 czerwca OpenAI ogłosił z kolei duże rozszerzenie Codex jako narzędzia dla „knowledge work”, nie tylko dla developerów. Według firmy Codex ma ponad 5 mln użytkowników tygodniowo, a osoby nietechniczne stanowią ok. 20% bazy i rosną ponad trzykrotnie szybciej niż developerzy. Nowe funkcje:

- **role-specific plugins** - 6 zestawów wtyczek dla analityki danych, produkcji kreatywnej, sprzedaży, projektowania produktu, inwestowania public equity i bankowości inwestycyjnej; łącznie 62 aplikacje i 110 umiejętności;
- **Sites** - podgląd dla klientów Business/Enterprise pozwalający generować i udostępniać interaktywne strony/aplikacje w workspace;
- **Annotations** - wskazywanie konkretnych fragmentów dokumentów, arkuszy, slajdów lub stron do poprawy przez agenta.

Znaczenie: OpenAI przesuwa Codex z kategorii „agent kodujący” w stronę warstwy orkiestracji pracy biurowej i narzędzi SaaS. W praktyce konkurencja między modelami zaczyna obejmować nie tylko jakość odpowiedzi, ale też możliwość działania w realnych systemach firmy, kontrolę uprawnień i audytowalność.

Źródła:

- OpenAI, „OpenAI frontier models and Codex are now available on AWS”, 1.06.2026: <https://openai.com/index/openai-frontier-models-and-codex-are-now-available-on-aws/>
- AWS, „GPT-5.5, GPT-5.4, and Codex from OpenAI are now generally available on Amazon Bedrock”, 1.06.2026: <https://aws.amazon.com/about-aws/whats-new/2026/06/amazon-bedrock-openai-models-codex-generally-available/>
- OpenAI, „Codex for every role, tool, and workflow”, 2.06.2026: <https://openai.com/index/codex-for-every-role-tool-workflow/>

### 1.5. MiniMax M3 i NVIDIA Cosmos 3: otwarte lub zapowiedziane otwarte modele dla agentów, multimodalności i „physical AI”

W końcówce tygodnia pojawiły się też dwie premiery istotne dla otwartego ekosystemu:

- **MiniMax M3** - MiniMax opisał model jako natively multimodalny, z kontekstem do 1 mln tokenów, nastawiony na kodowanie i pracę agentową, zdolny do operowania komputerem. Firma twierdzi, że API jest już dostępne, a raport techniczny i wagi mają zostać opublikowane w ciągu 10 dni od premiery.
- **NVIDIA Cosmos 3** - 31 maja NVIDIA ogłosiła otwarty model foundation dla „physical AI”, łączący reasoning wizyjny, generowanie świata i predykcję akcji. Dostępne mają być warianty Cosmos 3 Super i Nano, a Edge ma nadejść później.

Znaczenie: oba przykłady pokazują, że możliwości do niedawna kojarzone głównie z zamkniętymi modelami frontier - bardzo długi kontekst, multimodalność, obsługa komputera, modele świata dla robotyki i autonomii - są coraz silniej przenoszone do ekosystemu otwartego lub półotwartego.

Źródła:

- MiniMax, „MiniMax M3: Frontier Coding, 1M Context, Native Multimodality - All in One Model”: <https://www.minimax.io/blog/minimax-m3>
- NVIDIA Newsroom, „NVIDIA Launches Cosmos 3, the Open Frontier Foundation Model for Physical AI”, 31.05.2026: <https://nvidianews.nvidia.com/news/nvidia-launches-cosmos-3-the-open-frontier-foundation-model-for-physical-ai>

### 1.6. Regulacja frontier AI w USA: Illinois przyjął projekt ustawy o audytach i raportowaniu bezpieczeństwa

27-28 maja legislatura stanu Illinois przyjęła SB 315, określaną jako Artificial Intelligence Safety Measures Act. Według relacji Ars Technica i opracowań branżowych projekt ma wymagać od największych developerów frontier AI publicznych planów bezpieczeństwa, corocznych niezależnych audytów, raportowania incydentów oraz kanałów ochrony sygnalistów. Gubernator J.B. Pritzker zapowiedział podpisanie ustawy.

Znaczenie: jeżeli ustawa wejdzie w życie w opisanym kształcie, Illinois stanie się kolejnym stanem USA próbującym stworzyć standard transparentności i audytu dla największych modeli, obok wcześniejszych działań Kalifornii i Nowego Jorku. Dla firm AI oznacza to narastającą presję na formalne frameworki bezpieczeństwa i dokumentowanie ryzyk.

Źródła:

- Ars Technica, relacja o SB 315: <https://arstechnica.com/tech-policy/2026/05/trump-loses-more-control-over-ai-regulation-as-illinois-passes-landmark-law/>
- OpenAI, „OpenAI's Frontier Governance Framework”, 28.05.2026: <https://openai.com/index/openai-frontier-governance-framework/>

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

### 2.1. Floryda: jednolita zasada weryfikacji cytowań w pismach sądowych zamiast lokalnych nakazów ujawniania AI

28 maja Sąd Najwyższy Florydy zmienił Florida Rule of General Practice and Judicial Administration 2.515(d)(2). Od 15 czerwca 2026 r. podpisujący pismo do sądu będzie reprezentował, że „the legal authorities identified exist and are accurately cited”. Sąd wyraźnie wskazał, że generatywna AI może tworzyć wiarygodnie brzmiące, ale fałszywe orzeczenia, cytaty lub analizy. Reguła upoważnia też sądy do sankcji za pisma sprzeczne z tą reprezentacją, po zawiadomieniu i możliwości wysłuchania.

Równocześnie Administrative Order AOSC26-12 usuwa mozaikę lokalnych wymogów certyfikacji/ujawniania AI w poszczególnych circuit courts. Sąd uznał, że jednolity standard stanowy lepiej równoważy potrzeby systemu sądowego i użytkowników zewnętrznych. Co ważne, Floryda nie wprowadza generalnego obowiązku ujawnienia każdego użycia AI; skupia się na odpowiedzialności za realność i dokładność cytowanych autorytetów prawnych.

Znaczenie praktyczne: to model regulacyjny „verify, not disclose everything”. Może być atrakcyjny dla sądów, które chcą ograniczyć halucynowane cytowania bez tworzenia trudnych do egzekwowania pytań o każdy etap użycia AI przy researchu lub redakcji.

Źródła:

- Supreme Court of Florida, Opinion SC2026-0673, 28.05.2026: <https://flcourts-media.flcourts.gov/content/download/2489374/opinion/Opinion_SC2026-0673.pdf>
- Supreme Court of Florida, Administrative Order AOSC26-12: <https://flcourts-media.flcourts.gov/content/download/2489379/29182858>
- The Florida Bar, omówienie zmian: <https://www.floridabar.org/the-florida-bar-news/supreme-court-amends-rules-to-address-ai-use-in-court-filings/>

### 2.2. USA federalnie: projekt Research and Oversight of AI in Courts Act koncentruje się na transkrypcji i oficjalnym rekordzie sądowym

W Kongresie USA pozostaje procedowany Research and Oversight of AI in Courts Act of 2026 (H.R. 7997 i S. 4154), a 1 czerwca National Court Reporters Association informowała o kolejnym współsponsorze z House Judiciary Committee. Projekt ustawy zakłada powołanie 15-osobowej grupy zadaniowej do oceny prawnych i etycznych skutków używania AI speech-to-text i automatycznego rozpoznawania mowy w systemie sądownictwa USA.

Zakres oceny ma obejmować m.in. dokładność, prywatność, cyberbezpieczeństwo, swobody obywatelskie oraz prawo stron do precyzyjnego oficjalnego protokołu. To ważne, bo w sądach AI nie musi od razu „wydawać wyroków”, aby wpływać na prawa stron; wystarczy, że błędnie utrwali zeznania, argumenty lub przebieg rozprawy.

Źródła:

- GovTrack, H.R. 7997: <https://www.govtrack.us/congress/bills/119/hr7997>
- GovTrack, S. 4154: <https://www.govtrack.us/congress/bills/119/s4154>
- Senator Peter Welch, komunikat o projekcie ustawy: <https://www.welch.senate.gov/wicker-welch-hageman-introduce-bipartisan-bill-to-examine-use-of-ai-speech-to-text-technologies-in-federal-courts/>
- Congress.gov, tekst S. 4154: <https://www.congress.gov/119/bills/s4154/BILLS-119s4154is.pdf>
- The Journal of Court Reporting, informacja o współsponsorze z 1.06.2026: <https://www.thejcr.com/2026/06/01/house-judiciary-committee-member-glenn-grothman-joins-as-co-sponsor-of-ncra-ai-courts-legislation/>

### 2.3. Kalifornia: pilotaż „AI clerk” w sądach Los Angeles i Riverside oraz polityki użycia generatywnej AI przez sądy

CalMatters i LAist opisały pilotaż narzędzia Learned Hand w sądach hrabstw Los Angeles i Riverside. Los Angeles County Superior Court rozpoczął testy w lutym; sześciu sędziów cywilnych i ich research attorneys mają używać narzędzia do researchu, streszczania motions i pomocy przy projektach tentative rulings. Riverside testuje narzędzie głównie przy cywilnych i probate research memos. Learned Hand ma korzystać z modeli Anthropic, OpenAI i Google.

Kontrowersje dotyczą przede wszystkim:

- potencjalnej ekspansji z postępowań cywilnych na sprawy karne lub wrażliwe obszary;
- braku obowiązku ujawnienia stronom, że AI analizowała materiał w konkretnej sprawie, o ile dokument nie jest w całości wygenerowany przez AI;
- braku publicznych wyników testów biasu i dokładności.

Kontekst regulacyjny: California Rules of Court, rule 10.430, obowiązująca od 1 września 2025 r., wymaga, aby sądy, które nie zakazują użycia generatywnej AI przez personel lub judicial officers, przyjęły pisemną politykę użycia AI do 15 grudnia 2025 r. Standard 10.80 zaleca sędziom m.in. weryfikację dokładności materiału AI, korektę halucynacji i rozważenie ujawnienia użycia AI przy treściach udostępnianych publicznie.

Znaczenie praktyczne: Kalifornia pokazuje dwie ścieżki jednocześnie - realne pilotaże narzędzi wspomagających orzekanie oraz formalizację polityk użycia AI przez sądy. To jeden z najbardziej konkretnych przykładów „AI as clerk”, a nie „AI as judge”.

Źródła:

- CalMatters, „How Southern California judges are testing an AI clerk”: <https://calmatters.org/economy/technology/2026/05/ai-los-angeles-riverside-courts/>
- LAist, wersja lokalna relacji: <https://laist.com/news/criminal-justice/california-judges-testing-ai-clerk>
- Judicial Branch of California, Rule 10.430: <https://courts.ca.gov/cms/rules/index/ten/rule10_430>
- Judicial Branch of California, Standard 10.80: <https://courts.ca.gov/cms/rules/index/standards/Standard10_80>

### 2.4. Chiny: Najwyższy Sąd Ludowy zapowiada doprecyzowanie reguł dla treści generowanych przez AI i praw do danych

28 maja oficjalny portal chińskich sądów podał, że sądy w Chinach będą w latach 2026-2030 doprecyzowywać reguły orzecznicze dotyczące AI i praw do danych. Liu Guixiang z Najwyższego Sądu Ludowego wskazał, że prace obejmą m.in. prawa do danych, transakcje danymi oraz treści generowane przez AI. Cel: wsparcie gospodarki cyfrowej i lepsze standardy rozstrzygania sporów w nowych sektorach.

Kontekst sądowego użycia AI w Chinach jest szerszy. South China Morning Post opisywał w maju system w Shenzhen, zbudowany od 2024 r. jako domenowy LLM dla sądownictwa, obejmujący 85 procedur w sprawach cywilnych, administracyjnych i karnych, w tym filing, hearings i przygotowanie dokumentów. Według sądu w Shenzhen liczba spraw obsługiwanych przez sędziego wzrosła o ok. 50% rok do roku.

Znaczenie praktyczne: Chiny łączą intensywne wdrażanie AI w workflow sądowym z budowaniem reguł dla sporów o dane i AI-generated content. W przeciwieństwie do ostrożniejszych modeli amerykańskich, chińskie sądy szybciej eksperymentują z systemami obejmującymi wiele etapów procesu, ale oficjalna narracja nadal mówi o wsparciu sędziów, nie zastąpieniu decyzji człowieka.

Źródła:

- Supreme People's Court of China / China Court, „China to refine AI-related legal framework”, 28.05.2026: <https://english.court.gov.cn/2026-05/28/c_1187213.htm>
- Science and Technology Daily, tekst chiński o regułach dla AI-generated content: <https://www.stdaily.com/web/gdxw/2026-05/27/content_523448.html>
- South China Morning Post, Shenzhen AI court assistant: <https://www.scmp.com/news/china/politics/article/3352161/ai-helped-shenzhen-judges-handle-cases-50-faster-future-china>

### 2.5. Indie: Sąd Najwyższy reaguje na fałszywe, AI-generowane orzeczenia i prosi Bar Council of India o panel ekspertów

W maju Sąd Najwyższy Indii zajął się sprawą, w której sąd niższej instancji miał powołać się na nieistniejące, AI-generowane orzeczenia. Według relacji Indian Express, Bar & Bench, LawBeat i Medianama sąd uznał, że decyzja oparta na takich fałszywych „orzeczeniach” nie jest zwykłym błędem decyzyjnym, lecz może stanowić misconduct z konsekwencjami prawnymi. Sąd poprosił Bar Council of India o powołanie komitetu ekspertów do zbadania ryzyk AI w postępowaniach.

Równolegle Indie rozwijają legal tech w sądach: The Hindu opisał uruchomienie przez Sąd Najwyższy inicjatywy **One Case One Data** oraz chatbota **Su Sahay**, który ma ułatwiać dostęp do informacji i usług sądowych dla stron.

Znaczenie praktyczne: Indie pokazują napięcie między dwiema ścieżkami: z jednej strony AI jako infrastruktura dostępu do sądu i zarządzania sprawami, z drugiej - konieczność odpowiedzialności za halucynowane precedensy. Sąd Najwyższy podkreśla, że nie chodzi o zakaz AI, lecz o regulację ryzyk i odpowiedzialność.

Źródła:

- Indian Express, „Fake judgments, AI hallucinations...”: <https://indianexpress.com/article/legal-news/supreme-court-bci-expert-committee-ai-fake-judgments-10675231/>
- Bar & Bench, relacja o panelu BCI: <https://www.barandbench.com/news/litigation/after-trial-judge-cites-ai-generated-judgment-supreme-court-asks-bci-to-set-up-expert-panel-to-examine-issue>
- Medianama, kontekst sprawy i ryzyk: <https://www.medianama.com/2026/05/223-supreme-court-seeks-ai-panel-over-fake-judgments/>
- The Hindu, „One Case One Data” i chatbot Su Sahay: <https://www.thehindu.com/news/national/cji-surya-kant-announces-one-case-one-data-initiative-launches-ai-chatbot-su-sahay/article70964750.ece>

### 2.6. Rumunia: Just.AI jako krajowe forum i memorandum dla AI w sądownictwie

5 maja w Rumunii odbyło się forum **Just.AI - Artificial Intelligence in the Service of the Judicial System**, zakończone memorandum między instytucjami wymiaru sprawiedliwości, środowiskiem akademickim, partnerami technologicznymi i reprezentantami europejskimi. W ostatnim tygodniu temat pozostawał obecny w mediach branżowych jako przykład krajowego frameworku współpracy.

Memorandum zakłada stały mechanizm dialogu, grupy robocze, diagnozę potrzeb sądownictwa, konsultacje z sędziami, prokuratorami, organami śledczymi i personelem pomocniczym, a do października 2026 r. raporty diagnostyczne. W rumuńskich omówieniach podkreślono zasadę: AI ma charakter wyłącznie pomocniczy i nie może naruszać niezależności decyzyjnej sędziego, prokuratora ani organów ścigania.

Znaczenie praktyczne: Rumunia nie zaczyna od pojedynczego narzędzia, lecz od mechanizmu koordynacji i standardów. To podejście jest zgodne z europejskim naciskiem na human oversight, niezależność sądownictwa i proporcjonalność.

Źródła:

- Juridice.ro, pełny tekst memorandum Just.AI: <https://www.juridice.ro/828195/inteligenta-artificiala-in-serviciul-sistemului-judiciar-memorandum-institutional-initiat-de-presedintele-romaniei-text-integral.html>
- Romania Insider, relacja o krajowych ramach współpracy: <https://www.romania-insider.com/romania-ai-justice-may-2026>
- UNBR, komentarz o charakterze pomocniczym AI: <https://unbr.ro/dialog-unbr-raspunsul-18-memorandumul-interinstitutional-just-ai-forum-inteligenta-artificiala-in-serviciul-sistemului-judiciar-intrebare-adresata-de-av-adrian-rusu-ba/>

### 2.7. Unia Europejska: AI Act klasyfikuje wiele narzędzi sądowych jako high-risk

W europejskim tle najważniejsze pozostaje Annex III, pkt 8(a) AI Act: systemy AI używane przez organ sądowy lub w jego imieniu do pomocy w badaniu i interpretacji faktów i prawa oraz stosowaniu prawa do konkretnego stanu faktycznego należą do kategorii high-risk. W praktyce obejmuje to narzędzia do researchu prawnego, analizy stanu faktycznego i wspomagania decyzji, jeżeli są używane przez sądy lub na ich rzecz.

Znaczenie praktyczne: europejskie sądy i dostawcy narzędzi legal AI muszą myśleć nie tylko o dokładności, ale też o zarządzaniu ryzykiem, jakości danych, dokumentacji technicznej, nadzorze człowieka i ochronie praw podstawowych. Projekty takie jak JUDGEASSIST mają pomóc stworzyć ramy ewaluacji AI wspierającej decyzje sądowe.

Źródła:

- EU Artificial Intelligence Act, Annex III: <https://artificialintelligenceact.eu/annex/3/>
- Komisja Europejska / CORDIS, projekt JUDGEASSIST: <https://cordis.europa.eu/project/id/101230213>
- Council of Europe CEPEJ, European Ethical Charter on the use of AI in judicial systems: <https://www.coe.int/en/web/cepej/cepej-european-ethical-charter-on-the-use-of-artificial-intelligence-ai-in-judicial-systems-and-their-environment>

## Najważniejsze wnioski tygodnia

1. **Agentowość staje się główną osią rywalizacji modeli.** Claude Opus 4.8, Codex Sites/plugins, MAI-Code-1-Flash i MiniMax M3 pokazują, że „model” jest coraz częściej częścią systemu wykonującego zadania, a nie tylko generującego tekst.
2. **Enterprise governance jest równie ważne jak benchmarki.** AWS Bedrock dla OpenAI, Microsoft Foundry, kontrola uprawnień w Codex i Frontier Tuning wskazują, że duzi klienci kupują model razem z audytem, bezpieczeństwem, danymi i integracją.
3. **Cyberbezpieczeństwo jest najbardziej napiętym polem frontier AI.** Project Glasswing pokazuje, że modele zdolne do znajdowania podatności są jednocześnie przełomem obronnym i ryzykiem ofensywnym.
4. **Sądy nie zakazują AI, ale przesuwają odpowiedzialność na weryfikację i nadzór człowieka.** Floryda wymaga prawdziwych cytowań, Indie badają misconduct przy fałszywych orzeczeniach, Kalifornia formalizuje polityki użycia AI, a UE klasyfikuje sądowe narzędzia AI jako high-risk.
5. **Wymiar sprawiedliwości testuje AI głównie jako narzędzie pomocnicze.** Najczęstsze zastosowania to research, streszczanie pism, drafty orzeczeń, transkrypcja, zarządzanie sprawami i dostęp do informacji dla stron. Decyzja człowieka pozostaje centralnym wymogiem w deklarowanych frameworkach USA, UE, Indii i Rumunii.
