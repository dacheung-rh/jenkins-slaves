FROM registry.redhat.io/ocp-tools-4/jenkins-agent-base-rhel8:v4.12.0-1675702335

LABEL com.redhat.component="jenkins-skopeo-slave" \
      name="rhel8/jenkins-skopeo-slave" \
      architecture="x86_64" \
      io.k8s.display-name="Jenkins Slave Image Management" \
      io.k8s.description="Image management tools on top of the jenkins slave base image" \
      io.openshift.tags="openshift,jenkins,slave,copy"
USER root

RUN dnf -y module enable container-tools:rhel8; dnf -y update; dnf -y reinstall shadow-utils; dnf -y install skopeo; rm -rf /var/cache /var/log/dnf* /var/log/yum.*

USER 1001
