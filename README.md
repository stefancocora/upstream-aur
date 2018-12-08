# aur


## docs
- https://wiki.archlinux.org/index.php/Arch_User_Repository#Sharing_and_maintaining_packages
- steps: most steps for each pkg
  - once: create ssh key_pair
  - once:  update AUR with this pub key
  - [ ] ~~create a new empty(most of the time) git repo for your pkg~~ Better yet add these as submodules `git submodule add -b master git+ssh://aur@aur.archlinux.org/kubeless.git`
    - gets cloned from upstream and might not be empty.
  - [ ] setup gpg signing for commits ( inside each pkg maintained )
    - use CC7911F4AFE1C6C2 for signing
  - [ ] add .SRCINFO and PKGBUILD to the repo
  - [ ] git stage => commit => push to upstream origin
  - [ ] vote for this pkg
    - https://wiki.archlinux.org/index.php/Arch_User_Repository#How_can_I_vote_for_packages_in_the_AUR?
    - through AUR web UI
    - using cli: aurvote / aurvote-git
    - using openssh: "ssh aur@aur.archlinux.org vote kubeless-bin"


