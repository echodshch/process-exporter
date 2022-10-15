# Prometheus process-exporter ansible playbook
This playbook created for install&configure prometheus exporters and Percona management&monitoring client on nodes. 

Configurate system, install pmm-client, register node and exporters on pmm monitoring server. Include node_exporter, nginx_exporter, puma_exporter, postgres_exporter, redis_exporter and sidekiq_exporter.
Useful for debian-like and RHEL-like os, contain configurating system: disable SElinux, opening ports in firewalld and other.

All exporters, except postgres_exporter, will installed for one created user, postgres_exporter user may be default postgresql user.

Puma and sidekiq exporters suitable with Ruby Bundler.

NB: This playbook is not perfect - explore it carefully before using it

Role nginx_exporter was created based on https://github.com/bdellegrazie/ansible-role-nginx_exporter/
Role redis_exporter was created based on https://github.com/idealista/prometheus_redis_exporter_role/
