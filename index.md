<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device width, initial-scale=1">
	<title>Bin</title>
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
	<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.0/jquery.min.js"></script>

	<style type="text/css">
		.choix {
		}

		.cargen{
			border-bottom: 1px dashed black;
			padding-bottom: 10px;
			margin-bottom: 10px;
		}

		@font-face {
			font-family: ethnocentric_rg;
			src:url(font/ethnocentric_rg.ttf);
		}

		.textbig {
			font-weight: bold;
			margin-bottom: 1em;
			font-size: 1.7em;
			margin: 0.5em;
			font-family: ethnocentric_rg;
			background-color: #b3b3b3;
			text-align: center;
			border: 2px solid black;
			border-radius: 1em;
		}

		.texttitle {
			margin-bottom: 1em;
			font-size: 1.5em;
			font-style: italic;
			margin: 0;
			margin-bottom: 0.5em;
			font-family: ethnocentric_rg;
			color: #e53607;
			text-align: center;
		}

		.textres {
			font-weight: bold;
			font-size: 1.2em;
			text-align: center;
		}

		.imageres {
			width: 100px;
			transform: rotate(180deg);
		}

		.selectlabel {
			padding: 0;
			font-weight: bold;
			margin-top: 10px;
			text-align: center;
			margin-bottom: 0;
		}

		.selectbox {
			margin-bottom: 2px;
			margin-left: 1em;
			margin-right: 1em;
			padding: 3px;
			padding-left: 15px;
			cursor: pointer;
			border-radius: 40px;
			background-color: #dddddd;
			color: black;
			font-weight: bold;
			border: 2px solid black;
		}
	</style>

</head>

<body>
	<div class="col mb-3">
		<div class="textbig">Configurateur de bineuse</div>
		<div class="texttitle">Caracteristiques generales</div>
		<div class="row justify-content-center cargen">
			<div class="col-5 col-sm-4 col-md-3 col-lg-2 my-auto mr-2">
				<div class="row choix">
					<label class="col-12 selectlabel" for="type">Type de bineuse</label>
					<select class="col selectbox" id="type" name="type">
						<option>Fixe</option>
						<option>Repliable</option>
					</select>
				</div>
				
				<div class="row choix">
					<label class="col-12 selectlabel" for="rang">Nombre de rangs</label>
					<select class="col selectbox" id="rang" name="rang">
						<option>4</option>
						<option>5</option>
						<option>6</option>
						<option>7</option>
						<option>8</option>
						<option>9</option>
						<option>10</option>
						<option>11</option>
						<option>12</option>
					</select>
				</div>
				
				<div class="row choix">
					<label class="col-12 selectlabel" for="ecart">Ecartement entre rangs</label>
					<select class="col selectbox" id="ecart" name="ecart">
						<option>450</option>
						<option>500</option>
						<option>550</option>
						<option>600</option>
						<option>700</option>
						<option>750</option>
						<option>800</option>
					</select>
				</div>
			</div>
			<div class="col-4 my-auto ml-2">
				<div class="textres">Largeur de poutre</div>
				<div class="textres" id="largbin">3.5 m</div>
				<hr />
				<div class="textres">Prix de la bineuse</div>
				<div class="textres" id="prixbin">8277 €</div>
			</div>
		</div>
		
		<div class="texttitle">Choix du module</div>
		<div class="row justify-content-center">
			<div class="col-5 col-sm-4 col-md-3 col-lg-2 mr-2">
				<div class="row choix">
					<label class="col-12 selectlabel" for="nbdent">Nombre de dents</label>
					<select class="col selectbox" id="nbdent" name="nbdent">
						<option value="20">3 (Rang <= 600)</option>
						<option value="10">5 (Rang > 600)</option>
					</select>
				</div>
				
				<div class="row choix">
					<label class="col-12 selectlabel" for="dent">Type de dents</label>
					<select class="col selectbox" id="dent" name="dent">
						<option value="0">32x10 patte d'oie</option>
						<option value="20">Soc scalpeur</option>
						<option value="40">Lame lelièvre</option>
					</select>
				</div>
				
				<div class="row choix">
					<label class="col-12 selectlabel" for="optav">Option avant</label>
					<select class="col selectbox" id="optav" name="optav">
						<option value="0"></option>
						<option id="pav" value="3">Protège plant</option>
						<option id="kav" value="6">Doigt Kress</option>
					</select>
				</div>
				
				<div class="row choix">
					<label class="col-12 selectlabel" for="optar">Option arrière</label>
					<select class="col selectbox" id="optar" name="optar">
						<option value="0"></option>
						<option value="2">Herse peigne</option>
						<option id="kar" value="1">Doigt Kress</option>
					</select>
				</div>
			</div>
			<div class="col-4 ml-2">
				<div class="textres">Prix du module</div>
				<div class="textres" id="prix">776 €</div>
				<center><img class="imageres" id="image" src="images/m20.png"></center>
			</div>
		</div>
	</div>
</body>
</html>

<script>
	$(document).ready(function(){
		var nb = 0;
		$('#rang').val(5);
		$('#ecart').val(500);
		$('select').on('change',function(){
			var prix = 0;
			var prixtot = 0;
			$('option').prop('disabled',false);
			var dent = parseInt($('#dent').val());
			var optav = parseInt($('#optav').val());
			var optar = parseInt($('#optar').val());
			var nbdent = parseInt($('#nbdent').val());
			var rang = parseInt($('#rang').val());
			var ecart = parseInt($('#ecart').val());
			var type = $('#type').val();
			if (dent == 40) {
				if (optav !== 0) {
					$('#optav').val(0);
					optav = 0;
				}
				$('#pav').prop('disabled',true);
				$('#kav').prop('disabled',true);
			} else if (optav == 6) {
				if (optar == 1) {
					$('#optar').val(0);
					optar = 0;
				}
				$('#kar').prop('disabled',true);
			}  else if (optar == 1) {
				if (optav == 6) {
					$('#optav').val(0);
					optav = 0;
				}
				$('#kav').prop('disabled',true);
			}
			nb = dent + optav + optar + nbdent;
			var image = 'images/m'+nb+'.png';
			$('#image').attr('src',image);

			if (nbdent == 10) {
				var nbd = 5;
				var dentmoins = 4;
				prix += 692;
			} else {
				var nbd =3;
				var dentmoins = 2;
				prix += 686.7;
			}
			if (dent == 0) {
				prix += 28 * nbd;
				var prixmoins = 28 * dentmoins;
			} else if (dent == 20) {
				prix += 77.64 * nbd;
				var prixmoins = 77.64 * dentmoins;
			} else {
				if (nbd == 5) {
					prix += 489.5;
					var prixmoins = 194;
				} else {
					prix += 463;
					var prixmoins = 176;
				}
			}
			if (optav == 3){
				prix += 247.83;
				prixmoins += 247.83;
			} else if (optav == 6) {
				prix += 1029.83;
				prixmoins += 1029.83;
			}
			if (optar == 1) {
				prix += 1046;
				prixmoins += 1046;
			} else if (optar == 2) {
				if (nbd == 5){
					prix += 128.44;
				} else {
					prix += 104.125;
				}
			}
			prix *= 100;
			prix = parseInt(prix);
			prix /= 100;
			$('#prix').text(prix+' €');

			var larg = ecart * rang / 100;
			larg = parseInt(larg);
			larg += 2;
			larg /= 10;
			if (type == 'Fixe') {
				var rampe = [3.5,4.2,5,6,6.6];
				var prixrampe = [3677,3731,3783,3844,3881];

			} else {
				var rampe = [4.2,5,6,6.6];
				var prixrampe = [4331,4383,4444,4481];
			}
			for (var i = 0; i < rampe.length; i++) {
				if (larg <= rampe[i]) {
					larg = rampe[i];
					prixtot = prixrampe[i];
					i = rampe.length;
				}
			}
			prixtot += (rang + 1) * prix;
			prixtot -= prixmoins;
			prixtot = parseInt(prixtot);

			$('#largbin').text(larg+' m');
			$('#prixbin').text(prixtot+' €');

		});
	});
</script>