Identity Harmonization Role
====================================

Configure and start [IDH]([CDMI](https://github.com/indigo-dc/CDMI)).

This role has been specifically developed to be used for the deployment of the *Identity Harmonization* service in the framework of the *INDIGO-DataCloud* project.

Role Variables
--------------

- `idh_version`: (default 1.0) The version of IDH to install.
  There need to be appropriatly named `.rpm` and `.deb` files in the main
  [git repository](https://github.com/indigo-dc/CDMI).

Requirements
------------
- Only *CentOS 7* or *Ubuntu 14.04 LTS* on the nodes are explicily supported

Example Playbook
----------------

- From ansible galaxy:

  ```sh
   $ ansible-galaxy install indigo-dc.idh
  ```
  Create a playbook like this:

  ```yaml
  - hosts: idh-servers
    roles:
    - indigo-dc.idh
  ```

  ```sh
   $ ansible-playbook -i tests/inventory <path-to-playbook>
  ```
- From git:

  ```yaml
  - hosts: idh-servers
    roles:
    - <path-to-repo>
  ```

  ```sh
   $ ansible-playbook -i tests/inventory <path-to-playbook>
  ```

Of course, you will need to adapt `sample/inventory` according to your needs, or leave the `--inventory` option out and use the default `/etc/ansible/hosts`.

See also: `sample/test.yml`.

License
-------

Apache Licence v2 [1]

[1]: http://www.apache.org/licenses/LICENSE-2.0
