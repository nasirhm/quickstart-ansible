## Some info about Heartbleed 
The Heartbleed attack works by tricking servers into leaking information stored in their memory.

This ansible playbook calls a role `fix-heartbleed` which has the following workflow :
- Updating `openssl` to the latest by `dnf`
- Restarts the following services:
  - nginx
  - apache2
  - postgresql
  - php5-fpm
  - openvpn
  - postfix
  - monit
  - unbound
- Verifies the Heartbleed bug by executing the following command on shell to check if we are either vulnerable or not:
  - `if [ "$(sudo lsof -n | grep ssl | grep DEL | wc -l)" = "1" ]; then echo "We are Valnurable"; checkrestart; exit 1; fi`
- If everything goes well it prints out `You are not valnureable with Heartbleed` 

To execute the playbook : `ansible-playbook -K main.yml`

#### More on Heartbleed:
- [HeartBleed.com](https://heartbleed.com/)
- [Wiki](https://en.wikipedia.org/wiki/Heartbleed)
