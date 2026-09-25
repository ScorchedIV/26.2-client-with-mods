## Single-page launcher

After building the browser client, you can open the single launcher page in a browser:

```bash
./gradlew :target_teavm_javascript:buildEaglerJS
./gradlew :target_teavm_javascript:stageClient
python3 -m http.server 8080 --directory .
```

Then open:

- http://localhost:8080/single-file.html

This page auto-loads the generated TeaVM client from `dist/client/classes.js` and starts the game from one entry point.

> Important: this workspace is still a browser-client template and does not include the actual proprietary 26.2 game source/assets. The single launcher only wraps the generated browser build once the real client is present.
