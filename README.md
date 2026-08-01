# LumiChats Desktop — Releases

Installers for **[LumiChats Desktop](https://lumichats.com/desktop)**. This
repository holds release binaries and nothing else — the application source is
not open and is not here.

**Download the latest version from [lumichats.com/downloads](https://lumichats.com/downloads).**

## Why this repository exists

Installed copies of LumiChats update themselves, and they read the update feed
from the Releases on this repository. It is public because that is what lets the
updater work without shipping a credential inside the app — a token embedded in
a desktop application is a token every user has.

## Each release contains

| File | What it is |
|---|---|
| `LumiChats-Setup-<version>.exe` | The Windows installer |
| `SHA256SUMS.txt` | Checksums, so you can verify what you downloaded |
| `latest.yml` | The update feed. Read by the app, not by people. |
| `*.blockmap` | Lets updates download only the changed parts |

## These builds are not code-signed yet

Windows SmartScreen will show an "unrecognised app" screen. Choose **More info**,
then **Run anyway**.

That warning is about who vouched for the file, not about what the file does —
but you have no way to tell that from the dialog, which is exactly why it is
written here. A code-signing certificate has to be bought from a certificate
authority and this one is not funded yet.

If you would rather check the download yourself:

```powershell
Get-FileHash LumiChats-Setup-*.exe -Algorithm SHA256
```

Compare the result with `SHA256SUMS.txt` on the release.

## Reporting a problem

Security issues: **security@lumichats.com**
Everything else: **support@lumichats.com**

Documentation lives at [lumichats.com/desktop](https://lumichats.com/desktop).
