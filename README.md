**SMT AI Data Analytics \[MVP\]**

\[UI Mockup\] 

* (./data/mockup\_smt\_ai\_data\_analytics.jpg)

Lekki, asynchroniczny Dashboard produkcyjny wspierany przez sztuczną inteligencję (Gemini 3.5 Flash), optymalizujący wykrywanie wąskich gardeł na liniach montażu powierzchniowego (SMT).

**O projekcie**

SMT AI Data Analytics to rozwiązanie stworzone z myślą o dziale inżynierii produkcji. Projekt ten powstał w połowie 2026 roku z misją zautomatyzowania i radykalnego skrócenia czasu analizy surowych logów z maszyn SMT – z kilkunastu godzin do zaledwie kilku sekund. 

Dzięki bezpośredniemu przetwarzaniu tysięcy rekordów w przeglądarce i bezpiecznej integracji z LLM na brzegu sieci (Edge), system oferuje wgląd w kluczowe wskaźniki (OEE, koszty złomowania, defekty) w czasie niemal rzeczywistym.

**Kluczowe Funkcjonalności**

* **Live View (Polling 10s):** Automatyczne wczytywanie i odświeżanie logów z lokalnego potoku produkcyjnego, odzwierciedlające fizyczny przepływ płytki PCBA (SPI, PnP, Reflow\_Oven, AOI).  
* **Client-Side Processing:** Pobieranie plików \`.csv\`, ich parsowanie i rozbudowana agregacja matematyczna odbywają się bezpośrednio w przeglądarce użytkownika, całkowicie odciążając serwer.  
* **Edge AI Integration (Raportowanie):** Generowanie inżynieryjnych wniosków "na żądanie" z użyciem wdrożonego systemu RAG. Model AI podsumowuje anomalie i sugeruje akcje korygujące.  
* **Zero-Trust Security:** Całkowita separacja kluczy API. Logika integracyjna z modelem AI została przeniesiona do architektury bez serwerowej (Cloudflare Workers).

**Technologia i Architektura**

Aplikacja w fazie MVP działa w modelu bezstanowym (brak bazy SQL), polegając na odczycie danych w locie, co gwarantuje błyskawiczne wdrożenie jako \*Proof of Concept\*.

* **Frontend:** HTML5, CSS3, JavaScript.  
* **Logika i Przetwarzanie:** Vanilla JavaScript.  
* **Wizualizacja**: Nowoczesne biblioteki Chartingowe (przemysłowe wskaźniki Gauge, Pareto)  
* **Backend / API Relay:** Cloudflare Workers (Serverless)  
* **LLM**: Google Gemini 3.5 Flash (optymalizacja opóźnień i tokenizacji)
