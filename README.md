# Shortcodes para o plugin Pods - Tipos de conteúdo e campos personalizados

## Para baixar o plugin [clique aqui](https://br.wordpress.org/plugins/pods/)

## Para que os shortcodes funcionem de acordo é preciso alterar uma configuração
__No painel do Wordpress e com o plugin instalado e ativo...__  
1 - Clique me Pods Admim;  
2 - Depois em Configurações;  
3 - Em Segurança;  
4 - Marque a opção __Unrestricted__

Lista do custom post type produtos, utilizando o template Produtos Relacionados em lista randômica com limite de 4 posts.  
````
[pods name="produtos" template="Produtos Relacionados" orderby="RAND()" limit="4"]  
````

Lista DESC com limite de 1000 posts.  
`````
[pods name="pagina_artista"  template="Artista Lista" orderby="date DESC" limit="1000" /]  
`````

Carrega os conteúdo de um custom post de um determinado ID.  
`````
[pods name="pagina_artista"  template="Artista Page"  id="702" /]  
`````

Carrega a lista de posts de terminados campos personalizados nesse caso o campo tipo_de_midia com o slug album e o campo nome_artista com o slug iza-sabino.  
`````
[pods name="musica"  template="Musica Lista Singles" where="tipo_de_midia.slug = 'single' " where="nome_artista.slug = 'iza-sabino'" orderby="date DESC" limit="1000" /]
`````
