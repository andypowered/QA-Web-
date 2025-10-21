# Fișe de Lucru - Analiza și Testarea Cerințelor

## Fișă de lucru 1 – Clasificarea cerințelor

### Scenariu analizat:
Aplicație web pentru bibliotecă online care trebuie să permită:
- Autentificare pe bază de e-mail și parolă
- Căutare după titlu, autor sau gen literar
- Împrumutarea online a cărților digitale cu termen de 14 zile
- Interfața disponibilă în 2 limbi (română și engleză)
- Timpul de încărcare al paginilor ≤ 2 secunde
- Respectarea GDPR pentru protecția datelor

### Clasificare cerințe:

| Cerință | Tip cerință | Justificare |
|---------|-------------|-------------|
| Autentificare pe bază de e-mail și parolă | Funcțională | Descrie o funcționalitate specifică a sistemului |
| Căutare după titlu, autor sau gen literar | Funcțională | Definește o funcție concretă a aplicației |
| Împrumutarea online a cărților digitale cu termen de 14 zile | Funcțională | Specifică o acțiune pe care sistemul trebuie să o poată executa |
| Interfața disponibilă în 2 limbi | Nefuncțională | Definește o caracteristică de calitate a interfeței |
| Timpul de încărcare ≤ 2 secunde | Nefuncțională | Specifică o constrângere de performanță |
| Respectarea GDPR | Business | Impusă de reglementări externe și afectează întregul business |

## Fișă de lucru 2 – Proprietățile cerințelor de calitate

### Analiza cerințelor:

1. **"Sistemul trebuie să fie rapid."**
   - **Problema**: Lipsește **verificabilitatea** și **claritatea**
   - **Sugestie de îmbunătățire**: "Sistemul trebuie să răspundă la cereri în mai puțin de 2 secunde în 95% din cazuri"

2. **"Utilizatorul trebuie să se autentifice."**
   - **Problema**: Lipsește **completitudinea**
   - **Sugestie de îmbunătățire**: "Utilizatorul trebuie să se autentifice folosind adresa de e-mail și o parolă de minim 8 caractere"

3. **"Sistemul trebuie să răspundă în mai puțin de 2 secunde la fiecare cerere de căutare."**
   - **Calitate**: Cerință bună - verificabilă, clară, completă

4. **"Sistemul trebuie să fie sigur și compatibil cu toate browserele."**
   - **Problema**: Lipsește **claritatea** și **testabilitatea**
   - **Sugestie de îmbunătățire**: "Sistemul trebuie să implementeze autentificare cu hash parolă și să fie compatibil cu Chrome 90+, Firefox 88+, Safari 14+"

5. **"Aplicația trebuie să permită exportul rapoartelor."**
   - **Problema**: Lipsește **completitudinea**
   - **Sugestie de îmbunătățire**: "Aplicația trebuie să permită exportul rapoartelor în formatele PDF și CSV"

## Fișă de lucru 3 – Testarea cerințelor prin review

### Cerință analizată:
**"Utilizatorul trebuie să poată rezerva un bilet la cinema."**

### Criterii de acceptare:

1. **CA1**: Utilizatorul autentificat poate selecta un film din lista de filme disponibile
   - **Scenariu de test**: 
     - Utilizatorul se autentifică
     - Accesează secțiunea "Filme"
     - Selectează un film disponibil
     - Verifică că poate accesa ecranul de rezervare

2. **CA2**: Sistemul permite selectarea datei, orei și numărului de locuri
   - **Scenariu de test**:
     - Utilizatorul selectează data spectacolului
     - Alege ora din opțiunile disponibile
     - Selectează numărul de locuri (1-10)
     - Verifică că poate vedea locurile disponibile pe hala sălii

3. **CA3**: Sistemul procesează rezervarea și generează un bilet electronic
   - **Scenariu de test**:
     - Utilizatorul confirmă rezervarea
     - Sistemul generează un bilet cu cod QR unic
     - Utilizatorul primește confirmarea pe e-mail
     - Biletul apare în istoricul rezervărilor

## Fișă de lucru 4 – Trasabilitate

### Tabel de trasabilitate:

| Cerință | Tip cerință | Caz de test corespunzător |
|---------|-------------|---------------------------|
| Utilizatorul se poate înregistra cu e-mail și parolă | Funcțională | **TC-REG-01**: Test înregistrare cu date valide<br>**TC-REG-02**: Test înregistrare cu e-mail duplicat<br>**TC-REG-03**: Test înregistrare cu parolă invalidă |
| Pagina se încarcă în < 2 secunde | Nefuncțională | **TC-PERF-01**: Test timp de încărcare pagină principală<br>**TC-PERF-02**: Test timp de răspuns la căutare<br>**TC-PERF-03**: Test încărcare pe diferite conexiuni |
| Sistemul va contribui la creșterea vânzărilor cu 20% | Business | **TC-BUS-01**: Analiză raport vânzări lunar<br>**TC-BUS-02**: Test satisfacție clienți<br>**TC-BUS-03**: Monitorizare metrici de utilizare |
| Interfața va fi accesibilă pentru persoane cu deficiențe de vedere | Utilizabilitate | **TC-ACC-01**: Test compatibilitate cu screen readers<br>**TC-ACC-02**: Test contrast culori<br>**TC-ACC-03**: Test navigare doar cu tastatura |

## Fișă de lucru 5 – Exercițiu de prototipare

### Wireframe - Pagină de "Înregistrare utilizator"

### figma link

### Specificații tehnice:

1. **Câmpuri obligatorii**:
   - Nume complet (text)
   - E-mail (validare format)
   - Parolă (minim 8 caractere)
   - Confirmare parolă (potrivire cu parola)

2. **Validări**:
   - Butonul "ÎnREGISTRARE" este activ doar când toate câmpurile sunt completate corect
   - Iconița ochi permite vizualizarea parolei
   - Mesaj de eroare sub fiecare câmp invalid

3. **Flux confirmare**:
   - După înregistrare, utilizatorul primește mesaj: "Verifică-ți e-mailul pentru a confirma contul"
   - E-mail de confirmare cu link de activare
   - Redirect către pagină de autentificare după confirmare

### Elemente de accesibilitate:
- Etichete clare pentru screen readers
- Contrast suficient între text și fundal
- Navigație posibilă doar cu tastatura
- Mesaje de eroare descriptive
