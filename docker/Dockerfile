ARG CORA_DOCKER_JAVA_VERSION
FROM cora-docker-java:${CORA_DOCKER_JAVA_VERSION}

ARG projectname=classicfedorasynchronizer
ARG workdir=/synchronizer


COPY /${projectname}*.jar ${workdir}/${projectname}.jar

COPY /*.properties ${workdir}/properties/

WORKDIR ${workdir}

CMD java -classpath properties/:classicfedorasynchronizer.jar \ 
se.uu.ub.cora.classicfedorasynchronizer.messaging.MessengerListenerStarter \
${messaginghostname} ${messagingport} ${messagingroutingKey} ${messagingusername} \
${messagingpassword} ${databaseurl} ${databaseuser} ${databasepassword} \
${fedorabaseUrl} ${coraapptokenVerifierUrl} ${corabaseUrl} ${corauserId} ${coraapptoken}