properties([pipelineTriggers([pollSCM('* * * * * ')])])
node {
    stage("clone") {
        git branch: 'master', url: 'https://github.com/danielshine1/MySoftware.git'
    }
    stage("show files"){
        sh "ls -l"
    }
}