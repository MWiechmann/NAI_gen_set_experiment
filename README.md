# Analyzing Text Complexity of AI generated Texts (Novel AI)

This project has come together as a community effort of users in the official discord channel of [Novel AI (NAI)](https://novelai.net/). Novel AI uses [transformer models](https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)) that serve as "interactive AI storytellers". Discord user Basileus developed the idea to study the impact of various model settings on the readability (i.e. text complexity) of the generated texts.

Initial data collection from Basileus was done by varying what NAI calls "randomness". This setting is more commonly called [temperature](https://huggingface.co/blog/how-to-generate) for transformers models. For this experiment, sampling settings were Top-K Sampling: 140 and Nucleus sampling: 0.9. While data collection was still ongoing, interest about [Tail-Free Sampling (TFS)](https://trentbrick.github.io/Tail-Free-Sampling/) and its possible interaction with randomness arose in the community. Therefore, Basileus collected further outputs, varying temperature and TFS settings.

This data was rated by Basileus using [ProWritingAid](https://prowritingaid.com/) on several automated ratings for text complexity and quality. For readability the [Flesch-Kincaid grade level](https://en.wikipedia.org/wiki/Flesch%E2%80%93Kincaid_readability_tests#Flesch%E2%80%93Kincaid_grade_level) was used. Short explanations for other measures is provided below.

Data can be obtained [here](https://docs.google.com/spreadsheets/d/1a-oHJdBUvwTUam7Y9U9vqEvrcd4fK2q3oqm3H4iI4G0/edit#gid=116999801)

## Variables in the dataset

Variable|Meaning|Target
-|-|-
Randomness|Generator Setting|Predictor
Tail-Free|Generator Setting|Predictor
Grammar/Style/Spelling|Your writing can have no spelling or grammar mistakes but still be awkward, clumsy, and hard to read. Style can make your writing easier and more enjoyable to read. Style covers issues like repeated sentence starts, clunky word order and phrasing, hidden verbs, and more.|Higher is better
Readability Grade|A readability score is a measure of how easy your text is to read. Your readability score shows what grade level of students could understand and engage with your writing. For instance, a score of 7 means that seventh-grade students could read your work.|Depends (see explanation below)
Glue Index|Glue words are words that are common, low-quality, or nondescript, and too many of them can make your sentences "sticky". Sticky sentences slow your reader down; try to avoid them.|Lower is better

## Information on Readability Grade
Data conclusions are still ongoing, so conclusions at this point are  tentative. However, given the data so far readability seems to be emerging as the most interesting target variable that can be influenced by generator settings.

Information on readability grade (provided by Basileus):
Best-selling fiction is in the range of 4-9 on Readability Grade.

**Readability Grade 8-9: "Complex"** *(James Patterson, F. Scott Fitzgerald, Leo Tolstoy)*: relatively complex language, variety in word choice; can sometimes be abstruse\
**Readability Grade 7: "Poetic"** *(J.R.R. Tolkien, Dan Brown, Thomas Pynchon)*: enough complexity to have clever turns of phrase, without having to stop and think/reread\
**Readability Grade 6: "Casual"** *(Hunter S. Thompson, Steven King, Stephanie Meyer)*: flows well, easy to read large quantities of without getting tired\
**Readability Grade 4-5: "Punchy"** *(Ernest Hemingway, Cormac McCarthy, Susan Collins)*: concise, punchy language with straightforward sentence structure and word choice
