# elasticsearch-container   

Adds an elasticsearch service to your [Ansible Container](https://github.com/ansible/ansible-container) project. To install the service, do the following:

```
# Set the working directory to your Ansible Container project
$ cd myproject

# Install the role
$ ansible-container install chouseknecht.elasticsearch-container
```


## Requirements

- [Ansible Container](https://github.com/ansible/ansible-container)
- An Ansible Container project. To create a project, run the following:
   ```
   # Create a new directory
   $ mkdir myproject
   
   # Set the working directory to the new directory
   $ cd myproject

   # Initialize the project
   $ ansible-container init
   ```

## Role Variables

elasticsearch_network_host: 0.0.0.0 
> The IP address or hostname associated with the interface listening for inbound connections. Defaults to 0.0.0.0. 

elasticsearch_http_port: 9200
> The port that accepts inbound connections. Defaults to 9200.

elasticsearch_script_inline: true <br />
elasticsearch_script_indexed: true
> Allow users to execute inline scripts. Defaults to true. Know that this can be a security risk, and you should review [Enabling Dynamic Scripting]
(https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-scripting.html#enable-dynamic-scripting).

java_packages:
> Override the list of Java packages installed by [geerlingguy.java](https://galaxy.ansible.com/geerlingguy/java). The role will 
install the default package for the OS family of the base image.

java_home: ""
> Set the global value of JAVA_HOME to this value. Defaults to "". 

## Dependencies

- geerlingguy.java


## License

Apache v2

## Author Information

[@chouseknecht](https://github.com/chouseknecht)
