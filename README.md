# PDFStitcher Flatpak
This is the Flatpak repository for PDFStitcher. To see the source code, visit the [PDFStitcher repository](https://github.com/cfcurtis/pdfstitcher).

## Flatpak Permissions
By default, this Flatpak requests permission to access files in the user's Desktop, Documents, and Downloads directories, as well as `/mnt`, `/media`, and `/run/media`. This allows PDFStitcher to access files on the user's computer, as well as files on external drives and network shares mounted in common locations. FlatHub no longer allows blanket access to the user's home, so these locations were chosen as the most likely places for PDF documents.

If you would like to access files in different locations (e.g. for a custom network share mount point), try installing [Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal) and modifying the permissions for PDFStitcher, or use `flatpak override` to grant additional permissions.