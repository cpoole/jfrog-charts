# JFrog Artifactory Chart Changelog
All changes to this chart will be documented in this file.
## [7.18.0] - Sep 17, 2019
* Enabled configuring cache as a secondary disk mount

## [7.17.4] - Sep 11, 2019
* Updated Artifactory version to 6.12.2

## [7.17.3] - Sep 9, 2019
* Updated Artifactory version to 6.12.1

## [7.17.2] - Aug 22, 2019
* Fix the nginx server_name directive used with ingress.hosts

## [7.17.1] - Aug 21, 2019
* Enable the Artifactory container's liveness and readiness probes

## [7.17.0] - Aug 21, 2019
* Updated Artifactory version to 6.12.0

## [7.16.11] - Aug 14, 2019
* Updated Artifactory version to 6.11.6

## [7.16.10] - Aug 11, 2019
* Fix Ingress routing and add an example

## [7.16.9] - Aug 5, 2019
* Do not mount `access/etc/bootstrap.creds` unless user specifies a custom password or secret (Access already generates a random password if not provided one)
* If custom `bootstrap.creds` is provided (using keys or custom secret), prepare it with an init container so the temp file does not persist

## [7.16.8] - Aug 4, 2019
* Improve binarystore config
    1. Convert to a secret
    2. Move config to values.yaml
    3. Support an external secret 

## [7.16.7] - Jul 29, 2019
* Don't create the nginx configmaps when nginx.enabled is false 

## [7.16.6] - Jul 24, 2019
* Simplify nginx setup and shorten initial wait for probes 

## [7.16.5] - Jul 22, 2019
* Change Ingress API to be compatible with recent kubernetes versions 

## [7.16.4] - Jul 22, 2019
* Updated Artifactory version to 6.11.3

## [7.16.3] - Jul 11, 2019
* Add ingress.hosts to the Nginx server_name directive when ingress is enabled to help with Docker repository sub domain configuration 

## [7.16.2] - Jul 3, 2019
* Fix values key in reverse proxy example

## [7.16.1] - Jul 1, 2019
* Updated Artifactory version to 6.11.1

## [7.16.0] - Jun 27, 2019
* Update Artifactory version to 6.11 and add restart to Artifactory when bootstrap.creds file has been modified

## [7.15.8] - Jun 27, 2019
* Add the option for changing nginx config using values.yaml and remove outdated reverse proxy documentation  

## [7.15.6] - Jun 24, 2019
* Update chart maintainers

## [7.15.5] - Jun 24, 2019
* Change Nginx to point to the artifactory externalPort

## [7.15.4] - Jun 23, 2019
* Add the option to provide an IP for the access-admin endpoints

## [7.15.3] - Jun 23, 2019
* Add values files for small, medium and large installations

## [7.15.2] - Jun 20, 2019
* Add missing terminationGracePeriodSeconds to values.yaml

## [7.15.1] - Jun 19, 2019
* Updated Artifactory version to 6.10.4

## [7.15.0] - Jun 17, 2019
* Use configmaps for nginx configuration and remove nginx postStart command

## [7.14.8] - Jun 18, 2019
* Add the option to provide additional ingress rules

## [7.14.7] - Jun 14, 2019
* Updated readme with improved external database setup example

## [7.14.6] - Jun 11, 2019
* Updated Artifactory version to 6.10.3
* Updated installer-info template

## [7.14.5] - Jun 6, 2019
* Updated Google Cloud Storage API URL and https settings

## [7.14.4] - Jun 5, 2019
* Delete the db.properties file on Artifactory startup

## [7.14.3] - Jun 3, 2019
* Updated Artifactory version to 6.10.2

## [7.14.2] - May 21, 2019
* Updated Artifactory version to 6.10.1

## [7.14.1] - May 19, 2019
* Fix missing logger image tag

## [7.14.0] - May 7, 2019
* Updated Artifactory version to 6.10.0

## [7.13.21] - May 5, 2019
* Add support for setting `artifactory.async.corePoolSize`

## [7.13.20] - May 2, 2019
* Remove unused property `artifactory.releasebundle.feature.enabled`

## [7.13.19] - May 1, 2019
* Fix indentation issue with the replicator system property

## [7.13.18] - Apr 30, 2019
* Add support for JMX monitoring

## [7.13.17] - Apr 25, 2019
* Added support for `cacheProviderDir`

## [7.13.16] - Apr 18, 2019
* Changing API StatefulSet version to `v1` and permission fix for custom `artifactory.conf` for Nginx

## [7.13.15] - Apr 16, 2019
* Updated documentation for Reverse Proxy Configuration

## [7.13.14] - Apr 15, 2019
* Added support for `customVolumeMounts`

## [7.13.13] - Aprl 12, 2019
* Added support for `bucketExists` flag for googleStorage

## [7.13.12] - Apr 11, 2019
* Replace `curl` examples with `wget` due to the new base image

## [7.13.11] - Aprl 07, 2019
* Add support for providing the Artifactory license as a parameter

## [7.13.10] - Apr 10, 2019
* Updated Artifactory version to 6.9.1

## [7.13.9] - Aprl 04, 2019
* Add support for templated extraEnvironmentVariables

## [7.13.8] - Aprl 07, 2019
* Change network policy API group

## [7.13.7] - Aprl 04, 2019
* Bugfix for userPluginSecrets

## [7.13.6] - Apr 4, 2019
* Add information about upgrading Artifactory with auto-generated postgres password

## [7.13.5] - Aprl 03, 2019
* Added installer info

## [7.13.4] - Aprl 03, 2019
* Allow secret names for user plugins to contain template language

## [7.13.3] - Apr 02, 2019
* Allow NetworkPolicy configurations (defaults to allow all)

## [7.13.2] - Aprl 01, 2019
* Add support for user plugin secret

## [7.13.1] - Mar 27, 2019
* Add the option to copy a list of files to ARTIFACTORY_HOME on startup

## [7.13.0] - Mar 26, 2019
* Updated Artifactory version to 6.9.0

## [7.12.18] - Mar 25, 2019
* Add CI tests for persistence, ingress support and nginx

## [7.12.17] - Mar 22, 2019
* Add the option to change the default access-admin password

## [7.12.16] - Mar 22, 2019
* Added support for `<artifactory|nginx>.<readiness|liveness>Probe.path` to customise the paths used for health probes

## [7.12.15] - Mar 21, 2019
* Added support for `artifactory.customSidecarContainers` to create custom sidecar containers
* Added support for `artifactory.customVolumes` to create custom volumes

## [7.12.14] - Mar 21, 2019
* Make ingress path configurable

## [7.12.13] - Mar 19, 2019
* Move the copy of bootstrap config from postStart to preStart

## [7.12.12] - Mar 19, 2019
* Fix existingClaim example

## [7.12.11] - Mar 18, 2019
* Add information about nginx persistence

## [7.12.10] - Mar 15, 2019
* Wait for nginx configuration file before using it

## [7.12.9] - Mar 15, 2019
* Revert securityContext changes since they were causing issues

## [7.12.8] - Mar 15, 2019
* Fix issue #247 (init container failing to run)

## [7.12.7] - Mar 14, 2019
* Updated Artifactory version to 6.8.7
* Add support for Artifactory-CE for C++

## [7.12.6] - Mar 13, 2019
* Move securityContext to container level

## [7.12.5] - Mar 11, 2019
* Updated Artifactory version to 6.8.6

## [7.12.4] - Mar 8, 2019
* Fix existingClaim option

## [7.12.3] - Mar 5, 2019
* Updated Artifactory version to 6.8.4

## [7.12.2] - Mar 4, 2019
* Add support for catalina logs sidecars

## [7.12.1] - Feb 27, 2019
* Updated Artifactory version to 6.8.3

## [7.12.0] - Feb 25, 2019
* Add nginx support for tail sidecars

## [7.11.1] - Feb 20, 2019
* Added support for enterprise storage

## [7.10.2] - Feb 19, 2019
* Updated Artifactory version to 6.8.2

## [7.10.1] - Feb 17, 2019
* Updated Artifactory version to 6.8.1
* Add example of `SERVER_XML_EXTRA_CONNECTOR` usage

## [7.10.0] - Feb 15, 2019
* Updated Artifactory version to 6.8.0

## [7.9.6] - Feb 13, 2019
* Updated Artifactory version to 6.7.3

## [7.9.5] - Feb 12, 2019
*  Add support for tail sidecars to view logs from k8s api

## [7.9.4] - Feb 6, 2019
* Fix support for customizing statefulset `terminationGracePeriodSeconds`

## [7.9.3] - Feb 5, 2019
* Add instructions on how to deploy Artifactory with embedded Derby database

## [7.9.2] - Feb 5, 2019
* Add support for customizing statefulset `terminationGracePeriodSeconds`

## [7.9.1] - Feb 3, 2019
* Updated Artifactory version to 6.7.2

## [7.9.0] - Jan 23, 2019
* Updated Artifactory version to 6.7.0

## [7.8.9] - Jan 22, 2019
* Added support for `artifactory.customInitContainers` to create custom init containers

## [7.8.8] - Jan 17, 2019
* Added support of values ingress.labels

## [7.8.7] - Jan 16, 2019
* Mount replicator.yaml (config) directly to /replicator_extra_conf

## [7.8.6] - Jan 13, 2019
* Fix documentation about nginx group id

## [7.8.5] - Jan 13, 2019
* Updated Artifactory version to 6.6.5

## [7.8.4] - Jan 8, 2019
* Make artifactory.replicator.publicUrl required when the replicator is enabled

## [7.8.3] - Jan 1, 2019
* Updated Artifactory version to 6.6.3
* Add support for `artifactory.extraEnvironmentVariables` to pass more environment variables to Artifactory

## [7.8.2] - Dec 28, 2018
* Fix location `replicator.yaml` is copied to

## [7.8.1] - Dec 27, 2018
* Updated Artifactory version to 6.6.1

## [7.8.0] - Dec 20, 2018
* Updated Artifactory version to 6.6.0

## [7.7.13] - Dec 17, 2018
* Updated Artifactory version to 6.5.13

## [7.7.12] - Dec 12, 2018
* Fix documentation about Artifactory license setup using secret

## [7.7.11] - Dec 10, 2018
* Fix issue when using existing claim

## [7.7.10] - Dec 5, 2018
* Remove Distribution certificates creation.

## [7.7.9] - Nov 30, 2018
* Updated Artifactory version to 6.5.9

## [7.7.8] - Nov 29, 2018
* Updated postgresql version to 9.6.11

## [7.7.7] - Nov 27, 2018
* Updated Artifactory version to 6.5.8

## [7.7.6] - Nov 19, 2018
* Added support for configMap to use custom Reverse Proxy Configuration with Nginx

## [7.7.5] - Nov 14, 2018
* Fix location of `nodeSelector`, `affinity` and `tolerations`

## [7.7.4] - Nov 14, 2018
* Updated Artifactory version to 6.5.3

## [7.7.3] - Nov 12, 2018
* Support artifactory.preStartCommand for running command before entrypoint starts

## [7.7.2] - Nov 7, 2018
* Support database.url parameter (DB_URL)

## [7.7.1] - Oct 29, 2018
* Change probes port to 8040 (so they will not be blocked when all tomcat threads on 8081 are exhausted)

## [7.7.0] - Oct 28, 2018
* Update postgresql chart to version 0.9.5 to be able and use `postgresConfig` options

## [7.6.8] - Oct 23, 2018
* Fix providing external secret for database credentials

## [7.6.7] - Oct 23, 2018
* Allow user to configure externalTrafficPolicy for Loadbalancer

## [7.6.6] - Oct 22, 2018
* Updated ingress annotation support (with examples) to support docker registry v2

## [7.6.5] - Oct 21, 2018
* Updated Artifactory version to 6.5.2

## [7.6.4] - Oct 19, 2018
* Allow providing pre-existing secret containing master key
* Allow arbitrary annotations on primary and member node pods
* Enforce size limits when using local storage with `emptyDir`
* Allow providing pre-existing secrets containing external database credentials

## [7.6.3] - Oct 18, 2018
* Updated Artifactory version to 6.5.1

## [7.6.2] - Oct 17, 2018
* Add Apache 2.0 license

## [7.6.1] - Oct 11, 2018
* Supports master-key in the secrets and stateful-set
* Allows ingress default `backend` to be enabled or disabled (defaults to enabled)

## [7.6.0] - Oct 11, 2018
* Updated Artifactory version to 6.5.0

## [7.5.4] - Oct 9, 2018
* Quote ingress hosts to support wildcard names

## [7.5.3] - Oct 4, 2018
* Add PostgreSQL resources template

## [7.5.2] - Oct 2, 2018
* Add `helm repo add jfrog https://charts.jfrog.io` to README

## [7.5.1] - Oct 2, 2018
* Set Artifactory to 6.4.1

## [7.5.0] - Sep 27, 2018
* Set Artifactory to 6.4.0

## [7.4.3] - Sep 26, 2018
* Add ci/test-values.yaml

## [7.4.2] - Sep 2, 2018
* Updated Artifactory version to 6.3.2
* Removed unused PVC

## [7.4.0] - Aug 22, 2018
* Added support to run as non root
* Updated Artifactory version to 6.2.0

## [7.3.0] - Aug 22, 2018
* Enabled RBAC Support
* Added support for PostStartCommand (To download Database JDBC connector)
* Increased postgresql max_connections
* Added support for `nginx.conf` ConfigMap
* Updated Artifactory version to 6.1.0
