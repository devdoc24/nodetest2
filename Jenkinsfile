
#! groovy

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
  

}
