# Homebrew tap for Halo

[Halo](https://github.com/tharunS123/Halo) is local push-to-talk dictation for
macOS. Hold F9, speak, let go — clean text lands at your cursor in any app.
Your audio never leaves your Mac.

```bash
brew tap tharuns123/halo
brew trust tharuns123/halo
brew install halo
halo setup
```

Homebrew 7 will not load a formula from a third-party tap until you trust it,
so `brew trust` is required — without it `brew install` stops with "Refusing to
load formula ... from untrusted tap". The build instructions it is asking you
to vouch for are in [Formula/halo.rb](Formula/halo.rb).

Requires an Apple Silicon Mac on macOS 14 or newer.

This tap builds Halo from source on your machine. That is deliberate: a
downloaded app bundle would carry `com.apple.quarantine`, and Halo is signed
ad-hoc rather than with a paid Apple Developer ID, so macOS would refuse it
outright as "damaged". Building locally means there is no Gatekeeper prompt at
all.

Issues and pull requests belong on the
[main repository](https://github.com/tharunS123/Halo).
