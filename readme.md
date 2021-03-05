# Guide to Google Apps Manager

## Rationale

Our number of chapters is continuously growing and along with it the size of our G Suite. As the number of accounts has surpassed 150, it's becoming increasingly necessary to perform bulk operations for managing user information like group memberships, profile information, email signatures, etc.

[![Chapter map](assets/chapter-map.png)](https://studenten-bilden-schueler.de/standorte)

Google Apps Manager (GAM) is a powerful command line utility with comprehensive batch operations for all manner of G Suite functionality. It's available at <https://github.com/jay0lee/GAM>. Install it by opening a terminal and running

```sh
bash <(curl -s -S -L <https://git.io/install-gam>)
```

`gam` will guide you step by step through the authentication and authorization process.

## Usage Examples

To add multiple (usually newly created) accounts to a group, use a CSV file containing all (and only) the emails to be added to the group in one column:

```sh
gam csv path/to/file.csv gam update group kommunikation@studenten-bilden-schueler.de add member user ~"Email Address [Required]"
```

![Bulk add accounts to group](assets/bulk-add-accounts-to-group.png)

```sh
gam group (schueler|studenten|kommunikation) update photo path/to/image.png
```

![Bulk set profile picture](assets/bulk-set-profile-picture.png)

## Helpful Links

- [GAM docs](https://github.com/jay0lee/GAM/wiki): very detailed and comprehensive
- [StudentenBildenSchueler/gam](https://github.com/StudentenBildenSchueler/gam): link to this repo
- [GAM commands](https://sites.google.com/jis.edu.bn/gam-commands): extensive list of usage examples
- [Google Drive](https://drive.google.com/drive/folders/1FfvgltvxH_fb1ee7efXcXgAZxO4HcBP4): Link to a folder with CSV files for bulk adding new users (requires authentication)