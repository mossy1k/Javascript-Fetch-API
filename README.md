<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Fetch Api Example</title>
</head>
<body>
<!--
This simple project is the display of new feature of javascript. Instead of using third party http server request like old ajax xmlHttpRequest, jQuery.Ajax or axios, we make use of http request in-built with javascript without the need to use any third party library. This is pretty cool..:) 
-->

    <h1>Using Javascript Fetch API:</h1>

    <!-- Down here we create a button that by clicking it, it triggers or invoke or call fetchUserData() function which fetch our user details from remote api with the url of dummy/API testing server [https://jsonplaceholder.typicode.com]-->

    <button id="fetchUserDetailsBtn">Fetch User Data</button>

    <!-- Down here, the result from the API call displays-->

    <div id="response"></div>
   

    <script>
        /* Comment::) Down here, the button is listening and patiently waiting for user to click it  in other to call the callback function of [fetchUserData()]*/

        document.getElementById('fetchUserDetailsBtn').addEventListener('click',fetchUserData)

        /* Comment::)  Down here, this is the main FETCH API code which asynchroniously fetches user data from the remote url*/

        function fetchUserData() {

        /* Comment::)  The logic is very simple. fetch method is a new javascript PROMISED-BASED function.i.e It promises us that if the API endpoint is correct and everything went well without any error, then give us the response from the remote API*/

            fetch('https://jsonplaceholder.typicode.com/user/1')

        /* Comment::)  Down here is the response received in json format(object) so that we can display it after a successful fetch*/

                .then(response => response.json())

        /* Comment::) Finally, run this script/page in a browser and press ctrl + Shift I to see the response/result in the console. 
        Here we go... We now know how to successfully use in-built javascript http server method (fetch API) to get data from the server without making use of any external library. Thanks:))
        */
                .then(json => console.log(json))
        }
    </script> 
</body>
</html>
