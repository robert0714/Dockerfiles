FROM  robert0714/oracle-java-8:8u151
LABEL MAINTAINER Robert lee <robert0714@gmail.com>


# Define commonly used JAVA_HOME variable

ENV LANGUAGE        zh_TW.UTF-8
ENV LANG            zh_TW.UTF-8
ENV LC_ALL          zh_TW.UTF-8

RUN apt-get update && \
    apt-get install -y  \
    zip  curl \
    unzip  &&  \
    rm -rf /var/lib/apt/lists/*


RUN cd /tmp/ && \
    curl -k -LO "http://download.oracle.com/otn-pub/java/jce/8/jce_policy-8.zip" -H 'Cookie: oraclelicense=accept-securebackup-cookie'  --output   /tmp/jce_policy-8.zip &&   \
    unzip /tmp/jce_policy-8.zip    &&  \
    ls   -la  /tmp  && \
    rm /tmp/jce_policy-8.zip   &&  \
    yes |cp -v -f  /tmp/UnlimitedJCEPolicyJDK8/*.jar   /usr/lib/jvm/java-8-oracle/jre/lib/security/


# Define default command.
CMD ["bash"]
