# jenkis-configurations
contains the jenkins job configurations the s-case repository builds

Most of the jobs are simple mvn builds. Each respository has a 
* continuousbuild - runs mvn clean install
* checkstylefindbugs- runs mvn checkstyle:checkstyle findbugs:findbugs
* IT - runs integration tests 
* QM - runs mvn sonar:sonar
* CEV - runs org.owasp:dependency-check-maven:check (see [OWASP Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check))


A special job is `s-case_update-site_build`. This job builds and deploys
the eclipse plugin to an update site. This is a little bit more tricky due the tycho dependency
management.

