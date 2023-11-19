# this is for final code

In the provided code snippet, the preprocessing and preparation process of the audio data are as follows:

1.Data Loading:

Paths to audio files are stored in the file_path list.
Emotional labels (categories) of the audio files are stored in the file_emotion list and further transformed into a pandas DataFrame (emotion_df).
Data Visualization:
A count plot from the seaborn library is used to visualize the distribution of different emotions.

2.Audio Signal Processing:

Audio data is loaded and transformed into waveform data.
Visualization of waveplots and spectrograms is performed.

3.Feature Extraction:
Mel-frequency cepstral coefficients (MFCCs) are extracted from the audio signals. MFCCs are common features used in audio analysis that capture the short-term power spectrum and frequency characteristics of audio signals.
13 MFCC features are calculated for each audio sample.

4.Data Padding:
The MFCC feature sequences are padded to ensure uniform length using tf.keras.preprocessing.sequence.pad_sequences. This step is crucial for training LSTM networks as recurrent networks require all samples to have the same number of time steps.
Dataset Splitting:
The dataset is split into training, validation, and test sets.

5.Model Construction:

A neural network model comprising two LSTM layers and several fully connected layers is constructed. This model structure is suited for classification tasks with time-series data.
Model Compilation:
The model is compiled using the Adam optimizer and sparse_categorical_crossentropy loss function. This loss function is appropriate for multi-class classification problems where the class labels are integers.

6.Model Training:

The model is trained using the training set data and validated with the validation set to assess performance.
Model Evaluation:
The loss and accuracy of the model are evaluated on the test set.

7.Model Saving:
The trained model is saved for future use or further analysis.

8.Confusion Matrix:

