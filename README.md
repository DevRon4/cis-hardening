# CIS Benchmark Hardening — Ubuntu (AWS Lightsail)

Automated CIS Benchmark Level 1 hardening for Ubuntu using Ansible, with scored compliance reports.

## Requirements
- Ansible 2.12+
- Python 3.8+
- AWS Lightsail Ubuntu instance

## Usage

### Run full hardening
ansible-playbook site.yml

### Audit only (no changes)
ansible-playbook audit.yml

### Level 1 controls only
ansible-playbook site.yml --tags level1

### Dry run
ansible-playbook site.yml --check --diff

## Reports
After running, find your HTML compliance report at:
reports/lightsail_server_cis_report.html

## CI
GitHub Actions runs Molecule tests on every push using a Docker Ubuntu container.