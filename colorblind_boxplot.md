{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Visualize data from multiple conditions in a boxplot grouped by colour in a colourblind friendly format"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```python\n",
    "# Make a box plot with simon condition as the x-axis, RT on the y-axis, and flanker condition as the hue\n",
    "sns.catplot(kind = 'box',\n",
    "            data = df_false,\n",
    "            x = 'simon',\n",
    "            y = 'rt (s)',\n",
    "            hue = 'flankers',\n",
    "            palette = 'colorblind'\n",
    "            )\n",
    "            \n",
    "# Show the plot\n",
    "plt.show()\n",
    "```"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "base",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "name": "python",
   "version": "3.9.13"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}