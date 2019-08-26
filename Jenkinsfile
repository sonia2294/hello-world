

node{
    skipDefaultCheckout()
    

    properties([
        parameters([
            choice(choices:['master','develop'].join('\n'), description: 'Select a branch', name: 'branch', defaultValue = 'master')
        ])
    ])

  
    
}
