# Home Assistant Dashboard Snapshot

This directory versions the Home Assistant dashboard state that was adjusted and validated on `2026-04-23`.

## What is included

- `storage/lovelace.gwm_brasil.json`
  Current working snapshot of the `GWM Brasil` dashboard from Home Assistant `.storage`.
- `storage/lovelace_resources.json`
  Snapshot of the Lovelace resources registered on that Home Assistant instance.
- `config-snippets/frontend.card-mod.yaml`
  Required `frontend` snippet used to load `card-mod`.
- `www/images/haval_h6/`
  Local image assets used by the dashboard overlays.

## Notes

- This snapshot reflects the dashboard as it was running in Home Assistant storage, not the original `files/HomeAssistant_Dashboard_GWM.yaml`.
- The exported dashboard currently uses the fixed VIN `lgwffua59sh903754`.
- The Home Assistant instance still had some legacy Lovelace resources registered. The dashboard snapshot no longer depends on `config-template-card`, but the resource remains present in the exported resource snapshot because it existed on the working instance.

## Reapplying the snapshot

1. Copy `www/images/haval_h6/` to your Home Assistant `config/www/images/haval_h6/`.
2. Merge `config-snippets/frontend.card-mod.yaml` into your `configuration.yaml`.
3. Ensure the custom card resources from `storage/lovelace_resources.json` are available in Lovelace.
4. Import or replace the Home Assistant dashboard storage entry with `storage/lovelace.gwm_brasil.json`.

## Custom card families referenced by the exported dashboard

- `lovelace-card-mod`
- `stack-in-card`
- `button-card`
- `lovelace-mushroom`
- `template-entity-row`
- `bar-card`
- `fold-entity-row`
- `collapsable-cards`
- `mini-graph-card`
- `map-card`
- `auto-entities`
- `hassio-havaleiros-charging-hist-card`
