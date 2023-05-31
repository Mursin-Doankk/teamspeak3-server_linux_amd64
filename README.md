# ts3server-crack
semoga kita semua dalam lindungan allah


1.  sudo apt-get autoremove -y
2.  sudo apt autoclean
3.  sudo apt-get update && sudo apt-get upgrade -y && sudo reboot
4.  sudo adduser teamspeak
5.  su - teamspeak
6.  wget https://github.com/Mursin-Doankk/ts3server-crack.git
7.  tar xvfj teamspeak3-server_linux_amd64-3.13.5.tar.bz2
8.  cp teamspeak3-server_linux_amd64/* -R /home/teamspeak/
9.  rm -rf teamspeak3-server_linux_amd64 teamspeak3-server_linux_amd64-3.13.5.tar.bz2
10. touch .ts3server_license_accepted
11. exit

1.  sudo nano /lib/systemd/system/ts3server.service

[Unit]
Description=Teamspeak Service
Wants=network.target

[Service]
WorkingDirectory=/home/teamspeak
User=teamspeak
ExecStart=/home/teamspeak/ts3server_minimal_runscript.sh
ExecStop=/home/teamspeak/ts3server_startscript.sh stop
ExecReload=/home/teamspeak/ts3server_startscript.sh restart
Restart=always
RestartSec=15

[Install]

WantedBy=multi-user.target

2.  sudo systemctl daemon-reload
3.  sudo systemctl start ts3server.service
4.  sudo systemctl enable ts3server.service
5.  sudo systemctl status ts3server
6.  ss -antpl | grep ts3server
7.  sudo systemctl stop ts3server
8.  su - teamspeak
9.  ./ts3server_startscript.sh start serveradmin_password=your_password
10. ./ts3server_startscript.sh stop
11. exit

