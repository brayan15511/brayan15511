<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>GitHub Stats</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
      $(document).ready(function(){
        // Informações do perfil
        $.getJSON("https://api.github.com/users/SEU_USERNAME", function(data){
          $("#nome-usuario").html(data.name);
          $("#avatar-usuario").attr("src", data.avatar_url);
          $("#bio-usuario").html(data.bio);
          $("#seguidores-usuario").html(data.followers);
          $("#seguindo-usuario").html(data.following);
          $("#repositorios-usuario").html(data.public_repos);
        });

        // Informações dos repositórios
        $.getJSON("https://api.github.com/users/SEU_USERNAME/repos", function(data){
          for(var i=0; i<data.length; i++){
            var repo = data[i];
            var html = "<li><a href='" + repo.html_url + "'>" + repo.name + "</a>: " + repo.description + " (" + repo.language + ")</li>";
            $("#repositorios-lista").append(html);
          }
        });
      });
    </script>
  </head>
  <body>
    <h1>GitHub Stats</h1>
    <h2>Perfil</h2>
    <div>
      <img id="avatar-usuario" alt="Avatar do usuário" width="100">
      <h3 id="nome-usuario"></h3>
      <p id="bio-usuario"></p>
      <p>Seguidores: <span id="seguidores-usuario"></span></p>
      <p>Seguindo: <span id="seguindo-usuario"></span></p>
      <p>Repositórios públicos: <span id="repositorios-usuario"></span></p>
    </div>
    <h2>Repositórios</h2>
    <ul id="repositorios-lista"></ul>
  </body>
</html>

