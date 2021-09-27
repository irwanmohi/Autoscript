# Autoscript

Step 1

apt update && apt upgrade -y --fix-missing && apt install -y linux-headers-$(uname -r) && update-grub && sleep 2 && reboot

Step 2 (Version 1)

sysctl -w net.ipv6.conf.all.disable_ipv6=1 && sysctl -w net.ipv6.conf.default.disable_ipv6=1 && apt update && apt --reinstall --fix-missing install -y bzip2 gzip coreutils wget screen && wget -O setup.sh 'https://raw.githubusercontent.com/irwanmohi/Autoscript/main/setup.sh' && chmod +x setup.sh && screen -S setup ./setup.sh && rm -rf ./setup.sh
