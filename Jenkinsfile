node {
  
 
  checkout([$class: 'GitSCM', 
    branches: [[name: '*/master']], 
    doGenerateSubmoduleConfigurations: false, 
    extensions: [], 
    submoduleCfg: [], 
    userRemoteConfigs: [[]]
])
  
   stage 'build'
   openshiftBuild(bldCfg: 'gitbook-opeshift-wiki')
}
