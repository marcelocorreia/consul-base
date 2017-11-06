consul-base


Variables

```yml
---
systemd:
  path: "{{ systemd_path | default('/lib/systemd/system') }}"
dnsmasq:
  path: "{{ dnsmasq_path | default('/etc/dnsmasq.d') }}"

consul:
  bootstrap_server: ""
  bootstrap_expect: ""
  nginx_hostname_pattern: ""
  config_dir: "/etc/consul.d"
hashicorp:
  system_user: "ubuntu"
  system_group: "ubuntu"
  apps:
    - name: consul
      state: present
      version: 1.0.0
    - name: consul-template
      state: present
      version: 0.19.4
```

