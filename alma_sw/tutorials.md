<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Cómo hacer deployment de herramientas offline en preproducción</a></li>
</ul>
</div>
</div>

# Cómo hacer deployment de herramientas offline en preproducción<a id="sec-1" name="sec-1"></a>

1.  Conectar por SSH a máquina de configuraciones

    ssh root@adrastea.sco.alma.cl

1.  Descargar tar con release del branch a hacer deployment

2.  Conectar por SSH a la máquina correspondiente al componente a desplegar

    ssh root@eduarda.sco.alma.cl

1.  Hacer backup de aplicación previa

    cd /usr/local/tomcat;
    cp -rp webapps webapps-$(date +%Y%m%d);

1.  Bajar servidor Tomcat

    supervisorctl stop tomcat

1.  Eliminar archivos de aplicación anterior

    cd webapps;
    rm -rf *;

1.  Copiar desde máquina de configuraciones archivo WAR de aplicación

    rsync -a root@adrastea.sco.alma.cl:/alma/ACS-2016.5/ACSSW-201608-CYCLE4-OFF-B-2016-09-15-19-00-00/lib/cas-server-webapp.war .

1.  Lanzar servidor Tomcat

    supervisorctl start tomcat