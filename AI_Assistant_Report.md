## :test_tube: Tasks

Perform **3 challenges** with each AI. You must use the **same prompt** for all three.

### :white_check_mark: Task 1: Explain a Function

**Prompt:**  
> “Explain this JavaScript function in detail. Add comments as needed.”

```js
function mysteryOp(arr) {
  return arr.reduce((acc, val) => acc ^ val, 0);
}
```
Answer:
What it does 
1. It combines all numbers in the array using the XOR (^) operator
2. The final result is a single number
3. Uses .reduce() to loop through array
4. Starts from 0
6. Cancels duplicate numbers
7. Often used to find non-repeating element

Key concept: XOR (^)

XOR compares bits:
Same → 0
Different → 1

Examples:
0 ^ 4 = 4
4 ^ 1 = 5
5 ^ 2 = 7
7 ^ 1 = 6
6 ^ 2 = 4

Important property:
✅ a ^ a = 0
✅ a ^ 0 = a

Step-by-step with comments
function mysteryOp(arr) {
  return arr.reduce((acc, val) => {
    // acc = accumulated value (starts at 0)
    // val = current number from the array

    // XOR the accumulator with current value
    return acc ^ val;

  }, 0); // initial value = 0
}
<br />

### :white_check_mark: Task 2: DOM Manipulation

**Prompt:**  
> “Write a function that changes the text of an HTML element with id `status` when a button is clicked. Use vanilla JavaScript and follow accessibility best practices.”

<Answer:>
HTML
<div id="status" role="status" aria-live="polite">
  Waiting for action...
</div>

<button id="updateBtn" type="button">
  Update Status
</button>

JavaScript
function updateStatus() {
  const statusEl = document.getElementById("status");
  statusEl.textContent = "Status updated successfully!";
}

// attach event listener
document
  .getElementById("updateBtn")
  .addEventListener("click", updateStatus);

Why this is accessible
role="status" + aria-live="polite"
→ Screen readers announce the change automatically
textContent instead of innerHTML
→ Safer (prevents HTML injection)
type="button"
→ Prevents accidental form submission
Event listener (not inline JS)
→ Cleaner and better practice

Why this is accessible
role="status" + aria-live="polite"
→ Screen readers announce the change automatically
textContent instead of innerHTML
→ Safer (prevents HTML injection)
type="button"
→ Prevents accidental form submission
Event listener (not inline JS)
→ Cleaner and better practice

<br />

### :white_check_mark: Task 3: Refactor Obfuscated Code

**Prompt:**  
> “Refactor this function to make it readable and efficient. Add meaningful variable names and comments.”

```js
function r(a){let b=0;for(let i=0;i<a.length;i++){if(a[i]%2===0){b+=a[i]}}return b}
```

<Answer>
function sumEvenNumbers(numbers) {
  let sum = 0;

  // Loop through each number in the array
  for (let i = 0; i < numbers.length; i++) {
    const currentNumber = numbers[i];

    // Check if the number is even
    if (currentNumber % 2 === 0) {
      sum += currentNumber; // Add it to the total
    }
  }

  return sum;
}

What changed
1. a → numbers (what the array actually is)
2. b → sum (what it stores)
3. i is fine (standard loop index)
4. Same logic 
5. Much easier to read 
6. Better variable naming 
7. More maintainable 

<br />

## :bar_chart: AI Evaluation Table

| AI Tool     | Task | Clarity (1–5) | Accuracy (1–5)   | Speed (1–5) | Tone (1–5)  | Notes |
|-------------|------|----------------|-----------------|-------------|-------------|-------|
| ChatGPT     | 1    |      5         |      5          |     5       |    5        |       |
| ChatGPT     | 2    |      5         |      5          |     5       |    5        |       |
| ChatGPT     | 3    |      5         |      5          |     5       |    5        |       |
| Claude      | 1    |      4         |      5          |     5       |    4        |       |
| Claude      | 2    |      4         |      5          |     5       |    4        |       |
| Claude      | 3    |      4         |      5          |     5       |    4        |       |
| Your Pick   |      |                |                 |             |             |       |
| Your Pick   |      |                |                 |             |             |       |
| Your Pick   |      |                |                 |             |             |       |

ChatGPT was clearer by the method it uses to simplify the answers from the prompt and also offering questions to update the answers if the provided one was not sufficient enough.

Claude was also good, sometimes the answer were similar to ChatGPT. Claude uses a method that provides more content but less examples unlike Chatgpt
# AI Assistant Trials – Final Report

## :trophy: My Pick:
ChatGPT

## :white_check_mark: Pros & Cons

### ChatGPT
- :white_check_mark: [simple and faster to comprehend]
- :x: [no limitations recorded]

### Claude
- :white_check_mark:[more content but less examples to comprehend the content]
- :x:[less examples]

### [Your Pick]
- :white_check_mark:
- :x:

## :pushpin: Task-by-Task Highlights
- Task 1: swift in performance
- Task 2: swift in perfomanc
- Task 3: ...

## :mag: Surprises & Bugs
- There were no bugs, no hallucinations

## Final Thoughts
Which AI would you trust in a real project? Why?
chatGPT because it was quick for me to understand the contents

<br />

##  Reflection Prompts

Write in your journal or digital notebook:

- Which AI helped *you* learn better? 
ChatGPT helped me learn better
- Was there a big difference in explanation quality? 
The quality of explanation in Claude was more but i had to read it twice to comprehend
- Which one matched your communication style? 
ChatGPT matched my communication style
- How might you use different AIs for different types of work? 
When i need more content structure i would use Claude but when i need to make contents easier to comprehend i would use chatGPT