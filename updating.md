## Manual Updating
Notes to self, because it's infrequent enough that I forget every time.

1. Create new branch

2. Run x-checker to update hashes etc:

    ```bash
    flatpak run org.flathub.flatpak-external-data-checker --edit-only org.pdfstitcher.pdfstitcher.json
    ```

3. Run the linter on the manifest:
   ```bash
   flatpak run --command=flatpak-builder-lint org.flatpak.Builder manifest org.pdfstitcher.pdfstitcher.json
   ```

4. Build locally:

    ```bash
    flatpak-builder --force-clean --user --install-deps-from=flathub --install build org.pdfstitcher.pdfstitcher.json 
    ```

5. Run to test:

    ```bash
    flatpak run org.pdfstitcher.pdfstitcher
    ```

6. Open PR to merge changes, cross fingers and hope for the best.