# AntMan
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/cdaf0c6222a44595adfb04a21e65e4f1)](https://www.codacy.com/gh/Neutron-Toolchains/antman/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Neutron-Toolchains/antman&amp;utm_campaign=Badge_Grade)

**[AntMan](https://github.com/Neutron-Toolchains/antman.git)** `(A Nonsensical Toolchain Manager)` is a manager written in bash, It is used by [Neutron Clang](https://github.com/Neutron-Toolchains/clang-build-catalogue) to download/sync, upgrade and manage toolchain builds.

Here's an exmaple on how to sync latest build using AntMan:
```bash
mkdir -p "$HOME/toolchains/neutron-clang"
cd "$HOME/toolchains/neutron-clang"
curl -LO "https://raw.githubusercontent.com/Neutron-Toolchains/antman/main/antman"
./antman -S
```

AntMan can also be ran without actually downloading the script:
```bash
mkdir -p "$HOME/toolchains/neutron-clang"
cd "$HOME/toolchains/neutron-clang"
bash <(curl -s "https://raw.githubusercontent.com/Neutron-Toolchains/antman/main/antman") -S
```

Some basic AntMan commands:
- To sync latest toolchain build. `./antman -S` or `./antman -S=latest`
- To sync a specific toolchain release. `./antman -S=<release tag>`
- To check for updates. `./antman -C`
- To check for updates and sync update. `./antman -U`
- To sync a specific update. `./antman -U=<release tag>`
- To delete synced build. `./antman -D`
- To show information on synced build. `./antman -I`

Run `./antman --help` for more information about all AntMan commands.
