# asb_antenne-sb

<ul>
<li>1 - Installation d'un wordpress vierge</li>
<li>2 - Installer all in one</li>
<li>3 -  Importer le fichier .wpress</li>
</ul>




<p>Les étapes à suivre si all in one ne fonctionne pas  : </p>

<ul>
<li>1 - Import de la base de données </li>
<li>2 - Execute les scripts UDATE...SET (comme mon script)</li>
<li>3 - Installation d'un wordpress vierge qui pointe vers la BDD importé</li>
<li>4 - Editer le wp-config.php et remplacer $table_prefix avec la donnée : $table_prefix = 'wp_asb';</li>
<li>5 - Modifie les defines pour que ça pointe vers la bdd local si ce n'est pas le cas</li>
<li>6 - Relance sur l'url localhost/wordpress/wp-login.php</li>
</ul>


<p>UPDATE h5cfd277dboptions SET option_value = replace(option_value, 'https://oceanepubantenne.live-website.com/', 'http://localhost/wordpress%27) ;</p>
<p>UPDATE h5cfd277dbposts SET post_content = replace(post_content, 'https://oceanepubantenne.live-website.com/', 'http://localhost/wordpress%27) ;</p>
<p>UPDATE h5cfd277dbposts SET guid = replace(guid, 'https://oceanepubantenne.live-website.com/', 'http://localhost/wordpress%27) ;</p>
<p>UPDATE h5cfd277dblinks SET link_url = replace(link_url, 'https://oceanepubantenne.live-website.com/', 'http://localhost/wordpress%27) ;
</p>


