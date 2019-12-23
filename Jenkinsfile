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
        tool name: 'node', type: 'nodejs' //use tool from predefined tool installation
        sh 'npm config ls'
        }
}
