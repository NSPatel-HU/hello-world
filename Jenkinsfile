node {
    stage('Checkout SCM'){
        git branch:'jenkins_test', url:'https://github.com/NSPatel-HU/hello-world.git'
    }

    stage('Install node modules'){
        bat "npm install"
    }

    stage('Test'){
        bat "npm run test:headless"    //"npm run test-headless"
    }

    stage('Build'){
        bat "npm run build --prod"
    }

    
}