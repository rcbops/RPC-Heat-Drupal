- Out-of-the-box performance enhancements made to Drupal, Apache, PHP, and Galera. Enhancements include PHP object caching, Memcached integration, Apache and performance configuration settings, and more.

- Enhanced Cloud security through network isolation and security group isolation at various levels within the stack. To protect your data, the database servers are isolated from the web tier DMZ and are only available through a bastion gateway load balancer.

- A true multi-master MySQL backend provided by Galera clustering and MariaDB. This backend enables the application to better withstand the higher failure rates of commodity and older infrastructure found in Cloud environments.

- Decentralized file servers that use csync2 and lsyncd to push data to other servers on creation events. Centralized network file servers have higher failure rates in cloud environments, are more difficult to ensure data integrity, and almost always suffer performance loss. The csync2 and lsyncd model minimizes data traffic and allows substantially more application servers to participate in the cluster. We also utilize sticky sessions on the front-end load balancer to maintain user experience while the sync events are taking place.

- SSL termination at the load balancer. This feature enables secure customer transactions without the additional CPU overhead of computing SSL on application instances. Network isolation and firewalling keep non-SSKL traffic isolated from outside networks.

