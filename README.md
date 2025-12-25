# 🍱 FoodgramAI: Multimodal AI Social Media Assistant

## 🚀 Project Overview

**FoodgramAI** is an intelligent backend system designed to revolutionize how foodies share their experiences. By leveraging the multimodal capabilities of **Google Gemini 1.5 Flash**, the platform transforms raw meal photos and casual voice memos into professional-grade Instagram content. It bridges the gap between a simple dining moment and a high-quality social media post.

---

## ✨ Key Features

### 1. AI-Driven Visual Enhancement

* **Warm Tone Optimization**: Instead of static filters, the AI analyzes the specific lighting and composition of your food photo to determine the perfect `brightness` and `contrast` parameters (typically targeting a cozy, appetizing aesthetic).
* **Posing & Composition Guide**: Utilizing **Few-shot Prompting**, the system recognizes the user's camera view and suggests the best posing overlays to help users capture the "perfect shot."

### 2. Intelligent Content Recommendation

* **Smart Overlays**: The system compares the user's current photo against a curated library of high-quality food photography (Hotpot, Ramen, Desserts, etc.) and recommends the most relevant visual styles and stickers.

### 3. Multimodal Caption Generation

* **Text-to-Caption**: Converts store names, dish lists, and raw reviews into engaging IG posts complete with emojis and trending hashtags.
* **Voice-to-Caption**: Users can simply speak their thoughts. The AI transcribes the **audio (.aac)**, extracts key sentiments, and drafts a creative caption automatically.

---

## 🛠 Tech Stack

* **Backend**: Python / Flask
* **AI Engine**: Google Gemini 1.5 Flash (Multimodal)
* **Vision Processing**: OpenCV & Pillow
* **API Management**: Google Generative AI SDK

---

## 🔌 API Endpoints Reference

| Endpoint | Method | Input | Description |
| --- | --- | --- | --- |
| `/save_image` | `POST` | Image File | Stores the user's photo on the server. |
| `/get_processed_image` | `POST` | File Path | AI calculates parameters and returns a warm-toned image. |
| `/get_caption_from_audio` | `POST` | Audio File | Transcribes voice memos into IG-ready captions. |
| `/get_overlay_image` | `POST` | Category / Path | Recommends 3 similar professional food photos. |

---

## 🧠 AI Logic: Few-Shot Prompting

The project utilizes a sophisticated "History-based" prompt engineering technique. By pre-loading Gemini with a specific context of 21+ example food images, the model gains a "professional photographer's intuition," allowing it to categorize and recommend content with high accuracy without additional fine-tuning.

![FoodgramAI-01](FoodgramAI_ppt/FoodgramAI-01.png)
![FoodgramAI-02](FoodgramAI_ppt/FoodgramAI-02.png)
![FoodgramAI-03](FoodgramAI_ppt/FoodgramAI-03.png)
![FoodgramAI-04](FoodgramAI_ppt/FoodgramAI-04.png)
![FoodgramAI-05](FoodgramAI_ppt/FoodgramAI-05.png)
![FoodgramAI-06](FoodgramAI_ppt/FoodgramAI-06.png)
![FoodgramAI-07](FoodgramAI_ppt/FoodgramAI-07.png)
![FoodgramAI-08](FoodgramAI_ppt/FoodgramAI-08.png)
![FoodgramAI-09](FoodgramAI_ppt/FoodgramAI-09.png)
![FoodgramAI-10](FoodgramAI_ppt/FoodgramAI-10.png)
![FoodgramAI-11](FoodgramAI_ppt/FoodgramAI-11.png)
![FoodgramAI-12](FoodgramAI_ppt/FoodgramAI-12.png)
