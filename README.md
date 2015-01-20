velk-demo-packages
==================

Repo for holding binary packages for running the velk-demo offline.

Packages for installing java and Elasticsearch/Kibana and Logstash stack in separate directories.

buildtarballs.sh can be used to create gzipped tar file of all packages in the install directories

Adding more 
-----------

1. Start up a vagrant machine 
2. Use 'vagrant ssh' to loging
3. Go to the /vagrant/packages directory and create a new sub-directory reflecting a new tarball you want to add
4. Go to the subdirectory created in step 3.
5. Run 'apt-get -s pacakgename' to determine dependent packages
6. Run 'apt-get download packagename dependencyname1 dependencynameN' to downloard locally
7. Go to the velk-demo-packages
8. Add a directory called install-packagename and copy the files from the velk-demo/packages/install-packagename directory to it
9. Amend the buildtarballs.sh script to create a tarball
10. Run ./buildtarballs.sh

If hosting yourself you can now incorporate more offline package install to velk-demo , or you may have forked and want to pull request.

