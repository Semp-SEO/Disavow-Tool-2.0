Disavow Tools — Sempai
Wewnętrzne narzędzie SEO do weryfikacji i generowania plików disavow.
Działa w całości po stronie przeglądarki (no-backend) — wystarczy otworzyć index.html.

Funkcje
🔍 Zakładka: Analiza DNS
Wczytuje plik disavow.txt lub listę domen/podstron (drag & drop lub wklejenie)
Weryfikuje każdy wpis przez DNS over HTTPS (Cloudflare lub Google)
Dla podstron dodatkowo wykonuje request HTTP
Zwraca statusy: AKTYWNA / NIEAKTYWNA / NIEOKREŚLONA
Wielowątkowe sprawdzanie (konfigurowalne 1–20 wątków)
Eksport wyników do CSV
📄 Zakładka: Generator Disavow
Blok A — automatycznie pobiera aktywne wpisy z analizy DNS
Blok B — ręczne dopisanie dodatkowych domen i podstron
Blok C — import z Ahrefs CSV (wyciąga domeny oznaczone Is spam = TRUE)
Generuje plik disavow.txt zgodny z wytycznymi Google
Podgląd pliku na żywo przed pobraniem
Kopiowanie do schowka jednym kliknięciem
⚙️ Logika generatora
Priorytet domeny nad podstroną — jeśli dana domena jest już zablokowana jako domain:xyz.com, generator automatycznie pomija wszelkie podstrony tej domeny z pozostałych bloków (nie ma sensu dublować blokady)
Deduplikacja wpisów między wszystkimi blokami
Opcjonalne komentarze na początku i końcu pliku
Użycie
Narzędzie nie wymaga instalacji ani serwera.
Otwórz plik index.html w przeglądarce i gotowe.

Zalecane przeglądarki: Chrome 90+, Firefox 90+, Edge 90+

Struktura pliku disavow
Generator tworzy plik zgodny z wytycznymi Google Search Console:

# Komentarz opcjonalny

domain:spammydomain.com
domain:linkfarm.net

https://bad-site.ru/konkretna-podstrona
Technologie
Vanilla JavaScript (no dependencies)
DNS over HTTPS — Cloudflare (cloudflare-dns.com) / Google (dns.google)
Google Fonts (Inter)
Autor
Sempai — Let us perform!
