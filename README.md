# msg-GrapheneOS-test

Custom GrapheneOS builds featuring **custota** integration for seamless OTA updates. These builds allow you to switch between different variants without requiring a data wipe.

## Available Variants

| Variant | Description |
| :--- | :--- |
| **Clean** | A "vanilla" experience that mimics the official GrapheneOS release, with the only addition being `custota` support. |
| **Custom** | Includes experimental enhancements, such as Work-In-Progress (WIP) application isolation. |
| **Rooted** | Includes **KernelSU (SukiSU)** + **SUSFS** and custom changes. Features a unique "on-demand" root mechanism. |

-----

## On-Demand Root (Rooted Variant)

The Rooted variant is designed with a "security-first" approach. Root functionality is not active by default; it must be explicitly triggered during the boot process.

### How to Activate Root

1.  Reboot the device.
2.  When the **GrapheneOS logo** appears, press **Volume Up**.
3.  If the button is not pressed, the kernel will boot without exposing any root functionality.

### Why On-Demand?

  * **Security:** Prevents persistent root access from being exploited by background processes when not needed.
  * **Stealth:** If the phone reboots automatically, it returns to a non-rooted state.
  * **Maintenance:** Easily enable root only when you need to perform specific tasks, such as full backups (e.g., using **NeoBackup**) or system-level configurations.

### Managing Permissions

To manage root access, you must boot with root enabled and install the **[SukiSU Manager APK](https://github.com/SukiSU-Ultra/SukiSU-Ultra)**.

  * **Granular Control:** KernelSU allows you to grant only the specific capabilities an app requires (e.g., granting Network Admin to a firewall without granting full file system access).
  * **Minimal Footprint:** The manager app is only required to configure profiles. Once permissions are granted, you can uninstall the manager; the kernel will remember the settings.

-----

## Installation & Updates

These builds utilize **custota** for OTA (Over-The-Air) installations.

  * **Switching Variants:** You can move between Clean, Custom, and Rooted variants freely. **No data wipe is required** when switching between these specific builds.
  * **Kernel Modules:** For manual flashing of `dlkm` files, ensure you utilize `fastboot` mode.

-----

### Credits & Resources

  * [GrapheneOS](https://grapheneos.org/)
  * [custota](https://www.google.com/search?q=https://github.com/GrapheneOS/custota)
  * [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra)
  * [SUSFS](https://gitlab.com/simonpunk/susfs4ksu)

-----

