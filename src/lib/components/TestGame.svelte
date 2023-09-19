<script>
    let random = 0;
    let tries = 5;
    let highestNumber = 0;
    let highestTries = 0;
    let win = "";
    let stopped = false;
    let buttonText = "Play"

    function Reset() {
        random = 0;
        tries = 5;
        highestNumber = 0;
        highestTries = 0;
        win = "";
        stopped = false;
        buttonText = "Play!"
    }

    function ChangeTries() {
        console.log("Clicked!");
        if (stopped) {
            Reset();
        }
        else if (tries > 0) {
            --tries;
            random = GetRandomNumber();
            HighestNumber();
            win = "Current Highest is " + highestNumber + " on try " + highestTries;
        }
        else {
            StopGame();
        }
    }

    function StopGame() {

        if (stopped) {
            Reset();
        }

        buttonText = "Reset"

        let tempHighest = 0;
        let tempIndex = 0;
        for (let i = tries; i >= 0; i--) {
            let temp = GetRandomNumber();

            if (tempHighest < temp) {
                tempHighest = temp;
                tempIndex = 5 - i;
            }
        }

        if (random > highestNumber) {
            win = "You Lose " + tempHighest + " was bigger than ${}on try " + tempIndex 
        }
        else if (tempHighest > highestNumber) {
            win = "You Lose " + tempHighest + " was bigger on try " + tempIndex 
        }
        else{
            win = "You Win! " + highestNumber + " was the biggest number on try " + highestTries + "!"
        }

        stopped = true;
    }

    function GetRandomNumber() {
        return Math.floor(Math.random() * 1000);
    }

    function HighestNumber(){
        if (highestNumber < random){
            highestNumber = random;
            highestTries = 5 - tries;
        }
    }
</script>

<style>
    .center {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    .button {
        margin: 10px;
    }
</style>

<h1>{ random }</h1>

<div class= "center">
    <button class="button" on:click={ChangeTries}>
	    { buttonText }
    </button>
    <button class="button" on:click={StopGame}>
	    Stop!
    </button>
    <p>{ tries } tries left!</p>
    <p>{ win }</p>
</div>