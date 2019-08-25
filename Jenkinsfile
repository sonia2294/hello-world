def _setGit(){
    withCredentials([usernamePassword(credentialsId: 'demoId', usernameVariable: 'GIT_USER', passwordVariable: 'GIT_PASS')]){
        sh 'git config --global user.email "soniatandel.st@gmail.com"'
        sh 'git config --global user.name "Sonia Tandel"'
        
 
        
        sh 'git config remote.origin.url https://github.com/sonia2294/hello-world.git'
        
        sh 'git remote set-url origin https://github.com/sonia2294/hello-world.git'
        
        sh 'git checkout master'
        sh 'git pull'
    }
}



node{
    skipDefaultCheckout()
    
    _setGit()
    /*
    properties([
        parameters([
            choice(choices:['master','develop'].join('\n'), description: 'Select a branch', name: 'branch')
        ])
    ])
    */
   
 
    
}
