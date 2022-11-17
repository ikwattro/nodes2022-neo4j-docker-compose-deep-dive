* Make sure the directories have the correct permissions
* Make sure that if you run the Enterprise Edition, you accepted the License Agreement
* Check file permissions on mounted folders
* Load plugins if necessary
* Set Docker specific configurations
** log rotation policy : 100M size
** page cache size : 512M
** default listen address : 0.0.0.0
** server discovery and cluster advertised address using container $(hostname)
* Apply configuration settings provided via the environment ( writes them at the end of neo4j.conf )
* Set neo4j's initial password
* Execute the Docker container's CMD