
cd /etc/systemd/system

```
cloud-final.service.wants  getty.target.wants       network-online.target.wants  sshd.service          timers.target.wants
default.target.wants       graphical.target.wants   remote-fs.target.wants       sysinit.target.wants
final.target.wants         multi-user.target.wants  sockets.target.wants         syslog.service

```


![image](https://user-images.githubusercontent.com/33985509/74242636-95544500-4cde-11ea-9fd3-258ecb11be3f.png)


cd /lib/systemd/system

```
accounts-daemon.service                 netfilter-persistent.service       stop-bootlogd.service
apt-daily.service                       networking.service                 stop-bootlogd-single.service
apt-daily.timer                         network-online.target              suspend.target
apt-daily-upgrade.service               network-pre.target                 swap.target
apt-daily-upgrade.timer                 network.target                     sys-fs-fuse-connections.mount
auth-rpcgss-module.service              nfs-client.target                  sysinit.target
autovt@.service                         nfs-config.service                 sysinit.target.wants
basic.target                            nfs-idmapd.service                 sys-kernel-config.mount
binfmt-support.service                  nfs-utils.service                  sys-kernel-debug.mount
bluetooth.target                        nss-lookup.target                  syslog.socket
bootlogd.service                        nss-user-lookup.target             systemd-ask-password-console.path
bootlogs.service                        paths.target                       systemd-ask-password-console.service
bootmisc.service                        plymouth-halt.service              systemd-ask-password-plymouth.path
busnames.target                         plymouth-kexec.service             systemd-ask-password-plymouth.service
busnames.target.wants                   plymouth-log.service               systemd-ask-password-wall.path
checkfs.service                         plymouth-poweroff.service          systemd-ask-password-wall.service
checkroot-bootclean.service             plymouth-quit.service              systemd-backlight@.service
checkroot.service                       plymouth-quit-wait.service         systemd-binfmt.service
console-getty.service                   plymouth-read-write.service        systemd-bootchart.service
console-setup.service                   plymouth-reboot.service            systemd-bus-proxyd.service
console-shell.service                   plymouth.service                   systemd-bus-proxyd.socket
containerd.service                      plymouth-start.service             systemd-exit.service
container-getty@.service                plymouth-switch-root.service       systemd-fsckd.service
cron.service                            portmap.service                    systemd-fsckd.socket
cryptdisks-early.service                poweroff.target                    systemd-fsck-root.service
cryptdisks.service                      poweroff.target.wants              systemd-fsck@.service
cryptsetup-pre.target                   printer.target                     systemd-halt.service
cryptsetup.target                       proc-fs-nfsd.mount                 systemd-hibernate-resume@.service
ctrl-alt-del.target                     procps.service                     systemd-hibernate.service
dbus-org.freedesktop.hostname1.service  proc-sys-fs-binfmt_misc.automount  systemd-hostnamed.service
dbus-org.freedesktop.locale1.service    proc-sys-fs-binfmt_misc.mount      systemd-hwdb-update.service
dbus-org.freedesktop.login1.service     quotaon.service                    systemd-hybrid-sleep.service
dbus-org.freedesktop.network1.service   rc-local.service                   systemd-initctl.service
dbus-org.freedesktop.resolve1.service   rc.local.service                   systemd-initctl.socket
dbus-org.freedesktop.timedate1.service  rc-local.service.d                 systemd-journald-audit.socket
dbus.service                            rc.service                         systemd-journald-dev-log.socket
dbus.socket                             rcS.service                        systemd-journald.service
debug-shell.service                     reboot.service                     systemd-journald.socket
default.target                          reboot.target                      systemd-journal-flush.service
dev-hugepages.mount                     reboot.target.wants                systemd-kexec.service
dev-mqueue.mount                        remote-fs-pre.target               systemd-localed.service
docker.service                          remote-fs.target                   systemd-logind.service
docker.socket                           rescue.service                     systemd-machine-id-commit.service
emergency.service                       rescue.target                      systemd-modules-load.service
emergency.target                        rescue.target.wants                systemd-networkd-resolvconf-update.path
exit.target                             resolvconf.service                 systemd-networkd-resolvconf-update.service
final.target                            resolvconf.service.wants           systemd-networkd.service
friendly-recovery.service               rmnologin.service                  systemd-networkd.socket
friendly-recovery.target                rpcbind.service                    systemd-networkd-wait-online.service
fuse.service                            rpcbind.socket                     systemd-poweroff.service
getty@.service                          rpcbind.target                     systemd-quotacheck.service
getty-static.service                    rpc-gssd.service                   systemd-random-seed.service
getty.target                            rpc-statd-notify.service           systemd-reboot.service
getty.target.wants                      rpc-statd.service                  systemd-remount-fs.service
graphical.target                        rpc-svcgssd.service                systemd-resolved.service
graphical.target.wants                  rsync.service                      systemd-resolved.service.d
gssd.service                            rsyslog.service                    systemd-rfkill.service
halt.service                            runlevel0.target                   systemd-rfkill.socket
halt.target                             runlevel1.target                   systemd-suspend.service
halt.target.wants                       runlevel1.target.wants             systemd-sysctl.service
hibernate.target                        runlevel2.target                   systemd-timedated.service
hostname.service                        runlevel2.target.wants             systemd-timesyncd.service
hwclock.service                         runlevel3.target                   systemd-timesyncd.service.d
hybrid-sleep.target                     runlevel3.target.wants             systemd-tmpfiles-clean.service
idmapd.service                          runlevel4.target                   systemd-tmpfiles-clean.timer
ifup@.service                           runlevel4.target.wants             systemd-tmpfiles-setup-dev.service
initrd-cleanup.service                  runlevel5.target                   systemd-tmpfiles-setup.service
initrd-fs.target                        runlevel5.target.wants             systemd-udevd-control.socket
initrd-parse-etc.service                runlevel6.target                   systemd-udevd-kernel.socket
initrd-root-fs.target                   run-rpc_pipefs.mount               systemd-udevd.service
initrd-switch-root.service              sendsigs.service                   systemd-udev-settle.service
initrd-switch-root.target               serial-getty@.service              systemd-udev-trigger.service
initrd-switch-root.target.wants         setvtrgb.service                   systemd-update-utmp-runlevel.service
initrd.target                           shutdown.target                    systemd-update-utmp.service
initrd-udevadm-cleanup-db.service       sigpwr-container-shutdown.service  systemd-user-sessions.service
iptables.service                        sigpwr.target                      system.slice
kexec.target                            sigpwr.target.wants                system-update.target
kexec.target.wants                      single.service                     timers.target
keyboard-setup.service                  sleep.target                       timers.target.wants
killprocs.service                       -.slice                            time-sync.target
kmod.service                            slices.target                      ubuntu-fan.service
kmod-static-nodes.service               smartcard.target                   udev.service
local-fs-pre.target                     snapd.autoimport.service           ufw.service
local-fs.target                         snapd.core-fixup.service           umountfs.service
local-fs.target.wants                   snapd.failure.service              umountnfs.service
machine.slice                           snapd.seeded.service               umountroot.service
mail-transport-agent.target             snapd.service                      umount.target
module-init-tools.service               snapd.snap-repair.service          unattended-upgrades.service
motd.service                            snapd.snap-repair.timer            urandom.service
mountall-bootclean.service              snapd.socket                       ureadahead.service
mountall.service                        snapd.system-shutdown.service      ureadahead-stop.service
mountdevsubfs.service                   sockets.target                     ureadahead-stop.timer
mountkernfs.service                     sockets.target.wants               user@.service
mountnfs-bootclean.service              sound.target                       user.slice
mountnfs.service                        ssh.service                        uuidd.service
multi-user.target                       ssh@.service                       uuidd.socket
multi-user.target.wants                 ssh.socket                         x11-common.service


```
![image](https://user-images.githubusercontent.com/33985509/74244820-51fbd580-4ce2-11ea-8dba-c1ea4e17d37a.png)



$ cat systemd-timedated.service

```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.

[Unit]
Description=Time & Date Service
Documentation=man:systemd-timedated.service(8) man:localtime(5)
Documentation=http://www.freedesktop.org/wiki/Software/systemd/timedated

[Service]
ExecStart=/lib/systemd/systemd-timedated
BusName=org.freedesktop.timedate1
CapabilityBoundingSet=CAP_SYS_TIME
WatchdogSec=3min
PrivateTmp=yes
ProtectSystem=yes
ProtectHome=yes

```



cat systemd-resolved.service


```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.

[Unit]
Description=Network Name Resolution
Documentation=man:systemd-resolved.service(8)
After=systemd-networkd.service network.target

# On kdbus systems we pull in the busname explicitly, because it
# carries policy that allows the daemon to acquire its name.
Wants=org.freedesktop.resolve1.busname
After=org.freedesktop.resolve1.busname

[Service]
Type=notify
Restart=always
RestartSec=0
ExecStart=/lib/systemd/systemd-resolved
CapabilityBoundingSet=CAP_SETUID CAP_SETGID CAP_SETPCAP CAP_CHOWN CAP_DAC_OVERRIDE CAP_FOWNER
ProtectSystem=full
ProtectHome=yes
WatchdogSec=3min

[Install]
WantedBy=multi-user.target

```


$ cat systemd-networkd.service


```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.

[Unit]
Description=Network Service
Documentation=man:systemd-networkd.service(8)
ConditionCapability=CAP_NET_ADMIN
DefaultDependencies=no
# systemd-udevd.service can be dropped once tuntap is moved to netlink
After=systemd-udevd.service network-pre.target systemd-sysusers.service systemd-sysctl.service
Before=network.target multi-user.target shutdown.target
Conflicts=shutdown.target
Wants=network.target

# On kdbus systems we pull in the busname explicitly, because it
# carries policy that allows the daemon to acquire its name.
Wants=org.freedesktop.network1.busname
After=org.freedesktop.network1.busname

[Service]
Type=notify
Restart=on-failure
RestartSec=0
ExecStart=/lib/systemd/systemd-networkd
CapabilityBoundingSet=CAP_NET_ADMIN CAP_NET_BIND_SERVICE CAP_NET_BROADCAST CAP_NET_RAW CAP_SETUID CAP_SETGID CAP_SETPCAP CAP_CHOWN CAP_DAC_OVERRIDE CAP_FOWNER
ProtectSystem=full
ProtectHome=yes
WatchdogSec=3min

[Install]
WantedBy=multi-user.target
Also=systemd-networkd.socket

```



$ cat systemd-logind.service

```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.

[Unit]
Description=Login Service
Documentation=man:systemd-logind.service(8) man:logind.conf(5)
Documentation=http://www.freedesktop.org/wiki/Software/systemd/logind
Documentation=http://www.freedesktop.org/wiki/Software/systemd/multiseat
Wants=user.slice
After=nss-user-lookup.target user.slice
ConditionPathExists=/lib/systemd/system/dbus.service

# Ask for the dbus socket. If running over kdbus, the socket will
# not be actually used.
Wants=dbus.socket
After=dbus.socket

[Service]
ExecStart=/lib/systemd/systemd-logind
Restart=always
RestartSec=0
BusName=org.freedesktop.login1
CapabilityBoundingSet=CAP_SYS_ADMIN CAP_MAC_ADMIN CAP_AUDIT_CONTROL CAP_CHOWN CAP_KILL CAP_DAC_READ_SEARCH CAP_DAC_OVERRIDE CAP_FOWNER CAP_SYS_TTY_CONFIG
WatchdogSec=3min

# Increase the default a bit in order to allow many simultaneous
# logins since we keep one fd open per session.
LimitNOFILE=16384

```



$ cat systemd-localed.service

```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.

[Unit]
Description=Locale Service
Documentation=man:systemd-localed.service(8) man:locale.conf(5) man:vconsole.conf(5)
Documentation=http://www.freedesktop.org/wiki/Software/systemd/localed

[Service]
ExecStart=/lib/systemd/systemd-localed
BusName=org.freedesktop.locale1
CapabilityBoundingSet=
WatchdogSec=3min
PrivateTmp=yes
PrivateDevices=yes
PrivateNetwork=yes
ProtectSystem=yes
ProtectHome=yes

```


$ cat systemd-hostnamed.service

```
#  This file is part of systemd.
#
#  systemd is free software; you can redistribute it and/or modify it
#  under the terms of the GNU Lesser General Public License as published by
#  the Free Software Foundation; either version 2.1 of the License, or
#  (at your option) any later version.
[Unit]
Description=Hostname Service
Documentation=man:systemd-hostnamed.service(8) man:hostname(5) man:machine-info(5)
Documentation=http://www.freedesktop.org/wiki/Software/systemd/hostnamed

[Service]
ExecStart=/lib/systemd/systemd-hostnamed
BusName=org.freedesktop.hostname1
CapabilityBoundingSet=CAP_SYS_ADMIN
WatchdogSec=3min
PrivateTmp=yes
PrivateDevices=yes
PrivateNetwork=yes
ProtectSystem=yes
ProtectHome=yes

```

