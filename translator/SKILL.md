---
name: translator
description: Translate text between any languages and display the result in a beautiful visual card showing both the original and translated text with language information.
metadata:
  homepage: https://github.com/YOUR_USERNAME/translator-skill
---

# Translator

## Instructions

When the user asks to translate text from one language to another:

1. First, identify the source language (or detect it from the input text if not specified).
2. Translate the text into the target language accurately and naturally.
3. Then call the `run_js` tool with the following exact parameters:
   - script name: `index.html`
   - data: A JSON string with the following fields:
     - `sourceText`: String. The original text to translate.
     - `translatedText`: String. The translated text you produced.
     - `sourceLang`: String. The full name of the source language (e.g. "English", "Spanish", "Japanese").
     - `targetLang`: String. The full name of the target language (e.g. "French", "German", "Chinese").
     - `sourceLangCode`: String. The ISO 639-1 two-letter code of the source language (e.g. "en", "es", "ja").
     - `targetLangCode`: String. The ISO 639-1 two-letter code of the target language (e.g. "fr", "de", "zh").

## Example usage

User: "Translate 'Good morning, how are you?' to Japanese"

You should:
1. Translate the text: "おはようございます、お元気ですか？"
2. Call `run_js` with:
   ```json
   {
     "sourceText": "Good morning, how are you?",
     "translatedText": "おはようございます、お元気ですか？",
     "sourceLang": "English",
     "targetLang": "Japanese",
     "sourceLangCode": "en",
     "targetLangCode": "ja"
   }
   ```
