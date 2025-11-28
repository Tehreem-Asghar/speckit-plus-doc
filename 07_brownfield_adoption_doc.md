# Brownfield Adoption (Roman Urdu Document)

## Brownfield Adoption — Simple Roman Urdu Guide

### Greenfield vs Brownfield

**Greenfield Project:**
- Naya project hota hai.
- Koi purana code ya rules nahi.
- `specifyplus init` seedha kaam karta hai.

**Brownfield Project:**
- Purana project jahan pehle se code, CLAUDE.md, commands, aur team ki settings hoti hain.
- Yahan `specifyplus init --here` chalane se kuch files overwrite ho sakti hain.

---

## Kya Overwrite Hota Hai?

### ❌ Overwrite Hone Wali Files:
- **CLAUDE.md** (purana content delete ho jata hai)
- Purana `.specify/` folder (agar ho to reset ho jata hai)

### ✅ Safe Files (Bilkul Save Rehti Hain):
- `.claude/commands/` ke tamam custom commands
- `src/`, `lib/` ka code
- Tests, config files, docs
- Git history

**Sabse Bara Risk:** CLAUDE.md ka purana team knowledge **lost** ho sakta hai.

---

## Brownfield Scenarios

### 1. Blog / Website Project
- CLAUDE.md replace hoga
- Code safe hoga
- Commands safe

### 2. API Project
- Coding standards wala CLAUDE.md overwrite
- `.specify` create hoga
- Code & tests safe

### 3. Docs Project
- Documentation rules overwrite honge
- Commands safe
- Docs safe

---

## Safe Brownfield Workflow (Backup + Test)

### **STEP 1: New branch banao:**
```
git checkout -b experiment/specifykit
```

### **STEP 2: Backup files banao:**
```
cp CLAUDE.md CLAUDE.md.backup
cp -r .claude .claude.backup
```

### **STEP 3: Backup commit karo:**
```
git add -A
git commit -m "backup: preserve team knowledge"
```

### **STEP 4: Ab safe ho → command chalao:**
```
specifyplus init --here
```

---

## Changes Check Karna
```
git diff --name-only
```
Isse pata chalega ke kaun si files change hui.

Backup files me purana content safe hai.

---

## Purane Content Ko Merge Karna

### **1. constitution.md ke liye:**
- Coding standards
- Architecture rules
- Naming conventions

### **2. CLAUDE.md ke liye:**
- AI collaboration patterns
- Team ka workflow style

---

## Merge Example

### constitution.md me add karna:
```
echo "## Project Development Standards
[purana content]" >> .specify/memory/constitution.md
```

### CLAUDE.md me append karna:
```
echo "## Team Collaboration Patterns
[purana content]" >> CLAUDE.md
```

---

## Self Check — Tumhara Content Kahan Jayega?

### **constitution.md:**
- Development standards
- Architecture decisions

### **CLAUDE.md:**
- AI collaboration rules

---

## Recommended Prompts (AI ke liye)

### Prompt 1
"Meray project me pehle se CLAUDE.md hai. Mujhe Spec-Kit Plus adopt karna hai bina data lose kiye. Safe strategy batao."

### Prompt 2
"Ye mera CLAUDE.md ka content hai: [paste content]. Merge plan bana do."

### Prompt 3
"Kaunsa content constitution me aur kaunsa CLAUDE.md me jayega? Mere project type ke example ke sath batao."

---

## Safety Note
**Brownfield me hamesha teen backup rakho:**
1. Git branch
2. Manual file copy
3. Git commit backup

Isse 100% data loss se protection milti hai.

