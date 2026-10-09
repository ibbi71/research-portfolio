# Astronomical Transient Classification

*LSE Artificial Intelligence group project*

## The question

Can attention mechanisms help a neural network distinguish genuine astronomical transients from imaging artefacts? We were particularly interested in how the models would perform when genuine events are extremely rare.

## How we approached it

Using the Tomo-e Gozen dataset, we compared a baseline convolutional neural network with four attention mechanisms: CBAM, ECA-Net, Coordinate Attention and SimAM. The models shared a common backbone and evaluation procedure, with 99,955 three-channel image cutouts used for training and validation. Genuine transients made up roughly 0.1% of the independent test set.

We evaluated ranking performance across three random seeds. We also calibrated the predicted probabilities, corrected for the difference in class prevalence between training and test data, and chose detection thresholds that aimed to maximise precision while recovering at least 70% of genuine events.

## What we found

ECA-Net achieved the highest mean area under the precision-recall curve (AUPRC), making it the strongest ranking model in our comparison. After calibration and threshold selection, Coordinate Attention gave the best detection result: it recovered 205 of 292 genuine transients with 68 false positives, giving 75.1% precision.

The preferred model therefore depended on whether we wanted to rank candidates or make a final detection decision. These results remain tentative: we used three seeds for the ranking comparison, and the calibration and threshold results came from one representative run per architecture.
