# Fișă de laborator – Testarea aplicațiilor web

## Scenariu
Aplicație web e-commerce cu funcționalități:
- Înregistrare utilizatori
- Căutare produse
- Adăugare produse în coș
- Finalizare comandă online
- Mediu: server local + MySQL

## Sarcina 1 – Obiectivele testării

### 5 Obiective concrete de testare:

1. **Obiectiv funcțional** - Verificarea fluxului complet de cumpărare
   - Testarea procesului de la adăugare în coș până la confirmarea comenzii

2. **Obiectiv securitate** - Protejarea datelor sensibile
   - Asigurarea că datele de plată și personale sunt criptate și protejate

3. **Obiectiv performanță** - Gestionarea traficului crescut
   - Testarea aplicației cu 1000+ utilizatori simultan în perioade de promoții

4. **Obiectiv compatibilitate** - Funcționarea cross-browser
   - Verificarea că aplicația funcționează corect pe Chrome, Firefox, Safari, Edge

5. **Obiectiv utilizabilitate** - Experiență utilizator intuitivă
   - Asigurarea că interfața este ușor de utilizat și navigarea este intuitivă

## Sarcina 2 – Principiile testării

### Asociere principii cu scenariu e-commerce:

1. **Testarea arată prezența defectelor, nu absența lor**
   - **Situație**: Toate testele de plasare comandă trec, dar un client reportează că nu primește email de confirmare pentru anumite produse
   - **Explicație**: Chiar dacă testele noastre nu au găsit defecte, acest lucru nu garantează că aplicația este perfectă

2. **Testarea completă este imposibilă**
   - **Situație**: Nu putem testa toate combinațiile posibile de produse, cantități, promoții și metode de plată
   - **Explicație**: Există prea multe variabile pentru a testa exhaustiv fiecare scenariu posibil

3. **Defectele se grupează**
   - **Situație**: Majoritatea problemelor sunt descoperite în modulul de procesare plăți și calcul taxe
   - **Explicație**: Zonele complexe sau modificate frecvent tind să conțină mai multe defecte

4. **Paradoxul pesticidei**
   - **Situație**: Rularea aceleiași suite de teste lună de lună nu mai găsește defecte noi
   - **Explicație**: Testele existente devin "obișnuite" cu codul și nu mai detectează defecte noi

## Sarcina 3 – Axiomele testării

### Explicații în contextul aplicației:

1. **„Testarea trebuie planificată”**
   - **Riscuri fără planificare**:
     - Depășirea bugetului și a termenelor
     - Acoperire incompletă a funcționalităților critice
     - Imposibilitatea de a reproduce defectele
     - Eșec în identificarea problemelor de securitate

2. **„Testarea nu poate dovedi că sistemul este fără defecte”**
   - **Exemplu**: Toate testele de înregistrare trec, dar utilizatorii din Franța nu se pot înregistra din cauza formatului de telefon francez neacceptat
   - **Justificare**: Testele noastre nu au acoperit toate formatele internaționale de telefon

3. **„Testarea este dependentă de context”**
   - **Diferențe e-commerce vs forum educațional**:
     - **E-commerce**: Testare intensivă a securității plăților, performanță la vârfuri de trafic
     - **Forum**: Testare focusată pe gestionarea conținutului, căutare avansată, managementul utilizatorilor

## Sarcina 4 – Mini-caz practic

### Analiză eroare 500 la introducerea "DROP TABLE":

1. **Principiu și axiomă aplicabile**:
   - **Principiu**: Testarea arată prezența defectelor
   - **Axiomă**: Testarea trebuie să acopere scenarii de securitate

2. **Metode de testare suplimentară**:
   - **Testare SQL Injection**: Verificarea tuturor câmpurilor de input pentru vulnerabilități
   - **Validare input**: Implementarea filtrării și sanitizării datelor pe server-side

## Sarcina 5 – Crearea planului de testare

### Mini-plan de testare e-commerce:

**Obiectivele testării**:
- Asigurarea funcționalității corecte a tuturor modulelor
- Verificarea securității datelor și a tranzacțiilor
- Confirmarea performanței under load

**Tipuri de teste**:
- **Funcționale**: Flux comenzi, gestionare coș, căutare
- **Performanță**: Testare load cu 500+ utilizatori simultan
- **Securitate**: Testare SQL injection, XSS, protecție date
- **Compatibilitate**: Cross-browser (Chrome, Firefox, Safari, Edge)

**Criterii de intrare**:
- Toate funcționalitățile sunt implementate
- Mediu de testare configurat
- Date de test pregătite

**Criterii de ieșire**:
- Toate testele critice trecute
- Defectele critice și majore rezolvate
- Raport de testare finalizat și aprobat

## Sarcina 6 – Teste pozitive și negative

### Modulul "Adăugare produs în coș":

**Teste pozitive**:
1. Adăugare produs existent în stoc cu cantitate validă (ex: 2 bucăți)
2. Adăugare multiple produse diferite în coș

**Teste negative**:
1. Adăugare produs cu cantitate 0 sau negativă
2. Adăugare produs care nu mai este în stoc

## Sarcina 7 – Clasificarea testelor

### Modulul "Căutare produse":

**Teste pozitive** (sistemul ar trebui să funcționeze corect):
1. ✅ Căutarea după „Laptop Dell”
4. ✅ Căutarea după „Mouse wireless”

**Teste negative** (sistemul ar trebui să respingă sau să afișeze eroare):
2. ❌ Căutarea după un număr foarte mare: „999999999999”
3. ❌ Căutarea după șir gol („”)

## Sarcina 8 – Analiza riscurilor

### 3 Riscuri majore și strategii de testare:

1. **Risc funcțional - Procesare plăți**
   - **Stategie**: Testare end-to-end a tuturor metodelor de plată
   - **Acțiuni**: Testare cu carduri valide/invalide, verificare tranzacții

2. **Risc securitate - Protecția datelor**
   - **Strategie**: Testare de securitate intensivă
   - **Acțiuni**: Testare SQL injection, XSS, verificare criptare date sensibile

3. **Risc performanță - Trafic crescut**
   - **Strategie**: Testare de load și stress
   - **Acțiuni**: Simulare trafic intens, verificare timpi de răspuns, testare scalare
