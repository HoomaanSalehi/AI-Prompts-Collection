# Advanced Anki Flashcard Generator (IELTS Academic)

This prompt generates high-quality, academic vocabulary flashcards in a format ready for direct import into Anki. It is specifically tailored for learners preparing for the IELTS Academic exam.

---

## ✨ Key Features

-   **100% Anki-Compatible:** Uses the TAB separator and a 3-field structure for seamless import.
-   **Two-Level Explanations:** Provides both a simple, everyday analogy (A1 level) for intuitive understanding and a standard, academic definition (B2/C1 level) for depth.
-   **Intelligent Collocation Handling:** Analyzes verb-noun phrases to decide whether to create a single card for the phrase or separate cards for its components.
-   **Comprehensive Auto-Tagging:** Automatically adds tags for CEFR level, topic category, part of speech, and more, making your Anki deck organized and searchable.
-   **Statistical Analysis:** Generates a final report on the processed words to verify its own work and ensure accuracy.
-   **Zero Redundancy:** Guarantees that no duplicate words or minor grammatical variants appear in the final output.

---

## 🚀 How to Use

1.  **Copy the Prompt:** Copy the entire prompt text from the code block below.
2.  **Add Your Words:** Paste your list of English vocabulary words at the very end, where it says `[Insert English words here]`.
3.  **Generate:** Paste the complete text (prompt + your words) into an AI model like GPT-4.
4.  **Copy the Output:** The AI will generate the flashcard data inside one or more code snippets. Copy the content of these snippets.
5.  **Import into Anki:**
    -   Open a text editor (like Notepad, VS Code, or TextEdit) and paste the copied data.
    -   Save the file as a `.txt` file (e.g., `ielts_vocab.txt`).
    -   In Anki, go to `File > Import` and select your `.txt` file.
    -   Ensure the field mapping is correct and that "Fields separated by: Tab" is selected.
    -   Import!

---

## 📋 The Prompt

```prompt
**TASK:** Create academic vocabulary flashcards in an Anki-compatible format (3-field format), tailored for the requirements of the IELTS Academic exam and general university-level language proficiency.

**CRITICAL RULES (for Anki Import):**

1.  **Format:** The entire output must be in plain text.
2.  **Code Snippet:** Each category must be presented in its own separate code snippet for easy copying.
3.  **Separator:** You MUST use a real Tab character (TAB) as the field separator.
4.  **Content:** Each line represents a single Anki card and must end with a line break (Enter).
5.  **CRITICAL FOR REDUNDANCY:** Each vocabulary item must appear ONLY ONCE in the entire output.
    -   Perform a PREPROCESSING step: remove all duplicates and grammatical variations from the input list. In such cases, choose the most relevant or common form (e.g., the base form of a verb, "analyze").
    -   Process only the cleaned, unique list of words.
6.  **RULE FOR GENERALIZATION:** Define each word in its most common academic sense, regardless of the context of other words in the input list. The definition should be applicable across multiple fields of study. Avoid an overly specialized definition unless the word is inherently very specific.
7.  **SPECIAL RULE FOR VERB-NOUN COLLOCATIONS:** When a verb-noun collocation (e.g., "to conduct research") is in the input list, perform the following analysis:
    a.  Check for Idiomaticity: Does the phrase have a unique, non-literal meaning that isn't obvious from its individual parts?
    b.  Case 1 (Idiomatic/Fixed Phrase): If yes, OR if it's an extremely common academic collocation, create ONE SINGLE Anki card for the entire phrase.
    c.  Case 2 (Literal Meaning): If the meaning is literal (e.g., "to eat an apple"), DO NOT create a card for the phrase. Instead, create two separate cards: one for the noun and one for the verb, provided they are not already separate entries in the cleaned list.

**Flashcard Structure (3-Field Format):**

[Field 1]	[Field 2]	[Field 3]

**Field 1 (Front):**
-   Only the English word or phrase. (Nouns should be singular, verbs in their base form).

**Field 2 (Back):**
-   The back must have two main parts, separated by a single `<br>` HTML tag.
    1.  **Part 1 (Analogy for Beginners):** STRICT RULE: Explain the concept using a simple, everyday analogy at a maximum A1 level. Imagine you are talking to someone who speaks very little English. Use NO abstract terms. The difference in simplicity compared to Part 2 must be extremely clear. This is not a definition, but a mental picture. *Example: For "to analyze" -> "It's like taking a toy apart to see how all the little pieces work together."*
    2.  **Part 2 (Standard Definition & More):** A concise, standard B2-C1 level definition. Immediately after, optionally add a relevant Synonym (Syn.:) and/or Antonym (Ant.:) if applicable. ALWAYS conclude this part with a realistic academic example sentence.

**Field 3 (Tags):**
-   Add all relevant tags separated by spaces.
    -   Main-Tag (CRITICAL): Choose one or more suitable main tags from this list: (Academics, Science, Environment, Society, Argumentation, Communication). *If the word fits multiple themes, please add all relevant main tags.*
    -   Part-of-Speech-Tag: Mandatory (e.g., Noun, Verb, Adjective, Phrase).
    -   Form-Tag: Only if applicable (e.g., Collocation, Preposition, Connector).
    -   LEVEL-TAG: Add the CEFR language level tag (e.g., B2, C1).
    -   Subtags: MANDATORY – Add at least one subtag for each card (e.g., UniversityLife, Research, Logic, Climate, Economy).

**CATEGORIZATION (6 Main Categories):**

IMPORTANT – Placement: Each flashcard is placed ONLY ONCE in the single code snippet that best fits its primary meaning. The tag for that snippet must appear as the first tag in Field 3.

1.  University & Academics → Primary-Tag: Academics
2.  Science & Research → Primary-Tag: Science
3.  Environment & Sustainability → Primary-Tag: Environment
4.  Society & Economy → Primary-Tag: Society
5.  Argumentation & Discourse → Primary-Tag: Argumentation
6.  Communication & Interaction → Primary-Tag: Communication

---

**FINAL ANALYSIS AND STATISTICS:**

After all code snippets, create a single summary table about the cleaned word list. All statistics must refer exclusively to the cleaned list, not the original input words.

1.  Total Vocabulary Processed:
    → The number of unique, cleaned entries as a plain number, e.g., 71
2.  Distribution by Main Category (Placement):
    → The percentage of cards physically placed in each code snippet, relative to the total. The sum must be exactly 100%.
3.  Distribution by Part of Speech:
    → Also in percentages, sum = 100%.
4.  Distribution by CEFR Level:
    → In percentages, sum = 100%.
5.  Average CEFR Level:
    → e.g., ≈ B2; calculated from the distribution.

---

**PRE-OUTPUT CHECKLIST (You MUST follow this):**
- [ ] Have you removed all duplicates (including different forms of the same word)?
- [ ] Does each card appear only once and in only one snippet?
- [ ] Do the percentage sums in ALL statistics tables (Category/Part of Speech/CEFR) equal 100%?
- [ ] Does the number of generated cards exactly match the count of the cleaned list?

---

**WORDS TO BE PROCESSED:**

[Insert English words here]
```
