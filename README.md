<div align="center">
     <h1 align="center">Google Home Theme for Home Assistant</h1>
</div>

A theme and the configuration I have used in Home Assistant that closely resembles the Google Home Application design.
This theme has a light and dark mode to keep inline with the functionality of the Google Home Applications.

This is not for personal use only, as it uses a lot of Google Design features which are their commercial property.

---

> <picture>
>   <source media="(prefers-color-scheme: light)" srcset="https://github.com/Mqxx/GitHub-Markdown/blob/main/blockquotes/badge/light-theme/info.svg">
>   <img alt="Info" src="https://github.com/Mqxx/GitHub-Markdown/blob/main/blockquotes/badge/dark-theme/info.svg">
> </picture><br>
>
> **Please be aware that this repository and instructions held within are still very much Work In Progress**
>
> I am also aware that a fair amount of my configuration and code can be reduced or shortened by use of templates. This is a planned update and will come in due course

---

<div align="left">
  <br>
  <img src="https://img.shields.io/badge/built_for-Home_Assistant-47BFF5?style=for-the-badge"> &nbsp
  <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img src="https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-lightgrey?style=for-the-badge"></a> &nbsp
  <img src="https://img.shields.io/github/downloads/beecho01/Google-Home-Theme-For-Home-Assistant/total?style=for-the-badge"> &nbsp
  <img src="https://img.shields.io/github/v/release/beecho01/Google-Home-Theme-For-Home-Assistant?style=for-the-badge"> &nbsp
  <img src="https://img.shields.io/github/size/beecho01/Google-Home-Theme-For-Home-Assistant/dist%2Fmaterial-symbols.js?style=for-the-badge"> &nbsp
  <img src="https://img.shields.io/github/last-commit/beecho01/Google-Home-Theme-For-Home-Assistant?style=for-the-badge"> &nbsp
  <img src="https://img.shields.io/github/issues-closed/beecho01/Google-Home-Theme-For-Home-Assistant/icon%20request?label=community%20requests&style=for-the-badge">
  <br>
  <br>
</div>

## Table of contents

- [Installation](#installation)
- [Usage and Preview](#usage-and-preview)
- [Troubleshooting](#Troubleshooting)
- [Community](#community)
- [Thanks](#thanks)
- [Copyright and license](#copyright-and-license)

---

## <a name="installation"></a>Installation

This Theme uses a fair amount of pre-requist resources to function as desired. Please make sure to install the following using the methods designated by their individual installation guides:
- [Button Card by RomRider](https://github.com/custom-cards/button-card)
- [Material Symbols for Home Assistant](https://github.com/beecho01/material-symbols)
- [Lovelace swipe card](https://github.com/bramkragten/swipe-card)
- [card-mod 3](https://github.com/thomasloven/lovelace-card-mod)
- [Big Slider Card](https://github.com/nicufarmache/lovelace-big-slider-card)
- [auto-entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Frigate Lovelace Card](https://github.com/dermotduffy/frigate-hass-card)
- [Search Card](https://github.com/postlund/search-card)

Unfortunately Google Home Theme for Home Assistant has not yet been accepted into the [Home Assistant Community Store (HACS)](https://hacs.xyz) default list yet.

However, you can, add this repository via a few methods:

### My Home Assistant Link (Recommended):
<a href="https://my.home-assistant.io/redirect/hacs_repository/?owner=beecho01&category=Lovelace&repository=Google-Home-Theme-For-Home-Assistant" target="_blank"><img src="https://my.home-assistant.io/badges/hacs_repository.svg" alt="Open your Home Assistant instance and open a repository inside the Home Assistant Community Store." /></a>

### Add HACS Custom Repository:
To install follow the below steps:

- Open HACS (installation instructions are [here](https://hacs.xyz/docs/installation/installation/)).
- Open the menu in the upper-right and select "Custom repositories".
- Enter the repository:
```
https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant
```
- Select the category "Lovelace".
- Select "ADD".
- Open your "configuration.yaml" via File editor or other means.
- Add the following (if it does not already exist), save and restart Home Assistant.
```
frontend:
  themes: !include_dir_merge_named themes
```

### Manual:
- Create the folder `Google_Home` into your `/homeassistant/themes/` folder.
- Upload the file `google_home.yaml` to the newly created folder `/homeassistant/themes/Google_Home`
- Add the following (if it does not already exist), save and restart Home Assistant.
```
frontend:
  themes: !include_dir_merge_named themes
```
- Save, restart Home Assistant.

---

## <a name="usage-and-preview"></a>Usage and Preview
I have done my best to break down each individual page/view I have created and the necessary configuration and and components I have used.
Please be aware that some methods I have used to gain access to Home Assitant components may not work for yourself and I hope methods that work for you can be found within the [Home Assistant Community Forum](https://community.home-assistant.io/).

### Favourites

This pertains to the Favourites View or the default view in the configuration

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 2 - Line 858` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L2-L858) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Favourites/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Favourites/Image2.png' width='250'> |

### Devices

This pertains to the Devices View. This is a self-populating page for each Area defined within.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 859 - Line 3965` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L859-L3965) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Devices/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Devices/Image2.png' width='250'> |

### Automations

This pertains to the Automations View. This is a self-populating page for each Automation that exists and a way to create new ones.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 3966 - Line 4402` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L3966-L4402) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Automations/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Automations/Image2.png' width='250'> |

### Activity

This pertains to the Activity View. This is a log of each activity for the domains: switch, light, climate annd camera.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 4403 - Line 4466` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L4403-L4466) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Activity/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Activity/Image2.png' width='250'> |

### Settings

This pertains to the Settings View.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 4467 - Line 5586` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L4467-L5586) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Settings/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Settings/Image2.png' width='250'> |

### Updates

This pertains to the Updates View. This shows sensors and notifications for updates from within HACs and HA itself.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 5587 - Line 6038` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L5587-L6038) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Updates/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Updates/Image2.png' width='250'> |

### Network

This pertains to the Network View.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 6039 - Line 6513` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L6039-L6513) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network/Image2.png' width='250'> |

### Network Devices

This pertains to the Network Devices sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 6514 - Line 6742` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L6514-L6742) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network%20Devices/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network%20Devices/Image2.png' width='250'> |

### Network Points

This pertains to the Network Points sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 6743 - Line 6781` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L6743-L6781) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network%20Points/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Network%20Points/Image2.png' width='250'> |

### Connected Devices

This pertains to the Connected Devices sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 6782 - Line 7133` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L6782-L7133) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Connected%20Devices/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Connected%20Devices/Image2.png' width='250'> |

### Share Password

This pertains to the Share Password sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 7134 - Line 7276` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L7134-L7276) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Share%20Password/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Share%20Password/Image2.png' width='250'> |

### Lighting

This pertains to the Lighting sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 7277 - Line 7634` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L7277-L7634) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Lighting/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Lighting/Image2.png' width='250'> |

### Cameras

This pertains to the Cameras sub-view.

| Code Snippet Lines | Link to Configuration |
| --- | --- |
| `Line 7635 - Line 7737` | [Link](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/View-Configuration.yaml?plain=1#L7635-L7737) |

| Application Reference | Home Assistant View |
| --- | --- |
| <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Cameras/Image1.png' width='250'> | <img src='https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/blob/main/Images/Cameras/Image2.png' width='250'> |


## <a name="Troubleshooting"></a>Troubleshooting

### Can't see the icons?
If you cannot see the new icons, or you get an empty box where you're expecting an icon, clear you brpwser cache and reload the Home Assistant interface.

### Icons don't show on first load of the dash?
Did you add the resource in your configuration.yaml? See the [installation section](#installation) for details.

---

### <a name="community"></a>Community
There's a thread over at the [home assistant forums](https://community.home-assistant.io/t/material-symbols-for-home-assistant/599573) that tracks this repo.

---

## <a name="thanks"></a>Thanks
- Big thanks to @Nerwyn for the inspiration for this repository and work he's undertaken so far in his own [repository](https://github.com/Nerwyn/material-rounded-theme).

### Stargazers
[![Stargazers repo roster for @beecho01/Google-Home-Theme-For-Home-Assistant](https://reporoster.com/stars/beecho01/Google-Home-Theme-For-Home-Assistant)](https://github.com/beecho01/Google-Home-Theme-For-Home-Assistant/stargazers)

---

### <a name="copyright-and-license"></a>Copyright and license

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].
I do this for fun, without charge, and to give back to the community. You may remix, tweak, and build upon this work non-commercially, as long as you credit the original author, provide a link to the license, and indicate if any changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use unless agreed. If you remix, transform or build upon the material, you must distribute your contributions under the same or compatible license as the original. 
