pipeline {
    agent any

    options {
        buildDiscarder(logRotator(numToKeepStr:'10'))
    }

    stages {
        stage('Gradle Env access') {
            steps {
                echo "Starting build ${BUILD_ID} for ${JOB_NAME}"
                sh "./gradlew printBuildId -Pbuild_id=${BUILD_ID}"
            }
        }
    }
}