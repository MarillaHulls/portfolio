## Visualize data from multiple conditions in a boxplot grouped by colour in a colourblind friendly format

```python
# Make a box plot with simon condition as the x-axis, RT on the y-axis, and flanker condition as the hue
sns.catplot(kind = 'box',
            data = df_false,
            x = 'simon',
            y = 'rt (s)',
            hue = 'flankers',
            palette = 'colorblind'
            )
            
# Show the plot
plt.show()
```