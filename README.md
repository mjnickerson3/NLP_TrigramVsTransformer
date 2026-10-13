# NLP Trigram Vs Transformer

## Description

This project compares a trigram language model with a transformer-inspired attention approach. The trigram model predicts the next word using only the previous two words as context, while the transformer simulation uses attention weights to consider important words throughout the entire sentence.

---

## Example Output

### Prompt 1

**Sentence:** The cat sat on the ___

**Context:** `on the`

1. mat (0.500)
2. rug (0.500)

### Prompt 2

**Sentence:** I want to eat ___

**Context:** `to eat`

1. pizza (0.333)
2. pasta (0.333)
3. dinner (0.333)

### Prompt 3

**Sentence:** She picked up the phone because ___

**Context:** `phone because`

1. it (0.500)
2. she (0.500)

---

## Trigram Analysis

### Sentence 1: The cat sat on the ___

**Prediction:** mat

**Did the prediction make sense?**

Yes. The prediction made sense because the training data included the sentence "The cat sat on the mat."

**What two words did the trigram model use as context?**

`on the`

**What important information did the model ignore?**

The model ignored the words "cat" and "sat" and only used the previous two words when making its prediction.

---

### Sentence 2: I want to eat ___

**Prediction:** pizza, pasta, or dinner

**Did the prediction make sense?**

Yes. All three predictions are reasonable foods or meals that could follow the phrase "I want to eat."

**What two words did the trigram model use as context?**

`to eat`

**What important information did the model ignore?**

The model ignored the rest of the sentence, including who is speaking and any information that might help determine the most appropriate food choice.

---

### Sentence 3: She picked up the phone because ___

**Prediction:** it or she

**Did the prediction make sense?**

Partially. The word "it" makes sense because it can continue into "it rang." The word "she" is grammatically correct but does not clearly explain the reason.

**What two words did the trigram model use as context?**

`phone because`

**What important information did the model ignore?**

The model ignored the overall meaning of the sentence and only used the previous two words to make its prediction.

---

## Transformer Attention Simulation

### Sentence 1: The cat sat on the ___

| Word | Weight |
|--------|--------|
| cat | 0.40 |
| sat | 0.25 |
| on | 0.15 |
| the | 0.10 |
| other words | 0.10 |

**Prediction:** mat

**Explanation:**

I assigned the highest weight to "cat" and "sat" because those words provide the strongest clues about what object the cat is sitting on. Looking at more of the sentence makes "mat" the most likely prediction.

---

### Sentence 2: I want to eat ___

| Word | Weight |
|--------|--------|
| eat | 0.40 |
| want | 0.30 |
| I | 0.20 |
| to | 0.10 |

**Prediction:** pizza

**Explanation:**

The word "eat" received the highest weight because it directly suggests that a food item should follow. Considering the entire sentence makes pizza a reasonable prediction.

---

### Sentence 3: She picked up the phone because ___

| Word | Weight |
|--------|--------|
| phone | 0.35 |
| because | 0.25 |
| picked | 0.15 |
| she | 0.15 |
| up | 0.10 |

**Prediction:** it rang

**Explanation:**

The words "phone" and "because" received the highest attention weights because they provide the most important context for explaining why the phone was picked up. This leads to the prediction "it rang."

---

## Comparison

The trigram model worked pretty well when the answer was directly related to the last two words in the sentence. For example, it was able to predict words like "mat" because that pattern appeared in the training data. However, the trigram model only looked at the previous two words when making a prediction, so it missed important information from earlier in the sentence.

The transformer-style approach produced better predictions because it considered important words throughout the entire sentence instead of only the last two words. By using attention weights, I was able to focus on words like "cat," "eat," and "phone" when deciding what word should come next. This provided more context and led to predictions that were more meaningful and accurate.

Attention helps solve the limited-context problem because the model can look at multiple important words across the sentence instead of only the two words that came before the prediction. This is one of the main reasons transformer-based language models perform better than traditional trigram models.

---

## What I Learned

This assignment helped me better understand the difference between trigram models and transformer-based language models. A trigram model only uses the previous two words to predict the next word, which can limit how much context it understands. While the trigram model was able to make reasonable predictions, it often ignored important information that appeared earlier in the sentence.

Transformers use attention to focus on important words throughout the entire sentence instead of only the last two words. By using more context, transformers can make more accurate and meaningful predictions. Completing this assignment helped me better understand why modern AI tools like ChatGPT and Microsoft Copilot use transformer architectures instead of simpler n-gram models.

---

## Trigram Model Output

<img width="281" height="342" alt="image" src="https://github.com/user-attachments/assets/bd94570f-b502-4bd0-9c36-b74b79dadf07" />


