### **Engineer Efficient Github Copilot Prompts**
#### #1 count how many columns have one word in a column of text but not a second, common, follow up word

#### #2 Find how many times the most common hashtag appears in a dataset

### #1

``` python
# Count the rows that have Musk but not Elon in the text column
df[(df['text'].str.contains('Musk')) & (~df['text'].str.contains('Elon'))].shape[0]

```

### #2

``` python
# Find the count of the most common hashtag
df['hashtags'].value_counts().head(1)

```

### Giving Github Copilot these prompts results in code that results in the necessary outputs without manual changes to the code