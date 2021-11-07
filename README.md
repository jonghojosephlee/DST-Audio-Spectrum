# DST-Audio-Spectrum
The STFT (Short-Time Fourier Transform) is one of the essential tools of music technology for the analysis of complex non-periodic waveforms. 
The main idea behind the STFT is to create overlapping slices of audio (buffers) to process one at the time for the extraction of the frequency magnitude through the FFT without losing any information. 
The result of each slice is then displayed in a time-frequency plot which, taken as a whole, represents a spectrogram.
This exercise aims at exploring the trade-off between time-frequency resolutions inherent to the STFT algorithm and learning matrix-based coding skills.

The general overview:

1. Slice signal into overlapping buffer frames (a function to do this is provided)

2. Apply a window to each frame

3. Extract the frequency magnitude at each frame by doing the following:
  a. fft and magnitude extraction, remove replicas
  b. normalize
  c. transformation into dB scale
  d. output the result in a matrix

4. Compute and return the appropriate axis ticks for plotting (y-axis = frequency, x-axis = time)
Given the inputs shown below and specified in the provided header, the function should analyze audio data by buffering the signal into overlapping frames and modify it by using the requested type of window and finally computing the STFT. 
The return of the function should be a 2-dimensional matrix where each value represents the magnitude (in dB) of the signal at a specific frequency and a specific time. 
The “y” axis (rows) will represent frequencies and the “x” axis (columns) will represent time.
