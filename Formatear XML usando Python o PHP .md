---
title: Formatear XML usando Python o PHP 
date: 2019-03-22 12:33:13
categories: []
tags: []
authors: sedlav
---
        
				<p class="main-title" itemprop="headline">
				LibreByte
		</p>
				<p class="site-description">
			Noticias y tutoriales sobre software libre
		</p>
				Inicio
Acerca de
GNU/Linux
MySql
Apache
PHP
FTP
Trucos
OpenEMR
Donar
Contácteme
English
			Skip to content
	<h1 class="entry-title">Formatear XML usando Python o PHP</h1>							
				abril 21, 2016 by sedlav
				<p>Para formatear ficheros XML generalmente uso la variante 3 descrita en Formatear ficheros XML pero recientemente he tenido la necesidad de trabajar con ficheros XML que además de estar ofuscado una parte del XML usa entidades html, partamos de que debemos trabajar con un fichero XML como el siguiente:</p>
&lt;?xml version="1.0" encoding="UTF-8" ?&gt;
&lt;!DOCTYPE Edit_Mensaje SYSTEM "Edit_Mensaje.dtd"&gt;
&lt;Edit_Mensaje&gt;
     &lt;Mensaje&gt;
          &lt;Remitente&gt;
               &lt;Nombre&gt;Nombre del remitente&lt;/Nombre&gt;
               &lt;Mail&gt; Correo del remitente &lt;/Mail&gt;
          &lt;/Remitente&gt;
          &lt;Destinatario&gt;
               &lt;Nombre&gt;Nombre del destinatario&lt;/Nombre&gt;
               &lt;Mail&gt;Correo del destinatario&lt;/Mail&gt;
          &lt;/Destinatario&gt;
          &lt;Texto&gt;
               &lt;Asunto&gt;
                    Este es mi documento con una estructura muy sencilla
                    no contiene atributos ni entidades...
               &lt;/Asunto&gt;
               &lt;Parrafo&gt;
                    Este es mi documento con una estructura muy sencilla
                    no contiene atributos ni entidades...
               &lt;/Parrafo&gt;
          &lt;/Texto&gt;
     &lt;/Mensaje&gt;
&lt;/Edit_Mensaje&gt;
<p>Nota: Fichero Obtenido de Wikipedia: Extensible Markup Language</p>
<p>pero que en lugar de tenerlo como se muestra más arriba lo tenemos de la siguiente manera:</p>
&lt;Edit_Mensaje&gt;&lt;Mensaje&gt;&amp;lt;Remitente&amp;gt;&amp;lt;Nombre&amp;gt;Nombre del remitente&amp;lt;/Nombre&amp;gt;&amp;lt;Mail&amp;gt;Correo del remitente&amp;lt;/Mail&amp;gt;&amp;lt;/Remitente&amp;gt;&amp;lt;Destinatario&amp;gt;&amp;lt;Nombre&amp;gt;Nombre del destinatario&amp;lt;/Nombre&amp;gt;&amp;lt;Mail&amp;gt;Correo del destinatario&amp;lt;/Mail&amp;gt;&amp;lt;/Destinatario&amp;gt;&amp;lt;Texto&amp;gt;&amp;lt;Asunto&amp;gt;Este es mi documento con una estructura muy sencilla no contiene atributos ni entidades...&amp;lt;/Asunto&amp;gt;&amp;lt;Parrafo&amp;gt;Este es mi documento con una estructura muy sencilla no contiene atributos ni entidades... &amp;lt;/Parrafo&amp;gt;&amp;lt;/Texto&amp;gt;&lt;/Mensaje&gt;&lt;/Edit_Mensaje&gt;
<p>¿No muy bonito verdad? y no podemos aplicar las soluciones ofrecidas en Formatear ficheros XML debido a que el XML contiene entidades html así que tuve echarle mano y hacer un script primero en Python y luego en PHP:</p>
<h2>Scripts</h2>
<p>Ambos script ejecutan la siguiente lógica:</p>
<h3>Script en Python</h3>
 Fork me on Github
#!/usr/bin/python
import os
import re
import HTMLParser as parser
import xml.dom.minidom as minidom
import sys
try:
    # Read de file name from standard input
    filename = sys.argv[1]
    if os.path.isfile(filename) and os.access(filename, os.R_OK):
        # Open the file in read only mode
        file = open(filename, 'r')
        # Read the file and decode html entities
        xml = parser.HTMLParser().unescape(file.read())
        # Pretify the xml
        xml = minidom.parseString(xml).toprettyxml()
        # Handle issue with CDATA section due minidom add extraspace
        # before/after CDATA
        xml = re.sub('&gt;\s+&lt;!', '&gt;&lt;!', xml)
        xml = re.sub(']&gt;\s+&lt;', ']&gt;&lt;', xml)
        # Remove empty lines
        # Thanks to http://stackoverflow.com/questions/1140958/whats-a-quick-one-liner-to-remove-empty-lines-from-a-python-string
        print "".join([s for s in xml.strip().splitlines(True) if s.strip()])
    else:
        print "File is missing or is not readable!"
except IndexError:
    print "You must specify a file name!"
<h3>Script en PHP</h3>
 Fork me on Github
#!/usr/bin/env php
&lt;?php
// Check the scripts is called with arguments
if (empty($argv[1])) {
    die('You must specify a file!');
}
// Set the file name
$file = $argv[1];
// Verify if filename exists
if (!is_readable($file)) {
    die('File is missing or is not readable!');
}
// Get the file content
$content = file_get_contents($file);
// Verify the content is not empty
if (empty($content)) {
    die('File is empty nothing to do ;)');
}
// Decode html entities
$content = html_entity_decode($content);
// Parse the xml and format it
$doc = new DOMDocument();
$doc-&gt;preserveWhiteSpace = false;
$doc-&gt;formatOutput = true;
$doc-&gt;loadXML($content);
// Print the result
echo $doc-&gt;saveXML();
<p>Ahora podemos integrar los scripts anteriores con gedit para ello (En este caso solo lo haremos para el script desarrollado en PHP):</p>
<p></p>
<p>Abrimos nuestro fichero xml al cual le llamamos garbage.xml</p>
<p></p>
<p>Luego lo formateamos usando la combinación de teclas que establecimos cuando integramos la herramientas externa en el gedit y nos quedaría como muestra la figura.</p>
<p></p>
<h3>Lecturas recomendadas</h3>
<p>* Formatear ficheros XML </p>
(adsbygoogle = window.adsbygoogle || []).push({});
<h3 class="sd-title">Comparte esto:</h3>
	Posted in GNU/Linux, PHPTagged Python, XML			
			<h2 class="comments-title">
			2 thoughts on “Formatear XML usando Python o PHP”		</h2>
						danesc87 dice:					
								mayo 19, 2016 a las 9:48 pm							
					<p>Excelente post, estoy usando el script en python con unas pequeñas modificaciones para hacerlo funcionar como acción personalizada en thunar, además de un port a python3.</p>
<p>El repo github donde lo tengo alojado es en:</p>
<p>https://github.com/danesc87/dotsAndConfs</p>
				Responder			
						sedlav dice:					
								mayo 19, 2016 a las 10:04 pm							
					<p>Gracias por tu contribución y hace un port a python3, los scripts anteriores también se pueden encontrar en: </p>
<p>Python: https://gist.github.com/yoander/ae488ac7465a9e77f6f63b0c61e58f5c
PHP:  https://gist.github.com/yoander/7b9821ad5d077dc88cc29e1ab031ea0f</p>
<p>Ambos script pueden usarse, distribuirse y modificarse libremente ya que son liberados bajos licencia GPLv2+</p>
				Responder			
</li>
</li>
		<h3 id="reply-title" class="comment-reply-title">Deja un comentario Cancelar respuesta
</h3>			
				<p class="comment-notes">Tu dirección de correo electrónico no será publicada. Los campos obligatorios están marcados con *</p>
<p class="comment-form-comment">Comentario </p>
<p class="comment-form-author">Nombre * </p>
<p class="comment-form-email">Correo electrónico * </p>
<p class="comment-form-url">Web </p>
<p class="form-submit"></p>
<p class="comment-subscription-form">Recibir un email con los siguientes comentarios a esta entrada.</p>
<p class="comment-subscription-form">Recibir un email con cada nueva entrada.</p>
<p style="display: none;"></p>
<p style="display: none;"></p>			
	<p class="akismet_comment_form_privacy_notice">Este sitio usa Akismet para reducir el spam. Aprende cómo se procesan los datos de tus comentarios.</p>
(adsbygoogle = window.adsbygoogle || []).push({});
				Search			
<h2 class="widget-title">Lo + Popular</h2>
<li>
MySQL ejecutar script SQL
</li>
<li>
lftp – Error certificado no confiable
</li>
<li>
rsync – 16 ejemplos prácticos
</li>
<li>
Dropbear SSH una alternativa ligera a OpenSSH
</li>
<li>
Como leer un fichero línea a línea desde Bash
</li>
<li>
Cómo instalar MySQL 5.7 en CentOS 7
</li>
<li>
Acceder/Montar particiones NTFS en GNU/Linux
</li>
<li>
12 ejemplos prácticos del comando grep
</li>
<li>
BIND: Resolver connection timed out; no servers could be reached
</li>
<li>
Crear / Modificar / Eliminar tablas en MySQL
</li>
<h2 class="widget-title">Entradas recientes</h2>		
<li>
					5 nuevas características de PHP 7.2
									</li>
											<li>
					Cómo reemplazar el Lanzador de Aplicaciones de GNOME por Synapse
									</li>
											<li>
					7 Características novedosas de PHP 7.1
									</li>
											<li>
					Cómo comparar objectos en PHP
									</li>
											<li>
					Cómo descargar archivos usando curl
									</li>
											<li>
					Como resolver Class ‘DOMDocument’ not found error
									</li>
											<li>
					Cómo Compilar/Instalar PHP-7.2 en CentOS
									</li>
											<li>
					pbt – Una herramienta para compilar PHP
									</li>
											<li>
					Fondos Piña dona un millón de dollares a la Fundación de Software Libre
									</li>
											<li>
					Cómo compilar PHP 7.1 en Ubuntu 16.04
									</li>
					<h2 class="widget-title">Suscríbete al blog por correo electrónico</h2>
<p>Introduce tu correo electrónico para suscribirte a este blog y recibir notificaciones de nuevas entradas.</p>
                    <p id="subscribe-email">
							Dirección de email                        
                        </p>
                    <p id="subscribe-submit">
	                        Suscribir                        
                    </p>
(adsbygoogle = window.adsbygoogle || []).push({});
                    <p>
                        </p>
<p>Copyleft LibreByte. Toda la información disponible en LibreByte es liberada bajo los términos de Licencia Pública General GNU / Licencia de Documentación Libre GNU.</p>
<p>Enlaces y referencias a terceros se acogen a la licencia adoptada por terceros</p>
<p>Impulsado por Wordpress, GiottoPress y mck host</p>
<p></p>
		window.WPCOM_sharing_counts = {"https:\/\/www.librebyte.net\/gnulinux\/formatear-xml-usando-python-o-php\/":2694};
			Enviar a dirección de correo electrónico
			Su Nombre
				Tu dirección de correo electrónico
				Cancelar
				La entrada no fue enviada. ¡Comprueba tus direcciones de correo electrónico!			
				Error en la comprobación de email. Por favor, vuelve a intentarlo			
				Lo sentimos, tu blog no puede compartir entradas por correo electrónico.			
/*  */
/*  */
var windowOpen;
			jQuery( document.body ).on( 'click', 'a.share-facebook', function() {
				// If there's another sharing window open, close it.
				if ( 'undefined' !== typeof windowOpen ) {
					windowOpen.close();
				}
				windowOpen = window.open( jQuery( this ).attr( 'href' ), 'wpcomfacebook', 'menubar=1,resizable=1,width=600,height=400' );
				return false;
			});
var windowOpen;
			jQuery( document.body ).on( 'click', 'a.share-twitter', function() {
				// If there's another sharing window open, close it.
				if ( 'undefined' !== typeof windowOpen ) {
					windowOpen.close();
				}
				windowOpen = window.open( jQuery( this ).attr( 'href' ), 'wpcomtwitter', 'menubar=1,resizable=1,width=600,height=350' );
				return false;
			});
var windowOpen;
			jQuery( document.body ).on( 'click', 'a.share-linkedin', function() {
				// If there's another sharing window open, close it.
				if ( 'undefined' !== typeof windowOpen ) {
					windowOpen.close();
				}
				windowOpen = window.open( jQuery( this ).attr( 'href' ), 'wpcomlinkedin', 'menubar=1,resizable=1,width=580,height=450' );
				return false;
			});
var windowOpen;
			jQuery( document.body ).on( 'click', 'a.share-tumblr', function() {
				// If there's another sharing window open, close it.
				if ( 'undefined' !== typeof windowOpen ) {
					windowOpen.close();
				}
				windowOpen = window.open( jQuery( this ).attr( 'href' ), 'wpcomtumblr', 'menubar=1,resizable=1,width=450,height=450' );
				return false;
			});
pre.hljs { padding: 5px; }
pre.hljs code {}
        jQuery(document).ready(function($) {
            $('pre').each(function (index, elem) {
                var code = elem;
                // Remove any inline style
                $(code).removeAttr('style');
                var chd = $(elem).children('code');
                if (chd.length > 0) {
                    code = chd;
                    // Remove any inline style
                     $(code).removeAttr('style');
                }
                var langAttr = $(code).attr('lang') || $(code).attr('language');
                if (langAttr !== undefined) {
                    $(code).attr('class', langAttr);
                    $(code).removeAttr('lang language autolinks');
                } else {
                    var defaultLang = "";
                    var htmlClass = $(code).attr('class');
                    if (htmlClass !== undefined) {
                        // Detect if language definition is compatible with Crayon
                        // Or SyntaxHighligther
                        var pattern = /(lang|brush|crayon)\s*:\s*(\w+-?)+/i;
                        var matches = pattern.exec(htmlClass);
                        if (null !== matches) {
                            htmlClass = "false" == matches[2].toLowerCase() ? "nohighlight" : matches[2];
                            $(code).attr('class', htmlClass);
                        // Find if class attribute is compatible with Crayon or
                        // SyntaxHighligther definition, ex: "toolbar:false nums:false"
                        } else if (htmlClass.match(/(\w+-?)+\s*:\s*(\w+-?)+/i)) {
                            // Set default language to bash to avoid erroneus
                            // language detection for single line
                            $(code).attr('class', defaultLang);
                        }
                    } else {
                        // Set default language to bash to avoid erroneus
                        // language detection for single line
                        $(code).attr('class', defaultLang);
                    }
                }
                hljs.highlightBlock(elem);
            });
        });
	_stq = window._stq || [];
	_stq.push([ 'view', {v:'ext',j:'1:7.1.1',blog:'61595422',post:'2694',tz:'-5',srv:'www.librebyte.net'} ]);
	_stq.push([ 'clickTrackerInit', '61595422', '2694' ]);


[Link](https://www.librebyte.net/gnulinux/formatear-xml-usando-python-o-php/)
