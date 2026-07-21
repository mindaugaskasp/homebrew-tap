# mindaugaskasp/homebrew-tap

Homebrew tap for [Diff Bro](https://github.com/mindaugaskasp/diff-bro) — an
offline-only desktop diff viewer.

```bash
brew tap mindaugaskasp/tap
brew install --cask diff-bro
xattr -dr com.apple.quarantine "/Applications/Diff Bro.app"
```

Requires an Apple silicon Mac on macOS 12 (Monterey) or later.

The build is not yet signed or notarized, so macOS quarantines it on install
and may report it as "damaged". The `xattr` line clears that once — Homebrew 6
removed the `--no-quarantine` flag that used to skip it.

`Casks/diff-bro.rb` is generated and republished automatically by the
`homebrew` job in the main repo's release workflow on every tagged release.
Do not edit it by hand — changes belong in `scripts/gen-homebrew-cask.mjs`
upstream.
