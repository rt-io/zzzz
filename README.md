# zzzz
[Unit]
Description=Start x11vnc at startup.
After=multi-user.target

[Service]
Type=simple

ExecStart=/usr/bin/x11vnc -forever -loop -noxdamage -repeat -rfbport 5901 -shared -display :0 -passwd 1234aa

[Install]
WantedBy=multi-user.target
