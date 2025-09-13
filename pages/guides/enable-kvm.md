### How to enable Virtualization (KVM)

To run Windows applications efficiently on your Linux system using WinBoat, you need to enable Virtualization (KVM) in your BIOS/UEFI settings. Here’s how you can do that:
1. **Restart your computer** and enter the BIOS/UEFI settings. This is usually done by pressing a key such as `F2`, `F10`, `Delete`, or `Esc` during the initial boot screen. The specific key may vary depending on your computer's manufacturer, so refer to your computer's manual if you're unsure.
2. **Locate the Virtualization settings**. This is typically found under sections like `Advanced`, `CPU Configuration`, `System Configuration`, or `Security`.
3. **Enable the Virtualization option**. Change the setting to `Enabled`.
4. **Save your changes and exit** the BIOS/UEFI settings.
5. **Boot into your Linux operating system** and verify that KVM is enabled by running the following command in the terminal:
   ```bash
   egrep -c '(vmx|svm)' /proc/cpuinfo
   ```
If the output is greater than `0`, KVM is enabled and you are ready to use WinBoat!