# वेबसाइट फ्री में ऑनलाइन कैसे करें

1. GitHub.com पर login करें और नया **Public repository** बनाएं: `sarswati-puja-samiti`.
2. इस ZIP को extract करें।
3. इसके अंदर की सभी files और folders को GitHub repository के root में upload करें।
4. Repository → **Settings → Pages** खोलें।
5. **Deploy from a branch** चुनें।
6. Branch `main` और folder `/(root)` चुनकर Save करें।
7. GitHub द्वारा दिया गया `https://USERNAME.github.io/sarswati-puja-samiti/` URL खोलें।
8. Website पर QR अपने-आप live URL से बन जाएगा। **QR डाउनलोड करें** बटन से PNG save कर सकते हैं।

## APK डाउनलोड चालू करने से पहले
आपके अभी दिए APK में AI provider API keys मौजूद हैं। पहले Groq/Gemini/OpenAI keys rotate/revoke कराएं और सुरक्षित नया APK बनाएं। पुराने APK को public न करें।

सुरक्षित APK को `downloads/app.apk` नाम से रखें। फिर `js/site.js` में:
`const APP_DOWNLOAD_ENABLED = false;`
को `true` करें और बदलाव GitHub पर upload करें।

## Backend
`portal.html` आपके पहले से मौजूद Supabase project को इस्तेमाल करता है। कोई नया paid server या दूसरा Supabase project नहीं बनाया गया है। Supabase Free plan की limits लागू होंगी।
