# teracy-dev-override-bug

- follow https://github.com/teracyhq/dev-setup/tree/develop
- clone this project into `~/teracy-dev/workspace`
- add `workspace/teracy-dev-override-bug/dev-setup/vagrant_config_default.json` to the `config_paths`
- `$ vagrant status` to see the actual warning:

```bash
macbook-pro:teracy-dev hoatle$ vagrant status
_op = o is invalid for non-existing id: {"_id"=>"data_configs_0", "project"=>"app", "storages"=>{"local"=>"file:///backups/hoatle/app", "origin"=>"gs://ds-hoatle-app", "upstream"=>"gs://ds-teracy-app", "hoatle"=>"gs://ds-hoatle-app"}, "usage"=>{"storage"=>"upstream", "branch"=>"develop", "time"=>"", "force_reset"=>false}, "_op"=>"o"}
Current machine states:

default                   poweroff (virtualbox)

The VM is powered off. To restart the VM, simply run `vagrant up`
```

- expect: no warning, we can override the `data_configs_0` and it should be added into the final config
