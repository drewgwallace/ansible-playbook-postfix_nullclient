# Ansible Role


## Purpose
  Execute this role against supported server(s), it will gather-facts and save them to a logfile for viewing or archiving.
  
----

## Execution
<pre>
    - hosts: all
      tasks:
      - include_role:
          name: drewgwallace.ansible-role-postfix_nullclient
        vars:
          destination_mail_server: <b>"me@mymailserver.example.com"</b>
          mail_recipient: <b>"friend@example.com"</b>
          testemail: <b>True</b>
</pre>

----

## Notes
+ Will need a destination_mail_server mail server configured for outgoing messages or authenticating to a cloud service (yahoo, google, etc.)
++ The destination_mail_server will need to establish trust to the IP/subnets of the null-client mail servers for unauthenticate messages to be relayed