# paperScissorsRock

  var userInput = ("Rock");
userInput = userInput.toLowerCase();


function getComputerChoice() {
 var x = Math.floor(Math.random() * 3);
  switch (x) { 
  case 0:
    return "rock";
  case 1:
    return "paper";
  case 2:
    return "scissors";
  }
} 

function determineWinner (userChoice, computerChoice) {
  if (userChoice === computerChoice) {
		return "Game is a tie!";
	}
  if (userChoice === "rock") {
		if (computerChoice === "paper") {
			return "The computer win!";
		} else {
			return "You win!";
		}
	}
  if (userChoice === "paper") {
    if (computerChoice === "scissors") {
      return "The computer wins!";
    } else {
      return "You win!";
    }
  }
  if (userChoice === "scissors") {
    if (computerChoice === "rock") {
      return "The computer wins!"
    } else {
      return "You win!";
     }
  }
}
function playGame() {
  var userChoice = userInput;
  var computerChoice = getComputerChoice();
  console.log("You threw: " + userChoice);
  console.log("The computer threw: " + computerChoice);
  console.log(determineWinner(userChoice, computerChoice));
}

playGame();
