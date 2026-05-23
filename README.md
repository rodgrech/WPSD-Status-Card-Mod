# WPSD Status Card Mod

A custom Lovelace card for displaying WPSD/DMR hotspot activity in Home
Assistant.

The card currently supports two styles:

- `mcs2000`: Motorola MCS2000-inspired control head
- `r7`: modern handheld/R7-inspired screen

## Installation

### Manual

Copy:

```text
dist/wpsd-radio-card.js
```

to Home Assistant:

```text
/config/www/wpsd-radio-card.js
```

Then add the Lovelace resource:

```text
/local/wpsd-radio-card.js
```

Resource type:

```text
JavaScript module
```

### HACS

Add this repository to HACS as a custom repository with category:

```text
Dashboard
```

After installing, add this dashboard resource if HACS does not add it
automatically:

```text
/hacsfiles/WPSD-Status-Card-Mod/wpsd-radio-card.js
```

Resource type:

```text
JavaScript module
```

Then hard refresh your browser or clear the Home Assistant frontend cache. If
the resource has not loaded, Home Assistant will show:

```text
Custom element not found: wpsd-radio-card
```

## MCS2000 Example

```yaml
type: custom:wpsd-radio-card
style: mcs2000
title: Home Assistant WPSD
callsign_entity: sensor.dmr_hotspot_callsign
talkgroup_entity: sensor.dmr_hotspot_talkgroup
mode_entity: sensor.dmr_hotspot_mode
source_entity: sensor.dmr_hotspot_source
loss_entity: sensor.dmr_hotspot_loss
name_entity: sensor.dmr_hotspot_name
country_entity: sensor.dmr_hotspot_country
last_heard_entity: sensor.dmr_hotspot_last_heard
status_entity: sensor.dmr_hotspot_status
```

Click the left-side `Opt` button to invert the LCD colours.

## R7 Example

```yaml
type: custom:wpsd-radio-card
style: r7
callsign_entity: sensor.dmr_hotspot_callsign
talkgroup_entity: sensor.dmr_hotspot_talkgroup
mode_entity: sensor.dmr_hotspot_mode
source_entity: sensor.dmr_hotspot_source
loss_entity: sensor.dmr_hotspot_loss
ber_entity: sensor.dmr_hotspot_ber
name_entity: sensor.dmr_hotspot_name
timestamp_entity: sensor.dmr_hotspot_timestamp
```

## Related Integration

This card pairs with:

[WPSD Home Assistant](https://github.com/rodgrech/WPSD-home-assistant)

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for release history.

Recent changes:

- `0.1.4`: polished the MCS2000 control layout, expanded the LCD area,
  removed unused top-strip icons, and shifted the left-side controls.
- `0.1.3`: updated the MCS2000 LCD info line to show callsign plus
  `Name - Country`.
