# runbook

Install SOPS

    brew sops install


Following tutorial at:

https://oteemo.com/2019/06/20/hashicorp-vault-is-overhyped-and-mozilla-sops-with-kms-and-git-is-massively-underrated/

```
sops secrets.env # edit in vim to create production_bosh_ip
vim nats.md # write run book
```

Then commit and push


Run runbook

```
sops exec-env secrets.env 'bash'
...
$ echo credhub generate -n /toolingbosh/productionbosh/uaa_ssl -t certificate --ca /toolingbosh/productionbosh/default_ca --common-name ${production_bosh_ip} --alternative-name production-bosh-bosh-director --alternative-name ${production_bosh_ip}

credhub generate -n /toolingbosh/productionbosh/uaa_ssl -t certificate --ca /toolingbosh/productionbosh/default_ca --common-name 10.1.2.3 --alternative-name production-bosh-bosh-director --alternative-name 10.1.2.3
```
