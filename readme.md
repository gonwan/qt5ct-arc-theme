# qt5ct-arc-theme
Color schemes of arc-theme, work in qt5ct & qt6ct.

### Install

Copy those 2 file into `~/.config/qt5ct/color`, open `qt5ct`:
- Go to Appearance --> Platte --> Check custom and select arc.
- Go to Fonts --> Select your Gnome/Cinnamon font.
- Go to Icon Theme --> Select your Gnome/Cinnamon icon theme.
- Edit `~/.config/qt5ct/qt5ct.conf`, change `standard_dialogs=default` to `standard_dialogs=gtk3`.
- Add to `~/.profile`:
```bash
export QT_AUTO_SCREEN_SCALE_FACTOR=1
export QT_QPA_PLATFORMTHEME=qt5ct
#export QT_STYLE_OVERRIDE=
#export QT_DEBUG_PLUGINS=1
```

![vlc_default](doc/vlc_default.png)

![vlc_themed](doc/vlc_themed.png)

### Alternatives

|         | has theme? | has style? | QT_QPA_PLATFORMTHEME | QT_STYLE_OVERRIDE     | Description                                                  |
| ------- | ---------- | ---------- | -------------------- | --------------------- | ------------------------------------------------------------ |
| Gtk2    | Yes        | Yes        | gtk2                 | gtk2 or empty         | Good for widgets, indicators in radio button and checkbox can be styled, follows current Gtk theme. But It has HiDPI issues, and not certianly not maintained. |
| Gtk3    | Yes        | No         | gtk3 or empty        | style values in qt5ct | No style plugin. Fusion is used by default, which is not consistent with other themed Gtk applications. |
| qt5ct   | Yes        | Yes        | qt5ct                | style values in qt5ct | No style plugin, Fusion is used by default, which is not consistent with other themed Gtk applications. Color scheme and font can be further customized. Button indicators are not styled. |
| Kvantum | Yes        | Yes        | qt5ct                | kvantum               | Use Kvantum Manager to further customize the theme. Button indicators are styled. KvArc theme is provided, but is still somehow different in visual. Kvantum also installs several KDE component, which is odd. |

