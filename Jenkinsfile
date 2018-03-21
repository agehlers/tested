node {
  
 
  checkout([$class: 'GitSCM', 
    branches: [[name: '*/master']], 
    doGenerateSubmoduleConfigurations: false, 
    extensions: [], 
    submoduleCfg: [], 
    userRemoteConfigs: [[]]
])
  
  checkout([$class: 'GitSCM', branches: [[name: ':^(?(pull/refs/)).*']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanBeforeCheckout']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github0-ae', url: 'https://github.com/agehlers/tested.git']]])

  checkout([$class: 'GitSCM', branches: [[name: '${BRANCH_NAME}']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanBeforeCheckout']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'github0-ae', url: 'https://github.com/agehlers/tested.git']]])
  
  
  
   stage 'build'
   openshiftBuild(bldCfg: 'gitbook-opeshift-wiki')
}
