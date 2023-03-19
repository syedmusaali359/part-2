1- Use the same image as part 1
# docker images > hello-world:v2
 
2- run the docker container
# sudo docker run -p 8080:8080 hello-world:v2
udo docker run -p 8080:8080 hello-world:v2
 * Serving Flask app 'app' (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 887-199-190


3- run the following commands 
# docker ps 
CONTAINER ID   IMAGE            COMMAND           CREATED         STATUS         PORTS                                       NAMES
c312b283da9e   hello-world:v2   "python app.py"   4 minutes ago   Up 4 minutes   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   sweet_knuth

# docker stop 
sudo docker stop c312b283da9e
c312b283da9e
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
 
# docker rm
sudo docker rm <container ID>
to delete the stoped container

# docker logs
sudo docker logs 8e9f232a5700
 * Serving Flask app 'app' (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: on
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 371-823-526

# docker inspect
sudo docker inspect 8e9f232a5700
[
    {
        "Id": "8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173",
        "Created": "2023-03-19T16:33:44.827718443Z",
        "Path": "python",
        "Args": [
            "app.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 6678,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-03-19T16:33:46.268498343Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:bfbfac95ac5cdeae86e8d90d720eb712f288867a8f5d95b14a0b1b2cec88ed69",
        "ResolvConfPath": "/var/lib/docker/containers/8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173/hostname",
        "HostsPath": "/var/lib/docker/containers/8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173/hosts",
        "LogPath": "/var/lib/docker/containers/8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173/8e9f232a57000977b421868540e3d90e677b19d6f2ee82573e3af3544dd36173-json.log",
        "Name": "/dazzling_easley",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
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
            "CgroupnsMode": "host",
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
                "LowerDir": "/var/lib/docker/overlay2/3ea2f2954109bf1d6ea124b9a684a0fc7c9a8f4cec3aed01ae27721fa9638076-init/diff:/var/lib/docker/overlay2/61ce8fdefcb2765933cea7f2416c2192ef89f1dae446c42a1c00f5530e5adf9d/diff:/var/lib/docker/overlay2/0d0963051b75265241a02ae92f0563872430e6d23b396aff1f24e0cb0bbf200a/diff:/var/lib/docker/overlay2/1a82d1870b6df88dd9563a4796d305e12e32e6fe9fbfa0f2668284accea6fe5d/diff:/var/lib/docker/overlay2/c9676c6f62ccbd64e6e7c13c87c46a3410258c7f04723e26a43f89963b9ba267/diff:/var/lib/docker/overlay2/c7c1ad68eba9dad94e80eeacd42d83c5ddba7344a65247347b1229711681fd6c/diff:/var/lib/docker/overlay2/985737c174a67eaafd708694af2c2f526f856030440f2cfb245b08362fbad7db/diff:/var/lib/docker/overlay2/36f41af56f9995f7a5d846df4e215c9c03245afb47e0f5a5decd1e6664809b6a/diff:/var/lib/docker/overlay2/d8d9d2263504bf85df6d367c46f2f41f12e03486d73011f1d45f2b077419bec3/diff",
                "MergedDir": "/var/lib/docker/overlay2/3ea2f2954109bf1d6ea124b9a684a0fc7c9a8f4cec3aed01ae27721fa9638076/merged",
                "UpperDir": "/var/lib/docker/overlay2/3ea2f2954109bf1d6ea124b9a684a0fc7c9a8f4cec3aed01ae27721fa9638076/diff",
                "WorkDir": "/var/lib/docker/overlay2/3ea2f2954109bf1d6ea124b9a684a0fc7c9a8f4cec3aed01ae27721fa9638076/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "8e9f232a5700",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": true,
            "AttachStderr": true,
            "ExposedPorts": {
                "8080/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568",
                "PYTHON_VERSION=3.9.16",
                "PYTHON_PIP_VERSION=22.0.4",
                "PYTHON_SETUPTOOLS_VERSION=58.1.0",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637",
                "NAME=world"
            ],
            "Cmd": [
                "python",
                "app.py"
            ],
            "Image": "hello-world:v2",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "59536b2a878d084e12518f9a91f3f04063f999a7dc8658fd9464a27446375600",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "8080/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "8080"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "8080"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/59536b2a878d",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "fc7e3d8097d3209d1f96c50b5527ea6f4065614b83cbd07b5a99a3d76d2a473a",
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
                    "NetworkID": "7ce17e0d25dabf263a76de6097babcda6b584b466d038f1a2677df5880907586",
                    "EndpointID": "fc7e3d8097d3209d1f96c50b5527ea6f4065614b83cbd07b5a99a3d76d2a473a",
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

# docker exec
sudo docker exec -it 8e9f232a5700 sh
> exit

# docker attach
sudo docker attach 8e9f232a5700
to attach a running container

# docker commit
sudo docker commit 0e175cfc79ce hello-musa
sha256:38f41a81a4818ffee87b7612b221a934776384ca2bbb2a61752bb1037b368105
 
# docker cp
sudo docker cp requirements.txt 0e175cfc79ce:/usr/share
sudo docker exec -it 0e175cfc79ce /bin/bash
root@0e175cfc79ce:/app# ls
Dockerfile  app.py  requirements.txt

# docker stats
sudo docker stats
CONTAINER ID   NAME               CPU %     MEM USAGE / LIMIT     MEM %     NET I/O      BLOCK I/O    PIDS
0e175cfc79ce   jovial_ramanujan   0.37%     37.35MiB / 3.832GiB   0.95%     3.6kB / 0B   139kB / 0B   3

# docker top
sudo docker top 0e175cfc79ce 
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                8294                8273                0                   12:50               ?                   00:00:00            python app.py
root                8325                8294                0                   12:50               ?                   00:00:02            /usr/local/bin/python /app/app.py

# docker start
sudo docker start eadcf25de6a3
eadcf25de6a3

# docker pause
sudo docker pause eadcf25de6a3
eadcf25de6a3

# docker unpause
sudo docker unpause eadcf25de6a3
eadcf25de6a3

# docker rename
sudo docker ps
CONTAINER ID   IMAGE            COMMAND           CREATED         STATUS              PORTS                                       NAMES
eadcf25de6a3   hello-world:v2   "python app.py"   3 minutes ago   Up About a minute   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   upbeat_rosalind

sudo docker rename eadcf25de6a3 musa

sudo docker ps
CONTAINER ID   IMAGE            COMMAND           CREATED         STATUS         PORTS                                       NAMES
eadcf25de6a3   hello-world:v2   "python app.py"   3 minutes ago   Up 2 minutes   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp   musa

# docker wait
sudo docker stop musa
musa

sudo docker wait musa
0

# docker attach
sudo docker run -dit --name musa1 hello-world:v2
6b2232b9c960b19befd92698f8e096af4961ea30cfd60a675d158860bbd5c2e1

sudo docker attach musa1

sudo docker ps -a --filter name=musa1
CONTAINER ID   IMAGE            COMMAND           CREATED         STATUS          PORTS      NAMES
6b2232b9c960   hello-world:v2   "python app.py"   2 minutes ago   Up 54 seconds   8080/tcp   musa1

# docker port
sudo docker run -p 8080:8080 hello-world:v2

# docker restart
sudo docker restart c698c7385749
c698c7385749
