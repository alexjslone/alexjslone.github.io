<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Expense Tracker</title>
</head>
<body>
    

<form>
<label for="Expense"><strong>Expense:</strong></label>
<input type= "number" id="Expense"><br>
<br><button onclick="myFunction()" type="button">Submit</button>
</form>

<br><label for="TotalBudget"><strong>What is your total budget?</strong>:</label>
<input type= "number" id="TotalBudget"><br>
<br><button onclick= "budgetFunction()" type="button">Submit</button>
</form>

<style>
    body {background-color: gray;text-align: center; color: floralwhite; }

</style>
<h2 id="TotalExpenses"></h2><br>
<h2 id="MoneyLeft"></h2>


<script>
    var totalExpenses = 0;
    var totalBudget = 0
    function myFunction() {
        let expense= document.querySelector("#Expense");
        totalExpenses = totalExpenses + Number(expense.value);
        document.getElementById("TotalExpenses").innerHTML= "Your total expenses are " + totalExpenses + "$";
        if (totalBudget!=0) {
            totalBudget = totalBudget - totalExpenses; 
            document.getElementById("MoneyLeft").innerHTML = "Your budget is " + totalBudget + "$";
        }
    }
    function budgetFunction() { 
        let currentBudget = document.querySelector("#TotalBudget");
        totalBudget = Number(currentBudget.value) - totalExpenses; 
        document.getElementById("MoneyLeft").innerHTML = "Your budget is " + totalBudget+ "$";

    }

</script>


</body>


</html>
