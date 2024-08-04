---
title: SMB
---

# Shares

kyuuto-transfer  
Accessible via LAN only (<span class="pathvalue">\\smb.local.gensokyo.zone\kyuuto-transfer</span>) with guest access[^1].
The transfer share used for quick file transfers onto the server for temporary sharing purposes.
Make sure to let someone know when you’ve added something here that should be moved to a media library or organized for some specific service!

<!-- -->

kyuuto-library  
Accessible via LAN only (<span class="pathvalue">\\smb.local.gensokyo.zone\kyuuto-library</span>) with read-only guest access.

The Kyuuto library directory is where most media and shared data belongs.
Adding new files to an appropriate directory will typically automatically add it to the corresponding Plex library or similar.

<!-- -->

kyuuto-library-net  
The [Kyuuto library](#library) share is also available globally via <span class="pathvalue">\\smb.gensokyo.zone\kyuuto-library-net</span>

kyuuto-media  
Top-level access to the disk containing the [Kyuuto library](#library).

shared  
Accessible both via LAN (<span class="pathvalue">\\smb.local.gensokyo.zone\shared</span>) or globally (<span class="pathvalue">\\smb.gensokyo.zone\shared</span>).

A special share used for remote working data, typically used to set up mount points or similar.

Services  
- [Steam Library](./steam.md#library)
- [Steam](./steam.md#setup)
  - [Beat Saber](./steam.md#beatsaber)

opl  
For local use by OPL only.

[^1]: Guest access is available by logging in with a non-existent username and password.
