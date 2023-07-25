node {
    stage ('Checkout') {
    sh '''
    mkdir ~/.gradle
    echo systemProp.artifactory.username=${ARTIFACTORY_USER} >> ~/.gradle/gradle.properties
    echo systemProp.artifactory.username=${ARTIFACTORY_APIKEY} >> ~/.gradle/gradle.properties
    echo systemProp.artifactory.server=${ARTIFACTORY_SERVER} >> ~/.gradle/gradle.properties
    chmod a+x gradlew
    '''
    }
    stage ('Build') {
    sh '''
    ./gradlew clean build -x test
    '''
    }
    stage ('Unit Test') {
    sh ''
    ./gradlew test
    '''
    }
}