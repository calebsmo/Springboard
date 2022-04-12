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


### Current Models
- PyOCR for intital numeric detection; EasyOCR to clean up misses.
- EasyOCR for all text base.
- Rather than image recognition, I'm going with a simple Gaussian approach to evaluate check-box columns.

### Areas for Improvement:
EasyOCR is wicked accurate, but much slower than PyOCR.

If the image resolution is very high, performance will increase.
