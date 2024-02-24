properties([pipelineTriggers([pollSCM('* * * * * ')])])
node {
    stage("clone") {
        git branch: 'main', url: 'https://github.com/danielshine1/MySoftware.git'
    }
    stage("show files"){
        sh "ls -l"
    }
}