# Modelul în V în Testarea Software

## Principiul de Lucru (ideea, informația de bază necesară pentru crearea scenariilor de testare, scopul)
Modelul în V reprezintă o extensie a modelului cascadă, unde fiecărei etape de dezvoltare îi corespunde o etapă paralelă de testare. Ideea de bază este că testarea se planifică și se proiectează în paralel cu dezvoltarea, iar fiecare nivel de testare se aliniază cu un anumit nivel de specificații și proiectare. Scopul este de a identifica defectele cât mai devreme în ciclul de viață al dezvoltării software, reducând costul remedierii și asigurând calitatea la fiecare etapă.

## Utilizarea (de către cine poate fi utilizată)
- **Echipe de dezvoltare software** – pentru a organiza fazele de testare în paralel cu cele de dezvoltare.
- **Ingineri QA și testeri** – pentru a planifica și executa testarea pe niveluri definite.
- **Manageri de proiect** – pentru a vizualiza și coordona activitățile de dezvoltare și testare.
- **Organizații cu procese structurate și proiecte de dimensiuni medii spre mari** – în special în domenii reglementate (ex: medical, automotive, financiar).

## Avantaje
- **Testare timpurie** – testarea este planificată de la început, ceea ce permite identificarea defectelor în faze incipiente.
- **Structură clară** – fiecare etapă de testare are o etapă corespunzătoare de dezvoltare.
- **Calitate crescută** – asigură că cerințele sunt validate la fiecare nivel.
- **Documentație completă** – necesită documentare detaliată atât pentru dezvoltare, cât și pentru testare.
- **Potrivit pentru proiecte cu cerințe clare și stabile** – unde schimbările sunt minime pe parcursul dezvoltării.

## Dezavantaje
- **Rigiditate** – dificil de adaptat la schimbările frecvente ale cerințelor.
- **Cost ridicat și timp lung** – necesită resurse și timp pentru documentare și planificare detaliată.
- **Testarea începe târziu** – deși este planificată devreme, executarea testelor se face după finalizarea codării.
- **Neadaptat la metodologii agile** – nu se potrivește bine cu cicluri de dezvoltare scurte și iterative.
- **Dependență de documentație** – dacă specificațiile sunt incomplete sau incorecte, întregul proces este afectat.
