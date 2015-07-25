# ubuntu-for-rails

Ubuntu Dockerfile for building Rails apps

Adds in ruby, nginx, build-essentails, and other useful utilities

    docker run -it --rm -p 3000:3000 -v "${PWD}:/hpwd" faroe228/rails2
    cd /hpwd
    rails new blog
    cd blog
    bin/rails server s -b 0.0.0.0
    # above line is so we can access from host machine web browser.

Settings for VirtualBox boot2docker-vm:
    
    Settings/Network/Adapter1
        Attach to: NAT
        
        Advanced:
            Port Forwarding
                Name                 Protocol Host IP   Host Port Guest IP Guest Port
                Rule_expose_port3000 TCP      127.0.0.1 3000               3000
                
       * This allows us to use browser on host machine to access server ports
         running in docker (this should work for sockets bound to 127.0.0.1 or
         0.0.0.0).
         
         
        
