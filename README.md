# Alien Response Callouts updates

Public update information for **Alien Response Callouts**, by **Alien (Mattia C.)**.

The mod checks this repository once when it loads. It contains version information only; it does not distribute the plugin or its source code.

[Download Alien Response Callouts on LCPDFR](https://www.lcpdfr.com/downloads/gta5mods/scripts/55757-alien-response-callouts/) · [Support Alien](https://ko-fi.com/alienita)

## Stable update — red notice

1. Publish the tested mod package on the download page first.
2. Edit `version.txt` on the `main` branch to contain only the new stable version, such as `1.2.1` or `1.3`.
3. Commit the change. Players with older compatible versions and update checks enabled will see a notice the next time the mod loads.

Do not put beta or upcoming version numbers in `version.txt`.

## Upcoming version — orange notice

Edit `announcements.txt` and set `UpcomingVersion` to the version being developed. For example:

```ini
UpcomingVersion=1.3
BetaVersion=
```

Players see that v1.3 is coming soon. This does not claim that it is available to download.

## Public beta — purple notice

First make the beta available on the LCPDFR download page, clearly labelled as a test build. Then set `BetaVersion` in `announcements.txt`. For example:

```ini
UpcomingVersion=
BetaVersion=1.3
```

Players see that a v1.3 beta is available. Use a numeric value such as `1.3`, not `1.3-beta`; the notification adds the beta label.

## Disabling announcements

Leave both values empty:

```ini
UpcomingVersion=
BetaVersion=
```

Clear a beta or upcoming value when it is cancelled or released. Old announcements are also ignored automatically once that version has been installed or published as stable.

## Behavior and settings

- At most one notice appears per mod load: stable update first, then beta, then upcoming.
- News must name a version newer than both the installed version and the stable version.
- The installed version shown in an update notice comes from the loaded mod.
- Stable update checks are supported from v1.2. Upcoming and beta notices require v1.2.1 or newer; older DLLs cannot gain this feature from a repository edit alone.
- `ShowReleaseAnnouncements=false` hides beta/upcoming news and skips that request, while retaining stable update checks.
- `CheckForUpdates=false` disables all of these checks.
- Invalid or unavailable announcement data does not disable stable update notices. If the stable version cannot be checked, all notices are skipped for that load.
- GitHub may cache edits for a few minutes. Reload the mod after the public raw files show the saved values.
- Requests have a short timeout and do not block gameplay. Nothing is downloaded or installed automatically.

Keep this repository public and keep the file paths unchanged. Version values must contain only 2–4 numeric components. Both announcement fields are optional; an empty value disables that notice.
