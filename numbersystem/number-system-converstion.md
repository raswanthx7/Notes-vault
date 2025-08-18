# Number System Conversions (For Cloud, Linux & Networking)

Understanding number systems is essential for working with Linux, Cloud Computing, and Networking.  
This guide covers the three most important conversions you need to master.

---

## 1. Decimal ↔ Binary

**Decimal (Base 10):** Digits 0–9  
**Binary (Base 2):** Digits 0–1  

### Conversion: Decimal → Binary
- Repeatedly divide the decimal number by 2.  
- Record the remainders.  
- Read the remainders **from bottom to top**.

**Example:**

We convert **25 (decimal)** to binary using repeated division by 2:

| Step | Division             | Quotient | Remainder |
|------|----------------------|----------|------------|
| 1    | 25 ÷ 2               | 12       | 1          |
| 2    | 12 ÷ 2               | 6        | 0          |
| 3    | 6 ÷ 2                | 3        | 0          |
| 4    | 3 ÷ 2                | 1        | 1          |
| 5    | 1 ÷ 2                | 0        | 1          |

Now, read the remainders **from bottom to top**:

**25 (decimal) = 11001 (binary)**

### Conversion: Binary → Decimal
- Multiply each binary digit by 2^position (from right, starting at 0).  
- Add the results.

**Example:**
```text  
Binary: 11001
= (1 × 2^4) + (1 × 2^3) + (0 × 2^2) + (0 × 2^1) + (1 × 2^0)
= 16 + 8 + 0 + 0 + 1
= 25
```

---

## 2. Binary ↔ Octal

**Octal (Base 8):** Digits 0–7  

### Conversion: Binary → Octal
- Group binary digits in **sets of 3** (from right).  
- Convert each group into octal.

**Example:**
```text  
Binary: 111000101
Group: (111) (000) (101)
Octal: 7 0 5 → 705
```

### Conversion: Octal → Binary
- Convert each octal digit into **3-bit binary**.

**Example:** 
```text 
Octal: 705
7 → 111
0 → 000
5 → 101
Binary = 111000101
```

---

## 3. Binary ↔ Hexadecimal

**Hexadecimal (Base 16):** Digits 0–9 and A–F  

### Conversion: Binary → Hexadecimal
- Group binary digits in **sets of 4** (from right).  
- Convert each group into hex.

**Example:** 
```text 
Binary: 111000101
Group: (1110) (0010) (1) → pad left → (0001)
= (1110) (0010) (0001)
Hex: E21
``` 

### Conversion: Hexadecimal → Binary
- Convert each hex digit into **4-bit binary**.

**Example:**  

```text
Hex: E21
E → 1110
2 → 0010
1 → 0001
Binary = 11100010001
```

---

##  Key Use Cases
- **Decimal ↔ Binary:** Basic computer & network addressing.  
- **Binary ↔ Octal:** Linux file permissions (e.g., `chmod 755`).  
- **Binary ↔ Hexadecimal:** IP addressing, MAC addresses, memory representation.  

---
