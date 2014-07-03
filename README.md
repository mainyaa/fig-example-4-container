Fig example 4 container
======================

Instalation
-----
`$ sudo pip install -U fig`
```
$ fig --version
fig 0.4.2
```

more: ![fig documenation](http://orchardup.github.io/fig/)

Usage
-----

`$ git clone https://github.com/mainyaa/fig-example-4-container`
`$ fig up -d`

```zsh
$ fig up -d
Recreating ctlcblog_serf_1...
Recreating ctlcblog_db_1...
Recreating ctlcblog_web_1...
Creating ctlcblog_lb_1...

$ fig ps
     Name              Command         State                Ports               
-------------------------------------------------------------------------------
ctlcblog_serf_1   /run.sh              Up      49252->7373/tcp, 49253->7946/tcp 
ctlcblog_db_1     /run.sh              Up      49254->3306/tcp                  
ctlcblog_web_1    /run.sh              Up      49255->80/tcp                    
ctlcblog_lb_1     /run.sh              Up      80->80/tcp                       

$ fig scale web=2
Starting ctlcblog_web_2...

$ fig ps
     Name              Command         State                Ports               
-------------------------------------------------------------------------------
ctlcblog_serf_1   /run.sh              Up      49252->7373/tcp, 49253->7946/tcp 
ctlcblog_db_1     /run.sh              Up      49254->3306/tcp                  
ctlcblog_web_2    /run.sh              Up      49256->80/tcp                    
ctlcblog_web_1    /run.sh              Up      49255->80/tcp                    
ctlcblog_lb_1     /run.sh              Up      80->80/tcp  
```

Original
--------
![BUILDING COMPLEX APPS FOR DOCKER ON COREOS AND FIG](http://www.centurylinklabs.com/building-complex-apps-for-docker-on-coreos-and-fig/)

