
//Task1:Always Hungry
function alwaysHungry(arr) {
    // your code here 
    for(var i = 0; i < arr.length; i++){
        if(arr[i] == "food"){
            arr[i] = "yummy";
            console.log(arr[i]);
        } else {
            console.log("I'm Hungry");
        }
    }
}
alwaysHungry([3.14, "food", "pie", true, "food"]);
// this should console log "yummy", "yummy"
alwaysHungry([4, 1, 5, 7, 2]);
// this should console log "I'm hungry"


//Task2: High Pass Filter
function highPass(arr, cutoff) {
    var filteredArr = [];
    // your code here
    for(var i = 0; i < arr.length; i++){
        if(arr[i] > cutoff){
            filteredArr.push(arr[i]);
        }
    }
    return filteredArr;
}
var result = highPass([6, 8, 3, 10, -2, 5, 9], 5);
console.log(result); // we expect back [6, 8, 10, 9]


//Task3: Better Than Average
function betterThanAverage(arr) {
    var sum = 0;
    // calculate the average
    for(var i = 0; i < arr.length; i++){
        sum =(sum + arr[i]);
    }
    var avg = sum / arr.length;
    var count = 0
    // count how many values are greated than the average
    for(var i = 0; i < arr.length; i++){
        if(arr[i] > avg){
            count++;
        }
    }
    return count;
}
var result = betterThanAverage([6, 8, 3, 10, -2, 5, 9]);
console.log(result); // we expect back 4

//Task4: Array Reverse
function reverse(arr) {
    // your code here
    arr.reverse();
    return arr;
}

var result = reverse(["a", "b", "c", "d", "e"]);
console.log(result); // we expect back ["e", "d", "c", "b", "a"]

//Task5: Fibonacci Array

function fibonacciArray(n) {
    // the [0, 1] are the starting values of the array to calculate the rest from
    var fibArr = [0, 1];
    // your code here
    fibArr[0] = 0;
    fibArr[1] = 1;
    sum = [];
    sum.push(fibArr[0]);
    sum.push(fibArr[1]);
    for(var i = 2; i < n; i++){
        sum[i] = fibArr[0] + fibArr[1];
        fibArr[0] = fibArr[1];
        fibArr[1] = sum[i];
    }
    return sum;
}
var result = fibonacciArray(10);
console.log(result); // we expect back [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
