# mindaugaskasp/homebrew-tap

Homebrew tap for [Diff Bro](https://github.com/mindaugaskasp/diff-bro) — an
offline-only desktop diff viewer.

```bash
brew tap mindaugaskasp/tap
brew install --cask diff-bro
```

Requires an Apple silicon Mac on macOS 12 (Monterey) or later.

The build is not yet signed or notarized. The cask clears macOS's quarantine
flag after install, so it opens without being reported as "damaged". If it
still is (an install made before the cask did this), clear it once:

```bash
xattr -dr com.apple.quarantine "/Applications/Diff Bro.app"
```

`Casks/diff-bro.rb` is generated and republished automatically by the
`homebrew` job in the main repo's release workflow on every tagged release.
Do not edit it by hand — changes belong in `scripts/gen-homebrew-cask.mjs`
upstream.
