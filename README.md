# Jugantar-Newspaper-Annotation-OCR-Pipeline

This repository contains the guidelines and workflow for annotating layout elements and verifying Optical Character Recognition (OCR) outputs for the *Jugantar* newspaper using **Label Studio**. All annotated images, along with their respective bounding boxes and OCR results, will be submitted in separate intern-wise folders for **quality checks** necessary for data preparation.

## Prerequisites & Tools

Before starting the annotation process, ensure you have the following set up:
* **Label Studio:** Running via your assigned server. LABEL_STUDIO_URL=<http://localhost:8080>
* **Python Terminal:** Running the backend OCR processing script connected to Label Studio.
* **Avro Keyboard:** Installed and active on your system for typing and correcting Bengali text.

---

## ⚠️ Critical Annotation Rules

1. **Select Proper Class Labels**: Always ensure you select the accurate, corresponding class label for every bounding box you draw.
2. **Strictly Exclude All Advertisements:** Do **not** draw bounding boxes around any advertisements whatsoever.
3. **Watch Out for Camouflaged Ads:** Be extra cautious of text-only advertisements. Some ads are intentionally formatted to blend in as regular news articles due to their all-text layout, font structure, and positioning on the newspaper page. Always read the content carefully to ensure you do not annotate disguised ads.
4. **Use Avro Bengali Keyboard for Edits:** All manual corrections to the generated Bengali OCR text must be typed using the **Avro Bengali keyboard** to maintain consistent character encoding.

---

## Step-by-Step Annotation Workflow

Follow these steps for each newspaper page:

1. **Draw Bounding Boxes:** Draw bounding boxes around all valid newspaper content on the page (carefully excluding all ads, including text-only ads disguised as news) and click **Submit**.
2. **Wait for OCR Processing:** Switch to your Python terminal and wait for the `"patched annotation .."` message to appear.
3. **Inspect OCR Results:** Return to Label Studio and allow some time before you click on each bounding box to inspect its generated OCR text.
4. **Correct & Update:** Using the **Avro Bengali keyboard**, correct any OCR errors you find, click **Update** to save your changes.
5. Move on to the next page and repeat the process.

---

## 💡 Quick Tips for Annotators
* **Box Everything First Before Submitting**: Do not hit **Submit** after drawing each individual bounding box. Complete all bounding boxes on the entire page first, and only click **Submit** once at the end to avoid maxing out the free daily API call limits (Sarvam / Gemini).
* **Double-Check Before Submitting:** Ensure no disguised advertisements were accidentally boxed before hitting **Submit**, as this triggers the backend OCR script.
* **Save Your Edits:** Always remember to click **Update** (not just close the box) after fixing Bengali text errors, otherwise your OCR corrections will not be saved.
