# Tygodniowy przeglad AI - 2026-06-01

**Zakres przegladu:** wydarzenia i publikacje z okresu ok. 25 maja - 1 czerwca 2026 r.  
**Uwaga metodologiczna:** w czesci modelowej priorytet maja oficjalne komunikaty producentow i repozytoria modeli. W czesci prawniczej priorytet maja zrodla instytucjonalne oraz relacje dotyczace realnych wdrozen w sadach.

## Najkrotsze podsumowanie

- Tydzien byl mocny w modelach multimodalnych i agentowych: NVIDIA pokazala otwarty model swiata **Cosmos 3** dla physical AI, Anthropic wydal **Claude Opus 4.8**, Microsoft rozwijal linie obrazowa **MAI-Image-2.5** i udostepnil badawczy model obrazu **Lens**, a OpenAI zaktualizowalo **GPT-5.5 Instant**.
- W prawie i wymiarze sprawiedliwosci najwazniejszy temat to nie sama dostepnosc AI, lecz granice jej uzycia: Kalifornia testuje "AI clerk" dla sedziow bez pelnego obowiazku ujawnienia czesciowego uzycia AI, Singapur opisuje model "swiatel drogowych", Czarnogora rozwija system AI do orzecznictwa, a UNDP opublikowal przekrojowy raport dla Azji i Pacyfiku.

---

## 1. Ogolne przelomy i nowe modele AI o istotnym znaczeniu

### 1.1. NVIDIA Cosmos 3: otwarty model foundation dla physical AI

NVIDIA oglosila **Cosmos 3**, otwarty model foundation dla tzw. physical AI, czyli systemow uczacych roboty, pojazdy autonomiczne i agentow wizyjnych rozumienia oraz symulowania swiata fizycznego. Wedlug komunikatu model laczy w jednej architekturze rozumowanie wizyjne, generowanie swiata oraz predykcje akcji. NVIDIA opisuje go jako "fully open omnimodel" zdolny do pracy na tekscie, obrazach, wideo, dzwieku otoczenia i trajektoriach dzialan.

Znaczenie:

- **Przejscie od osobnych modeli do jednego modelu swiata.** Wczesniejsze stosy dla physical AI zwykle laczyly osobne moduly: rozumienie sceny, predykcje przyszlych stanow, generowanie syntetycznych danych i modelowanie akcji. Cosmos 3 ma te funkcje integrowac w jednej rodzinie modeli.
- **Otwartosc i wdrozenia przemyslowe.** Modele Cosmos 3 Super i Cosmos 3 Nano sa dostepne, a Cosmos 3 Edge ma byc przeznaczony do inferencji czasu rzeczywistego na brzegu sieci. NVIDIA podaje tez partnerow z robotyki, pojazdow autonomicznych i vision AI.
- **Architektura mixture-of-transformers.** Producent opisuje polaczenie transformera rozumujacego z eksperckim transformerem generujacym, co ma pomagac w modelowaniu interakcji obiektow, ruchu i relacji czasoprzestrzennych.

Zrodla:

- NVIDIA Newsroom, "NVIDIA Launches Cosmos 3, the Open Frontier Foundation Model for Physical AI", 31 maja 2026: <https://nvidianews.nvidia.com/news/nvidia-launches-cosmos-3-the-open-frontier-foundation-model-for-physical-ai>
- NVIDIA Investor Relations, komunikat z 1 czerwca 2026: <https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Launches-Cosmos-3-the-Open-Frontier-Foundation-Model-for-Physical-AI/default.aspx>
- NVIDIA Technical Blog, opis techniczny Cosmos 3: <https://developer.nvidia.com/blog/develop-physical-ai-reasoning-world-and-action-models-with-nvidia-cosmos-3/>

### 1.2. Anthropic Claude Opus 4.8: mocniejszy model agentowy i kontrola "effort"

Anthropic wydal **Claude Opus 4.8** jako nastepce Opus 4.7. Firma pozycjonuje aktualizacje jako poprawe w pracy agentowej, kodowaniu, dlugich zadaniach profesjonalnych i uzyciu narzedzi. Model jest dostepny w Claude API jako `claude-opus-4-8`; standardowe ceny pozostaly bez zmian wzgledem Opus 4.7.

Najwazniejsze elementy:

- **Dynamic workflows w Claude Code.** Anthropic opisuje nowa funkcje pozwalajaca planowac i uruchamiac wiele rownoleglych subagentow w jednej sesji, np. do migracji kodu na skale calego repozytorium.
- **Kontrola wysilku modelu.** Uzytkownicy moga dobierac poziom "effort", czyli to, ile rozumowania model ma poswiecic na zadanie. Nizszy poziom ma dawac szybsze odpowiedzi, wyzszy - lepsze wyniki w trudniejszych zadaniach.
- **Mniej nieuzasadnionej pewnosci.** Anthropic podkresla, ze Opus 4.8 czesciej sygnalizuje niepewnosc i rzadziej przepuszcza wlasne bledy bez komentarza.
- **Znaczenie dla sektora profesjonalnego.** W komunikacie pojawiaja sie przyklady z kodowania, analizy dokumentow finansowych i zastosowan legal-tech, co pokazuje, ze konkurencja przenosi sie z samych benchmarkow na niezawodnosc dlugich workflow.

Zrodla:

- Anthropic, "Introducing Claude Opus 4.8", 28 maja 2026: <https://www.anthropic.com/news/claude-opus-4-8>
- LLM Stats, podsumowanie parametrow i dostepnosci Opus 4.8: <https://llm-stats.com/blog/research/claude-opus-4-8-launch>

### 1.3. Microsoft MAI-Image-2.5: model obrazowy wysoko w Arena

Microsoft AI oglosil **MAI-Image-2.5**, ktory wedlug firmy zajal 3. miejsce na leaderboardzie Arena dla modeli text-to-image. Model ma poprawiac szczegolnie renderowanie tekstu, spojnosc scen, obrazy produktowe, prace brandowe oraz rozumienie wizualne relacji przestrzennych.

Dlaczego to istotne:

- **Renderowanie tekstu pozostaje krytycznym problemem modeli obrazowych.** Microsoft akcentuje ostrzejsze napisy, lepsze uklady i wieksza uzytecznosc w materialach komercyjnych.
- **Wzrost znaczenia wlasnych modeli Microsoftu.** MAI-Image-2.5 jest kolejnym krokiem w linii MAI-Image, a Microsoft zapowiada dostepnosc w MAI Playground i Foundry.
- **Konkurencja w obrazach przesuwa sie ku zastosowaniom profesjonalnym.** W komunikacie wyraznie widac nacisk na opakowania, plakaty, layouty i fotografie produktowe, a nie tylko na efektowne generacje demonstracyjne.

Zrodlo:

- Microsoft AI, "MAI-Image-2.5 launches at No. 3 on Arena", 26 maja 2026: <https://microsoft.ai/news/mai-image-2-5-launches-at-no-3-on-arena-ai/>

### 1.4. Microsoft Lens: 3,8B-parametrowy model text-to-image nastawiony na efektywne trenowanie

Microsoft udostepnil w Hugging Face model **Lens**, opisany jako 3,8B-parametrowy foundation model text-to-image. Model korzysta z danych Lens-800M, gestych podpisow generowanych przez GPT-4.1, mieszanych rozdzielczosci i architektury MMDiT. Repozytorium zawiera tez warianty Lens-Turbo i Lens-Base.

Najwazniejsze informacje:

- **Skala i efektywnosc.** Lens ma konkurowac jakoscia z wiekszymi modelami obrazowymi przy mniejszym koszcie treningu.
- **Rozdzielczosc i formaty.** Model wspiera generowanie do 1440 x 1440 oraz proporcje od 1:2 do 2:1.
- **Wariant Turbo.** Lens-Turbo sluzy do szybkiego, 4-krokowego generowania.
- **Charakter badawczy.** Karta modelu wskazuje, ze model powinien byc uzywany w kontrolowanych warunkach badawczych z dodatkowymi zabezpieczeniami po stronie uzytkownika.

Zrodla:

- Hugging Face, `microsoft/Lens`: <https://huggingface.co/microsoft/Lens>
- GitHub, repozytorium Microsoft Lens: <https://github.com/microsoft/Lens/blob/main/README.md>
- TPS Report, informacja o wydaniu Lens, 26 maja 2026: <https://tpsreport.news/news/microsoft-lens-3-8b-text-to-image-model>

### 1.5. OpenAI GPT-5.5 Instant: aktualizacja modelu produkcyjnego i wygaszanie starszych modeli w ChatGPT

OpenAI opublikowalo aktualizacje **GPT-5.5 Instant** w ChatGPT i API. Zmiana dotyczy stylu i jakosci odpowiedzi: model ma odpowiadac bardziej naturalnie, czytelniej, lepiej dawkowac dlugosc odpowiedzi i rzadziej produkowac nadmiernie rozbudowane listy punktowane. Jednoczesnie OpenAI zapowiedzialo wycofanie z ChatGPT modeli OpenAI o3 i GPT-4.5 po okresach sunset.

Znaczenie:

- **Nie jest to nowy frontier model, ale wazna aktualizacja domyslnego doswiadczenia.** Tego typu zmiany oddzialuja na bardzo duza liczbe uzytkownikow i czesto maja wiekszy praktyczny wplyw niz niszowe premiery badawcze.
- **Konsolidacja portfolio.** Wycofywanie starszych modeli pokazuje kierunek: mniej modeli legacy w interfejsie, wiekszy nacisk na biezace rodziny GPT-5.x.
- **Zmiana funkcji canvas.** OpenAI wskazuje, ze canvas nie bedzie juz dostepny w GPT-5.5 Instant ani GPT-5.5 Thinking, a pisanie i kodowanie maja byc wspierane bezposrednio w odpowiedziach czatu.

Zrodlo:

- OpenAI Help Center, "Model Release Notes", wpis z 28 maja 2026: <https://help.openai.com/en/articles/9624314-model-release-notes>

### 1.6. Mistral Vibe: agent do pracy i kodu jako sygnal dojrzewania warstwy produktowej

Mistral oglosil, ze **Le Chat staje sie Vibe**, czyli jednym agentem obejmujacym prace biurowa i kodowanie. To nie jest sama premiera modelu foundation, ale wazny sygnal rynkowy: dostawcy modeli coraz mocniej przenosza rywalizacje do agentow wykonujacych wieloetapowe zadania.

Najwazniejsze elementy:

- **Work Mode.** Agent moze laczyc sie z narzedziami firmowymi, przeszukiwac wiedze organizacji, analizowac dane, tworzyc dokumenty i uruchamiac cykliczne zadania.
- **Code Mode.** Vibe ma uruchamiac zdalne sesje kodowania, pracowac w web app, terminalu i przez rozszerzenie VS Code, a finalnie doprowadzac zmiany do pull requestow.
- **Przejrzystosc narzedzi.** Mistral podkresla widocznosc krokow, tool calli i wynikow posrednich, co jest kluczowe dla adopcji agentow w organizacjach.

Zrodla:

- Mistral AI, "Vibe gets to work", 28 maja 2026: <https://mistral.ai/news/vibe-agent/>
- Mistral AI, "Remote agents in Vibe. Powered by Mistral Medium 3.5", 22 maja 2026 - kontekst modelowy dla Vibe: <https://mistral.ai/news/vibe-remote-agents-mistral-medium-3-5/>

### 1.7. MONET od Jasper Research: duzy otwarty zbior danych dla text-to-image

Jasper Research opublikowal **MONET**, otwarty zbior obraz-tekst zbudowany z 2,9 mld obrazow i przefiltrowany do 104,9 mln probek wysokiej jakosci. Razem z nim wydano `nano-t2i`, minimalny kod do trenowania modeli text-to-image.

Dlaczego to wazne:

- **Dane jako przewaga modelowa.** W obrazach jakosc danych i podpisow jest jednym z glownych ograniczen otwartych projektow. MONET ma zmniejszyc luke miedzy zamknietymi modelami komercyjnymi a badaniami akademickimi.
- **Reprodukowalnosc.** Autorzy prezentuja pipeline filtrowania, deduplikacji, bezpieczenstwa i captioningu, a takze walidacje na modelu ok. 4B parametrow.
- **Licencja i dostepnosc.** Wedlug wpisu zbior jest przeznaczony do uzytku komercyjnego na licencji Apache 2.0.

Zrodlo:

- Hugging Face Blog, "MONET: Lowering the bar for World-Class Image Generation research", 28 maja 2026: <https://huggingface.co/blog/jasperai/monet>

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwosci

### 2.1. USA, Kalifornia: sedziowie testuja "AI clerk" Learned Hand

CalMatters opisal pilotaz narzedzia **Learned Hand** w sadach hrabstw Los Angeles i Riverside. Narzedzie korzysta z modeli jezykowych Anthropic, OpenAI i Google, a jego zadaniem jest wspieranie sedziow i prawnikow sadowych w researchu, streszczaniu wnioskow oraz przygotowywaniu projektow rozstrzygniec lub notatek badawczych.

Najwazniejsze ustalenia:

- **Los Angeles County Superior Court** ma kontrakt wart ok. 314 tys. USD; szescioro sedziow i ich research attorneys uzywa narzedzia glownie w sprawach cywilnych.
- **Riverside County Superior Court** ma mniejsza umowe testowa, ok. 10 tys. USD; wedlug relacji narzedzie jest uzywane glownie przez prawnikow cywilnych i probate do notatek badawczych, nie do projektow tentative rulings.
- **Mozliwe obszary wysokiego ryzyka.** Dokumenty kontraktowe dopuszczaja testy w sprawach karnych, rodzinnych i probate, choc przedstawiciele sadu wskazuja, ze narzedzie nie wyszlo poza kontrolowany zakres i nie ma obecnie planow uzycia w petycjach na podstawie California Racial Justice Act.
- **Problem jawnosci.** Zasady Kalifornii wymagaja ujawnienia uzycia generatywnej AI, gdy finalna publiczna praca sklada sie w calosci z outputu AI. Czesciowa pomoc AI, taka jak research czy szkic, moze nie wywolac obowiazku ujawnienia. To jest centralny spor: strony moga nie wiedziec, czy AI uczestniczyla w przygotowaniu materialu w ich sprawie.

Znaczenie dla wymiaru sprawiedliwosci:

- To jeden z najkonkretniejszych przykladow przejscia AI z kancelarii do samego zaplecza decyzyjnego sadow.
- Sprawa pokazuje roznice miedzy deklaracja "czlowiek decyduje" a praktycznym ryzykiem zakotwiczenia sie sedziego w projekcie lub streszczeniu wygenerowanym przez system.
- Najwieksze ryzyka dotycza spraw karnych, gdzie blad moze oznaczac naruszenie wolnosci osobistej lub praw konstytucyjnych.

Zrodla:

- CalMatters, "How Southern California judges are testing an AI clerk", maj 2026: <https://calmatters.org/economy/technology/2026/05/ai-los-angeles-riverside-courts/>
- California Rules of Court, Rule 10.430 i Standard 10.80, zasady uzycia generatywnej AI w sadach Kalifornii: <https://courts.ca.gov/system/files/rules-court/2025-07-18-rules-effective-09-01-2025.pdf>
- TechTimes, omowienie watku braku obowiazku ujawnienia czesciowego uzycia AI, 28 maja 2026: <https://www.techtimes.com/articles/317333/20260528/ai-california-courts-drafts-orders-secret-litigants-get-no-disclosure.htm>

### 2.2. USA, Florida i sady federalne: coraz ostrzejsza odpowiedzialnosc za halucynacje w pismach

Rownolegle do uzycia AI przez sady narasta presja na prawnikow skladajacych pisma z blednymi cytowaniami. Law360 odnotowal w ostatnich dniach m.in. sprawe z Florydy, w ktorej sad apelacyjny nakazal prawnikowi wyjasnic potencjalne AI-generowane cytowania, oraz informacje o przyjeciu przez Florida Supreme Court polityki wymagajacej sprawdzania dokladnosci tresci wygenerowanych przez AI w dokumentach sadowych.

Znaczenie:

- **Standard odpowiedzialnosci przesuwa sie na czlowieka.** Nawet gdy AI jest tylko narzedziem, prawnik pozostaje odpowiedzialny za istnienie i trafnosc cytowanych precedensow.
- **Fragmentacja regulacji.** Poszczegolne sady i stany przyjmuja wlasne zasady, zanim pojawi sie jednolity standard federalny.
- **Praktyczny skutek.** Kancelarie musza wdrazac procedury weryfikacji cytowan, logowania uzycia AI i kontroli jakosci pism.

Zrodlo:

- Law360, wyniki wyszukiwania i streszczenia spraw z maja 2026 dotyczacych sankcji za AI-citations: <https://www.law360.com/articles/2481934/fla-panel-orders-atty-to-explain-ai-citations-in-roofing-case> oraz <https://www.law360.com/articles/2483079/florida-high-court-adopts-ai-policy-for-lawyers>

### 2.3. Singapur: "traffic light model" dla AI w sadach

Chief Justice Sundaresh Menon opisal podejscie singapurskiego sadownictwa do AI jako model **czerwony-zolty-zielony**.

Najwazniejsze elementy:

- **Czerwone pole:** decyzje sadowe i predykcje wynikow spraw nie sa obszarem do delegowania AI. Menon podkresla, ze nawet trafna predykcja moze naruszac integralnosc sadzenia, bo sadzenie wymaga ludzkiego wazenia dowodow, emocji, okolicznosci i normatywnej oceny.
- **Zolte pole:** ostroznie oceniane sa narzedzia pomagajace osobom bez prawnika lepiej porzadkowac argumenty oraz potencjalne streszczanie bardzo obszernych materialow dla sedziow.
- **Zielone pole:** tlumaczenia, streszczenia w prostszych postepowaniach i narzedzia wspierajace w Small Claims Tribunals oraz research prawny przez LawNet.
- **Odpowiedzialnosc zamiast nadmiernie szczegolowych zakazow.** Singapur wskazuje, ze AI bedzie wbudowana w powszechne narzedzia biurowe, wiec kluczowa jest zasada: prawnik lub strona odpowiada za wszystko, co sklada do sadu.

Znaczenie:

- Singapur pokazuje jeden z bardziej przejrzystych modeli zarzadzania ryzykiem: nie "AI albo brak AI", lecz klasyfikacja zadan wedlug dopuszczalnosci i ryzyka.
- Model dobrze rozroznia automatyzacje administracyjna od delegowania funkcji sedziowskiej.

Zrodla:

- The Straits Times, "Truth decay, echo chambers a challenge for Singapore courts: Chief Justice", 26 maja 2026: <https://www.straitstimes.com/singapore/courts-crime/era-of-truth-decay-rise-of-echo-chambers-a-challenge-for-singapore-courts-chief-justice-menon>
- The Online Citizen, szczegolowe omowienie modelu "traffic light", 26 maja 2026: <https://theonlinecitizen.com/2026/05/26/truth-decay-and-ai-in-courts-chief-justice-menon-on-challenges-facing-singapore-judiciary>

### 2.4. UNDP: raport "The Algorithm in the Courtroom" dla Azji i Pacyfiku

UNDP opublikowal dwutomowa publikacje **The Algorithm in the Courtroom: How Artificial Intelligence Is Reshaping Justice and the Rule of Law Across Asia and the Pacific** oraz operacyjny przewodnik **Responsible AI in Justice**. Raport mapuje uzycie AI w sadach, organach scigania, pomocy prawnej i administracji sprawiedliwosci w regionie Azji i Pacyfiku.

Zakres opisanych zastosowan:

- research prawny i zarzadzanie sprawami,
- transkrypcja i tlumaczenia,
- online dispute resolution,
- chatboty do pomocy prawnej,
- narzedzia wspierajace sady i ministerstwa sprawiedliwosci.

Najwazniejsze ostrzezenia:

- AI moze zwiekszyc dostep do sprawiedliwosci, ale jednoczesnie niesie ryzyka dla prawa do rzetelnego procesu, due process, niezaleznosci sadownictwa i rownosci wobec prawa.
- UNDP rekomenduje podejscie oparte na prawach czlowieka, wspolnych standardach regionalnych i zabezpieczeniach proceduralnych.

Znaczenie:

- To nie jest pojedynczy pilotaz, lecz przeglad systemowy. Raport moze stac sie punktem odniesienia dla panstw, ktore dopiero projektuja swoje zasady AI w wymiarze sprawiedliwosci.
- Dobrze pokazuje, ze AI w sadach to nie tylko generowanie tekstu, lecz caly ekosystem: od obslugi obywatela po analityke spraw i zarzadzanie zaleglosciami.

Zrodlo:

- UNDP Asia-Pacific, "The Algorithm in the Courtroom", 27 maja 2026: <https://www.undp.org/asia-pacific/publications/algorithm-courtroom>

### 2.5. Czarnogora: system AI do elektronicznego orzecznictwa w sadach

Sady Czarnogory, Sad Najwyzszy i Rada Sadownictwa rozwijaja **elektroniczny system orzecznictwa oparty na AI**, ktory ma byc dostepny we wszystkich sadach. System zostal opracowany wewnetrznie przez zespol ICT i multimedialny Sekretariatu Rady Sadownictwa, w ramach projektu wspieranego przez UE.

Najwazniejsze informacje:

- Pilotaz dziala w Sadzie Gospodarczym, a kolejnym etapem ma byc Sad Administracyjny.
- System ma wspierac efektywne wyszukiwanie orzecznictwa, standaryzacje praktyki, lepsze raportowanie i zarzadzanie sprawami.
- Wladze podkreslaja zgodnosc z regulacjami UE dotyczacymi AI i ochrony danych osobowych.
- Wedlug wypowiedzi ambasadora UE w Czarnogorze kolejnym krokiem jest operacyjne wdrozenie we wszystkich sadach do konca nastepnego roku.

Znaczenie:

- Czarnogora jest ciekawym przykladem mniejszego panstwa, ktore buduje AI dla sadownictwa na wlasnej infrastrukturze i w ramach przygotowan do standardow europejskich.
- Wdrozenie dotyczy przede wszystkim ujednolicania orzecznictwa i wyszukiwania, czyli obszaru o nizszym ryzyku niz automatyczne rozstrzyganie spraw.

Zrodla:

- Vijesti, "The first AI system in the Montenegrin judiciary soon in all courts", 28 maja 2026: <https://en.vijesti.me/news-b/society/810619/The-first-AI-system-in-the-Montenegrin-judiciary--soon-in-all-courts>
- Vijesti, "Montenegrin judiciary launches first AI system for case law", 20 marca 2026 - kontekst pilotazu i infrastruktury: <https://en.vijesti.me/news-b/society/801047/Montenegrin-judiciary-launches-first-AI-system-for-case-law>

### 2.6. Unia Europejska i TSUE: AI w sadach jako system wysokiego ryzyka

W kontekscie europejskim wazne jest, ze **AI Act** klasyfikuje systemy AI uzywane przez organy sadowe lub w ich imieniu do badania i interpretacji faktow oraz prawa, a takze stosowania prawa do konkretnego stanu faktycznego, jako systemy wysokiego ryzyka. TSUE informuje rowniez, ze w 2026 r. przyjal **Artificial Intelligence Ethics Charter**, ktora ma ograniczac negatywny wplyw AI na procesy sadowe i administracyjne Trybunalu.

Znaczenie:

- **Europejski standard jest bardziej formalny niz wiele podejsc krajowych.** Narzedzia podobne do "AI clerk" w sadzie moga w UE wchodzic w rezim high-risk, jesli pomagaja organowi sadowemu interpretowac fakty i prawo.
- **Akcent na human-centric AI.** TSUE podkresla zgodnosc z wartosciami UE, ochrona danych i AI Act.
- **Praktyczne konsekwencje dla wdrozen.** Dostawcy i sady musza uwzgledniac zarzadzanie ryzykiem, jakosc danych, nadzor czlowieka, dokumentacje i przejrzystosc.

Zrodla:

- AI Act Service Desk, Annex III, pkt 8(a) "Administration of justice and democratic processes": <https://ai-act-service-desk.ec.europa.eu/en/ai-act/annex-3>
- Court of Justice of the European Union, "Artificial Intelligence": <https://curia.europa.eu/site/jcms/p1_1000081817/en/artificial-intelligence>

### 2.7. Chiny: zaawansowane systemy "Smart Court" jako kontrast regulacyjny

W debacie porownawczej powraca przyklad Chin, gdzie systemy "Smart Court" obejmuja m.in. podobienstwo spraw, rekomendacje orzecznicze, analize dowodow i narzedzia wspierajace sedziow. W literaturze z 2026 r. podkresla sie, ze takie systemy moga poprawiac efektywnosc i spojnosc orzecznictwa, ale jednoczesnie rodza ryzyka dla due process, niezaleznosci sedziowskiej i indywidualnej oceny sprawy.

Znaczenie:

- Chiny sa najbardziej zaawansowanym kontrapunktem dla ostrozniejszych modeli Singapuru, Kalifornii czy UE.
- Kluczowe pytanie nie brzmi, czy sedzia formalnie pozostaje "w petli", ale czy presja organizacyjna, oceny wydajnosci i podpowiedzi systemu nie prowadza do mechanicznego orzekania.

Zrodla:

- ScienceDirect, "Artificial intelligence and adjudication: A new pathway to justice in China?", 2026: <https://www.sciencedirect.com/science/article/abs/pii/S2212473X26000015>
- University of New Hampshire Inquiry Journal, "Judicial Systems in the Age of Artificial Intelligence Implementation: The U.S. and China", kwiecien 2026: <https://www.unh.edu/inquiryjournal/blog/2026/04/judicial-systems-age-artificial-intelligence-implementation-us-china>

---

## Wnioski przekrojowe

1. **Modele staja sie bardziej agentowe i multimodalne.** Najwazniejsze premiery tygodnia nie dotycza tylko "lepszego czatu", ale dlugich workflow, kodowania, rozumienia przestrzeni i fizycznego swiata.
2. **Otwartosc ma kilka znaczen.** NVIDIA Cosmos 3, Microsoft Lens i MONET pokazuja rozne poziomy otwartosci: modele, repozytoria, dane, narzedzia treningowe i licencje. Dla rynku wazne bedzie nie tylko "czy mozna pobrac model", ale czy mozna go bezpiecznie wdrozyc.
3. **W sadach AI wchodzi najpierw przez zaplecze.** Research, streszczenia, notatki, wyszukiwanie orzecznictwa i zarzadzanie sprawami sa mniej widoczne niz automatyczne wyroki, ale moga realnie wplywac na proces decyzyjny.
4. **Najwieksza luka to przejrzystosc.** Kalifornia pokazuje problem czesciowego uzycia AI: jezeli dokument nie jest "w calosci" wygenerowany przez AI, strona moze nie dostac informacji, ze AI uczestniczyla w pracy nad jej sprawa.
5. **Najbardziej dojrzale podejscia rozdzielaja zadania wedlug ryzyka.** Singapurski model "traffic light", europejska klasyfikacja high-risk i rekomendacje UNDP sa probami oddzielenia bezpiecznej automatyzacji od niedopuszczalnego delegowania funkcji sedziowskiej.

