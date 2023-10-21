# Klipper conf backup for my Neptune 2S

## Dependencies
- [MainsailOS](https://github.com/mainsail-crew/MainsailOS)
- [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)
- [Moonraker-timelapse](https://github.com/mainsail-crew/moonraker-timelapse) (optional)
- [Obico](https://github.com/TheSpaghettiDetective/moonraker-obico) (optional)

## Setup
After installing and configuring the dependencies, SSH into the printer and run the following:
```sh
git clone https://github.com/eduhoribe/neptune_2S.git --recursive ~/printer_data/config/neptune_2S

echo "[include mainsail.cfg]
#[include timelapse.cfg] # uncomment to enable timelapse
[include neptune_2S/elegoo-neptune-2S.cfg]

[exclude_object]
" > ~/printer_data/config/printer.cfg
```

To restore the Mainsail interface settings (like macros grouping):
- open the mainsail in the browser
- go to the interface settings (the gears in the top-right corner) ⇾ general ⇾ restore
- and upload the [backup file](./backup-mainsail.json)
