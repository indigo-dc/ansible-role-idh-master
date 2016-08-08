# docker build --rm -t docker-idh .

FROM indigodatacloud/ubuntu-sshd:14.04
MAINTAINER Mario David <mariojmdavid@gmail.com>
LABEL description="Container image to run Identity Harmonization"

RUN ansible-galaxy install indigo-dc.ansible-role-idh-master && \
    ansible-playbook /etc/ansible/roles/indigo-dc.ansible-role-idh-master/tests/test.yml

EXPOSE 22 8443
# CMD [ "" ]

