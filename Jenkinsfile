def _setGit(){
    withCredentials([usernamePassword(credentialsId: 'demoId', usernameVariable: 'GIT_USER', passwordVariable: 'GIT_PASS')]){

        
        echo "${GIT_USER}"
        echo "${GIT_PASS}"

    }
}

def checkoutBranch(){

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
   
    checkoutBranch()
    
}
