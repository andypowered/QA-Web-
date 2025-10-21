# Întrebări și Răspunsuri - Testarea Software

## Obiectivele Testării

### Întrebarea 1:
**Care sunt cele trei obiective principale ale testării software?**

**Răspuns:**
1. **Identificarea defectelor** - Descoperirea erorilor, defectelor și problemelor în software
2. **Creșterea încrederii în calitate** - Asigurarea că software-ul îndeplinește cerințele așteptate
3. **Furnizarea de informații pentru decizii** - Oferirea de date despre calitatea software-ului pentru managementul proiectului

### Întrebarea 2:
**De ce este important să identificăm defectele cât mai devreme în ciclul de dezvoltare?**

**Răspuns:**
Costul remedierii defectelor crește exponențial pe măsură ce avansăm în fazele proiectului. Un defect identificat în faza de specificații costă de 10-100 de ori mai puțin decât același defect descoperit în producție sau după livrare.

### Întrebarea 3:
**Cum contribuie testarea la reducerea riscurilor de business?**

**Răspuns:**
Testarea reduce riscurile de business prin:
- Prevenirea pierderilor financiare cauzate de defecțiuni
- Protejarea reputației companiei
- Asigurarea conformității cu reglementările
- Prevenirea întreruperii operațiunilor clienților

## Principiile Testării

### Întrebarea 4:
**Care sunt cele 7 principii fundamentale ale testării conform ISTQB?**

**Răspuns:**
1. Testarea arată prezența defectelor
2. Testarea exhaustivă este imposibilă
3. Testarea timpurie economisește timp și bani
4. Defectele tind să se aglomereze
5. Paradoxul pesticidului
6. Testarea este dependentă de context
7. Absența erorilor este o iluzie

### Întrebarea 5:
**Explică principiul "Testarea arată prezența defectelor"**

**Răspuns:**
Acest principiu afirmă că testarea poate demonstra existența defectelor, dar nu poate dovedi absența lor. Chiar dacă niciun defect nu este găsit, acest lucru nu dovedește că software-ul este perfect, ci doar că defectele nu au fost descoperite cu tehnicile de testare aplicate.

### Întrebarea 6:
**Ce înseamnă "paradoxul pesticidului" în testare?**

**Răspuns:**
Dacă aceleași teste sunt rulate repetat, acestea vor deveni progresiv mai puțin eficiente în găsirea de defecte noi. La fel cum insectele devin imune la pesticide, software-ul "devine imun" la aceleași teste. Soluția este revizuirea și actualizarea periodică a cazurilor de test.

## Axiomele Testării

### Întrebarea 7:
**Care sunt principalele axiome ale testării și ce semnificație au?**

**Răspuns:**
Principalele axiome includ:
- **Axioma observației**: Rezultatele testării depind de condițiile și contextul în care sunt efectuate
- **Axioma exhaustivității**: Testarea completă a tuturor combinațiilor este imposibilă
- **Axioma relevanței**: Testele trebuie să se concentreze pe aspectele critice pentru utilizator

### Întrebarea 8:
**Cum afectează axioma observației procesul de testare?**

**Răspuns:**
Axioma observației afirmă că actul de a testa în sine poate modifica comportamentul sistemului. Acest lucru înseamnă că:
- Testarea în medii diferite poate produce rezultate diferite
- Monitorizarea performanței poate afecta performanța
- Testele trebuie proiectate pentru a minimiza impactul asupra sistemului testat

### Întrebarea 9:
**De ce este importantă axioma relevanței în alocarea resurselor de testare?**

**Răspuns:**
Axioma relevanței ne îndrumă să alocăm resurse pentru testarea funcționalităților care au cel mai mare impact asupra utilizatorilor și business-ului. Aceasta asigură că:
- Testăm mai intensiv zonele critice
- Optimizăm bugetul de testare
- Ne concentrăm pe riscurile cele mai mari
- Livrăm valoare maximă prin efortul de testare
