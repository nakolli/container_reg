docker build --rm -t nkolli/apache_httpd .

[root@unknown080027171612 docker_ce]# docker run -d -p 8080:8080  nkolli/apache_httpd
2123db4bb700a44079f0c01fbe01723884195bb630ef2dfb2490058c53b84209
[root@unknown080027171612 docker_ce]# docker ps
CONTAINER ID        IMAGE                 COMMAND             CREATED             STATUS                                                                                           PORTS                            NAMES
2123db4bb700        nkolli/apache_httpd   "/run-httpd.sh"     7 seconds ago       Up 3 seco                                                                             nds        80/tcp, 0.0.0.0:8080->8080/tcp   silly_fermi
[root@unknown080027171612 docker_ce]# docker inspect 2123db4bb700
[
    {
        "Id": "2123db4bb700a44079f0c01fbe01723884195bb630ef2dfb2490058c53b84209",
        "Created": "2020-02-11T03:27:55.915967443Z",
        "Path": "/run-httpd.sh",
        "Args": [],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 17542,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2020-02-11T03:27:58.379280288Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:6a0df3562227c39255fa0f112402079c77e62bfcdcab786428d3f8396346a96a",
        "ResolvConfPath": "/var/lib/docker/containers/2123db4bb700a44079f0c01fbe01723884195                                                                             bb630ef2dfb2490058c53b84209/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/2123db4bb700a44079f0c01fbe01723884195bb                                                                             630ef2dfb2490058c53b84209/hostname",
        "HostsPath": "/var/lib/docker/containers/2123db4bb700a44079f0c01fbe01723884195bb630                                                                             ef2dfb2490058c53b84209/hosts",
        "LogPath": "/var/lib/docker/containers/2123db4bb700a44079f0c01fbe01723884195bb630ef                                                                             2dfb2490058c53b84209/2123db4bb700a44079f0c01fbe01723884195bb630ef2dfb2490058c53b84209-json.                                                                             log",
        "Name": "/silly_fermi",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "8080/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "8080"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "CapAdd": null,
            "CapDrop": null,
            "Capabilities": null,
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "ConsoleSize": [
                0,
                0
            ],
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": null,
            "BlkioDeviceWriteBps": null,
            "BlkioDeviceReadIOps": null,
            "BlkioDeviceWriteIOps": null,
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "KernelMemory": 0,
            "KernelMemoryTCP": 0,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/d271bcd2fb0d27b1012bd042b5ac13d570f6c                                                                             f5be9f1defef6300388ebde2eae-init/diff:/var/lib/docker/overlay2/16e465a60d372e54fd73a62f3539                                                                             3d1aa80d714ca08c66a6d0b7b63fdb6d1964/diff:/var/lib/docker/overlay2/5ffe7ec1c691304bd5e19d7a                                                                             bf2f75a83845afb67e80295e0d834c7adfac15ac/diff:/var/lib/docker/overlay2/00aaca9717359e209fd4                                                                             96be19d7d55cda2723e473ceb84cfb014172348cd0c3/diff:/var/lib/docker/overlay2/c5598e9737952d03                                                                             d0c06ae1bc586b2e1c3fd270291c9bfcc756f50d3f56cf03/diff:/var/lib/docker/overlay2/c6867c2f2020                                                                             b9494247dfdd2d9d1b02c34d9b2d50cbd92e5188c0b83d03fc2c/diff:/var/lib/docker/overlay2/156f3ba7                                                                             624be24fbce1b17b1b61931659fb5dd170a4b4b3b9466668719c4ad6/diff",
                "MergedDir": "/var/lib/docker/overlay2/d271bcd2fb0d27b1012bd042b5ac13d570f6                                                                             cf5be9f1defef6300388ebde2eae/merged",
                "UpperDir": "/var/lib/docker/overlay2/d271bcd2fb0d27b1012bd042b5ac13d570f6c                                                                             f5be9f1defef6300388ebde2eae/diff",
                "WorkDir": "/var/lib/docker/overlay2/d271bcd2fb0d27b1012bd042b5ac13d570f6cf                                                                             5be9f1defef6300388ebde2eae/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "2123db4bb700",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "80/tcp": {},
                "8080/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/run-httpd.sh"
            ],
            "Image": "nkolli/apache_httpd",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "License": "GPLv2",
                "Vendor": "CentOS",
                "Version": "2.4.6-40",
                "org.label-schema.build-date": "20191001",
                "org.label-schema.license": "GPLv2",
                "org.label-schema.name": "CentOS Base Image",
                "org.label-schema.schema-version": "1.0",
                "org.label-schema.vendor": "CentOS"
            }
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "ec062e2ba8d872873cc7f1541cc952e5bdf1a11f6b44ba418ebee4ac5067f25e"                                                                             ,
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "80/tcp": null,
                "8080/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "8080"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/ec062e2ba8d8",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "f592576ccf8812950be778705f68836be3f9f3f8d2cc87045e49a52af60f90c4                                                                             ",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "8376a7ea42a883ff413854d95188b9f883f5f7625da1db1d9403cc07a                                                                             c27db4a",
                    "EndpointID": "f592576ccf8812950be778705f68836be3f9f3f8d2cc87045e49a52a                                                                             f60f90c4",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]
[root@unknown080027171612 docker_ce]# curl http://172.17.0.2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Create a Docker Container with Centos6 image</title>
</head>
<body>
    <h1>Asst:Task 3
Create a Docker Container with Centos6 image.
Build a Apache http server 2.4x package on Centos6 on the Centos6 Container
Create a Bitbucket or github repository for docker
Push your repository changes to the Bitbucket or github and make them available for publ</h                                                                             1>
</body>
</html>
