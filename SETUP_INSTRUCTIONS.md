# How to Get Your Windows Executable (Step-by-Step)

No Python installation required! GitHub will build it for you automatically.

---

## Step 1: Create a GitHub Account (if you don't have one)

1. Go to https://github.com
2. Click "Sign up"
3. Follow the prompts (free account is fine)

---

## Step 2: Create a New Repository

1. Click the **+** button in the top-right corner
2. Select **"New repository"**
3. Name it: `binary-input-extractor`
4. Select **"Public"** (required for free builds)
5. Check **"Add a README file"**
6. Click **"Create repository"**

---

## Step 3: Upload the Files

1. In your new repository, click **"Add file"** → **"Upload files"**

2. Drag and drop these files from the ZIP:
   - `binary_input_gui.py`
   - `README.md` (replace the existing one)

3. Click **"Commit changes"**

4. Now create the workflow folder:
   - Click **"Add file"** → **"Create new file"**
   - In the filename box, type: `.github/workflows/build.yml`
   - Copy-paste the entire contents of the `build.yml` file
   - Click **"Commit changes"**

---

## Step 4: Wait for the Build

1. Click the **"Actions"** tab at the top
2. You'll see "Build Executables" running (yellow dot)
3. Wait 3-5 minutes for it to complete (green checkmark)

---

## Step 5: Download Your Executable

1. Click the **"Releases"** link in the right sidebar
2. Find the latest release
3. Download `BinaryInputExtractor.exe` (for Windows)

---

## 🎉 Done!

You now have a standalone Windows executable that works on any Windows PC without Python.

---

## Troubleshooting

### "Actions" tab is missing
- Make sure your repository is **Public**
- Go to Settings → Actions → General → Allow all actions

### Build failed
- Click on the failed run to see the error
- Most common: typo in the workflow file

### Can't find Releases
- The first release is created automatically after a successful build
- Or go to: `https://github.com/YOUR-USERNAME/binary-input-extractor/releases`

---

## Alternative: Build on Your Own Windows PC

If you prefer to build locally:

1. Install Python from https://python.org (check "Add to PATH")
2. Open Command Prompt
3. Run:
   ```
   pip install pdfplumber openpyxl pyinstaller
   pyinstaller --onefile --windowed --name BinaryInputExtractor binary_input_gui.py
   ```
4. Find `BinaryInputExtractor.exe` in the `dist` folder
