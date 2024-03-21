# dqx_en_launcher

Modifies the DQX launcher with a number of English assets to make for a more readable experience to an English audience.

# ci

This builds on pushes to main and tags.

On pushes to main, check the GHA logs for the "Build launcher exe" step and make sure the log output looks OK. For tags, this will build and create a new release, attaching the modified executable to the release.

# updating

- Open a PR and replace `DQXLauncher.exe` in the `assets` folder with the latest launcher
- Merge PR and verify that the executable built (check the previous GHA logs)
- Cut a new tag, which will publish a new release

# development

You can build this locally, but the asset swaps for the two ETPs folders in `assets/ETP` are only done in CI. This only builds locally with the ETPs that were already in the executable.

To run:

```powershell
cd app
port_assets.bat
```

This will spit out a `DQXLauncher.log` file, and if successful, a `DQXLauncher.exe` in the `app` directory.
