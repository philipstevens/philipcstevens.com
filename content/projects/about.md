---
title: "Pet Predictor"
date: 2019-09-27T11:11:15+07:00
draft: false
---

<style>
form {
    margin: auto;
    width: 100%;
}

.result {
    margin: auto;
    width: 100%;
    border: 1px solid #ccc;
}
</style>

<!-- <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

<script>
    $("form#form").submit(function(){
        var formData = new FormData(this);
        $.post($(this).attr("action"), formData, function() {
                // success    
        });
        return false;
    });
</script>

<form id='form' action='http://localhost:3000/classify' method='POST' name="upload-image" enctype="multipart/form-data">
    Select image to upload:
    <input type="file" name="image" onchange="document.getElementById('image').src = window.URL.createObjectURL(this.files[0])" required>
    <br><br>
    <img id="image" src="#" width="500" height="500" align="center">
    <br><br>
    <input id="sub" type="submit" value="Upload Image">
</form> -->

<form id='form' action='http://localhost:3000/classify' method='POST' enctype="multipart/form-data">
    Select image to upload:
    <input type="file" name="image" required>
    <input id="sub" type="submit" value="Upload Image">
</form>


<br>

<div class="result" align="center">
    Predicted breed:
    <p id='pred' style="font-size:50px">Prediction</p>
</div>

<!-- <script >
    document.forms['form'].addEventListener('submit', (event) => {
        event.preventDefault();
        document.getElementById('pred').innerHTML = type(event['image'])
        fetch(event.target.action, {
            method: 'POST',
            body: new URLSearchParams(new FormData(event.target)) // event.target is the form
        }).then((resp) => {
            return resp.json(); // or resp.text() or whatever the server sends
        }).then((body) => {
            body.getElementById('pred').innerHTML = 'Worked!';
        }).catch((error) => {
           // document.getElementById('pred').innerHTML = 'Didn't work :(';
        });
    });
</script> -->
