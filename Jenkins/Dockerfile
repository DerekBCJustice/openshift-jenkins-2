# Useful command to see installed plugins
# Jenkins Script Console: http://<jenkins-url>/script
#
#Jenkins.instance.pluginManager.plugins.each{
#  plugin ->
#    println ("${plugin.getShortName()}:${plugin.getVersion()}")
#}

FROM openshift/jenkins-2-centos7:v3.11

COPY ./config/plugin.txt /opt/openshift/configuration/plugins.txt
RUN /usr/local/bin/install-plugins.sh /opt/openshift/configuration/plugins.txt

ENV OPENSHIFT_ENABLE_OAUTH=true
ENV OPENSHIFT_ENABLE_REDIRECT_PROMPT=true
ENV OPENSHIFT_JENKINS_JVM_ARCH=x86_64
ENV KUBERNETES_MASTER="https://kubernetes.default:443"
ENV KUBERNETES_TRUST_CERTIFICATES=true
ENV JENKINS_PASSWORD=EC5qFhMx5f2hKKvLgtxG
ENV JAVA_OPTS="-XX:MaxMetaspaceSize=512m -Duser.timezone=America/Vancouver -Dhudson.model.DirectoryBrowserSupport.CSP="
ENV OPENSHIFT_ENABLE_OAUTH=true
ENV ACCEPT_EULA=Y
	
USER root


	
EXPOSE 8080


