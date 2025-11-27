# Plan Phase 

## 1. Plan Phase Kya Hai?
Plan Phase me hum decide karte hain **kaam kaise hoga**. Spec batati hai "kya karna hai" aur Plan batata hai "kaise karna hai".

---

## 2. /sp.plan Kya Karta Hai?
- Spec ko analyze karta hai
- Architecture banata hai
- Phases banata hai (Research → Writing → Polish)
- Dependencies batata hai (pehle kya karna zaroori hai)
- Important decisions highlight karta hai
- Ek plan.md file banata hai

**Yaad rakho:**
- Clear spec → Clear plan
- Weak spec → Weak plan

---

## 3. Plan Me Kya Hona Chahiye?
- Overall architecture
- 3–5 clear phases
- Components (research, writing, quality check)
- Dependencies
- Important design decisions

---

## 4. ADRs (Architectural Decision Records)
ADRs un decisions ke liye bante hain jo:
- Long-term effect rakhte hain
- Jinki multiple choices hoti hain
- Jinko future me koi pooch sakta hai “Yeh kyun choose kiya?”

### ADR Me Kya Hota Hai?
- Decision
- Context
- Alternatives
- Rationale (kyun choose kiya)
- Consequences (faide & nuksan)

---

## 5. /sp.adr Kya Karta Hai?
- Plan ko read karta hai
- Important decisions find karta hai
- ADR files banata hai

---

## 6. Example Simple ADR
**Decision:** Research writing ke sath-sath hogi (concurrent)
- **Alternative:** Pehle research phir writing
- **Reason:** Concurrent se research focused hoti hai
- **Consequence:** + Fast work, - Kabhi beech me extra research

---

## 7. Complete Workflow
- **Spec:** Kya karna hai
- **Plan:** Kaise karna hai
- **Tasks:** Step-by-step kaam

---

## 8. Useful Commands
- `/sp.plan` → Plan banane ke liye
- `/sp.adr` → ADR banane ke liye

