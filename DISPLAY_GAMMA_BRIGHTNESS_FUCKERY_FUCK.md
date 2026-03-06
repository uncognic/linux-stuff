Did some more digging myself, and Fedora does not use ppd by default, it uses tuned-ppd.

I copied the balanced, balanced-battery, and powersave profiles from /usr/lib/tuned/profiles to /etc/tuned/profiles as recommended by the tuned-ppd documentation (versions in /etc/tuned/profiles override the defaults installed to /usr/lib/tuned/profiles by the package), changing the parameter panel_power_savings to 0. That has fixed the issue for me while running what Fedora ships out of the box.

Didn’t even have to reboot; the next time I shifted profiles it picked up on the overriding profile in /etc/tuned/profiles.

https://discuss.kde.org/t/power-profiles-are-adjusting-my-screens-gamma-how-can-i-stop-it-from-happening/35878
