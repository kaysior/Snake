# Snake Game Project

Jest to projekt znanej już wszystkim w różnych wydaniach popularnej gry Snake. 

**Inicjalizacja:** Po uruchomieniu programu, główne okno gry zostaje utworzone jako instancja klasy Form1. W oknie tym znajduje się obszar rysowania (picCanvas), na którym odbywa się rozgrywka, przycisk "Start" (startButton) do rozpoczęcia nowej gry oraz przycisk "Save" (saveButton) do zapisania wyniku gry.

**Sterowanie:** Gracz steruje wężem za pomocą strzałek na klawiaturze. Funkcje KeyIsDown i KeyIsUp obsługują naciśnięcia i zwolnienia klawiszy, ustawiając odpowiednie flagi kierunków (goLeft, goRight, goUp, goDown). Sterowanie jest ograniczone w ten sposób, że wąż nie może zawracać, czyli nie może poruszać się w przeciwnym kierunku do swojego obecnego kierunku poruszania się.

**Rozpoczęcie gry:** Po naciśnięciu przycisku "Start", funkcja RestartGame() przygotowuje nową rozgrywkę. Ustawia ona niezbędne parametry, takie jak szerokość i wysokość planszy, oraz resetuje stan węża, jedzenia i punktacji.

**Logika gry:** Główna pętla gry znajduje się w zdarzeniu GameTimerEvent, które jest wyzwalane cyklicznie przez timer. W każdej iteracji, wąż przesuwa się o jedną pozycję w zależności od aktualnego kierunku.

**Kolizje:** Podczas poruszania się wąż sprawdza kolizje z granicami planszy oraz ze swoim ciałem. Jeśli wąż zderzy się z granicami planszy lub z samym sobą, gra się kończy, a funkcja GameOver() jest wywoływana.

**Jedzenie:** Na planszy losowo pojawia się jedzenie, które wąż może zjeść. Gdy wąż zje jedzenie, jego długość się zwiększa, a gracz zdobywa punkty. Funkcja EatFood() obsługuje zdarzenie zjedzenia jedzenia przez węża.

**Punkty:** Za każde zjedzenie jedzenia gracz zdobywa punkty, które są wyświetlane na ekranie. Aktualna liczba punktów jest przechowywana w zmiennej score.

**Zapis wyniku:** Gracz ma możliwość zapisania swojego wyniku poprzez naciśnięcie przycisku "Save". Po kliknięciu tego przycisku, plansza gry wraz z informacjami o uzyskanych punktach i najlepszym wyniku jest zapisywana jako obraz w formacie JPG.

**Koniec gry:** Gra kończy się, gdy wąż zderzy się z granicami planszy lub z samym sobą. Po zakończeniu gry, funkcja GameOver() zatrzymuje timer gry, umożliwiając graczowi rozpoczęcie nowej gry od nowa.

**Najlepszy wynik:** Najwyższy uzyskany wynik jest przechowywany i wyświetlany na ekranie. Jeśli gracz uzyska nowy rekord, zostaje on wyświetlony na ekranie i zaktualizowany.
