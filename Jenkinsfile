def _setGit(){

        

        
        sh 'git config remote.origin.url https://github.com/sonia2294/hello-world.git'
        
        sh 'git remote set-url origin https://github.com/sonia2294/hello-world.git'
        
        sh 'git checkout master'
        sh 'git pull'

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
