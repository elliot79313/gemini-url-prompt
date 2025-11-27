# **Gemini URL Prompt Extension**

A simple but powerful Chrome extension that allows you to prefill the prompt in [Google Gemini](https://gemini.google.com/) using URL parameters.

Gemini currently does not natively support passing prompts via the URL (like ?prompt=Hello). This extension bridges that gap, enabling seamless integration with productivity tools like Alfred, Raycast, Shortcuts, or simple browser bookmarks.

## **🚀 Features**

* **URL Parameter Support**: Use ?prompt= or ?q= to send text to Gemini.  
* **Auto-Focus**: Automatically focuses the input box so you can hit Enter immediately (or review the text).  
* **Smart Detection**: Works even if Gemini takes a few seconds to load (SPA support).  
* **Privacy First**: Runs entirely locally. No data is collected or sent to third-party servers.

## **📥 Installation**

### **From Chrome Web Store**

*(Link to your store page will go here once published)*

### **Manual Installation (Developer Mode)**

1. Clone or download this repository.  
2. Open Chrome and navigate to chrome://extensions/.  
3. Toggle **Developer mode** in the top right corner.  
4. Click **Load unpacked**.  
5. Select the folder containing the extension files.

## **💡 Usage**

Simply append ?prompt= followed by your text to the Gemini URL.

**Example:**

[https://gemini.google.com/app?prompt=Write a poem about coding](https://gemini.google.com/app?prompt=Write%20a%20poem%20about%20coding)

**Alternative parameter:**

[https://gemini.google.com/app?q=Explain quantum computing](https://gemini.google.com/app?q=Explain%20quantum%20computing)

### **Integration Examples**

#### **Alfred / Raycast / Spotlight**

Create a custom web search or workflow with the following URL pattern:  
https://gemini.google.com/app?prompt={query}

#### **Windows Run / Mac Shortcuts**

Create a shortcut that opens Chrome with the URL:  
chrome.exe "https://gemini.google.com/app?prompt=Your fixed prompt"

## **🛠 Development**

The extension uses a Content Script (content.js) to inject the text. Since Gemini uses a complex framework (likely Angular/Lit), the script simulates native user input events (input, textInput) to ensure the internal state of the application recognizes the text change.

## **🔒 Privacy**

This extension does not collect, store, or transmit any personal data. It only operates on gemini.google.com to fill the input field based on your current URL.

## **📄 License**

MIT License