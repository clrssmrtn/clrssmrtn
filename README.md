<!DOCTYPE html>
<html>
<head>
  <title>Liste déroulante avec sélection multiple</title>
</head>
<body>

<select id="maListe" multiple>
  <option value="valeur1">Option 1</option>
  <option value="valeur2">Option 2</option>
  <option value="valeur3">Option 3</option>
  <option value="valeur4">Option 4</option>
</select>

<script>
// Récupérer l'élément select
var liste = document.getElementById('maListe');

// Écouter les changements de sélection
liste.addEventListener('change', function() {
  var options = liste.options;
  var selectedValues = [];
  
  // Parcourir toutes les options pour récupérer les valeurs sélectionnées
  for (var i = 0; i < options.length; i++) {
    if (options[i].selected) {
      selectedValues.push(options[i].value);
    }
  }

  // Afficher les valeurs sélectionnées dans la console
  console.log("Valeurs sélectionnées : ", selectedValues);
});
</script>

</body>
</html>
