# Digitalocean Docker container with NGINX

macOS: 14.4.1

Ubuntu: 20-04-x64

Docker: 25.0.3

## Instructions

1. Add your machine SSH to DigitalOcean account

2. Update ssh_key variable in provision.yml with your ssh fingerprint

3. Create API token and add to your DigitalOcean project

4. Export your API token:

        export DO_API_TOKEN=YOUR_API_TOKEN_HERE

5. Run provision.yml playbook to deploy new droplet on DigtalOcean and automatically add ip dinamically to hosts.

         ansible-playbook provision.yml

6. Run main.yml to install Docker and create NGINX container
 
        ansible-playbook main.yml

7. Enjoy!

## Droplet Delete

If you would like to delete droplet, simply switch state of "Create Digitalocean droplet" from PRESENT to ABSENT and run playbook.

## Useful Links

[community.digitalocean](https://github.com/ansible-collections/community.digitalocean/tree/main)


[Dynamic-Inventory](https://github.com/geerlingguy/ansible-for-devops/tree/master/dynamic-inventory/digitalocean)

[NGINX](https://www.nginx.com/)
