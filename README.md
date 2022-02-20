# Repo Layout

- `hosts/` - Machines/Hardware definitions.

- `mixins/` - Dotfiles/Configurations. Instead of imperatively configuring
  `/etc/` or `~/.config`, everything in here is written in Nix instead. This
  nix code implements the changes I want that would traditionally be done by
  modifying something in `/etc/` or `~/.config` using `vim`.

- `modules/` - [Modules](https://nixos.wiki/wiki/Module) that aren't in nixpkgs
  that I want to hack on.

- `pkgs/` -
  [Packages/Derivations](https://nixos.org/manual/nix/unstable/expressions/derivations.html)
  that aren't in nixpkgs that I want to hack on.

- `profiles/` - Configurations that are often comprised of mixins that are
  intended to be imported into a given system.

- `secrets/` - [`age`](https://github.com/FiloSottile/age) encrypted secrets,
  made possible by [`agenix`](https://github.com/ryantm/agenix)

- `environments/` - Environments/Shells for things I need to work with, such as
  [Yocto](https://www.yoctoproject.org/).

- `users/` - [home-manager](https://github.com/nix-community/home-manager) configuration per user.

- `examples` - Things I don't necessarily want to use, but want to keep around
  and link to people online.
