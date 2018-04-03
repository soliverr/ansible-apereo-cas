apereo-cas
==========

Ansible role to install and configure Apereo CAS.

# Synopsis

  vars:
    # Apereo CAS role variables
    # - JDK JAVA_HOME
    apereo_cas_java_home: "/usr/lib/jvm/default-java"
    # Service name
    apereo_cas_service: 'cas'
    # Enable/disable upgrade
    apereo_cas_upgrade: true
    # Default logger level
    apereo_cas_loglevel: 'info'

    # Service registry
    apereo_cas_service_registry:
      - type: 'json'
        initFromJson: 'true'
        location: 'services'
        services:
          - name: 'Wild_card_service'
            service: '^(https|imaps)://.*' 
            id: 100001
            oredr: 100

    # LDAP Authentication 
    apereo_cas_ldap:
      # LDAP type: AD|AUTHENTICATED|DIRECT|ANONYMOUS
      #type: 
      # URL to connect to
      #url: 
      #connectionStrategy:
      #useSsl: 
      #useStartTls:
      #connectTimeout: 
      #baseDn:
      #userFilter: 
      #subtreeSearch:
      #bindDn:
      #bindCredential:
      # Connection pool: NONE|CLOSE|BIND
      #poolPassivator: 
      #minPoolSize:
      #maxPoolSize: 
      #validateOnCheckout: 
      #validatePeriodically: 
      #validatePeriod: 
      #validateTimeout: 

  roles:
    - apereo-cas


# Description


# Dependencies

* [silpion.lib][1]


# <a name="role_variables"></a>Role Variables



# License


# Author

## Contributors



[1]: https://github.com/silpion/ansible-lib


<!-- vim: set ts=4 sw=4 et nofen: -->
