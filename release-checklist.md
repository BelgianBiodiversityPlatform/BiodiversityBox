# Checklist for releases

- Make sure RAM is set to 2Gb
- Make sure network/file shares are removed
- Make free space with `$ paccache -r` and `pacman -Rns $(pacman -Qtdq)`
- Update changelog
- When exporting in VB, sets:
    - Name: BiodiversityBox
    - Product URL: https://github.com/BelgianBiodiversityPlatform/BiodiversityBox
    - Vendor: Belgian Biodiversity Platform
    - Version: YYYY-MM-DD
- Make sure the link is updated (!2 places) in README.md
- Twitter announcement
