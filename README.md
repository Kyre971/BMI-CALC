# BMI-CALC
<script type='text/javascript'> <!--
function oblicz bmi() {
   var bmi;
   var weight = document.bmiform.gewicht.value;
   var height = document.bmiform.groesse.value;
   if (weight < 10 || weight > 200) { alert("Podana zla waga, prosze podac ponownie"); return null; }
   if (height < 50 || height > 250) { alert("Podany zly wzrost, prosze podac powonie"); return null; }
   bmi = Math.round(weight / (Math.pow((height/100),2)));
   output = "BMI WYNOSI " + bmi + ".\n";
   if (bmi < 18) output += "wysoka nadwaga.";
   if (bmi == 18) output += "niedowaga.";
   if (bmi == 19) output += "lekka nadwaga.";
   if (bmi >= 20 && bmi <= 24) output += "idealnie w normie.";
   if (bmi >= 25 && bmi <= 29) output += "lekka nadwaga.";
   if (bmi >= 30 && bmi <= 39) output += "wysoka nadwaga.";
   if (bmi >= 40) output += "bardzo wysoka nadwaga.";
   alert(output);
}
//-->
</script>
<form name="bmiform">
<input type="text" name="wzrost" />
wzrost w cm<br />
<input type="text" name="waga" />
Waga w kg<br />
<input type="button" name="submit" value="oblicz" onclick="oblicz();">
<br />
