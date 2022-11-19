```bash
dnf install https://zfsonlinux.org/epel/zfs-release.el8_5.noarch.rpm -y
rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-zfsonlinux
dnf config-manager --disable zfs
dnf config-manager --enable zfs-kmod
dnf install zfs -y
echo zfs >/etc/modules-load.d/zfs.conf
modprobe zfs
zpool create data  /dev/sdb
```