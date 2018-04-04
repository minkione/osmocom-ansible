#osmocom-ansible

apt dist-upgrade

reboot on the latest linux image 4.15 at this time

apt install openssh-server ansible

cd /root

git clone https://github.com/bbaranoff/osmocom-ansible test

cp /root/test/hosts /etc/ansible/hosts

cp /root/test/sshd_config /etc/ssh/sshd_config

ssh-keygen

service ssh restart

ssh-copy-id localhost

ansible all -m ping

if it answer pong you're good

cd /root/test/

rm -rf /root/gnuarm /root/osmocom-ansible /root/trx /root/lcr /root/opencore-amr /root/sofia-sip /root/asterisk-1.8.13.1 /root/libosmocore /root/libosmo-dsp /root/.osmocom

ansible-playbook osmocom.yml


