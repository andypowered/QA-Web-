## Test Case: Login cu parolă greșită - Afișare mesaj eroare

**ID:** TC-LOGIN-015
**Priority:** High
**Status:** ❌ FAILED

### 🧪 Test Steps
1. Introdu email valid: `user@example.com`
2. Introdu parolă greșită: `WrongPassword`
3. Click 'Login'

### ✅ Expected Results
- Mesaj eroare: "Warning: No match for E-Mail Address and/or Password."

###  Actual Results
- ✅ Apare mesaj de eroare [ No match for E-Mail and/or Password.]
- ✅ Utilizatorul rămâne pe pagina de login 
- ✅ Nu se creează sesiune (corect)

### 🐛 Bug Identificat
**Severitate:** none
**Descriere:** -
**Steps to reproduce:** -
**Environment:** -

### 📎 Evidence
- [Screenshot - login page without error message](https://github.com/andypowered/QA-Web-/blob/main/Lab9/failedpassword.png)
