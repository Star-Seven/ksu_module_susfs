# A KernelSU module for SUS-FS patched kernel #

This module installs a userspace helper tool called **ksu_susfs** and **sus_su** into /data/adb/ and provides a script to communicate with SUS-FS kernel.
This module provides root hiding for KernelSU on the kernel level.

## Notes
- Make sure you have a custom kernel with SUS-FS patched in it. Check the custom kernel source to see if it has SUS-FS.
- Make sure the kernel is using SUS-FS 1.4.2 for effective hide.
- Do not mix/install with other root-hiding modules such as shamiko or zygisk assistant.
- HideMyApplist is acceptable
- Revanced root module compatible
- Recommended to use [my fork of systemless-hosts-KernelSU-module by symbuzzer](https://github.com/sidex15/systemless-hosts-KernelSU-module) if you want to use systemless hosts

## Adding ro.boot.vbmeta.digest value
This module will now have a directory called `VerifiedBootHash` in `/data/adb` containing `VerifiedBootHash.txt` for users with missing `ro.boot.vbmeta.digest` value to prevent partition modified and abnormal boot state detection. 
- Copy your VerifiedBootHash in the Key Attestation demo and paste it to `/data/adb/VerifiedBootHash/VerifiedBootHash.txt`

## Credits
susfs4ksu: https://gitlab.com/simonpunk/susfs4ksu/
