ansible-bamboo
==============

Bamboo Module for Ansible

module: bamboo
short_description: Pause/unpause Bamboo
description:
    - This module will let you pause/unpause Bamboo
version_added: ""
author: Kyle Varga
requirements:
    - "none"
options:
    state:
        description:
            - Define whether or not the check should be running or paused.
        required: true
        default: null
        choices: [ "RUNNING", "PAUSED" ]
        aliases: []
    url:
        description:
            - Bamboo URL of the check. https://bamboo.server.com
        required: true
        default: null
        choices: []
        aliases: []
    username:
        description:
            - Bamboo user name.
        required: true
        default: null
        choices: []
        aliases: []
    passwd:
        description:
            - Bamboo user password.
        required: true
        default: null
        choices: []
        aliases: []
notes:
    - This module is under development

# Pause the bamboo server
```- bamboo:  url=https://bamboo.server.com
           username=test
           passwd=password123
           state=PAUSED```

# Resume the bamboo server
```- bamboo:  url=https://bamboo.server.com
           username=test
           passwd=password123
           state=RUNNING```

How To Test:
```Shell
git clone git@github.com:ansible/ansible.git
ansible/hacking/test-module -m ./ansible-bamboo -a "passwd={pass} username={user} state={newstate} url={bamboo_url}"
```

