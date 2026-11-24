# 📱 StudentSpend — Android APK Build Project

> **Cloud-buildable Android Native App wrapper for StudentSpend.**  
> Completely standalone and isolated from your web application files.

---

## ⚡ How It Works

Because your PC has low system specifications and cannot run Android Studio, this project is configured with **GitHub Actions**. GitHub's cloud servers (with 16GB+ RAM, fast processors, and pre-installed Android SDKs) will compile the `.apk` file for you in the cloud for **free**.

---

## 🚀 3-Step Guide to Generate Your APK

### Step 1: Set Your Web App URL
Open [app/src/main/res/values/strings.xml](file:///e:/26projects/Expensetracker-apk/app/src/main/res/values/strings.xml):
```xml
<string name="default_web_url">https://your-studentspend-app.vercel.app</string>
```
* Change `default_web_url` to your live deployed URL (e.g. on Vercel or Render), or your PC's local Wi-Fi IP address (e.g. `http://192.168.1.5:3000`) for testing over home Wi-Fi.

---

### Step 2: Push this Folder to a GitHub Repository

In PowerShell or terminal, navigate to this folder and run:
```bash
cd e:\26projects\Expensetracker-apk

# Initialize git repository
git init
git add .
git commit -m "Initial StudentSpend Android project"

# Link to your GitHub repository (create a new empty repo on github.com first)
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
```

---

### Step 3: Download Your APK File from GitHub

1. Open your repository on **github.com**.
2. Click on the **"Actions"** tab at the top.
3. You will see a workflow running titled **"Build Android APK"** (takes about ~2 minutes).
4. Once finished (marked with a green checkmark ✅), click on the completed run.
5. Under the **Artifacts** section at the bottom of the page, click **`StudentSpend-debug-apk`**.
6. A zip file containing **`app-debug.apk`** will download to your PC or phone!

---

## 📲 How to Install on Your Android Phone

1. Transfer the downloaded `app-debug.apk` to your Android phone (via WhatsApp, Google Drive, USB, or download directly in phone browser).
2. Tap the `.apk` file to install.
3. If prompted by Android with *"Install unknown apps"*, tap **Settings > Allow from this source**.
4. Tap **Install**, then **Open**.
5. You now have **StudentSpend** running as a native Android app on your phone with:
   - Fullscreen app experience (no browser address bar).
   - Indigo app icon with ₹ rupee emblem on home screen.
   - Pull-to-refresh.
   - Hardware back button navigation.
   - Offline fallback screen.
