node {
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("peterkemley/cw2-webapp:version-1.0")

        /* Push the container to the custom Registry */
        customImage.push()


        sh("""docker run -p 49155:8080 -d peterkemley/cw2-webapp""")
    }
}
