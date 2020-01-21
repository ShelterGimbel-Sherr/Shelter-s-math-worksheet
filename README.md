<h1>Shelter's math Worksheet</h1>
<p>Do these fast and correctly</p>
<ul>
  const sad = document.getElementById("sad");
setInterval(onTimer, 1000);
function onTimer() {
  let theTimer = Number($("#theTimer").text());
  theTimer = theTimer + 1;
  $("#theTimer").text(theTimer);
}
  $("input").change(onChange);

function onChange(evt) {
  let correct = $(this).data("correct");
  let response = $(this).val();
  if (correct == response) {
    let score = Number($("#score").text());
    score = score + 1;
    $("#score").text(score);
    $(this)
      .removeClass("incorrect")
      .addClass("correct");
  } else {
    $(this)
      .removeClass("correct")
      .addClass("incorrect");
    if (Math.random() > .9) {
      sad.play();
    }
  }
}
  <li>5 + 5 = <input data-correct="10"/></li>
  <li>2 + 4.5 = <input data-correct="6.5"/></li>
  <li>2<sup>3</sup><input data-correct="8"/></li>
  <li>4<sup>0</sup><input data-correct="1"/></li> 
  <li>150 + 2478 = <input data-correct="2628"/></li>
  <li>17 + 12 = <input data-correct="29"/></li>
  <li>2 + 55249 = <input data-correct="55251"/></li>
  <li>15<sup>3</sup><input data-correct="3375"/></li>
  <li>7<sup>2</sup><input data-correct="49"/></li>
  <li>1804<sup>1</sup><input data-correct="1804"/></li> 
   
<ul>
.correct{
  background:green;
}

.incorrect{
  background:red;
}
