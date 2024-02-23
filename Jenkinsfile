properties([pipelineTriggers([pollSCM('*/30 * * * * ')])])
node {
    stage("clone") {
        git branch: 'main', url: 'https://github.com/danielshine1/MySoftware.git'
    }
    stage("run files"){
        sh 'python click.py'
        sh 'python newscreen.py'
    }
}