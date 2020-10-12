node{
    stage("check out"){
        dir("projecta"){
            git  credentialsId: 'yyl', url: 'https://github.com/yylstudy/jenkins.git',branch:"${ABRANCHNAME}"
            sh "mvn clean install"
        }
        dir("projectb"){
            git  credentialsId: 'yyl', url: 'https://github.com/yylstudy/jenkins.git',branch:"${BBRANCHNAME}"
            sh "mvn clean install"
        }
        sh "rm -rf baseline.yml"
        sh "echo ${ABRANCHNAME} > baseline.yml"
        sh "echo ${BBRANCHNAME} >> baseline.yml"

    }
}