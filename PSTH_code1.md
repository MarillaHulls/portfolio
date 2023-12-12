### Make a peri-stimulus time histogram from a 3-D numpy array of spike train data
```python
fig, axs = plt.subplots(1, 3, figsize=(15, 5))

for i in range(all_spike_arrays.shape[0]): 
    ax = axs[i]

    # Sum along the second dimension to get the total number of spikes at each time point across all trials
    spike_counts = np.sum(all_spike_arrays[i, :, :], axis=0)

    # Add shading to indicate time light was on
    ax.axvspan(light_onset_time, light_offset_time, color='greenyellow', alpha=0.5)

    # Create histogram 
    ax.hist(range(0, len(spike_counts)), weights=spike_counts, 
                    bins=range(0, len(spike_counts) + 1, 1))
    ax.set_title(f'Session {i+1}')
    ax.set_xlabel('Time (ms)')
    ax.set_ylabel('Number of Spike Occurrences')

plt.tight_layout()
plt.show()
```