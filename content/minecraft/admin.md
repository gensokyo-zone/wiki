---
title: "Minecraft Administration"
---

# Admin Console

Running a command is currently a bit awkward:

```bash
echo /asdf > /run/minecraft-java/stdin
```

... and any output ends up in journald logs.

# Imperative Updates

```bash
sudo -u minecraft-bedrock env -C /mnt/shared/minecraft/java/marka-server ./update.sh
```
