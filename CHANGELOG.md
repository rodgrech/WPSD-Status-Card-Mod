# Changelog

## 0.1.10 - 2026-05-23

- Added repository icon/logo assets for HACS presentation.
- Added a custom-card picker icon fallback.

## 0.1.9 - 2026-05-23

- Updated the README dashboard screenshot with the polished MCS2000 and R7
  card layout.

## 0.1.8 - 2026-05-23

- Slimmed the R7 card proportions.
- Centered the R7 channel line.
- Added R7 channel labels with default `91 Worldwide` support and optional
  `channel_names` YAML overrides.

## 0.1.7 - 2026-05-23

- Added custom-card metadata used by the Home Assistant card picker.
- Disabled generated preview rendering to avoid frontend configuration errors.

## 0.1.6 - 2026-05-23

- Added README screenshots from the card dashboard.
- Split the R7 caller area into separate callsign and `Name Country` lines.
- Added `country_entity` to the R7 README example.

## 0.1.5 - 2026-05-23

- Removed the yellow highlight from the MCS2000 volume knob.
- Aligned the microphone socket with the `Opt` button.

## 0.1.4 - 2026-05-23

- Removed MCS2000 LCD side arrows and expanded the screen into that space.
- Removed unused MCS2000 top-strip status icons.
- Enlarged the volume knob.
- Lowered the microphone socket.
- Shifted the left-side Zone/Page/Opt controls to the right.

## 0.1.3 - 2026-05-23

- Changed the MCS2000 LCD to show callsign on the main line and
  `Name - Country` on the info line.
- Added `country_entity` support.

## 0.1.2 - 2026-05-23

- Tuned MCS2000 proportions, LCD size, and text scaling.
- Fixed MCS2000 LCD invert state so it persists across card re-renders.
- Moved MCS2000 LCD invert toggle to a single click on the left-side `Opt`
  button.

## 0.1.1 - 2026-05-23

- Corrected HACS filename metadata.
- Added HACS resource path troubleshooting notes.

## 0.1.0 - 2026-05-23

- Initial card repository.
- Added `custom:wpsd-radio-card`.
- Added `style: mcs2000`.
- Added `style: r7`.
- Added example YAML files.
