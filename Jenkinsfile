node {
    stage('Checkout SCM'){
        git branch:'jenkins_test', url:'https://github.com/NSPatel-HU/hello-world.git'
    }

    stage('Install node modules'){
        bat "npm install"
    }

    stage('Test'){
        bat "npx ng test --browsers ChromeHeadless --no-watch --code-coverage"
    }

    stage('Scan'){
        steps{
            withSonarQubeEnv('installationName: sq1'){
                bat "npm run sonar"
            }

        }
    }

    stage('Build'){
        bat "npm run build --prod"
    }

    
}