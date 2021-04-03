@Library('jenkins-pipeline-libs')
import lulu.jenkins.utils.*
import lulu.jenkins.ci.*

node ("ci") {

    def pipeline = new K8sServicePipeline(this)
    pipeline.orgName = liyaka
    pipeline.projectName = "dummy-app-service"
    pipeline.dockerImageName = "dummy-app"
    pipeline.preBuildCommand = "VERSION=`cat version-base.txt`.${BUILD_NUMBER};echo \$VERSION > version.txt"

    pipeline.setBranchProperties()
    pipeline.run()

}
