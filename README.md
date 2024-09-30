# lab-2
### Proiectul: SnakeGame

**Descrierea proiectului**:  
SnakeGame este o implementare clasică a jocului retro "Snake". Jucătorul controlează un șarpe care se mișcă pe tablă, având scopul de a mânca mere pentru a crește în lungime.

**Regulile jocului**:  
Jocul implică controlarea unui șarpe într-un spațiu limitat. Jucătorul trebuie să mănânce mere care apar aleatoriu pe tablă. Fiecare măr mâncat face șarpele să crească, iar provocarea constă în a evita coliziunile cu pereții sau cu propriul corp. Jocul se încheie când jucătorul greșește.

### Funcția fișierelor

**point.hpp**:
- **Scop**: Definește structura **`Point`**, care reprezintă un punct în coordonate 2D (x, y). Aceasta este folosită pentru a gestiona pozițiile șarpelui, a merelor și a altor obiecte de pe tablă.
- **Structura Point**: Conține două variabile, **`x`** și **`y`**, care indică poziția pe tablă.
- **Constructor implicit**: Inițializează coordonatele la 0.
- **Constructor cu parametri**: Permite setarea coordonatelor x și y la valori specifice.

**snake.hpp**:
- **Scop**: Reprezintă comportamentul șarpelui și stochează segmentele acestuia.
- **Clasa Snake**: Gestionează mișcarea și creșterea șarpelui.
- **Array segments[100]**: Stochează până la 100 de segmente, fiecare reprezentat printr-un **`Point`**.
- **Variabila length**: Reține lungimea activă a șarpelui.
- **Constructorul**: Inițializează șarpele cu un segment la o poziție fixă (ex. (10, 10)).
- **Funcția Move(Point direction)**: Actualizează poziția șarpelui în funcție de direcția dată.
- **Funcția Grow**: Adaugă un segment la coadă pentru a crește lungimea șarpelui.
- **Funcția GetHeadPosition**: Returnează poziția capului șarpelui.

**board.hpp**:
- **Scop**: Definește tabla de joc, inclusiv dimensiunile acesteia și gestionarea desenării elementelor.
- **Clasa Board**: Reprezintă tabla pe care se desfășoară acțiunea.
- **Variabile width și height**: Specifică dimensiunile tablei.
- **Constructorul**: Setează dimensiunile tablei (de exemplu, 20x20).
- **Funcțiile GetWidth și GetHeight**: Returnează dimensiunile tablei, utile pentru a menține șarpele în limitele acesteia.

**Makefile**:
- **CXX**: Specifică compilatorul (g++).
- **CXXFLAGS**: Opțiuni de compilare, precum `-Wall` pentru avertismente și `-std=c++17` pentru standardul C++17.
- **EXEC**: Numele executabilului generat.
- **SRC**: Listează fișierele sursă `.cpp` care trebuie compilate.
- **OBJ**: Reprezintă fișierele obiect generate.
- **all**: Regula principală pentru construirea executabilului.
- **clean**: Regula pentru ștergerea fișierelor obiect și a executabilului.

**board.cpp**:
- **Constructorul Board(int w, int h)**: Setează dimensiunile tablei de joc.
- **Funcția GetWidth**: Returnează lățimea tablei.
- **Funcția GetHeight**: Returnează înălțimea tablei, asigurându-se că șarpele nu depășește limitele.

**snake.cpp**:
- **Constructorul Snake()**: Inițializează șarpele la poziția de start (10, 10) și lungimea sa.
- **Funcția Move()**: Mută șarpele conform direcției specificate.
- **Funcția Grow()**: Crește lungimea șarpelui prin adăugarea unui segment.
- **Funcția GetHeadPosition()**: Returnează poziția capului șarpelui.

**point.cpp**:
- **Scop**: Nu necesită cod suplimentar, deoarece structura **`Point`** a fost definită în fișierul header, iar constructorii sunt generați automat de compilator.
- **Structura Point**: Conține membri pentru coordonatele unui punct pe tablă (x și y).
