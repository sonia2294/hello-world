node{
properties(
    [parameters([choice(choices: ["master","develop"].join("\n"),
    description: 'Some choice parameter', 
    name: 'environment')])])
    
    switch(params.environment ){
        case 'master':
            echo "master will be processed"
            break
        case 'develop':
            echo "develop will be processed"
            break
    }
}
