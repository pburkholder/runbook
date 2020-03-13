credhub generate -n /toolingbosh/productionbosh/uaa_ssl -t certificate --ca /toolingbosh/productionbosh/default_ca --common-name ${production_bosh_ip} --alternative-name production-bosh-bosh-director --alternative-name ${production_bosh_ip}

