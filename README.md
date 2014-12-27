GithubManager
=============

But:
----
Pouvoir lister dans un seul dashboard la liste des issues par repos (projet) encore non résoluts

Étapes : 
-----------------
  1. Liste des repos dans l'organisation our l'utilisateur github : (exemple moztn)
    https://api.github.com/orgs/moztn/repos
  2. Pour chaque repo on liste ses issues : (exemple slides-moztn)
    https://api.github.com/repos/moztn/slides-moztn/issues
  3. Donner quelques statistiques 
    * Les issues closed
    * Les issues open
    * ...

Exemple : 
---------
'''
<script>
function printRepoCount() {
  var responseObj = JSON.parse(this.responseText);
  console.log(responseObj.name + "");
}
var request = new XMLHttpRequest();
request.onload = printRepoCount;
request.open('get', 'https://api.github.com/users/chaasof', true)
request.send()
</script>
'''
