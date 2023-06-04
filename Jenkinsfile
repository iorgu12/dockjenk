node {
    checkout scm
    def customImage = docker.build("my-image:${env.node:18-alpine}")
    customImage.push()
}
