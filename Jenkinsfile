node{
    
    stage('Print Branch name'){
        
        echo "Current branch is ${env.BRANCH_NAME}"
        sh 'whoami'
    }
    
    stage('SCM checkout master'){
        checkout scm
    }
    
    stage('Build enveronment') {
        
        if (env.BRANCH_NAME=='dev') {
            sh 'ansible-playbook -i dev.inventory site.yml'
        }
        else if(env.Branch_name=='qa'){
        sh 'ansible-playbook -i qa.inventory site.yml'
    
    }
    }
}
