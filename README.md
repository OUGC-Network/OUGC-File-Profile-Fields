<p align="center">
    <a href="" rel="noopener">
        <img width="700" height="400" src="https://github.com/OUGC-Network/OUGC-File-Profile-Fields/assets/1786584/497e34d3-abda-41b2-9b4d-c640c648cd06" alt="Project logo">
    </a>
</p>

<h3 align="center">OUGC File Profile Fields</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/OUGC-Network/OUGC-File-Profile-Fields.svg)](./issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/OUGC-Network/OUGC-File-Profile-Fields.svg)](./pulls)
[![License](https://img.shields.io/badge/license-GPL-blue)](/LICENSE)

</div>

---

<p align="center"> Maximize your profile with custom file profile fields.
    <br> 
</p>

## 📜 Table of Contents <a name = "table_of_contents"></a>

- [About](#about)
- [Getting Started](#getting_started)
    - [Dependencies](#dependencies)
    - [File Structure](#file_structure)
    - [Install](#install)
    - [Update](#update)
    - [Template Modifications](#template_modifications)
- [Settings](#settings)
- [Usage](#usage)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)
- [Support & Feedback](#support)

## 🚀 About <a name = "about"></a>

With File Profile Fields, users can easily upload files to their profiles using custom profile fields, making their
profiles more dynamic and personalized. Admins can manage the types of files allowed for each field, even restricting to
images only if needed. Plus, you can style the presentation of files on a per-field basis to match your forum's look.
Maximize your profile potential with this plugin – it's the perfect way to add a unique touch and functionality to your
MyBB profiles!

[Go up to Table of Contents](#table_of_contents)

## 📍 Getting Started <a name = "getting_started"></a>

The following information will assist you into getting a copy of this plugin up and running on your forum.

### Dependencies <a name = "dependencies"></a>

A setup that meets the following requirements is necessary to use this plugin.

- [MyBB](https://mybb.com/) >= 1.8
- PHP >= 7.0
    - WebP Image Support requires PHP >= 7.1
- [PluginLibrary for MyBB](https://github.com/frostschutz/MyBB-PluginLibrary) >= 13

### File structure <a name = "file_structure"></a>

  ```
   .
   ├── inc
   │ ├── languages
   │ │ ├── english
   │ │ │ ├── admin
   │ │ │ │ ├── ougc_fileprofilefields.lang.php
   │ │ │ ├── ougc_fileprofilefields.lang.php
   │ ├── plugins
   │ │ ├── ougc
   │ │ │ ├── FileProfileFields
   │ │ │ │ ├── templates
   │ │ │ │ │ ├── modcp.html
   │ │ │ │ │ ├── modcp_files_file.html
   │ │ │ │ │ ├── modcp_multipage.html
   │ │ │ │ │ ├── modcp_status_mod.html
   │ │ │ │ │ ├── postbit_status.html
   │ │ │ │ │ ├── profile_status_mod.html
   │ │ │ │ │ ├── usercp_status.html
   │ │ │ │ │ ├── modcp_file.html
   │ │ │ │ │ ├── modcp_filter_option.html
   │ │ │ │ │ ├── modcp_nav.html
   │ │ │ │ │ ├── modcp_update.html
   │ │ │ │ │ ├── postbit_status_mod.html
   │ │ │ │ │ ├── usercp.html
   │ │ │ │ │ ├── usercp_status_mod.html
   │ │ │ │ │ ├── modcp_file_thumbnail.html
   │ │ │ │ │ ├── modcp_logs.html
   │ │ │ │ │ ├── modcp_page.html
   │ │ │ │ │ ├── postbit.html
   │ │ │ │ │ ├── profile_file.html
   │ │ │ │ │ ├── usercp_file.html
   │ │ │ │ │ ├── usercp_update.html
   │ │ │ │ │ ├── modcp_files.html
   │ │ │ │ │ ├── modcp_logs_empty.html
   │ │ │ │ │ ├── modcp_remove.html
   │ │ │ │ │ ├── postbit_file.html
   │ │ │ │ │ ├── profile_file_thumbnail.html
   │ │ │ │ │ ├── usercp_file_thumbnail.html
   │ │ │ │ │ ├── modcp_files_empty.html
   │ │ │ │ │ ├── modcp_logs_log.html
   │ │ │ │ │ ├── modcp_status.html
   │ │ │ │ │ ├── postbit_file_thumbnail.html
   │ │ │ │ │ ├── profile_status.html
   │ │ │ │ │ ├── usercp_remove.html
   │ │ │ │ ├── admin.php
   │ │ │ │ ├── admin_hooks.php
   │ │ │ │ ├── core.php
   │ │ │ │ ├── forum_hooks.php
   │ │ ├── ougc_fileprofilefields.php
   ├── ougc_fileprofilefields.php
   ```

### Installing <a name = "install"></a>

Follow the next steps in order to install a copy of this plugin on your forum.

1. Download the latest package from the [MyBB Extend](https://community.mybb.com/mods.php?action=view&pid=399) site or
   from the [repository releases](https://github.com/OUGC-Network/OUGC-File-Profile-Fields/releases/latest).
2. Upload the contents of the _Upload_ folder to your MyBB root directory.
3. Browse to _Configuration » Plugins_ and install this plugin by clicking _Install & Activate_.

### Updating <a name = "update"></a>

Follow the next steps in order to update your copy of this plugin.

1. Browse to _Configuration » Plugins_ and deactivate this plugin by clicking _Deactivate_.
2. Follow step 1 and 2 from the [Install](#install) section.
3. Browse to _Configuration » Plugins_ and activate this plugin by clicking _Activate_.

### Template Modifications <a name = "template_modifications"></a>

This plugin requires no template edits.

[Go up to Table of Contents](#table_of_contents)

## 🛠 Settings <a name = "settings"></a>

Below you can find a description of the plugin settings.

### Global Settings

- **Moderator Groups** `select`
    - _Select which groups are allowed to manage files approval status and logs from the ModCP._
- **Items Per Page** `numeric`
    - _Default files and logs to display per page in the ModCP._
- **Moderate Groups** `select`
    - _You can moderate the files of specific groups, so their files will be visible only after they have been
      approved._
- **Image Auto Resize** `yesNo`
    - _Turn this on to automatically resize image files to fit their maximum dimensions setting._
- **Download Count Interval** `numeric`
    - _Set the amount of seconds between download increase from the same users (not guests). Set to 0 to always count._
- **Count Author Downloads** `yesNo`
    - _You can skip authors from increasing the download count of files. Please note that download logs are always
      stored for non thumbnails regardless of this setting._
- **Force File Downloads** `yesNo`
    - _By default specific file types (png, pdf, txt, etc.) are rendered in browser. If you enable this files will be
      forced to be downloaded instead._

[Go up to Table of Contents](#table_of_contents)

## 📖 Usage <a name="usage"></a>

### File Permissions

For automatic file edits the following files require to be chmod 777 (on *nix servers).

- modcp.php
- usercp.php
- member.php
- inc/functions_post.

This plugin has no additional configurations; after activating make sure to modify the global settings in order to get
this plugin working.

[Go up to Table of Contents](#table_of_contents)

## ⛏ Built Using <a name = "built_using"></a>

- [MyBB](https://mybb.com/) - Web Framework
- [MyBB PluginLibrary](https://github.com/frostschutz/MyBB-PluginLibrary) - A collection of useful functions for MyBB
- [PHP](https://www.php.net/) - Server Environment

[Go up to Table of Contents](#table_of_contents)

## ✍️ Authors <a name = "authors"></a>

- [@Omar G](https://github.com/Sama34) - Idea & Initial work

See also the list of [contributors](https://github.com/OUGC-Network/OUGC-File-Profile-Fields/contributors) who
participated in this project.

[Go up to Table of Contents](#table_of_contents)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- [The Documentation Compendium](https://github.com/kylelobo/The-Documentation-Compendium)

[Go up to Table of Contents](#table_of_contents)

## 🎈 Support & Feedback <a name="support"></a>

This is free development and any contribution is welcome. Get support or leave feedback at the
official [MyBB Community](https://community.mybb.com/thread-221815.html).

Thanks for downloading and using our plugins!

[Go up to Table of Contents](#table_of_contents)