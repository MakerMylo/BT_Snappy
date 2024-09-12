Snappy Mod aka Snapping Turtle
===
This is a modification for BoxTurtle based on the fantastic [EREC Cutter](https://github.com/kevinakasam/ERCF_Filament_Cutter) by [KevinAKASam](https://kevinakasam.com/).

Config
===
This assumes you're using Snappy with AFC and using an MG996R Servo.

`AFC_Hardware.cfg`
Ensure you have a Servo named 'cut' defined in your AFC Hardware file like so:
```
[servo cut]
pin: AFC:PA13               # Correct Pin for MMB
maximum_servo_angle: 180  	# Set this to 60 for a 60° Servo
minimum_pulse_width: 0.0005	# Adapt these for your servo
maximum_pulse_width: 0.0025	# Adapt these for your servo
```

`AFC.cfg`
Ensure that your AFC Config file has the correct hub_cut settings, like so:
```
# HUB Cutting Settings
hub_cut_active: 0
hub_cut_dist: 200                 # How much filament do you want to cut off? (in MM)
hub_cut_clear: 120                # How far should the filament be retracted back from the hub (in MM)
hub_cut_min_length: 300.0
hub_cut_servo_pass_angle: 10      # Bowden Aligned with the hole, able to load the toolhead.
hub_cut_servo_clip_angle: 180     # Cutting action angle.
hub_cut_servo_prep_angle: 80      # Align exit hole for cutting.
hub_cut_confirm: 0                # Set to 1 to enable a second confirmation cut sweep of the servo.
```
And as a safety measure, add `SET_SERVO SERVO=cut ANGLE=10` at the very bottom of the file under the `[delayed_gcode welcome]` section, after `PREP`, this will ensure the servo is always in the correct spot on boot.

Bill of Materials
===
Every link in the Bill of Materials is an affiliate link, This costs you nothing to use but helps buy me some filament and trinkets to make this kind of mod.

- EREC Filament Cutter BOM Kit: [AE Link](https://s.click.aliexpress.com/e/_DBtMz8X)
- Optionally you can also use a more powerful servo, I recommend this one: [AE Link](https://s.click.aliexpress.com/e/_DDc9vRH)

Upcoming Changes
===
 - Filament Tip Collection Drawer
 - Hood that covers the cutter to prevent tips firing off.

Thank Me
===
A few ways you can show your appreciation for my work:\
[Buy Me a Coffee](https://buymeacoffee.com/makermylo) | [Subscribe on YouTube](https://www.youtube.com/@makermylo) | [Follow on X](https://x.com/MakerMylo)
