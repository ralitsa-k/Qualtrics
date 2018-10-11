# Qualtrics

Qualtrics
Delay radiobuttons in qualtrics.

#the following delays the display of all Choices/radiobuttons (QID + "-" + i + "-label") of a selected Question (QID) for 2 seconds

Qualtrics.SurveyEngine.addOnload(function() { var QID = this.questionId; console.log(QID); for (var i = 1; i < 4; i++) { document.getElementById( QID + "-" + i + "-label" ).style.display="none"; }

(function(delay_container){ for (var i = 1 ; i < 4 ; i ++){ document.getElementById(QID + "-" + i + "-label").style.display="block"; } }).delay(2,this.questionContainer); });

#The following delays a question (either text or question + choices)

Qualtrics.SurveyEngine.addOnload(function() { var QID = this.questionId; console.log(QID); for (var i = 1; i < 4; i++) { document.getElementById( QID).style.display="none"; }

(function(delay_container){ for (var i = 1 ; i < 4 ; i ++){ document.getElementById(QID).style.display="block"; } }).delay(2,this.questionContainer);

});

#Delay a question show for some time and then hide it again (leave blank page until NEXT button is pressed).

Qualtrics.SurveyEngine.addOnload(function() { var QID = this.questionId; console.log(QID); for (var i = 1; i < 4; i++) { document.getElementById( QID).style.display="none"; }

(function(delay_container){ for (var i = 1 ; i < 4 ; i ++){ document.getElementById(QID).style.display="block"; } }).delay(3,this.questionContainer);

(function(delay_container) 
{
	for (var i = 1 ; i < 4 ; i ++){
		document.getElementById(QID).style.display="none";
		 }
}).delay(8,this.questionContainer);

});
