# zzzz
[Unit]
Description=Start x11vnc at startup.
After=multi-user.target

[Service]
Type=simple
ExecStart=/usr/bin/x11vnc -display :0 -auth /var/run/lightdm/root/:0 -forever -loop -noxdamage -repeat -rfbauth /home/your_username/.vnc/passwd -rfbport 5900 -shared

[Install]
WantedBy=multi-user.target
