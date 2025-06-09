# Loss Grapher

This project contains simple HTML tools for visualizing training loss values from your logs. Upload a log, and the page plots the loss over training steps. Two versions are provided:

- **enhanced-loss-extractor-2.html** – uses Chart.js with many features including moving averages and AI powered analysis.
- **loss-grapher-plotly.html** – a lightweight variant built with Plotly.

## Sample Images

You can overlay sample images generated during training:

1. Name image files so that the training step appears as the **second** number when more than one number exists. Examples:
   - `1749459275386__000028500_0.png` (step 28500)
   - `1749459275386__000028500_1.png`
   If only one number is found in the filename, that number is used as the step.
2. Click **Upload Samples** and select one or more images. You can pick multiple files at once.
3. Markers will appear on the loss chart at steps where images are available. Click a marker to preview the first four images for that step.

Use either HTML file directly in your browser to analyze your logs.
