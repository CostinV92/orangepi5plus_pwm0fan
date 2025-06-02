Install on armbian

1. enable pwm0 in `armbian-config`
2. `armbian-add-overlay <overlay_file.dts>`
3. add `user_overlays=rk3588-pwm0-pwm-fan` to `/boot/armbianEnv.txt`

Install on Ubuntu Jammy 6.1.43

1. enable pwm0 in `orangepi-config`
2. compile the .dts file to dtbo `dtc -@ -I dts -O dtb -o rk3588-pwm0-pwm-fan.dtbo ./rk3588-pwm0-pwm-fan.dts`
3. copy `rk3588-pwm0-pwm-fan.dtbo` to `/boot/dtb/rockchip/overlay/`
4. enable `pwm0-pwm-fan` in `orangepi-config`
