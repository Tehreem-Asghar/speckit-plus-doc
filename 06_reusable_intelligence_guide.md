# Reusable Intelligence Guide

## 1. Introduction

Tum ne SDD workflow complete kar liya hai (Lessons 01-08):

**Constitution ➞ Specify ➞ Clarify ➞ Plan ➞ Tasks ➞ Implement**

Tum ne:
- Specifications likhi
- Requirements refine ki
- Architecture plan ki
- AI ke saath implementation execute ki

Lekin AI-native developers ka fark AI-assisted developers se ye hai ke:
**Wo acchi sessions ko reusable skills mein tabdeel karte hain.**

Skills ke zariye, tum apni AI ko specific workflows, tools aur processes sikha sakte ho. Skill create karna matlab AI ko ek playbook dena jo wo reference kare jab bhi tumhe is type ka help chahiye—jaise research sections likhna, sources validate karna, ya outlines refine karna.

---

## 2. Kab Skill Create Karni Chahiye

Har workflow skill banane layak nahi hota. Skill create karo jab:

- Tum dobara ye kaam karoge? (3+ projects)
- Multiple decisions involve ho? (5+ decision points)
- Consistent high quality chahiye?

Agar 2+ answers YES ➞ Skill create karo.

**Example: Research Paper Project**

| Pattern                     | Frequency        | Complexity     | Value          | Create Skill? |
|------------------------------|----------------|---------------|----------------|---------------|
| Writing quality sections      | ✅ Har paper     | ✅ 6+ decisions | ✅ Consistency  | YES           |
| Validating research sources   | ✅ Har source    | ✅ 5+ decisions | ✅ Accuracy     | YES           |
| Refining outlines             | ✅ Har draft     | ✅ 5+ decisions | ✅ Structure    | YES           |
| Formatting citations          | ✅ Har source    | ❌ 2-3 decisions | ❌ Tool handles | NO            |
| Spell checking                | ✅ Har draft     | ❌ 1 decision   | ❌ Automated    | NO            |

---

## 3. Part A: Creating a Skill Through Conversation

Skill create karna AI ke saath conversation ka process hai:
- Tum apna approach explain karte ho
- Koi material include karte ho
- AI isay properly formatted skill mein tabdeel karta hai

### Step 1: Start the Conversation

```
I want to create a skill for writing research paper sections.

During our last session, I noticed my best sections had:
- Clear opening that establishes what the section explains
- Evidence integrated naturally
- Logical flow from paragraph to paragraph
- Conclusions that connect back to thesis

Can you help me turn this into a reusable skill?
```

### Step 2: Answer AI's Questions

AI tumse tumhari process ke baare mein poochega.

**Example Conversation:**

- AI: "What makes a section 'good'? How do you know if it’s ready?"
- Tum: "Good section ke teen cheezein:
  1. Har claim supported ho evidence/citation se
  2. Opening hook interest create kare, closing thesis se connect kare
  3. Kisi unfamiliar ko logic samajh aaye
  Needs work agar sentences samajh na aaye ya claims unsupported ho."

- AI: "Tumhara writing process kya hai? Outline pehle, linearly, ya iterate?"
- Tum: "Rough outline banata hoon, phir opening paragraph, evidence, transitions, aur closing. Read aloud karke flow check karta hoon."

- AI: "Quality checks kya hain?"
- Tum: "- Topic sentences clear hain?
- Factual claims cited?
- Flow smooth?
- Thesis se connected?"

### Step 3: AI Builds Skill File

AI conversation ko **SKILL.md** file mein tabdeel karega.

**Example SKILL.md:**

```yaml
---
name: "section-writer"
description: "Write clear, evidence-supported research paper sections with logical flow."
version: "1.0.0"
---
# Section Writing Skill

## When to Use
- User asks to write a section/draft content
- Thesis, evidence integration, academic writing involved
- Need structured research content

## Process Steps
1. Outline key points (3-5 main points)
2. Write opening paragraph (context + hook + thesis)
3. Develop each point: topic sentence → evidence → significance → transition
4. Closing: summarize + connect to thesis
5. Quality check: all claims cited, flow smooth

## Output Format
- Opening paragraph  
- Body segments (topic, evidence, significance)  
- Transitions  
- Closing paragraph  

## Quality Criteria
- Logic clear for unfamiliar reader  
- All claims supported  
- No confusing sentences  
- Opening hooks + closing connects to thesis  

## Example
**Input**: "Write Literature Review on AI in K-12 education. Key points: current AI state, teacher workload, student outcomes. Thesis: AI improves K-12 efficiency."  
**Output**:  
- Opening: context + hook  
- Body: 3 segments (topic, evidence, significance)  
- Closing: summary + thesis connection
```

### Step 4: Save the Skill File

```
mkdir -p .claude/skills/section-writer
Save as: .claude/skills/section-writer/SKILL.md
```

### Step 5: Test the Skill

Real task pe test karo aur output check karo.

### Step 6: Iterate Until It Works

Agar koi issue ho, AI ko update karke save karo.

---

## 4. Part B: Skill vs Subagent

**Decision Framework:**

- **Skill (2-6 decisions)** → Human guides, AI assists  
- **Subagent (7+ decisions)** → AI works autonomously

**Subagent Differences:**
- Role definition
- Decision authority
- Structured reporting format

---

## 5. Part C: Validating Your Skill

- Good skills → reasoning mode
- Bad skills → prediction mode (generic responses)

Test vague requests and ensure skill triggers clarification.

---

## 6. Part D: Building Your Intelligence Library

**Directory Structure Example:**

```
my-research-paper/
├── .claude/
│   ├── commands/
│   └── skills/
│       ├── section-writer/SKILL.md
│       ├── outline-refiner/SKILL.md
│       └── source-evaluator/SKILL.md
├── .specify/memory/constitution.md
├── specs/
└── ...
```

**Intelligence Reuse:**

- Project 2 → Use section-writer skill for new sections  
- Project 3 → Combine multiple skills (outline-refiner → section-writer → source-evaluator)

---

## 7. Common Mistakes

1. Skills for trivial patterns (1-2 decisions)
2. Skipping testing
3. Over-specific skills
4. No quality criteria

---

## 8. Skill Reuse in Practice

- Project 1: Full workflow from scratch (8-10 hrs)  
- Project 2: With section-writer skill (4 hrs, 50% faster)  
- Project 3: Multiple skills (3.5 hrs)

---

## 9. Practice Prompts with AI

1. **Start Skill Creation:**
```
I want to create a skill for writing research paper sections...
```

2. **Generate Complete Skill File:**
```
Create SKILL.md with YAML, usage, steps, output, example.
```

3. **Test Your Skill:**
```
Apply section-writer to Discussion section with key points...
```

4. **Iterate Based on Results:**
```
Update skill based on missing checks, save updated version.
```

5. **Decide Skill vs Subagent:**
```
Evaluate decision points, human vs AI role, then create skill or subagent.