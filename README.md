# Loss Grapher

This project contains simple HTML tools for visualizing training loss values from your logs. Upload a log, and the page plots the loss over training steps. Both tools automatically filter out obviously invalid loss values (e.g. negative or extreme outliers) to avoid interpreting corrupt data. Two versions are provided:

- **enhanced-loss-extractor-2.html** – uses Chart.js with many features including moving averages and AI powered analysis.
- **loss-grapher-plotly.html** – a lightweight variant built with Plotly.

## Sample Images

You can overlay sample images generated during training:

1. Name image files so that the training step appears as the **second** number when more than one number exists. Examples:
   - `1749459275386__000028500_0.png` (step 28500)
   - `1749459275386__000028500_1.png`
   If only one number is found in the filename, that number is used as the step.
   The grapher assumes images are generated **after** the logged step completes, so each filename's step is mapped to `step - 1` when overlaying.
2. Click **Upload Samples** and select one or more images. You can pick multiple files at once.
3. Markers will appear on the loss chart at steps where images are available. Click a marker to preview the first four images for that step.

Use either HTML file directly in your browser to analyze your logs.

## Chart.js version

The enhanced extractor uses Chart.js 3.9 with the zoom plugin. When you zoom or
pan the loss chart, the visible points are reduced to a maximum of 500 to keep
interaction smooth. You can tweak this limit by editing `MAX_VISIBLE_POINTS` in
the HTML file. The chart now enables pinch gestures and slower scroll zooming so
Mac trackpads work smoothly—use two fingers to pinch to zoom and click&drag to
pan across the steps.
