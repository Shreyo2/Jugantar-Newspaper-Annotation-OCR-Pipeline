# Jugantar Newspaper Annotation & OCR Pipeline

This repository contains the guidelines and workflow for annotating layout elements and verifying Optical Character Recognition (OCR) outputs for the *Jugantar* newspaper using **Label Studio**.

## 📋 Prerequisites & Tools

Before starting the annotation process, ensure you have the following set up:
* **Label Studio:** Running locally or accessible via your assigned server.
* **Python Terminal:** Running the backend OCR processing script connected to Label Studio.
* **Avro Keyboard:** Installed and active on your system for typing and correcting Bengali text.

---

## ⚠️ Critical Annotation Rules

1. **Strictly Exclude All Advertisements:** Do **not** draw bounding boxes around any advertisements whatsoever.
2. **Watch Out for Camouflaged Ads:** Be extra cautious of text-only advertisements. Some ads are intentionally formatted to blend in as regular news articles due to their all-text layout, font structure, and positioning on the newspaper page. Always read the content carefully to ensure you do not annotate disguised ads.
3. **Use Avro Bengali Keyboard for Edits:** All manual corrections to the generated Bengali OCR text must be typed using the **Avro Bengali keyboard** to maintain consistent character encoding.

---

## 🚀 Step-by-Step Annotation Workflow

Follow these steps for each newspaper page:

1. **Draw Bounding Boxes:** Draw bounding boxes around all valid newspaper content on the page (carefully excluding all ads, including text-only ads disguised as news) and click **Submit**.
2. **Wait for OCR Processing:** Switch to your Python terminal and wait for the `"annotations completed"` message to appear.
3. **Inspect OCR Results:** Return to Label Studio and click on each bounding box to inspect its generated OCR text.
4. **Correct & Update:** Using the **Avro Bengali keyboard**, correct any OCR errors you find, click **Update** to save your changes, and move on to the next page.

---

## 💡 Quick Tips for Annotators
* **Double-Check Before Submitting:** Ensure no disguised advertisements were accidentally boxed before hitting **Submit**, as this triggers the backend OCR script.
* **Save Your Edits:** Always remember to click **Update** (not just close the box) after fixing Bengali text errors, otherwise your OCR corrections will not be saved.