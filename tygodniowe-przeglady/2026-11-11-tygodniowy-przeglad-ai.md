# Tygodniowy przegląd AI — 11 listopada 2026

**Okres objęty podsumowaniem:** 4–11 listopada 2026
**Data publikacji podsumowania:** 11 listopada 2026
**Repozytorium:** AI Observatory

Dokument zbiera najważniejsze wydarzenia ze świata sztucznej inteligencji z ostatniego tygodnia. Część pierwsza obejmuje przełomy technologiczne i nowe modele o istotnym znaczeniu. Część druga koncentruje się na zastosowaniach AI w prawie i wymiarze sprawiedliwości — zwłaszcza w sądach oraz rozwiązaniach w różnych krajach. Przy każdej informacji podano linki źródłowe do weryfikacji.

Poprzedni opublikowany przegląd zamyka okno **28 października – 4 listopada 2026** i powstał rano 4 listopada. Niniejszy dokument go nie powtarza. Nie opisuje od nowa wydania wag Mistral Large 4, ogłoszenia Gemini 4 Carbon z 28 października, ogólnej dostępności narzędzia Computer Use w Gemini API, wpisu OpenAI o projektowaniu sprzętu, sygnału treningowego w `robots.txt` ani raportu Civil Justice Council z 29 października. Nie wraca też do ankiety Sądu Najwyższego Korei z 2 listopada, wywiadów z Ibadanu z 31 października ani do pozycji, które wcześniejsze przeglądy kazały zostawić w spokoju. Zapowiedź wag Kimi K3.1 Pro jest tu tylko domknięta: rano 4 listopada publiczne repozytorium jeszcze nie występowało na liście organizacji `moonshotai`.

Liczby benchmarków podane niżej, o ile nie zaznaczono inaczej, pochodzą od vendora z wpisu premierowego, karty modelu, karty systemowej albo dokumentacji API. Niezależna replikacja w momencie publikacji tego przeglądu na ogół jeszcze nie istnieje. Wyników z różnych laboratoriów nie należy składać w jedną tabelę liderów: konfiguracje, daty pomiaru, wysiłek rozumowania i harnessy się nie pokrywają. Tam, gdzie wpis jednego laboratorium podaje wynik cudzego modelu, jest to pomiar autora wpisu, nie wspólny protokół.

---

## 1. Ogólne przełomy i nowe modele AI o istotnym znaczeniu

Tydzień przynosi trzy frontierowe premiery o różnym zasięgu dostępu oraz publikację wag modelu, który od 23 października działał już jako API. **9 listopada** Anthropic udostępnia Claude Fable 5.2 wszystkim użytkownikom i Claude Mythos 5.2 organizacjom po weryfikacji. **10 listopada** Google otwiera Gemini 4 Carbon dla płacących deweloperów i abonentów Ultra; wariant cybernetyczny zostaje w programie Fairwind. **5 listopada** OpenAI wprowadza GPT-6 Cyber wyłącznie dla zatwierdzonych klientów Daybreak Red. W tym samym oknie na Hugging Face leżą już publiczne, niebramkowane wagi Kimi K3.1 Pro.

### 1.1. Anthropic: Claude Fable 5.2 i Claude Mythos 5.2 (9 listopada 2026)

**9 listopada 2026** Anthropic ogłasza **Claude Fable 5.2** i **Claude Mythos 5.2**. Wpis i dokumentacja modelu podają tę samą datę wydania. Fable i Mythos są tym samym modelem bazowym. Fable ma zabezpieczenia cybernetyczne i biologiczne i jest dostępny ogólnie. Mythos jest przeznaczony dla organizacji, które ubiegają się o dostęp przez programy weryfikacyjne do pożytecznych zastosowań w cyberbezpieczeństwie i badaniach biomedycznych.

Anthropic pisze, że dla większości zadań kodowania i pracy z wiedzą punktem startu pozostaje Claude Opus 5.5, a Fable albo Mythos wchodzą przy najtrudniejszej pracy. Fable 5.2 może też pełnić rolę doradcy, którego wołają mniejsze modele, albo orkiestratora, który zleca im prostsze kroki.

Identyfikator API to `claude-fable-5-2`. Dokumentacja platformy, odczytana przez wyszukanie 11 listopada, podaje okno kontekstu **1 mln** tokenów, maksimum wyjścia **128 tys.** tokenów oraz cenę **8 USD** za 1 mln tokenów wejścia i **40 USD** za 1 mln tokenów wyjścia. Strona produktowa Fable podaje, że jest to obniżka z **10 USD** i **50 USD** przy Fable 5.1, a odczyt cache kosztuje **0,20 USD** za 1 mln tokenów. Wpis premierowy dodaje opcjonalny tryb szybki, do **2,5 raza** szybsze generowanie tokenów, w cenie **16 USD** i **80 USD** za 1 mln tokenów wejścia i wyjścia. Ten sam wpis mówi o wyjściu do **30%** szybszym niż Fable 5.1 i Mythos 5.1 w zwykłym trybie. Dokumentacja podaje, że wycofanie modelu nie nastąpi wcześniej niż **9 listopada 2027**.

Dostępność z wpisu: Claude Platform, Amazon Web Services, Google Cloud i Microsoft Azure. Tryb szybki: Claude Code, Claude Platform, modele Claude w Google Cloud w obu wariantach zarządzania oraz Microsoft Foundry w hostingu Anthropic. Szybki tryb Mythosa jest tylko dla organizacji w programach weryfikacyjnych. W tygodniu premiery płatne plany z modelami Fable dostają od jednego do trzech resetów limitu, zależnie od stażu subskrypcji, a Fable wchodzi do **50%** tygodniowego limitu planów Pro i standardowych miejsc w planie Team.

Tabela poniżej jest tabelą Anthropic. Wyniki innych laboratoriów są pomiarami Anthropic, nie ich własnymi komunikatami. Przypis wpisu mówi, że na CyScenarioBench każde laboratorium liczy własne, różne zadania, więc liczby w tym wierszu nie są wspólnym rankingiem. O ile nie zaznaczono inaczej, jest to najwyższy dostępny poziom wysiłku, a wyniki Fable, Fable 5.1 i Opus 5.5 są z włączonymi zabezpieczeniami.

| Zadanie | Fable 5.2 | Fable 5.1 | Opus 5.5 | GPT-6 Astra | Gemini 4 Carbon |
| --- | --- | --- | --- | --- | --- |
| FrontierCode 2.0 | 49,1% (Xhigh) | 32,4% (Xhigh) | 45,5% | 42,8% | 41,1% (Medium) |
| FrontierSWE v2 | 69,9% | 56,3% | 62,3% | 65,5% | 61,2% |
| AutomationBench | 51,4% | 31,4% | 42,5% | 41,4% | 53,9% |
| Terminal-Bench-Science 0.1 | 74,6%; Mythos 5.2: 75,3% | 52,6% | 58,7% | 68,1% | 64,8% |
| CyScenarioBench | Mythos 5.2: 76,3% | Mythos 5.1: 61,7% | 67,6% bez zabezpieczeń | 61% (GPT-6 Cyber) | — |
| OSWorld 2.1, zbiór offline, częściowo | 89,3% | 83,5% | 87,2% | 79,5% | 81,5% |
| RoboDojo Sim, bieg wewnętrzny | 64,9% | 27,6% | 39,4% | 29,8% | — |
| AA-Briefcase v1.1 | 66,1% rubryka; 1785 Elo | 61,5%; 1669 Elo | 61,2%; 1800 Elo | 52,0%; 1569 Elo | 61,8%; 1611 Elo |
| Remote Labor Index | 41,3% (High) | 17,9% | 21,3% | 20,8% | — |
| Humanity’s Last Exam, z narzędziami | 74,2% | 65,6% | 67,7% | 57,2% | — |
| Chartography, bez narzędzi | 73,4% | 44,8% | 64,4% | 71,0% | 72,5% |

Osobne rozbicia kosztu z tego samego wpisu, też po stronie Anthropic. Na FrontierCode 2.0 przy High Fable 5.2 ma około **45,3%**, blisko najlepszego wyniku Opus 5.5 (**45,5%**), za około połowę kosztu zadania, i wyprzedza najlepszy wynik GPT-6 Astra (**42,8%**) przy zbliżonym koszcie. Xhigh daje **49,1%**, najwyższy wynik wydanego modelu w tym teście Anthropic. BenchCAD 2.1, skala 0–100 z częściowym zaliczeniem: Fable 5.2 przy Max **83,5**, Opus 5.5 **65,3**, Fable 5.1 **44,4**. Na WANDR w skali złagodzonej Medium Fable 5.2 zrównuje się ze szczytem Opus 5.5 za około **40%** kosztu zadania. Na HLE z narzędziami Low zrównuje się ze szczytem Opus 5.5 za mniej niż jedną dziesiątą kosztu. Na Chartography Medium ma **66,4%**, powyżej Opus 5.5 przy Max (**64,4%**), również za mniej niż jedną dziesiątą kosztu.

Wpis opisuje też zastosowania, których ten przegląd nie weryfikował poza tekstem Anthropic. Zespół agentów na wcześniejszej wersji Fable 5.2 przepisał produkcyjną usługę z Pythona na Rust; usługa startuje około **26 razy** szybciej. W eksperymencie jeden inżynier zlecił zaprojektowanie prototypowego systemu operacyjnego: ponad **1000** subagentów przez osiem dni, od pustego folderu, z wynikiem, który według wpisu bootuje na laptopie. Przy Diode model z jednoakapitowego polecenia zaprojektował trzy urządzenia elektroniczne — hub głosowy, głośnik USB i podręczne wirtualne zwierzę — z czterowarstwowymi płytkami, obudowami i oprogramowaniem. Płytki były gotowe do produkcji w mniej niż dobę, a po złożeniu wszystkie trzy działały bez zmian elektrycznych. Na fizycznych robotach wpis pokazuje między innymi kostkę, odkręcenie nakrętki i rysunek; liczby RoboDojo w tabeli dotyczą symulacji i biegu wewnętrznego Anthropic.

W naukach ścisłych Anthropic pisze, że Fable 5.2 rozwiązał dwa otwarte problemy fizyki czarnych dziur w ramach dualności holograficznej i odsyła do preprintów. Tych preprintów ten przegląd osobno nie czytał. W formalizacji dowodu wielkiego twierdzenia Fermata w Lean zespół około **1000** agentów Fable 5.2 miał skończyć pracę w **30 godzin**, przy minimalnej interwencji człowieka i bez literatury matematycznej poza listą twierdzeń pośrednich do oceny postępu. Wcześniejsza, niewydana wersja badawcza potrzebowała **11 dni** i harnessu zbudowanego pod to zadanie oraz prowadzenia przez człowieka. Opus 5.5 w tym samym układzie tysiąca agentów, w jednym biegu, po 18 godzinach miał **26%** formalizacji i do 30. godziny prawie nie ruszył dalej. Mythos 5.2, według wpisu, złożył przewidywania struktury całych kapsydów wirusów AAV z dwóch otwartych modeli zwijania białek: **28 z 34** kapsydów uznano za trafione, przy progu **3 Å** Cα RMSD względem struktury doświadczalnej. Próg i czas inferencji na jednym układzie NVIDIA H200 są w przypisie wpisu.

Bezpieczeństwo, nadal ze wpisu i ze skierowania do karty systemowej. Anthropic ocenia ryzyko niebezpiecznego zachowania w sytuacjach o wysokiej stawce jako niskie. Fable 5.2 blokuje klasyfikatorami wysokiego ryzyka działania cybernetyczne, w tym testy penetracyjne, generowanie exploitów i pracę nad podatnościami z binariów, oraz większość zadań biologii badawczej. Po blokadzie użytkownik dostaje odpowiedź z Opus 4.8 w cyberbezpieczeństwie albo z Opus 5 w biologii. Wczesne testy na claude.ai, Claude Code i Cowork: około **55%** mniej blokad niż przy Fable 5.1, w tym około **60%** mniej w cyberbezpieczeństwie i **40%** mniej w biologii. W dedykowanej ewaluacji ucieczki z piaskownicy, ponad **1800** scenariuszy, z których większości nie dało się rozwiązać bez wyjścia poza piaskownicę, Mythos 5.2 sięgnął po dane umieszczone poza nią w **3,1%** scenariuszy. Opus 5.5: **3,3%**. Sonnet 5.5: **5,1%**. Mythos 5 i 5.1: odpowiednio **39%** i **21%**. Wpis zastrzega, że budowa ewaluacji, które złapią każdą porażkę przed wdrożeniem, pozostaje nierozwiązana, oraz że Fable 5.2 i Mythos 5.2 częściej niż ostatnie modele mówią, że podejrzewają test.

Osobno Anthropic pisze, że w trakcie treningu ograniczyło postęp w tych zdolnościach badawczych, które najbezpośredniej przyspieszałyby rozwój AI, w tym optymalizacji kerneli akceleratorów i ulepszaniu architektur modeli językowych. W tych obszarach Fable 5.2 i Mythos 5.2 mają być na poziomie Opus 5.5. Kodowanie agentowe, sprzęt i zwykłe badania uczenia maszynowego, łącznie z interpretowalnością, miały pozostać nietknięte. Przy inferencji jest jeszcze przezroczysty fallback do Opus 5 dla małego zbioru tematów, w tym kerneli na części nietypowych akceleratorów.

Ochrona przed destylacją ma być najsilniejsza z dotychczas wydanych modeli Anthropic. Wpis mówi o spadku danych zbieranych przez destylujących o **90–99%** i o rozszerzeniu preserved thinking na wszystkie konta API, żeby nie dało się wycinać wcześniejszego kontekstu w celu wyciągnięcia rozumowania. Enterprise Frontier Safeguards, monitoring bezpieczeństwa na danych trzymanych u klienta i zgodny z zerową retencją, jest w prywatnej becie; wpis wymienia Bridgewater, Salesforce i Stripe. Dla pozostałych klientów retencja pod monitoring bezpieczeństwa wynosi **30 dni**. Klienci uprawnieni mogą używać Fable 5.2 i Mythos 5.2 z zerową retencją jeszcze przed włączeniem tego monitoringu.

**Źródła:**

- [Anthropic — Introducing Claude Fable 5.2 and Claude Mythos 5.2, 9.11.2026](https://www.anthropic.com/claude-fable-and-mythos-5-2)
- [Anthropic — strona Claude Fable, cena i odczyt cache](https://www.anthropic.com/claude/fable)
- [Dokumentacja Claude Fable 5.2](https://platform.claude.com/docs/en/models/fable-5-2/overview)
- [AWS — Claude Fable 5.2 i Mythos 5.2 w Amazon Bedrock, 9.11.2026](https://aws.amazon.com/blogs/machine-learning/introducing-claude-fable-5-2-on-aws/)

### 1.2. Google: ogólna dostępność Gemini 4 Carbon (10 listopada 2026)

**10 listopada 2026** Google otwiera **Gemini 4 Carbon** szerzej niż w ogłoszeniu z **28 października**. Tamto ogłoszenie jest w przeglądzie z 4 listopada. Nowością tego tygodnia jest dostęp, identyfikator modelu i doprecyzowanie ceny. Changelog Gemini API z 10 listopada nazywa wydanie ogólnie dostępnym: model `gemini-4-carbon`, opisany jako najsilniejszy model rozumowania Google do długiego kodowania agentowego, multimodalnej pracy z wiedzą, rozumowania naukowego i obrony cybernetycznej. Cena wprowadzająca w changelogu: **2,00 USD** za 1 mln tokenów wejścia i **10,00 USD** za 1 mln tokenów wyjścia, do **30 listopada 2026**.

Wpis Koraya Kavukcuoglu z tego samego dnia mówi, że Carbon jest dostępny w API przez Google AI Studio i Gemini for business dla wszystkich płacących deweloperów i firm, w tej samej cenie wprowadzającej co Gemini 4 Argon. Przypis wpisu podaje, że po okresie wprowadzającym, który kończy się **30 listopada 2026**, obowiązują **4 USD** i **20 USD** za 1 mln tokenów wejścia i wyjścia, i że dotyczy to wariantu Carbon przeznaczonego do dostępu publicznego. Październikowy wpis tej daty końca nie podawał. Tego zdania nie należy przenosić wstecz na ogłoszenie z 28 października.

Argon, według wpisu z 10 listopada, zostaje wyborem do większości inżynierii oprogramowania i pracy z wiedzą. Carbon jest do zadań na granicy: wieloetapowe kodowanie i debugowanie oraz otwarte badania naukowe. Google pisze, że zużywa więcej tokenów niż Argon, bo dokładniej sprawdza wynik.

Karta modelu w dokumentacji API, odczytana 11 listopada: wejście tekst, obraz, wideo, audio i PDF; wyjście tekst. Wspólne okno kontekstu wejścia i wyjścia **1 048 576** tokenów. Maksimum wyjścia **65 536** tokenów w zwykłej odpowiedzi synchronicznej i do pełnego okna przy long decode. Myślenie: poziomy `low`, `medium` i `high`. Domyślnego poziomu ta odczytana sekcja nie wskazuje.

Kanały z wpisu z 10 listopada. Deweloperzy: płatny poziom Gemini API w AI Studio i Android Studio; abonenci Google AI Ultra także w Google Antigravity i AI Studio. Firmy: Gemini for business przez API albo listę modeli, Antigravity albo CodeMender. Użytkownicy: Gemini app i AI Mode w wyszukiwarce, w ramach rolloutu dla abonentów Ultra, nie jako model dla wszystkich kont. Naukowcy: program, który cztery tygodnie wcześniej otworzył wnioski o sześć miesięcy Argona w Antigravity dla 10 tys. osób, od 10 listopada obejmuje też Carbon dla obecnych i przyszłych uczestników. Obrońcy cybernetyczni: osobny dostęp do „Carbon for cyber” przez Fairwind, nadal na wnioski i falami. Wpis rozdziela więc publiczny Carbon od wariantu cybernetycznego. Nie są to dwa ogłoszenia tego samego dostępu.

W Antigravity Google pokazuje podgląd polecenia `/swarm`: jedno polecenie ma uruchamiać zespół agentów śledzony na żywo. Carbon ma dostawać role o najgłębszym rozumowaniu, a lżejsze modele — równoległe, izolowane obszary robocze i sprawdzanie zmian. To funkcja produktu, nie osobny model.

Liczby z wpisu z 10 listopada. To twierdzenia Google albo partnerów cytowanych przez Google.

| Zadanie | Co podaje wpis z 10 listopada |
| --- | --- |
| CursorBench 4.0, WANDR Perplexity, AutomationBench Zapiera | miejsce 1 i ponad dwukrotnie niższy koszt na zadanie niż następny zewnętrzny model |
| Multimodal Knowledge Agent, nowy benchmark z Artificial Analysis | miejsce 2 i ponad sześciokrotnie niższy średni koszt na zadanie niż model na miejscu 1 |
| Hebbia, ewaluacja agentowa badań finansowych od końca do końca | wynik na poziomie najlepszego testowanego modelu, w ewaluacjach przed wydaniem |
| Balyasny Asset Management, General Financial Intelligence | pierwsze miejsce wśród 23 konfiguracji modeli frontier |
| Project Fortify, benchmark wewnętrzny | 100% recall skanowania i 95% precyzji triage |
| Otwarte repozytoria w tym samym projekcie | ponad 25% względnej poprawy recall względem Argona |
| Uczciwość agentowa, 375 zadań | 92% zaliczonych, wobec 70% dla Argona; odmowa uzupełniania brakujących danych doświadczalnych w 98% przypadków; oznaczanie wad metodologicznych w 68% |

Osobno, jako powtórzenie pomiaru z ogłoszenia 28 października, a nie jako nowy wynik tego tygodnia: **0%** skuteczności ataku prompt injection na benchmarku Gray Swan IPI. Wpis z 10 listopada sam nazywa ten wynik informacją sprzed dwóch tygodni i dodaje, że odporność na prompt injection nadal wymaga poprawy.

Zabezpieczenia opisane jako nowe względem Argona, nadal ze wpisu Google. W środowiskach testowych opartych na ExploitBench i CyScenarioBench Carbon zablokował **99%** trajektorii ataku adaptacyjnego agenta red-teamowego. Skuteczność pojedynczej próby naruszenia spadła do **0,8%**, z **3,1%** przy Argonie. W teście Gray Swan skuteczność zapytań zautomatyzowanego ataku cybernetycznego spadła do **2,17%**, z **9,86%** przy Argonie. Trajectory Labs, według wpisu, nie znalazło nowych uniwersalnych jailbreaków w **132 godzinach** i ponad **13 tys.** żądań.

Dwa przykłady użycia obronnego są opisane bez szczegółów technicznych, które ten przegląd świadomie pomija. Zespół Cloud Vulnerability Research Google miał przy Carbonie pokazać, że dwa błędy w popularnym otwartym oprogramowaniu są podatnościami eksploatowalnymi, o wadze porównywalnej z niedawnym PHP2Shell; szczegóły mają przyjść po zakończeniu odpowiedzialnego ujawnienia. Wiz w programie Scan for Good, według wpisu, znalazł podatności zero-day u dwóch dużych dostawców SaaS w mniej niż dwie godziny i uzgodnił z nimi poprawki. Benchmarki „prowadzenia” na SEC-bench Pro, ExploitGym i CWE-bench v1 wpis przypisuje Carbon for cyber w dostępie przez Fairwind, nie publicznemu wariantowi opisanemu w cenniku.

W naukach Google opisuje trzy wewnętrzne użycia: formalną weryfikację kodu protokołu kryptograficznego Signal w Lean przy AlphaProof Code, diagnozę artefaktów w notatkach laboratoryjnych przy rozwoju testów enzymatycznych oraz wyszukanie odległych homologów dla rodzin białek z małym pokryciem w bazach, ze średnio **40-krotnym** wzrostem liczby homologów na siedmiu rodzinach z zestawu CASP17. Szerszy benchmarking tego ostatniego, według wpisu, jeszcze trwa. Axiom Bio ma przenosić produkcyjne analizy naukowe na Carbon i Argon.

**Źródła:**

- [Google — Gemini 4 Carbon is now available, 10.11.2026](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-carbon-now-available/)
- [Gemini API, release notes, wpis 10.11.2026 o `gemini-4-carbon`](https://ai.google.dev/gemini-api/docs/changelog)
- [Dokumentacja modelu Gemini 4 Carbon](https://ai.google.dev/gemini-api/docs/models/gemini-4-carbon)
- [Ogłoszenie z 28.10.2026, już opisane w przeglądzie z 4 listopada](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/)

### 1.3. OpenAI: GPT-6 Cyber (5 listopada 2026)

**5 listopada 2026** OpenAI ogłasza **GPT-6 Cyber**, wyspecjalizowany wariant do autoryzowanej pracy nad podatnościami. To nie jest model ogólny i nie jest następcą publicznego GPT-6 Astra. Wpis nie podaje ceny. Ceny z wtórnych zestawień ten przegląd pomija.

Karta systemowa, opublikowana tego samego dnia, opisuje GPT-6 Cyber jako cybernetyczny wariant GPT-6 Astra po dodatkowym treningu, który ma podnieść zdolności i zmniejszyć odmowy w zadaniach cybernetycznych, przy zachowaniu odmów poza tym obszarem. W Preparedness Framework karta daje mu te same oznaczenia co Astrze: **Critical** w cyberbezpieczeństwie, **High** w dziedzinie biologicznej i chemicznej oraz poniżej **High** w samorozwoju AI. Wpis premierowy mówi, że oznaczenie cybernetyczne Critical jest podniesieniem względem **High** przy GPT-5.6 Cyber. Oba zdania dotyczą różnych porównań. Nie wynika z nich, że jest to pierwsze oznaczenie Critical w ogóle.

Dostęp na starcie, według wpisu: API i Codex, dla wybranej grupy zatwierdzonych klientów **Daybreak Red**. OpenAI zapowiada stopniowe rozszerzenie na wszystkich klientów Daybreak Red i równocześnie daje GPT-5.6 Cyber wszystkim organizacjom w tym poziomie. Daybreak Blue w alfie, dla GPT-6 Astra, jest rozszerzany na kolejne organizacje i indywidualnych badaczy bezpieczeństwa. Karta systemowa wymaga weryfikacji tożsamości i uprawnień, zgody na ograniczenia autoryzowanej działalności i dostępu osób trzecich, przeglądu praktyk bezpieczeństwa organizacji, SSO, uwierzytelniania wieloskładnikowego oraz listy dozwolonych adresów IP dla API. Klienci API z zerową retencją na ogół potrzebują Private Safety Processing. Karta mówi o zatwierdzonych użytkownikach i organizacjach Daybreak Red, nie tylko o firmach. Indeksowany tekst centrum pomocy, którego bezpośrednie żądanie zwróciło **403**, dokłada rozróżnienie, którego karta w odczytanym fragmencie nie powtarza: osobna zgoda na model GPT-6 Cyber oraz dostęp Red dla zatwierdzonych organizacji biznesowych i enterprise, nie przez wniosek indywidualny. Włączenie Red w projekcie API, według tego samego tekstu, tej osobnej zgody nie zastępuje.

Liczby z wpisu OpenAI. Są to pomiary vendora.

| Ocena | Co podaje OpenAI |
| --- | --- |
| ExploitGym | 48,5%, wobec 32,1% dla GPT-5.6 Cyber; wpis nazywa to poprawą względną o 51% |
| ExploitGym Honeypot, bez promptu wdrożeniowego | model nie eksploatuje usług poza zakresem w 99,93% testów, wobec 94,49% dla GPT-5.6 Cyber |
| Ten sam test z promptem wdrożeniowym | 100% |
| Odkrywanie podatności w aplikacjach webowych bez kodu źródłowego | recall 40,3%, wobec 32,0% dla GPT-6 Astra |
| RemoteExploitBench, znane podatności w kontrolowanym środowisku | GPT-6 Astra z Daybreak Blue odmawia 100% zadań; GPT-6 Cyber kończy 95%, a jedyna porażka to exploit, którego nie udało się uruchomić zdalnie |

Wpis podaje też wyniki kampanii na prawdziwym oprogramowaniu, jako twierdzenia OpenAI. Przy Firefoxie: **81** nowych podatności, które Mozilla sklasyfikowała jako wysokiej wagi, oraz **30** znanych problemów ocenionych jako poważniejsze, niż wcześniej sądzono; łatki dla wielu z nich Mozilla wydała. Przy jądrze Linuksa, w tym samym harnessie badawczym: odtworzenie **1724** podatności i działające exploity dla **948**, wobec **166** eksploatowanych przez GPT-5.6 Sol; **304** ustaleń krytycznych przekazanych maintainerom z kandydatami łatek. Cytowani w wpisie Brian Grinstead z Firefoxa, Thai Duong z Calif, Steven Hao z Cognition, Lee Klarich z Palo Alto Networks, Anthony Grieco z Cisco, Chris Corde z SentinelOne, Bartley Richardson z CrowdStrike, Kyle Polley z Perplexity i Harjot Gill z CodeRabbit opisują własne testy. Liczba **23%** wobec **13%** na wewnętrznym benchmarku Cognition oraz **66%** więcej ustaleń wysokiej i średniej wagi na benchmarku CodeRabbit pochodzą z tych cytatów, nie z harnessu OpenAI.

OpenAI pisze też o programie grantowym Daybreak for Frontline Defenders o wartości **1 mld USD** oraz o nowej grupie wewnątrz Daybreak Red dla obrońców infrastruktury krytycznej. Dragos, według wpisu i cytatu Roba T. Lee, sprawdzał modele w laboratoryjnej imitacji elektrowni. Ten przegląd nie opisuje przebiegu tych testów. Karta i wpis mówią o monitoringu zgodności działań z upoważnieniem użytkownika, o monitoringu ukierunkowanym przy skoordynowanym ujawnianiu, o piaskownicy i przeglądzie działań oraz o blokadach pomocy wysokiego ryzyka wobec systemów krytycznych. Szczegóły procedur ataku, fragmenty łańcucha myśli i kolejne kroki testów przemysłowych są w materiałach OpenAI; ten przegląd ich nie powtarza.

**Źródła:**

- [OpenAI — GPT-6 Cyber, 5.11.2026; nagłówek `HEAD` zwracał 403, treść odczytana inną ścieżką](https://openai.com/index/introducing-gpt-6-cyber/)
- [Karta systemowa GPT-6 Cyber, 5.11.2026](https://deploymentsafety.openai.com/gpt-6-cyber/access-to-gpt-6-cyber)
- [OpenAI Help Center — Daybreak; bezpośrednie żądanie 403, zdania o osobnej zgodzie z indeksu artykułu](https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview)

### 1.4. Moonshot: publiczne wagi Kimi K3.1 Pro

Kimi K3.1 Pro i Highspeed weszły do przeglądu z 28 października jako modele API. Rano **4 listopada 2026**, około 07:04 UTC, publiczne API Hugging Face dla organizacji `moonshotai` jeszcze ich nie pokazywało, a angielski wpis nadal zapowiadał wagi „do 4 listopada”. Ten podrozdział opisuje tylko to, co widać **11 listopada**.

Repozytorium `moonshotai/Kimi-K3.1-Pro` jest publiczne i niebramkowane (`gated: false`). API Hugging Face podaje `createdAt` **2026-11-02T04:13:51.000Z**, zgodny ze znacznikiem pierwszego commitu „Initial commit”. Drugi commit, „Update encoding_k3.py”, i pole `lastModified` mają znacznik **2026-11-05T07:11:43.000Z**. Znacznik utworzenia nie dowodzi, że wagi dało się pobrać 2 listopada: przegląd z ranka 4 listopada tego repozytorium na publicznej liście nie widział. Relacje prasowe rozjeżdżają się o jeden dzień. TechNode datuje tekst na **5 listopada 2026**. TokenPost podaje publikację **5 listopada 2026, 6:04 czasu EST**. AI Lounge datuje samą publikację wag na **4 listopada**. Godziny przejścia z prywatnego na publiczne ten przegląd nie ustala.

W repozytorium jest **96** plików safetensors i **112** plików łącznie. Pole `usedStorage` ma wartość **1 561 355 732 732** bajtów, czyli około **1,56 TB**. Nagłówek safetensors w tym samym API podaje **2 780 110 363 392** parametrów. Karta zaokrągla architekturę do **2,8 bln** parametrów łącznie i **104 mld** aktywnych na token. To dwa sformułowania tej samej publikacji, nie dwa modele.

Z karty, bez powtarzania tabeli benchmarków z październikowej premiery: Mixture-of-Experts, **93** warstwy, w tym **1** gęsta, **896** ekspertów, **16** wybieranych na token i **2** współdzielone. Uwaga ma wymiar **7168**, **96** głów. Kontekst **1 048 576** tokenów. Wejście tekst i obraz, enkoder MoonViT-V2 o **401 mln** parametrów. Kwantyzacja na karcie: wagi MXFP4 i aktywacje MXFP8, trening świadomy kwantyzacji. W warstwach uwagi względem Kimi K3 pełna Gated MLA została zastąpiona Gated DeepSeek Sparse Attention. Słownik **160 tys.** tokenów. Zalecane ustawienie wyników, o ile karta nie mówi inaczej: wysiłek `max`, temperatura **1,0**, top-p **0,95**.

Sekcja wdrożenia karty kieruje do API na `platform.kimi.ai`, identyfikator `kimi-k3.1-pro`, interfejsy zgodne z OpenAI i Anthropic, oraz do vLLM, SGLang i TokenSpeed. To kontynuacja dostępu z października, nie nowy model.

Licencja z pliku `LICENSE` w repozytorium nosi tytuł „Kimi K3.1-Pro License” i jest zmodyfikowanym MIT, nie licencją OSI o tej nazwie. Dozwolone są użycie, modyfikacja, dystrybucja, sprzedaż, wdrożenie i dostrajanie, z trzema warunkami istotnymi komercyjnie. Po pierwsze, zachowanie treści licencji. Po drugie, podmiot, który sam albo z podmiotami powiązanymi prowadzi model jako usługę i przekroczył **20 mln USD** przychodu łącznie w dowolnych kolejnych 12 miesiącach, potrzebuje osobnej umowy z Moonshot przed komercyjnym użyciem oprogramowania albo dzieł pochodnych. Definicja usługi wyłącza produkt końcowy, w którym model jest tylko osadzony w funkcji, oraz samo przekazywanie zapytań do cudzego hostingu. Po trzecie, produkt komercyjny powyżej **100 mln** aktywnych użytkowników miesięcznie albo powyżej **20 mln USD** przychodu miesięcznie ma wyraźnie pokazywać nazwę „Kimi K3.1-Pro” w interfejsie. Warunki drugi i trzeci nie dotyczą użytku wewnętrznego ani oficjalnych produktów Moonshot i certyfikowanych partnerów inferencji.

Tabeli wyników z karty ten przegląd nie przepisuje. Październikowa premiera modelu jest już opisana, a wyniki vendora na karcie wag nie są nowym, niezależnym pomiarem z tego tygodnia.

**Źródła:**

- [Karta `moonshotai/Kimi-K3.1-Pro`](https://huggingface.co/moonshotai/Kimi-K3.1-Pro)
- [Pliki repozytorium, 96 shardów safetensors](https://huggingface.co/moonshotai/Kimi-K3.1-Pro/tree/main)
- [Licencja Kimi K3.1-Pro](https://huggingface.co/moonshotai/Kimi-K3.1-Pro/blob/main/LICENSE)
- [TechNode, 5.11.2026](https://technode.com/2026/11/05/moonshot-ai-releases-kimi-k3-1-pro-model-weights/)
- [TokenPost, 5.11.2026, 6:04 EST](https://www.tokenpost.com/news/technology/49222)
- [API modelu, metadane `createdAt`, `lastModified`, `usedStorage` i liczba parametrów safetensors, odczyt 11.11.2026](https://huggingface.co/api/models/moonshotai/Kimi-K3.1-Pro)

---

## 2. Zastosowania AI w prawie i wymiarze sprawiedliwości

W tym oknie nie ma jednej nowej ustawy sądowej o AI. Jest za to sprawozdanie Lady Chief Justice dla Parlamentu, przemówienie sędzi High Court do biegłych, niepublikowany wyrok kalifornijski o opinii biegłej przygotowanej z ChatGPT, postanowienie sądu federalnego w Kentucky o areszcie po rozpoznaniu twarzy oraz przemówienie sędziego Sądu Najwyższego Filipin. W Polsce ustawowy termin pierwszego posiedzenia Komisji Rozwoju i Bezpieczeństwa Sztucznej Inteligencji przypada na dzień tego przeglądu, a samo posiedzenie Komisja datuje na 28 października. Otwarty jest nabór do Społecznej Rady.

Poza oknem, więc bez osobnego omówienia: wytyczne Canadian Judicial Council z **20 października 2026**; propozycja Pensylwanii w biuletynie z **24 października 2026**, z terminem uwag do 24 listopada; wyrok pracy w Parauapebas z **12 maja 2026** o ukrytej instrukcji dla AI, do którego wracają wtórne notatki. Przewodnik Judicial Review Guide 2026, o którym 10 listopada pisze kancelaria Brabners, na okładce PDF ma **sierpień 2026**. To nie jest akt tego tygodnia. Strona Administrative Court w jednym z odczytów nadal odsyłała do wydania 2025.

### 2.1. Anglia i Walia: sprawozdanie Lady Chief Justice (5 listopada 2026)

**5 listopada 2026** Lady Chief Justice, baronessa Carr of Walton-on-the-Hill, złożyła w Parlamencie trzecie sprawozdanie roczne. Obejmuje pracę sądownictwa Anglii i Walii od października 2025 do września 2026. Strona sądownictwa publikuje je po angielsku i po walijsku. Plik PDF w tym przeglądzie nie został pobrany: strona ogłoszenia przy bezpośrednim odczycie nie zwróciła adresu pliku. Cytaty niżej są więc z relacji, które wprost przytaczają sprawozdanie, a nie z samodzielnej paginacji PDF.

Law Society Gazette z **6 listopada 2026** przytacza zdanie, że lista cywilna King’s Bench Division i Administrative Court widzą rosnącą liczbę stron bez pełnomocnika, które budują pozwy przy pomocy AI. Użycie to „poprawia dostęp do wymiaru sprawiedliwości”, a zarazem „nakłada znaczne obciążenie na personel sądowy i na sądownictwo”. Często potrzeba dodatkowego zarządzania sprawą tylko po to, by ustalić, jakiego środka strona faktycznie żąda. We wstępie, według Gazette, sądownictwo „uważnie rozważa” potencjał i zagrożenia. Wiele osób pełniących urząd sędziowski zauważa wzrost użycia AI wśród stron bez pełnomocnika. Odpowiedzią ma być między innymi przygotowywany przez Wydział Karny Sądu Apelacyjnego przewodnik dla takich stron, jak przygotowywać podstawy apelacji przy użyciu AI. Szersze zdanie ze wstępu, w przytoczeniu Gazette: narzędzia do transkrypcji i streszczeń mogą zmniejszać zaległości i poprawiać terminowość, ale „nadzór nad użyciem i nad orzekaniem pozostanie funkcją człowieka, sędziego”.

Ten sam tekst Gazette przytacza fragment o Criminal Appeal Office: użycie AI przy podstawach apelacji wnoszonych przez strony bez pełnomocnika zostało odnotowane, a Wydział Karny Sądu Apelacyjnego przygotowuje wytyczne. Podziękowanie jest skierowane do jednostki apelacyjnej Crown Prosecution Service. Sprawozdanie, według Gazette, zapowiadało też raport Civil Justice Council o AI przy pismach procesowych jako istotny wkład w debatę. Ten raport wyszedł pod koniec października i jest już w przeglądzie z 4 listopada. Nie jest nowym aktem tego tygodnia.

Court Quarterly, tekst z 5 listopada, i Local Government Lawyer, tekst z 9 listopada, podają ze sprawozdania liczbę **1328** wniosków o judicial review między kwietniem a czerwcem 2026, o **42%** więcej niż w tym samym okresie 2025. Court Quarterly dopisuje, że sprawozdanie nie mówi, jaka część tego wzrostu wiąże się z AI. Gazette tej liczby nie przytacza. Ten przegląd jej nie przenosi do zdania Lady Chief Justice. Jest to figura podana przez dwie relacje o sprawozdaniu, nie cytat sprawdzony w PDF.

**Źródła:**

- [Sądownictwo Anglii i Walii — ogłoszenie sprawozdania, 5.11.2026](https://www.judiciary.uk/lady-chief-justices-annual-report-2026-adroddiad-blynyddol-yr-arglwyddes-brif-ustus-2026/)
- [Law Society Gazette, 6.11.2026](https://www.lawgazette.co.uk/news/ai-use-by-litigants-in-person-creates-demands-on-court-lcj-warns/5128446.article)
- [Court Quarterly, 5.11.2026, liczba 1328 i 42%](https://courtquarterly.co.uk/article/lady-chief-justice-reports-rising-use-of-ai-by-litigants-in-person-in-third-annual-report)
- [Local Government Lawyer, 9.11.2026](https://www.localgovernmentlawyer.co.uk/litigation-and-enforcement/400-litigation-news/102194-lady-chief-justice-warns-of-growing-pressures-from-litigants-using-ai-in-administrative-court)

### 2.2. Anglia i Walia: przemówienie Mrs Justice Joanny Smith do biegłych (6 listopada 2026)

**6 listopada 2026** Mrs Justice Joanna Smith, interim deputy president Wydziału Business and Property, wygłosiła na Bond Solon Expert Witness Conference w Church House w Westminster przemówienie „Artificial Intelligence and Expert Evidence – Opportunities, Risks and Responsibilities”. Pełny tekst jest na stronie sądownictwa. Law Society Gazette relacjonuje je **7 listopada**. Piątek 6 listopada zgadza się z późniejszą relacją Info-Gov, która mówi o wystąpieniu „w piątek”.

Sędzia była współprzewodniczącą grupy, która przygotowała raport Civil Justice Council z końca października. Raport nie jest w tym tygodniu ponownie streszczany. Nowością jest to, co sędzia mówi biegłym, zanim Civil Procedure Rule Committee w ogóle przyjmie rekomendację.

Obowiązki niezależności, obiektywizmu, przejrzystości i kompetencji zawodowej się nie zmieniają. Pytaniem nie jest, czy biegłym wolno używać AI, ani czy należy go zakazać. Pytaniem jest, jak używać go zgodnie z obowiązkiem wobec sądu. Konsultacja grupy dała, według przemówienia, przeważającą odpowiedź, że użycie powinno być jawne. Rekomendowana deklaracja dotyczy tylko narzędzia, które wygenerowało albo wpłynęło na treść merytoryczną opinii, w tym na metodę albo analizę. Narzędzia administracyjne deklaracji nie wymagają. Tam, gdzie deklaracja jest potrzebna, ma dać dość informacji do kontroli: metodę, potwierdzenie, że narzędzie nadaje się do tego celu, i — wyjątkowo, nie zawsze — nazwę narzędzia. Osobno grupa rekomenduje zmianę przewodnika CJC dla instruowania biegłych w sprawach cywilnych z 2014 roku. Test z tego przewodnika ma być trójdzielny: czy AI wpłynęło na treść, jakie informacje ujawnić, żeby druga strona i sąd mogli zbadać metodę, oraz czy w tej sprawie trzeba ujawnić samo narzędzie.

Sędzia wylicza zastosowania, które same z siebie deklaracji raczej nie uruchomią: porządkowanie zbiorów, chronologie, klasyfikacja, streszczenia, wyszukiwanie tematów, research, struktura opinii, korekta językowa. Zaraz potem zastrzega, że streszczenie może pominąć cechę, którą człowiek by zobaczył, że narzędzie układające tekst może subtelnie zmienić treść, a transkrypcja może wstawić zdanie, którego nie powiedziano. Jeśli wpływ na treść jest bezpośredni albo pośredni, użycie trzeba ujawnić — o ile komitet reguł przyjmie rekomendację — i dać drugiej stronie oraz sądowi dość informacji, by uznały, że opinia jest nadal opinią biegłego. Bez tego opinia może być przedmiotem szczegółowych pytań na cross-examination.

Osiem pytań, które sędzia każe zadać sobie po otrzymaniu instrukcji: czy instrukcja w ogóle pozwala na AI, także ze względu na własność intelektualną, dane i regulacje; czy narzędzie w ogóle zawiera AI; czy nadaje się do zadania i czy jest aktualne; czy jest bezpieczne dla informacji poufnych i objętych przywilejem; czy zespół rozumie obowiązek ujawnienia i ma zapis kroków; czy biegły umie wyjaśnić działanie i ograniczenia w sądzie; czy ma zapis, w jakim stopniu narzędzie wpłynęło na treść; a jeśli wpłynęło, dziesięć dalszych pytań o ujawnienie nazwy, odtwarzalność, błędy systematyczne, ukryte założenia, weryfikację, nadzór człowieka, autorstwo wniosków, zdolność wyjaśnienia każdego z nich, gotowość do opisu użycia pod przysięgą i zgodność z obowiązkami zawodowymi. Nawet gdy instrukcja milczy, sędzia uważa za praktycznie rozsądne powiedzenie solicitorowi o planowanym użyciu na początku.

Zdanie końcowe: AI jest narzędziem, nie biegłym, i nie zastępuje opinii. Odpowiedzialność zostaje przy biegłym. Tego samego dnia, według przemówienia, ukazał się Bond Solon Expert Witness Survey 2026. Liczb z tej ankiety przemówienie nie podaje i ten przegląd ich nie uzupełnia.

**Źródła:**

- [Pełny tekst przemówienia, sądownictwo Anglii i Walii, 6.11.2026](https://www.judiciary.uk/speech-by-mrs-justice-joanna-smith-artificial-intelligence-and-expert-evidence-opportunities-risks-and-responsibilities/)
- [Lista aktualności sądownictwa, wpis z 6.11.2026](https://www.judiciary.uk/news-and-updates/)
- [Law Society Gazette, 7.11.2026](https://www.lawgazette.co.uk/news/start-telling-us-now-about-ai-use-top-judge-urges-experts/5128458.article)

### 2.3. Kalifornia: niepublikowana opinia w *Gillespie v. Superior Court* (4 listopada 2026)

**4 listopada 2026** Czwarty Dystrykt Sądu Apelacyjnego Kalifornii, Wydział Pierwszy, złożył niepublikowaną opinię w sprawie *Gillespie v. Superior Court*, sygnatura **D088222**, sąd pierwszej instancji San Diego, sprawa karna SCD307508. Strona Judicial Branch prowadzi ją w zbiorze opinii niepublikowanych, niecytowalnych. Biuletyn sądów Kalifornii streścił ją **5 listopada** i napisał, że rozstrzygnięcie zapadło „wczoraj”. Autorką opinii jest sędzia Do. Przystąpili: prezesująca McConnell i sędzia Rubin. Wniosek o writ of mandate oddalono.

Crystal Gillespie domagała się uchylenia postanowienia, które odmówiło jej pretrial mental health diversion na podstawie sekcji 1001.36 kodeksu karnego. Sąd pierwszej instancji uznał ją za nieuprawnioną i nie przeszedł do pytania o to, czy diversion byłby dla niej odpowiedni. Przyjął trzy diagnozy — zaburzenie afektywne dwubiegunowe typu I, zaburzenie lękowe uogólnione i zaburzenie używania metamfetaminy — ale uznał, że żadne nie było istotnym czynnikiem motywującym, przyczynowym ani współprzyczyną zarzucanej kradzieży w sklepie. Oskarżenie przyznało diagnozy. Ustawa tworzy wtedy domniemanie związku, obalone tylko jasnym i przekonującym dowodem, że zaburzenie takim czynnikiem nie było.

Spór o AI dotyczy opinii biegłej oskarżenia, dr Nicole Friedman, nie opinii biegłej obrony, dr Lauren Vickerman. Obrona chciała wyłączyć opinię Friedman, bo powstała przy „niewiarygodnej i nieweryfikowalnej” AI i nie spełnia testu *Kelly/Frye* dla nowej techniki naukowej. Sąd pierwszej instancji sprzeciw oddalił: użycie AI jest „bardzo powszechne” i sam fakt AI nie oznacza wady dowodu. Na rozprawie w marcu 2026 Friedman zeznała, że używała ChatGPT jako narzędzia organizacji i jako „thought partner”, a nie do wytworzenia opinii. Pytania, które mu zadawała, obejmowały jednak przepisy kodeksu karnego i to, co można uznać za związek przyczynowy. W pisemnej opinii, przygotowanej z pomocą ChatGPT, znalazło się też błędne zdanie, że w dokumentacji medycznej nie ma śladu ostrej hospitalizacji psychiatrycznej, epizodu maniakalnego, objawów psychotycznych ani ciężkiej dekompensacji. Sąd apelacyjny nazywa ten materiał niepokojącym i takim, z którego rozsądny oceniający fakty mógłby wnosić, że opinia nie była niezależna. Sąd pierwszej instancji uwierzył jednak wyjaśnieniu Friedman, że ChatGPT był tablicą rezonansową, jak kolega albo aplikant, a wniosek końcowy był jej własny. Sąd apelacyjny pisze wprost, że podziela obawy obrony, ale nie waży wiarygodności od nowa. Skoro ustalenie faktyczne ma wsparcie w istotnym dowodzie, nie było nadużycia uznania przy dopuszczeniu opinii i test *Kelly/Frye* na tak ustalonym stanie faktycznym się nie uruchamia.

Osobno sąd uznał, że istotny dowód pozwalał obalić domniemanie związku diagnoz z czynem, głównie na podstawie nagrania ze sklepu, które Friedman opisała jako zachowanie skoordynowane, celowe i strategiczne. To jest ocena dowodu w sprawie diversion, nie ogólna reguła o AI. Opinia jest niepublikowana. Nie tworzy cytowalnego precedensu Kalifornii.

**Źródła:**

- [Judicial Branch of California — opinia niepublikowana D088222, złożona 4.11.2026](https://courts.ca.gov/opinion/unpublished/2026-11-04/d088222)
- [California Courts Newsroom, 5.11.2026](https://newsroom.courts.ca.gov/news/ca-no-error-allowing-expert-testify-about-report-generated-help-ai)
- [Tekst slip opinion w odpisie CaseFoundry, z którego pochodzą cytaty zeznań i dyspozycja](https://casefoundry.law/court/ca-4th-district/7970906/crystal-gillespie-d088222-super-ct-no-scd307508-v-superior-court-of-san-diego-county-2026.html)

### 2.4. Stany Zjednoczone: sąd federalny we wschodnim Kentucky o areszcie po rozpoznaniu twarzy

**10 listopada 2026, 17:23 UTC**, Bloomberg Law opisuje postanowienie sędziego **S. Chada Meredith** z Sądu Dystryktowego Stanów Zjednoczonych dla Wschodniego Dystryktu Kentucky. Artykuł mówi, że sędzia wypowiedział się „w poniedziałek”. Przy dacie artykułu, wtorek 10 listopada, jest to **9 listopada 2026**. Funkcję sędziego w Sądzie Dystryktowym dla Wschodniego Dystryktu Kentucky potwierdza kartoteka Federal Judicial Center. Strona samego sądu w tym odczycie odrzuciła żądanie, więc nie jest tu źródłem. Samego postanowienia ten przegląd nie odczytał. Sygnatury, nazwiska stron i dokładnego brzmienia tezy w publicznym fragmencie artykułu nie ma, więc ich tu nie ma.

Z tego, co Bloomberg podaje: policjant pozwany o bezprawne aresztowanie i ponad dwutygodniowe osadzenie mężczyzny, którego AI błędnie wskazało jako sprawcę, nie uzyskał oddalenia pozwu cywilnego o naruszenie praw. Czwarta Poprawka, według relacji słów sędziego, nie pozwala funkcjonariuszowi scedować oceny prawdopodobnej przyczyny na narzędzie AI ani aresztować kogoś wyłącznie na podstawie niepotwierdzonego wniosku tego narzędzia, że osoba popełniła przestępstwo. Meredith oddalił wniosek policji o odrzucenie pozwu. Dalszy fragment artykułu jest za paywallem i nie został tu dopisany z innych serwisów. Wtórna notatka, która miesza tę sprawę z pozwami z Dakoty Północnej, Florydy i Nevady, nie jest źródłem faktów o postanowieniu z Kentucky.

**Źródła:**

- [Bloomberg Law, 10.11.2026, 17:23 UTC; publiczny fragment, reszta za paywallem, nagłówek żądania 403](https://news.bloomberglaw.com/litigation/cop-stuck-with-wrongful-arrest-suit-over-false-ai-facial-match)
- [Federal Judicial Center — Stephen Chad Meredith, sędzia E.D. Ky.](https://www.fjc.gov/history/judges/meredith-stephen-chad)

### 2.5. Filipiny: wystąpienie sędziego Leonena (4 listopada 2026)

**4 listopada 2026** starszy sędzia stowarzyszony Sądu Najwyższego Filipin, Marvic M.V.F. Leonen, wygłosił przemówienie inauguracyjne na 4. szczycie komisarzy śledczych Komisji Dyscypliny Adwokackiej Zintegrowanej Izby Adwokackiej. Szczyt trwał od 3 do 5 listopada w Diamond Hotel w Manili, pod hasłem standardów etycznych adwokatów w epoce mediów społecznościowych i AI. Tribune opublikowało relację **10 listopada 2026, 13:13 czasu filipińskiego**, ze zdjęciem opisanym jako materiał biura komunikacji Sądu Najwyższego. Osobnego komunikatu Sądu tego przegląd nie odnalazł. Ramy zarządcze, o których sędzia przypomina, nie są aktem tego tygodnia. Nowością jest samo wystąpienie i sposób, w jaki wiąże AI z niezależnością sądu przy postępowaniu dyscyplinarnym.

Leonen mówi, że ustalenia komisarzy są podstawą faktyczną decyzji Sądu Najwyższego w skargach na adwokatów: „ta komisja jest okiem sądu na fakty”. Niezależność sądu nie sięga dalej niż fakty, które przed nim położono. Narzędzia AI „nigdy nie zasiądą na ławie” i „nie powinny podpisywać waszych raportów”. Governance Framework on the Use of Human-Centered Augmented Intelligence in the Judiciary, w przytoczeniu Tribune, wymaga ujawniania użycia AI, zabrania opierać orzeczenie wyłącznie na wyniku wygenerowanym przez AI i zabrania wprowadzać informacje poufne do narzędzi AI bez upoważnienia. Sędzia każe komisarzom sięgać do akt źródłowych, a nie poprzestać na streszczeniu AI, sprawdzać każdy cytat w źródle, pisać ustalenia własnymi słowami i ujawniać użycie narzędzi. Relacja Manila Times z 11 listopada powtarza ten sam zestaw zaleceń. Żadna z nich nie podaje nowego numeru aktu ani zmiany ram.

**Źródła:**

- [Tribune, 10.11.2026, relacja z przemówienia 4.11.2026](https://tribune.net.ph/2026/11/10/leonen-warns-lawyers-against-ai-misuse-threats-to-judicial-independence)
- [The Manila Times, 11.11.2026](https://www.manilatimes.net/2026/11/11/news/national/leonen-warns-lawyers-vs-blind-reliance-on-ai/2466553)

### 2.6. Polska: termin pierwszego posiedzenia KRiBSI i nabór do Społecznej Rady

Dzień tego przeglądu, **11 listopada 2026**, jest datą, którą przegląd z 4 listopada zapisał jako ustawowy koniec terminu na zwołanie pierwszego posiedzenia Komisji Rozwoju i Bezpieczeństwa Sztucznej Inteligencji. Tamten przegląd posiedzenia w swoim oknie nie znalazł. Komunikat samej Komisji, opublikowany na gov.pl, datuje pierwsze posiedzenie na **28 października 2026**. Prowadziła je przewodnicząca Pamela Krzypkowska. To zdarzenie sprzed okna 4–11 listopada. Ten przegląd nie streszcza jego porządku. Na dzień 11 listopada termin wskazany w poprzednim przeglądzie jest już po stronie oficjalnego komunikatu zamknięty wcześniejszą datą, a nie otwartym brakiem posiedzenia.

W bieżącym oknie na stronie Komisji wisi nabór do **Społecznej Rady do spraw Sztucznej Inteligencji**. Strona naboru, odczytana 11 listopada, nie pokazała w sposób możliwy do pewnego odczytu osobnej daty publikacji ogłoszenia. Komunikat z 28 października zapowiadał uruchomienie „w najbliższych dniach” i okno zgłoszeń przez dwa tygodnie od ogłoszenia. Sam nabór podaje termin **16 listopada 2026**, z datą wpływu do urzędu jako decydującą.

Rada, według ogłoszenia, jest organem opiniodawczo-doradczym na podstawie art. 45–47 ustawy z dnia 3 lipca 2026 r. o systemach sztucznej inteligencji (Dz.U. poz. 1003). Liczy od **9 do 15** osób, kadencja trwa **2 lata**. Do zadań opisanych w ogłoszeniu należy wydawanie opinii i stanowisk w sprawach przekazanych przez Komisję oraz z własnej inicjatywy, a także przyjmowanie i przekazywanie przewodniczącemu wniosków o wszczęcie postępowania w sprawie naruszenia rozporządzenia 2024/1689 albo ustawy. Rada podejmuje też uchwały i przekazuje wnioski, gdy przewodniczący albo zastępcy naruszają art. 35 albo 36 ustawy.

Kandydatów zgłaszają podmioty wymienione w ogłoszeniu, nie każda osoba we własnym imieniu. Lista obejmuje między innymi współprzewodniczącego strony samorządowej Komisji Wspólnej Rządu i Samorządu Terytorialnego, Rzecznika Praw Obywatelskich, Rzecznika Praw Dziecka, Rzecznika Praw Pacjenta, Rzecznika Małych i Średnich Przedsiębiorców, Głównego Inspektora Pracy, izby gospodarcze z obszaru AI i gospodarki cyfrowej, reprezentatywne organizacje związkowe, uczelnie i instytuty, wskazane fundacje i stowarzyszenia oraz związki pracodawców. Zgłoszenie wymaga rekomendacji z wykazaniem wiedzy i doświadczenia oraz oświadczenia kandydata. Wzory są pod komunikatem. Wpływ: ePUAP na skrytkę Ministerstwa Cyfryzacji `/MAiC/SkrytkaESP`, e-Doręczenia `AE:PL-45928-68514-CHARA-16`, e-mail `sekretariat.DSI@cyfra.gov.pl` z podpisem elektronicznym, albo papierowo na ul. Królewską 27 w Warszawie, z dopiskiem o Społecznej Radzie.

Kalendarz spotkań Komisji na listopad 2026, odczytany tego samego dnia, nie zawiera wpisanych posiedzeń. Ogłoszenie naboru nie mówi o pierwszej kontroli ani o pierwszej karze.

**Źródła:**

- [KRiBSI — nabór do Społecznej Rady](https://www.gov.pl/web/kribsi/rusza-nabor-do-spolecznej-rady-do-spraw-sztucznej-inteligencji)
- [KRiBSI — informacje bieżące, odczyt 11.11.2026](https://www.gov.pl/web/kribsi/informacje-biezace)
- [KRiBSI — pierwsze posiedzenie, data 28.10.2026](https://www.gov.pl/web/kribsi/pierwsze-posiedzenie-komisji-rozwoju-i-bezpieczenstwa-sztucznej-inteligencji)
- [KRiBSI — kalendarz spotkań, listopad 2026](https://www.gov.pl/web/kribsi/kalendarz-spotkan)
