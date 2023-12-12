{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### **Engineer Efficient Github Copilot Prompts**\n",
    "#### #1 count how many columns have one word in a column of text but not a second, common, follow up word\n",
    "\n",
    "#### #2 Find how many times the most common hashtag appears in a dataset\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### #1\n",
    "``` python\n",
    "# Count the rows that have Musk but not Elon in the text column\n",
    "\n",
    "df[(df['text'].str.contains('Musk')) & (~df['text'].str.contains('Elon'))].shape[0]\n",
    "\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### #2\n",
    "\n",
    "``` python\n",
    "# Find the count of the most common hashtag\n",
    "df['hashtags'].value_counts().head(1)\n",
    "\n",
    "```"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Giving Github Copilot these prompts results in code that results in the necessary outputs without manual changes to the code"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": []
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
