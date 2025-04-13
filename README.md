# Secux Linux Package Repository 📦🐧

Welcome to the official Pacman package repository for **Secux Linux**! 🎉

Secux Linux is a secure Linux distribution 🛡️ based on the powerful and flexible Arch Linux foundation. Our primary focus is enhancing security and providing a robust environment for security-conscious users.

This repository hosts specific packages built, configured, or pre-compiled for Secux Linux.

## Adding the Repository to Pacman ⚙️

If you are not using Secux Linux, to use the packages from this repository, you need to add it to your Pacman configuration file (`/etc/pacman.conf`).

1.  **Edit `/etc/pacman.conf`**:
    Open the file with your favorite text editor (with root privileges):
    ```bash
    sudo nano /etc/pacman.conf
    ```
    (Replace `nano` with `vim`, `micro`, or your preferred editor if needed).

2.  **Add the Repository Entry**:
    Scroll to the bottom of the file and add the following lines.

    ```ini
    [kolbanidze]
    Server = https://kolbanidze.github.io/secux-repo/x86_64/
    ```
    
3.  **Save and Close** the file (Ctrl+X, then Y, then Enter in `nano`).

4.  **Add kolbanidze GPG keys**:
    ```bash
    pacman-key --recv-keys CE48F2CC9BE03B4EFAB02343AA0A42D146D35FCE
    ```

4.  **Synchronize Pacman Databases**:
    Update your local package lists to include the new repository:
    ```bash
    sudo pacman -Syu
    ```

Now you can install packages from the repository using Pacman!

## Adding signing keys

## Available Packages ✨

This repository currently provides the following key packages:

*   **`shim-signed`** 🔑
    *   **Description**: Provides Secure Boot support for Secux Linux. This package contains the signed shim binaries, ported from the Ubuntu deb packages.
    *   **Purpose**: Essential for booting Secux Linux on modern UEFI systems with Secure Boot (Microsoft keys) enabled.

*   **`python-dlib`** 🐍🧠
    *   **Description**: A pre-compiled binary package for the powerful Dlib C++ toolkit's Python bindings.
    *   **Purpose**: Specifically included to support [KIRTapp](https://github.com/KIRT-king/KIRTapp), an application developed by my [partner](https://github.com/KIRT-king). Provides necessary machine learning and computer vision capabilities without requiring lengthy local compilation.

We may add more Secux-specific or pre-compiled packages in the future as needed.

## 🤝 Contributing

Contributions are welcome! If you find bugs or have suggestions, please open an issue on the GitHub repository. Pull requests are also appreciated.

## 📜 License

The individual software packages contained within the repository (`shim-signed`, `python-dlib`, etc.) retain their original upstream licenses.
