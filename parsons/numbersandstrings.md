---
layout: default
title: Example 2
---
<div id="Inputting Numbers-sortableTrash" class="sortable-code"></div> 
<div id="Inputting Numbers-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Inputting Numbers-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Inputting Numbers-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num1 = input(&quot;Enter the first number: &quot;)\n" +
    "num2 = input(&quot;Enter the second number: &quot;)\n" +
    "num1 = int(num1)\n" +
    "num2 = int(num2)\n" +
    "answer = num1*num2\n" +
    "print(answer)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Inputting Numbers-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Inputting Numbers-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Inputting Numbers-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
