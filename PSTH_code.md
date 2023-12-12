{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Make a peri-stimulus time histogram from a 3-D numpy array of spike train data"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "```python\n",
    "fig, axs = plt.subplots(1, 3, figsize=(15, 5))\n",
    "\n",
    "for i in range(all_spike_arrays.shape[0]): \n",
    "    ax = axs[i]\n",
    "\n",
    "    # Sum along the second dimension to get the total number of spikes at each time point across all trials\n",
    "    spike_counts = np.sum(all_spike_arrays[i, :, :], axis=0)\n",
    "\n",
    "    # Add shading to indicate time light was on\n",
    "    ax.axvspan(light_onset_time, light_offset_time, color='greenyellow', alpha=0.5)\n",
    "\n",
    "    # Create histogram \n",
    "    ax.hist(range(0, len(spike_counts)), weights=spike_counts, \n",
    "                    bins=range(0, len(spike_counts) + 1, 1))\n",
    "    ax.set_title(f'Session {i+1}')\n",
    "    ax.set_xlabel('Time (ms)')\n",
    "    ax.set_ylabel('Number of Spike Occurrences')\n",
    "\n",
    "plt.tight_layout()\n",
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
