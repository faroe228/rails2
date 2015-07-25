# ubuntu-for-rails

Ubuntu Dockerfile for building Rails apps

Adds in ruby, nginx, build-essentails, and other useful utilities

    docker run -it --rm -p 3000:3000 -v "${PWD}:/hpwd" faroe228/rails2
    cd /hpwd
    rails new blog
    cd blog
    bin/rails server s -b 0.0.0.0


