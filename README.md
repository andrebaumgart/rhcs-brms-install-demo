App Dev Cloud with JBoss BRMS Install Demo 
==========================================
This demo is to install JBoss BRMS in the Cloud based on leveraging the Red Hat Container Development Kit (CDK) and the
provided OpenShift Enterprise (OSE) image. It delivers a fully functioning JBoss BRMS containerized on OSE.


Install on Red Hat CDK OpenShift Enterprise image
-------------------------------------------------
1. First complete the installation and start the OpenShift image supplied in the [cdk-install-demo](https://github.com/eschabell/cdk-install-demo).

2. Install [OpenShift Client Tools](https://developers.openshift.com/managing-your-applications/client-tools.html) if you have not done so previously.

3. [Download and unzip this demo.](https://github.com/eschabell/rhcs-brms-install-demo/archive/master.zip)

4. Add products to installs directory.

5. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges.

6. Login to JBoss BRMS to start developing rules projects:

    [http://rhcs-brms-install-demo.10.1.2.2.xip.io/business-central](http://rhcs-brms-install-demo.10.1.2.2.xip.io/business-central)
    ( u:erics / p:jbossbrms1! )


Tip & Trick
-----------
This is a good way to look at what is being created during all the 'oc' commands above:

    ```
    $ oc get all

    NAME                        TYPE                                           FROM       LATEST
    rhcs-brms-install-demo      Docker                                         Binary     1

    NAME                        TYPE                                           FROM             STATUS     STARTED         DURATION
    rhcs-brms-install-demo-1    Docker                                         Binary@56ed14a   Running    2 minutes ago   2m11s
    
    NAME                        DOCKER REPO                                    TAGS                  UPDATED
    developer                   jbossdemocentral/developer                     1.0,jdk8-uid,latest   10 minutes ago
    rhcs-brms-install-demo      172.30.211.34:5000/rhcs-brms-install-demo/rhcs-brms-install-demo                         

    NAME                             READY                                     STATUS     RESTARTS   AGE
    rhcs-brms-install-demo-1-build   1/1                                       Running    0          2m


Supporting Articles
-------------------
comming soon...


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.0 - JBoss BRMS 6.2.0-BZ-1299002, JBoss EAP 6.4.4 and running on Red Hat CDK using OpenShift Enterprise image. 

![OSE pod](https://github.com/eschabell/rhcs-brms-install-demo/blob/master/docs/demo-images/rhcs-brms-pod.png?raw=true)

![OSE build](https://github.com/eschabell/rhcs-brms-install-demo/blob/master/docs/demo-images/rhcs-brms-build.png?raw=true)

![JBoss BRMS](https://github.com/eschabell/rhcs-brms-install-demo/blob/master/docs/demo-images/jboss-brms.png?raw=true)
