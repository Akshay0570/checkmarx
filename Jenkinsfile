pipeline {
      
    agent any
   
    stages {
        stage('Checkout using SOURCE_BRANCH') {
             
            steps { 
             git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
   }
        }
    stage('checkmarx ast scan') {
     steps { 
        checkmarxASTScanner additionalOptions: '', baseAuthUrl: 'https://ind.iam.checkmarx.net', branchName: 'master', checkmarxInstallation: 'chekmarx Cli', credentialsId: 'Checkmarx_latest_cred', projectName: 'Demo', serverUrl: 'https://ind.ast.checkmarx.net', tenantName: 'kpmg_ast' 
     }
        }

      
}
}
