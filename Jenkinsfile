node(){
        
        
  stage('prepareWorksapce'){
        echo "====Hello World===="
  }
  
  stage('checkout'){
    checkout([$class: 'GitSCM',
              poll: true,
              branches: [[name: '*/master']],
              doGenerateSubmoduleConfigurations: false,
              extensions: [], submoduleCfg: [],
              userRemoteConfigs: [[url: 'https://github.com/devdoc24/nodetest2.git']]])
  }
  stage('Prepare Environment'){
            env.NODEJS_HOME = "${tool 'node'}"
            // on linux / mac
           env.PATH="${env.NODEJS_HOME}/bin:${env.PATH}"
           // on windows
          //env.PATH="${env.NODEJS_HOME};${env.PATH}"
          sh '''
          npm --version
          node --version
          '''
        //tool name: 'node', type: 'nodejs' //use tool from predefined tool installation
        //sh 'npm config ls'
        }
        
        stage ('Build Nodejs'){
        sh 'npm pack'
        }
        
}
