# nvme-of-tcp-mdadm

```shell
sudo nvme connect -t tcp -n vdb1 -a 10.1.10.12 -s 4420
sudo nvme connect -t tcp -n vdc1 -a 10.1.10.12 -s 4420
```

```shell
sudo nvme list
```

```shell
sudo mdadm --create --verbose /dev/md0 --level=1 --raid-devices=2 /dev/nvme0n1 /dev/nvme1n1
```

```shell
cat /proc/mdstat
```

```shell
mdadm --detail --scan --verbose
```