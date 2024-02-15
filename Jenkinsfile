node {
    // Define your Git credentials ID (configured in Jenkins)
    def gitCredentialsId = 'fcae750f-f7b0-409c-b058-e51fe5b668d0'

    stage('Checkout') {
        // Checkout code from Git repository using credentials
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[credentialsId: gitCredentialsId , url: 'https://github.com/cmkgamer/cmk-container.git']]])
    }

    stage('Build') {
        // Add your build steps here
        // For example, you might use Maven, Gradle, or other build tools
        sh 'ls -a'
    }

    // Add more stages for additional steps (testing, deployment, etc.)

    try {
        // Actions to be performed if the build is successful
        echo 'Build successful!'
    } catch (Exception e) {
        // Actions to be performed if the build fails
        echo 'Build failed!'
    }
}
