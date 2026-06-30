[README.md](https://github.com/user-attachments/files/29514761/README.md)
<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# WormGPT (Talus Form)

Welcome to **WormGPT (Talus Form)**, an advanced, highly customizable client-side roleplay interface designed for deep, detailed, literary-style character interactions. 

Whether you want to use state-of-the-art **Google Gemini models** with intelligent local API key rotation or leverage custom open-source models via the **OpenRouter Proxy**, this app provides a powerful sandbox for seamless chat, character imports, lorebook integration, and model management.

---

## 🚀 Key Features

*   **Dual API Provider Modes**:
    *   **Gemini API (Pool)**: Input multiple Gemini API keys. The application will automatically rotate through the keys to bypass individual rate limits, allowing continuous generation.
    *   **OpenRouter Proxy**: Use any model hosted on OpenRouter (e.g., LLaMA, Claude, Mistral) by entering your custom OpenRouter key and model identifier.
*   **Built-In Key Testing & Validation**:
    *   Test each Gemini key individually before adding it to the pool.
    *   Validate OpenRouter connection and keys with the "Test Connection" button to catch errors immediately without wasting credits.
*   **Character Studio & Parser**:
    *   Fully compatible with Chub character formats, cards, and metadata.
    *   Customizable User Personas, Prompt presets, and depth parameters.
*   **Lorebooks & Vector Search**:
    *   Import custom lorebooks for contextually triggered knowledge injections during conversations.
*   **No Hardcoded Secrets**:
    *   All keys and configurations are saved strictly to local secure application state and database, keeping your private tokens safe from repository leaks.

---

## 🛠️ Installation & Setup (For Followers & Users)

To run **WormGPT (Talus Form)** on your computer, follow these simple, dummy-proof steps:

### 1. Download and Extract
*   **Download the ZIP**: Download the **`Roleplay studio.zip`** file from this repository.
*   **Unzip the File**: Extract/unzip the contents of the zip file into a folder on your computer.

### 2. Prerequisites
*   Make sure you have **Node.js** installed on your computer.
    *   If you don't have it, download and install the **LTS version** from the official website: **[https://nodejs.org/](https://nodejs.org/)** (Just click next, next, next during installation).

### 3. Run the Application
*   **Open Terminal / Command Prompt** inside the extracted folder.
    *   *Windows*: Open the folder, click on the address bar at the top, type `cmd` and press **Enter**.
    *   *Mac*: Right-click the folder, select **New Terminal at Folder** (or open Terminal and drag-and-drop the folder into it).
*   **Install the App (only need to do this once)**:
    Type the following command and press **Enter**:
    ```bash
    npm install
    ```
    *(Wait a moment for the installer to finish preparing the files).*
*   **Launch the App**:
    Type the following command and press **Enter**:
    ```bash
    npm run dev
    ```
*   **Open in Browser**:
    Open your web browser and go to: **`http://localhost:3000`**

---

## ⚙️ Configuration Guide

Click on **Settings & Theme** in the bottom left corner to open the configuration panel.

### 1. Gemini API (Pool) Mode
To use native Gemini models (such as `Gemini 1.5 Pro`, `Gemini 1.5 Flash`, or `Gemini 2.5 Flash`):
*   Select **Gemini API (Pool)** under API Provider Mode.
*   Enter a Gemini API Key in the "Enter new API Key" field.
*   *(Optional but Recommended)* Click **Test Key** to verify the validity of your key. It will make a tiny 1-token test call to ensure the key is active.
*   Click **Add** to add the key to your rotation pool.
*   You can add multiple keys! The application will automatically rotate through the active pool if one key encounters a rate limit.

### 2. OpenRouter Proxy Mode
To use open-source or premium models via OpenRouter:
*   Select **OpenRouter Proxy** under API Provider Mode.
*   Enter your **OpenRouter API Key** in the input field.
*   Specify your preferred model identifier in **Model Name (ID)** (e.g., `openrouter/owl-alpha` or `meta-llama/llama-3-8b-instruct:free`).
*   *(Optional)* Change the **Proxy Base URL** if you are using an alternative reverse proxy.
*   Click **Test Connection** to execute a validator request. You'll see a green "Success!" message once verified.

### 3. Api Keys
(Too lazy... there plenty tuto for that around)

---

## 🎭 Importing Characters & Customization

1.  Open the **Character Studio** from the left sidebar.
2.  Import character cards (JSON or PNG) exported from character sharing sites like Chub.
3.  Set up your **User Persona** details to let the character address you correctly.
4.  Configure **Lorebooks** and adjust generation preset variables like Temperature, Top P, or Custom System Prompts for fine-tuned responses.

---

## 📜 Production Build

To compile the application for optimal production performance or server hosting:
```bash
npm run build
npm run preview
```

---

*WormGPT (Talus Form) runs fully client-side inside your browser context. Your API keys are never sent to external servers other than directly to Google AI Studio or OpenRouter endpoints.*
