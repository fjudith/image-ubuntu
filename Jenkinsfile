def jenkinsfile
node {
    sh 'env'
    checkout([
        $class: 'GitSCM',
        poll: false,
        branches: [[name: 'jrmtb/distributed-build']],
        userRemoteConfigs: [[url: 'https://github.com/scaleway/image-tools.git']]
    ])
    jenkinsfile = load 'Jenkinsfile'
}

jenkinsfile()
