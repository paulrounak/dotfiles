# Dotfiles
### Feel free to use these dotfiles as you wish! Drop a star if you like it!

# Rice Demo
![10-06-2024-11-40-32](https://github.com/duckyfied/dotfiles/assets/172433021/f4480c6f-9907-4b42-8c5e-e528e659b600)


![11-06-2024-15-14-10](https://github.com/duckyfied/dotfiles/assets/172433021/4c830b36-7029-4f2a-82ff-0a5bc0fbb14a)



# Installation
1. Clone this repository.
    ```sh
    git clone https://github.com/paulrounak/dotfiles.git
    ```

2. Install an AUR helper (for example, `yay` in `"$HOME"/.srcs`).
    ```sh
    git clone https://aur.archlinux.org/yay.git "$HOME"/.srcs/yay
    cd "$HOME"/.srcs/yay/ && makepkg -si
    ```

3. Install dependencies.
    ```sh
    yay -S --needed acpi alsa-utils base-devel curl git pulseaudio pulseaudio-alsa xorg xorg-xinit alacritty btop code dunst feh ffcast firefox i3-gaps i3lock-color i3-resurrect libnotify light mpc mpd ncmpcpp nemo neofetch neovim oh-my-zsh-git pacman-contrib papirus-icon-theme pfetch picom polybar ranger rofi scrot slop xclip zathura zathura-pdf-mupdf zsh
    ```

4. Create default directories.
    ```sh
    mkdir -p "$HOME"/.config
    mkdir -p "$HOME"/Pictures/wallpapers
    mkdir -p  /usr/local/bin
    mkdir -p  /usr/share/themes
    ```

 5. Copy configs, scripts, fonts, wallpaper, vsc configs, zsh config.
    ```sh
    cp -r ./config/* "$HOME"/.config
    cp -r ./wallpapers/* "$HOME"/Pictures/wallpapers
    cp ./.zshrc "$HOME"
    sudo cp -r ./scripts/* /usr/local/bin
    sudo cp -r ./fonts/* /usr/share/fonts
    sudo cp ./paul.zsh-theme /usr/share/oh-my-zsh/custom/themes
    ```
6. Make Light executable, set zsh as default shell, refresh font cache.
    ```sh
    sudo chmod +s /usr/bin/light
    chsh -s /bin/zsh
    sudo chsh -s /bin/zsh
    fc-cache -fv
    ```

7. Install gtk theme.
    ```sh
    mkdir -p "$HOME"/.config/gtk-4.0
    git clone https://github.com/Fausto-Korpsvart/Rose-Pine-GTK-Theme
    sudo cp -r ./Rose-Pine-GTK-Theme/themes/RosePine-Main-BL  /usr/share/themes/RosePine-Main
    sudo cp -r ./Rose-Pine-GTK-Theme/themes/RosePine-Main-BL/gtk-4.0/* "$HOME"/.config/gtk-4.0
    ```

# Keybinds

These are the basic keybinds. Read through the [i3](./config/i3/config) config for more keybinds.

Note: `Win` refers to the `Super/Mod` key.

|        Keybind         |                 Function                 |
| ---------------------- | ---------------------------------------- |
| `Win + Enter`          | Launch terminal (alacritty)              |
| `Win + Shift + Q`      | Close window                             |
| `Win + Q`              | Stacking layout                          |
| `Win + W`              | Tabbed layout                            |
| `Win + E`              | Default layout                           |
| `Win + R`              | Resize mode                              |
| `Win + T`              | Restore layout                           |
| `Win + Y`              | Save layout                              |
| `Win + A`              | Rofi open windows menu                   |
| `Win + S`              | Rofi full menu                           |
| `Win + D`              | Rofi menu                                |
| `Win + Z`              | Rofi bookmarks                           |
| `Win + X`              | Rofi powermenu                           |
| `Win + C`              | Rofi screenshot script                   |
| `Win + G`              | Gaps settings                            |
| `Win + V`              | Set vertical orientation                 |
| `Win + H`              | Set horizontal orientation               |
| `Win + I`              | Lock screen                              |
| `Win + O`              | Show polybar                             |
| `Win + P`              | Hide polybar                             |
| `Win + B`              | Move workspace to another monitor        |
| `Win + N`              | Dual monitor mode                        |
| `Win + M`              | Single monitor mode                      |
| `Win + arrows (jkl;)`  | Resizing, moving windows                 |
| `Win + Shift + E`      | Exit i3                                  |
| `Win + Shift + R`      | Restart i3                               |

## Troubleshooting

If some of the polybar modules are not working:

    - Try changing the variables.
    - Open the polybar configuration `"$HOME"/.config/polybar/config.ini`.
    - Found `; Change it for yourself` line.
    - Follow the commands that are written below the `; Change it for yourself` line.
