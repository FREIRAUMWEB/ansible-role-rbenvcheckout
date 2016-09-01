Role Name
=========

installs rbenv

Requirements
------------

none

Role Variables
--------------

    - rbenv_user
      username for which rbenv should be installed
    - rbenv_home
      path to the home Directory, defaults to /home/{{ rbenv_user }}
    - rbenv_root
      path to the directory where rbenv should be installed, defaults to
      /home/{{ rbenv_user }}/.rbenv
    - rbenv_install_ruby
      should we install a ruby version? Which one? Default: 2.3.0
    - rbenv_install_gems
      which GEMs should be installed for new ruby version
    - rbenv_disable_gem_documentation
      should ri and rdoc documentations be disabled by default?
    - rbenv_plugins
      additional Plugins to install


Dependencies
------------

FREIRAUMWEB.git

Example Playbook
----------------

An example of how to use this role in your own playbooks

    - hosts: servers
      roles:
         - FREIRAUMWEB.rbenv
      vars:
        rbenv_plugins:
          - url: 'https://github.com/rbenv/rbenv-vars.git', dest: 'rbenv-vars', update: no
          - url: 'https://github.com/rbenv/rbenv-default-gems.git', dest: 'rbenv-default-vars', update: yes

License
-------

MIT

Author Information
------------------

This role was created in 2016 by Andreas Kleindiek @ FREIRAUMWEB (http://www.freiraumweb.de)
