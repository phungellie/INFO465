var readlineSync = require('readline-sync');

// Prompting the user to enter a list of integers
function getInput() {
    const numbers = [];

    while (true) {
        const input = readlineSync.question("Enter an integer (or 'q' to quit): ");

        if (input.toLowerCase() === "q") {
            break;
        }

        if (/^-?\d+$/.test(input)) {
            numbers.push(Number(input));
        }
        
        else {
            console.log("Invalid inout. Enter a valid integer (or enter 'q' to quit.");
        }
    }

    return numbers;
}

// Function to calculate the mean
function calculateMean(array) {
    return array.reduce((sum, num) => sum + num, 0) / array.length;
}

// Function to calculate the median
function calculateMedian(array) {
    const sorted = [...array].sort((a, b) => a - b);
    const mid = Math.floor(sorted.length / 2);

    return sorted.length % 2 === 0
        ? (sorted[mid - 1] + sorted[mid]) / 2
        : sorted[mid];
}

// Main function
function main() {
    const numbers = getInput();

    if (numbers.length === 0) {
        console.log("No valid numbers entered. Exiting.");
        return;
    }

    const mean = calculateMean(numbers);
    const median = calculateMedian(numbers);

    console.log(`You entered: ${numbers.join(", ")}`);
    console.log(`Mean: ${mean}`);
    console.log(`Median: ${median}`);
}

// Run the program
main();