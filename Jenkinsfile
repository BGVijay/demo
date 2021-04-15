node {
    checkout scm

    docker.withRegistry('vijaybg213/demo-test', 'dockerhub') {

        def customImage = docker.build("my-image:${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
