# XHR-POST-Requests-II
We are going to reconstruct the code from the previous exercise step-by-step until we have written a complete AJAX POST request.  Feel free to refer to the XHR POST diagram at any point while completing this exercise:  XHR POST diagram


### QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ

1.
Create a new XMLHttpRequest object using the new operator, and save it in a const called xhr.

The XMLHttpRequest object is used in JavaScript to interact with servers.

Checkpoint 2 Passed

Hint
The syntax will look like:

const nameOfVariable ='a string of sorts'
2.
Next, save the following URL to a const called url. Make sure the URL is wrapped in quotes so that it is a string.

https://api-to-call.com/endpoint
The URL will direct the request to the correct server.

Checkpoint 3 Passed
3.
Create a new const called data, and save this line of code to it:

JSON.stringify({id: '200'});
JSON.stringify() will convert a value to a JSON string. By converting the value to a string, we can then send the data to a server.

Checkpoint 4 Passed
4.
Set the responseType property of the xhr object to be 'json'.

Checkpoint 5 Passed

Hint
To access the responseType property, use dot notation like so: xhr.responseType. Then to assign it to 'json' you can use the following syntax:

xhr.responseType = 'json'
5.
Set the xhr.onreadystatechange event handler equal to an anonymous arrow function. Leave the function empty until the next step.

.onreadystatechange will contain the event handler that will be called when xhr‘s state changes.

Checkpoint 6 Passed

Hint
To assign xhr.onreadystatechange to an anonymous function, use the following syntax:

xhr.onreadystatechange = () => {}
6.
In the code block of the function you created in the previous step, add a conditional statement that checks to see if the readyState of xhr is equal to XMLHttpRequest.DONE.

Checkpoint 7 Passed

Hint
Make sure you’re inside the code block of the anonymous arrow function.

The if conditional will check to see if the request has finished.

To access the readyState of the xhr object, use dot notation like so: xhr.readyState.

When comparing two objects use ===.

The syntax will look like:

if(xhr.readyState === XMLHttpRequest.DONE){
 
}
7.
In the code block of the conditional statement, return the response property of xhr. The response property will contain the data that we’re getting back from the POST request.

Checkpoint 8 Passed

Hint
To access the response property, we can use dot notation like so: xhr.response.

8.
Below the function you created in the previous two steps, call the .open() method on the xhr object and pass it 'POST' and url as arguments.

.open() creates a new request and the arguments passed in determine what type of request is being made and where it’s being made to.

Checkpoint 9 Passed

Hint
The syntax will look like:

xhr.open('POST', url)
9.
On the following line, call the .send() method on the xhr object and pass data as an argument.

.send() will send the request to the server.

Nice work! You’ve written the boilerplate code for an AJAX POST request using an XMLHttpRequest object.

Checkpoint 10 Passed

Hint
The syntax will look like:

xhr.send(data)
