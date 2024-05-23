# ECG Data Analysis and Visualization Project

## Overview
This project was developed during my role as a research assistant at iHumEn, Universiti Teknologi Malaysia. It involves analyzing ECG data retrieved from the [MIT-BIH Arrhythmia ECG database](https://archive.physionet.org/cgi-bin/atm/ATM). The data is limited to the projection of time (seconds) and MLII signals (mV), saved in .CSV files. This Unity project integrates Python for data analysis.

## Prerequisites

### Software
- **Unity Hub**: Install Unity Editor version 2022.3.19f1 or later.
- **Python**: Version 3.10.

### Python Libraries
Install the following Python libraries using pip:
- `pandas`
- `numpy`
- `matplotlib`
- `scipy`
- `pywt`
- `re`

### Unity Packages
- **TMPro**: TextMeshPro for Unity.

## Limitations
1. **Data Format**: Limited to CSV files with 2 columns (time in seconds and MLII signal in mV).
2. **Real-Time Integration**: Not yet integrated with real-time ECG data (future work).
3. **Unity Version**: Requires Unity Editor version 2022.3.19f1 or later.
4. **Dependencies**: Must install required Python libraries and Unity packages.
5. **VR Integration**: Not yet integrated with VR (future work).
6. **Server Integration**: Not yet integrated with servers or databases (future work).
7. **Data Duration**: Tested with data limited to 10 seconds; not yet tested with longer datasets.

## How It Works

1. **Play the Unity Game**: Start the Unity application.
2. **Choose the CSV File**: Select the CSV file containing the ECG data.
3. **Data Analysis**: The C# script runs Python code in the background to analyze the signal.
   - Denoises the signal.
   - Marks P wave, QRS Complex, and T wave.
   - Determines heartbeat per minute (BPM).
   - Identifies bradycardia, sinus rhythm, or tachycardia.
   - Detects arrhythmias, limited to PAC (Premature Atrial Contractions) and PVC (Premature Ventricular Contractions).
4. **Output Generation**: Python code outputs a CSV file with updated data:
   - From 2 columns (time and MLII) to 5 columns (time, MLII, R Peak, BPM, A/V).
5. **Animation**: The C# script reads the updated CSV file and animates the heart based on the timestamp and R peak.
6. **Visualization**: The game displays a beating heart and panels indicating normal, arrhythmic, or ventricular rhythms based on the analyzed data.
7. **Prediction**: Click the "Predict" button to see predictions from a second Python script trained on a longer dataset.

## Future Work
- Integration with real-time ECG data.
- Compatibility with older versions of Unity Editor.
- VR integration.
- Server and database integration.
- Testing with longer datasets.
- Expanded arrhythmia classifications.

---

Feel free to contribute to this project by addressing any of the limitations or expanding its capabilities. Thank you for your interest!
