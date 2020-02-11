
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
