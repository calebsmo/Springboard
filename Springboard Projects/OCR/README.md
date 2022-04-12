# OCR: Pdf Text Processing

#### Summary

This repo is where I will be submitting my work for processing Pdf and object character recognition (OCR).

The project will involve:
- Preparing and pre-processing for the Pdf
- Model comparisons (pytesseract, pyocr, easyocr)
- Image processing for check-box selected determination
- Final Pipeline process with Streamlit.

My work will be mostly located in the jupyter notebooks, however I will also be linking a Streamlit app that will serve as an example for the complete pipeline.

![1506](https://github.com/calebsmo/Springboard/blob/main/Springboard%20Projects/OCR/Example.png)

### Pre-processing
For the scope of this project, I'm just focusing on Block 4 (Periods of Service). I'm processing the image in the following steps, but will be constantly looking to reduce the time it takes to process this information.

1. Do this
2. Do that

### Current Models
For the Periods of Service columns that are strictly numeric I am using PyOCR initially. If the cell is definitely not blank and PyOCR comes up short, then I used EasyOCR to double-check the cell. So far, EasyOCR is pretty much perfect, but too slow to use as the primary. Instead, it operates as cleanup for PyOCR and then primary for the "SERVICE" and "SOURCE DOCUMENTS" columns, which are text heavy. For the checkbox columns, I initially considered training a model for it, but decided a simple Gaussian approach would be easier and faster for evaluating the responses.

### Areas for Improvement:
EasyOCR is wicked accurate, but much slower than PyOCR. I've done a lot of local testing to see if I could improve PyOCR's predicitive accuracy with image pre-processing, but it struggles with some data too much to be left alone, which is why I'm backfilling its misses with EasyOCR. The majority of the time the pipeline takes to process an image is completely based on EasyOCR. If the image resolution is very high, performance will increase. However, I'm anticipating very poor quality images and can't sacrifice the outputs accuracy.
