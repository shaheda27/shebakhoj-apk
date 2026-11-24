BUILD THE SHEBAKHOJ APK IN THE CLOUD (no Android Studio needed)

1. Edit app/src/main/java/com/shebakhoj/app/MainActivity.java: change the SITE line to your live website address, e.g.
   private static final String SITE = "http://12.34.56.78/AUW26/yourfolder/";   (keep the slash at the end)
2. Make a free account at github.com and create a NEW repository (Public, name: shebakhoj-apk).
3. In the repository click Add file > Upload files. Drag in EVERYTHING from this folder (settings.gradle, build.gradle,
   gradle.properties, the app folder, README). Click Commit changes.
4. Click Add file > Create new file. In the name box type exactly:  .github/workflows/build.yml
   Paste the text of github-workflow-copy/build.yml into it. Click Commit changes.
5. Open the Actions tab. A run called "Build APK" starts (about 5 to 8 minutes). Wait for the green tick.
6. Click the run, scroll to Artifacts, click ShebaKhoj-apk to download a zip. Inside is app-debug.apk.
7. Send app-debug.apk to your phone, open it, allow "Install unknown apps" when asked, and install.
If the run shows a red cross, open it and send me the red error lines.
