FROM jenkins
LABEL maintainer 'oconnormi'

ENV PLUGINS="ace-editor blueocean-web git-server pam-auth ssh-credentials \
            analysis-core blueocean git pipeline-build-step ssh-slaves \
            ant bouncycastle-api github-api pipeline-github-lib structs \
            antisamy-markup-formatter branch-api github-branch-source \
            pipeline-graph-analysis token-macro authentication-tokens \
            build-timestamp github-organization-folder pipeline-input-step \
            variant aws-credentials cloud-stats github pipeline-maven \
            windows-slaves aws-java-sdk cloudbees-folder gradle \
            pipeline-milestone-step workflow-aggregator blueocean-autofavorite \
            config-file-provider handlebars pipeline-model-api workflow-api \
            blueocean-commons credentials-binding icon-shim \
            pipeline-model-declarative-agent workflow-basic-steps \
            blueocean-config credentials jackson2-api pipeline-model-definition \
            workflow-cps-global-lib blueocean-dashboard custom-tools-plugin \
            javadoc pipeline-model-extensions workflow-cps blueocean-display-url \
            display-url-api jquery-detached pipeline-rest-api \
            workflow-durable-task-step blueocean-events docker-commons \
            jquery pipeline-stage-step workflow-job blueocean-git-pipeline \
            docker-plugin junit pipeline-stage-tags-metadata workflow-multibranch \
            blueocean-github-pipeline docker-workflow ldap pipeline-stage-view \
            workflow-scm-step blueocean-i18n durable-task mailer \
            pipeline-utility-steps workflow-step-api blueocean-jwt ec2 \
            matrix-auth plain-credentials workflow-support \
            blueocean-personalization extended-choice-parameter matrix-project \
            pubsub-light yet-another-docker-plugin blueocean-pipeline-api-impl \
            external-monitor-job maven-plugin scm-api blueocean-pipeline-editor \
            favorite metrics script-security blueocean-rest-impl findbugs \
            momentjs sse-gateway blueocean-rest git-client node-iterator-api \
            ssh-agent"

COPY install_jenkins_plugin.sh /scripts/

USER root
RUN chmod 755 /scripts/*.sh \
    && chown jenkins.jenkins /scripts/*.sh \
    && /scripts/install_jenkins_plugin.sh $PLUGINS

USER jenkins
