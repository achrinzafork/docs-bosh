# Docker CPI Usage

---

## Networks {: #networks }

Schema for `cloud_properties` section used by dynamic network or manual
network subnet:

- **enable_ipv6** (Boolean, optional) - Assign an IPv6 subnet when creating a
  dynamic network.

---

## VM Types / VM Extensions {: #vm-types }

Schema for `cloud_properties` section:

- **ports** (Array&lt;String&gt;, optional) - Ports to publish for incoming
  network traffic in the format `<port_num>/<network protocol>` (Example:
  `8080/tcp`). Defaults to `[]`.
- **HostConfig** (Object, optional) - Docker Engine [host config
  options](https://github.com/moby/moby/blob/master/api/types/container/hostconfig.go#L418-L475),
  excluding:
    - `Privileged`
    - `PublishAllPorts`
    - `CgroupnsMode`
- **force_start_with_systemd** (Boolean, optional) - Overrides the global CPI
    config option
    [`docker_cpi.start_containers_with_systemd`](https://bosh.io/jobs/docker_cpi?source=github.com/cloudfoundry/bosh-docker-cpi-release#p%3ddocker_cpi.start_containers_with_systemd).
    Defaults to `false`.
- **force_start_without_systemd** (Boolean, optional) - Overrides the global CPI
    config option
    [`docker_cpi.start_containers_with_systemd`](https://bosh.io/jobs/docker_cpi?source=github.com/cloudfoundry/bosh-docker-cpi-release#p%3ddocker_cpi.start_containers_with_systemd).
    Defaults to `false`.
- **force_lxcfs_enabled** (Boolean, optional) - Overrides the global CPI
    config option
    [`docker_cpi.enable_lxcfs_support`](https://bosh.io/jobs/docker_cpi?source=github.com/cloudfoundry/bosh-docker-cpi-release#p%3ddocker_cpi.enable_lxcfs_support).
    Defaults to `false`.
- **force_lxcfs_disabled** (Boolean, optional) - Overrides the global CPI
    config option
    [`docker_cpi.enable_lxcfs_support`](https://bosh.io/jobs/docker_cpi?source=github.com/cloudfoundry/bosh-docker-cpi-release#p%3ddocker_cpi.enable_lxcfs_support).
    Defaults to `false`.
