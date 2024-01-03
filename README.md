# ansible-role-porkbun-automatic-dns

## Variables

### Required

- `porkbun_api_key`: Your Porkbun API key
- `porkbun_secret_key`: Your Porkbun secret key
- `pbad_domain`: The domain to update DNS records for
- `pbad_record_names`: A list of DNS records to update

`porkbun_api_key` and `porkbun_secret_key` should **not** be hardcoded and should be loaded from an [Ansible vault](https://docs.ansible.com/ansible/latest/vault_guide/index.html) file or other secrets manager.

### Optional

- `pbad_version`: The version to install
- `pbad_checksum`: The checksum of the downloaded release asset
- `pbad_install_dir`: The directory to copy the `pbad` script to, defaults to `/usr/local/bin`
- `pbad_keyfile`: The path to the keyfile that will be created, defaults to `${HOME}/.porkbunapi`
- `pbad_ext_ip_method`: The method to get the external IP with, defaults to `porkbun` (Porkbun API), also accepts `stdin` and `extif`
- `pbad_ext_if`: The interface to get the external IP from (required if `pbad_ext_ip_method` is `extif`)
- `pbad_cron_minute`: The minute field of the cron entry, defaults to `*/15` (every 15 minutes)
- `pbad_cron_hour`: The hour field of the cron entry, defaults to `*`
- `pbad_cron_day_of_month`: The day of month field of the cron entry, defaults to `*`
- `pbad_cron_month`: The month field of the cron entry, defaults to `*`
- `pbad_cron_day_of_week`: The day of week field of the cron entry, defaults to `*`
