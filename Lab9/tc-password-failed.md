### **Test Case: Login cu parolă greșită - Afișare mesaj eroare**

- **ID**: TC-LOGIN-015  
- **Priority**: High  
- **Status**: ✅ PASSED

#### 🧪 **Test Steps**:  
1. Introdu email valid: `user@example.com`  
2. Introdu parolă greșită: `WrongPassword`  
3. Click 'Login'

#### ✅ **Expected Results**:  
- Mesaj eroare: "Warning: No match for E-Mail Address and/or Password."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### ✅ **Actual Results**:  
- Apare mesaj de eroare: "Warning: No match for E-Mail Address and/or Password."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### 🐛 **Bug Identificat**:  
- **Severitate**: None  
- **Descriere**: Testul s-a comportat conform așteptărilor, fără erori.  
- **Steps to reproduce**: Email valid + parolă greșită  
- **Environment**: Browser Chrome, versiune 115.0, Windows 10

#### 📎 **Evidence**:  
- ![Screenshot - login page without error message](https://github.com/andypowered/QA-Web-/blob/main/Lab9/failedpassword.png)

---

### **Test Case: Login cu email invalid - Afișare mesaj eroare**

- **ID**: TC-LOGIN-016  
- **Priority**: Medium  
- **Status**: ✅ PASSED

#### 🧪 **Test Steps**:  
1. Introdu email invalid: `invalid-email`  
2. Introdu parolă corectă: `CorrectPassword123`  
3. Click 'Login'

#### ✅ **Expected Results**:  
- Mesaj eroare: "Warning: No match for E-Mail Address and/or Password."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### ✅ **Actual Results**:  
- Apare mesaj de eroare: "Warning: No match for E-Mail Address and/or Password."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### 🐛 **Bug Identificat**:  
- **Severitate**: None  
- **Descriere**: Comportament conform așteptărilor, nu sunt erori.

#### 📎 **Evidence**:  
- ![Screenshot - login page without error message](https://github.com/andypowered/QA-Web-/blob/main/Lab9/failedpassword.png)

---

### **Test Case: Login cu parolă goală - Afișare mesaj eroare**

- **ID**: TC-LOGIN-017  
- **Priority**: High  
- **Status**: ✅ PASSED

#### 🧪 **Test Steps**:  
1. Introdu email valid: `user@example.com`  
2. Lasă câmpul pentru parolă gol  
3. Click 'Login'

#### ✅ **Expected Results**:  
- Mesaj eroare: "Warning: Password must be between 4 and 20 characters!"  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### ✅ **Actual Results**:  
- Apare mesaj de eroare: "Warning: Password must be between 4 and 20 characters!"  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### 🐛 **Bug Identificat**:  
- **Severitate**: None  
- **Descriere**: Testul s-a comportat conform așteptărilor, fără erori.

#### 📎 **Evidence**:  
- ![Screenshot - login page without error message](https://github.com/andypowered/QA-Web-/blob/main/Lab9/failedpassword.png)

---

### **Test Case: Login cu cont inactiv - Afișare mesaj eroare**

- **ID**: TC-LOGIN-018  
- **Priority**: Medium  
- **Status**: ✅ PASSED

#### 🧪 **Test Steps**:  
1. Introdu email valid pentru cont inactiv: `inactive@example.com`  
2. Introdu parolă corectă: `ActivePassword123`  
3. Click 'Login'

#### ✅ **Expected Results**:  
- Mesaj eroare: "Warning: Your account is not currently active."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### ✅ **Actual Results**:  
- Apare mesaj de eroare: "Warning: Your account is not currently active."  
- Utilizatorul rămâne pe pagina de login  
- Nu se creează sesiune (corect)

#### 🐛 **Bug Identificat**:  
- **Severitate**: None  
- **Descriere**: Comportament corect conform specificațiilor.

#### 📎 **Evidence**:  
- ![Screenshot - login page without error message](https://github.com/andypowered/QA-Web-/blob/main/Lab9/failedpassword.png)
