# efi-repo

This is a tool to let you manage your Clover EFI partition in a regular directory.

It is not an installer. Use the Clover installer on disks first. `efidir` tries not to manage files created as part of a basic Clover install.

If you like git, you can clone this repository and then `git add efi; git commit` to version-control EFI. (I strongly suggest that you **not** push any repository with files like `HFSPlus.efi` to GitHub.)

This tool is in alpha. Don't use it on your hard drive's EFI partition until you've tried it out on a USB drive. Actually, don't use it on your hard drive at all yet.

## Usage

```
$ ./efidir pull /Volumes/EFI
$ ls efi
$ ls efi/CLOVER
$ rmdir efi/CLOVER/kexts/10.*
$ cp -r ~/VoodooPS2Controller.kext efi/CLOVER/kexts/Other/
$ ./efidir push /Volumes/EFI
```
