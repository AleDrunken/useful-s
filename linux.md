
Lutris:
1. [External dependencies](https://github.com/lutris/docs/blob/master/WineDependencies.md)
2. Environment variables
	1. __GL_SHADER_DISK_CACHE_PATH = Per game cache directory, example /home/ale/cache/game1
	2. __GL_SHADER_DISK_CACHE_SKIP_CLEANUP = 1
	3. DXVK_FRAME_RATE = Framerate limit, example 60
3. Global options
	1. Enable Feral GameMode
	2. Disable desktop effects

---

Garuda:
1. [Tweaks](https://averagelinuxuser.com/garuda-linux-after-install/#8-disable-grub-delay)
2. [Mouse accel. fix](https://askubuntu.com/questions/715093/how-do-i-disable-mouse-acceleration)

---

Virtual Machine:
1. Failed to start virtualization daemon
	1. https://forum.manjaro.org/t/liibvirtd-service-wont-start/49576
	2. sudo vim /etc/libvirt/libvirtd.conf
	3. uncomment #log_outputs="3:syslog:libvirtd"
	4. sudo systemctl restart libvirtd
	5. Try to start the kvm
	6. If it doesn't start comment log_outputs="3:syslog:libvirtd"
	7. Idk if rebooting helps but if this doesn't work reboot between the steps
	8. Maybe uncommenting and recommenting listen_tcp = 1 and setting listen_tls =0 helps
	9. Maybe installing fmt and ceph-libs helped

---

General
1. High cpu usage
	1. install cpupower-gui 
2. Mount virtual disk
	1. https://www.linuxquestions.org/questions/linux-general-1/how-to-mount-img-file-882386/
	2. sudo mount -o loop,offset=16777216 WINHDD.img /run/media/win/
	3. sudo umount /run/media/win/

---

Terminal
1. Remove fish shell intro message
	1. set -U fish_greeting ""
2. Xfce terminal settings
	1. xfce4-terminal --preferences