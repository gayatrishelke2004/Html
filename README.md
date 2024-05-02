1...
<html>
<head>
<title>MARKS SHEET USING HTML 
TABLES</title> <meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initialscale=1"> <meta name="Keywords" content="html, css, html tables, 
table"> <meta name="Description" content="html table"> <!-- add icon 
-->
<link rel="icon" href="/favicon.ico" type="image/x-icon">
<link href='http://fonts.googleapis.com/css?family=Lato:400,700' rel='stylesheet' 
type='text/css'>
<style>
td, th,table{
border: 2px dotted #000;
}
</style>
</head>
<body>
<div class="container">
<h2>HTML TABLE</h2>
<table>
<thead>
<tr>
<th>Roll No.</th>
<th>Name</th>
<th>English</th>
<th>Maths</th>
<th>Science</th>
<th>Computer Science</th>
<th>Social Studies</th>
<th>Total</th>
<th>Max Marks</th>
<th>Grade </th>
<tr>
</thead>
<tbody>
<tr>
<td>01</td>
<td>Bhasker</td>
<td>86</td>
<td>77</td>
<td>87</td>
<td>92</td>
<td>95</td>
<td>437</td>
<td>500</td>
<td>A</td>
</tr>
<tr>
<td>02</td>
<td>Balwant</td>
<td>86</td>
<td>77</td>
<td>87</td>
<td>92</td>
<td>95</td>
<td>437</td>
<td>500</td>
<td>A</td>
</tr>
<tr>
<td>03</td>
<td>Kailash</td>
<td>86</td>
<td>77</td>
<td>87</td>
<td>92</td>
<td>95</td>
<td>437</td>
<td>500</td>
<td>A</td>
</tr>
<tr>
<td>04</td>
<td>Nikhil</td>
<td>86</td>
<td>77</td>
<td>87</td>
<td>92</td>
<td>95</td>
<td>437</td>
<td>500</td>
<td>A</td>
</tr>
<tr>
<td>05</td>
<td>Shubham</td>
<td>86</td>
<td>77</td>
<td>87</td>
<td>92</td>
<td>95</td>
<td>437</td>
<td>500</td>
<td>A</td>
</tr>
</tbody>
</table>
</div>
</body>
</html>







2...

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calendar</title>
<style>
body {
font-family: Arial, sans-serif;
text-align: center;
}
#calendar {
margin: 20px auto;
border-collapse: collapse;
}
#calendar th, #calendar td {
padding: 10px;
border: 1px solid #ccc;
}
#calendar th {
background-color: #f2f2f2;
}
#month, #year {
margin-bottom: 10px;
}
#changeColorBtn {
margin-top: 20px;
}
</style>
</head>
<body>
<h1>Calendar</h1>
<div>
<label for="month">Month:</label>
<select id="month">
<option value="0">January</option>
<option value="1">February</option>
<option value="2">March</option>
<option value="3">April</option>
<option value="4">May</option>
<option value="5">June</option>
<option value="6">July</option>
<option value="7">August</option>
<option value="8">September</option>
<option value="9">October</option>
<option value="10">November</option>
<option value="11">December</option>
</select>
<label for="year">Year:</label>
<input type="number" id="year" min="1900" max="2100" value="2024"> 
<button onclick="generateCalendar()">Generate Calendar</button>
</div>
<table id="calendar">
<thead>
<tr>
<th>Sun</th>
<th>Mon</th>
<th>Tue</th>
<th>Wed</th>
<th>Thu</th>
<th>Fri</th>
<th>Sat</th>
</tr>
</thead>
<tbody id="calendar-body">
</tbody>
</table>
<button id="changeColorBtn" onclick="changeBackgroundColor()">Change Background 
Color</button>
<script>
function generateCalendar() {
const monthSelect = document.getElementById('month'); 
const yearInput = document.getElementById('year'); const 
month = parseInt(monthSelect.value); const year = 
parseInt(yearInput.value);
const calendarBody = document.getElementById('calendar-body'); 
calendarBody.innerHTML = '';
const firstDay = new Date(year, month, 1);
const lastDay = new Date(year, month + 1, 0);
const totalDays = lastDay.getDate();
let date = 1;
let nextDate = 1;
let row = calendarBody.insertRow();
for (let i = 0; i < 6; i++) {
for (let j = 0; j < 7; j++) {
const cell = row.insertCell();
if ((i === 0 && j < firstDay.getDay()) || date > totalDays) {
cell.textContent = nextDate;
cell.classList.add('empty');
nextDate++;
} else {
cell.textContent = date;
date++;
}
if (date > totalDays) break;
}
if (date > totalDays) break;
row = calendarBody.insertRow();
}
}
function changeBackgroundColor() {
const newColor = prompt("Enter a color (e.g., red, #00ff00, rgb(255, 0, 
0)):"); if (newColor) {
document.body.style.backgroundColor = newColor;
}
}
</script>
</body>
</html>








3.....

<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Form Validation</title>
 <style>
 body {
 font-family: Arial, sans-serif;
 background-color: #f4f4f4;
 margin: 0;
 padding: 0;
 }
 h2 {
 text-align: center;
 margin-top: 30px;
 }
 form {
 max-width: 400px;
 margin: 0 auto;
 background-color: #fff;
 padding: 20px;
 border-radius: 8px;
 box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
 }
 label {
 display: block;
 margin-bottom: 5px;
 }
 input[type="text"],
 input[type="password"],
 input[type="email"] {
 width: 100%;
 padding: 10px;
 margin-bottom: 15px;
 border: 1px solid #ccc;
 border-radius: 4px;
 box-sizing: border-box;
 font-size: 16px;
 }
 input[type="submit"] {
 background-color: #4CAF50;
 color: #fff;
 padding: 10px 20px;
 border: none;
 border-radius: 4px;
 cursor: pointer;
 font-size: 16px;
 transition: background-color 0.3s ease;
 }
 input[type="submit"]:hover {
 background-color: #45A049;
 }
 .error-message {
 color: red;
 margin-top: 5px;
 }
 </style>
 <script>
 function validateRegistration() {
 var username = document.getElementById("regUsername").value;
 var password = document.getElementById("regPassword").value;
 var confirmPassword = document.getElementById("regConfirmPassword").value;
 var email = document.getElementById("regEmail").value;
 if (username === "" || password === "" || confirmPassword === "" || email === "") {
 alert("Please fill out all fields.");
 return false;
 }
 if (password !== confirmPassword) {
 alert("Passwords do not match.");
 return false;
 }
 if (password.length < 8) {
 alert("Password must be at least 8 characters long.");
 return false;
 }
 // Regular expression to validate email format
 var emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
 if (!emailPattern.test(email)) {
 alert("Please enter a valid email address.");
 return false;
 }
 // Registration successful
 alert("Registration successful!");
 return true;
 }
 
 function validateLogin() {
 var username = document.getElementById("loginUsername").value;
 var password = document.getElementById("loginPassword").value;
 if (username === "" || password === "") {
 alert("Please fill out all fields.");
 return false;
 }
 // Login successful
 alert("Login successful!");
 return true;
 }
 function validateProfile() {
 var fullName = document.getElementById("fullName").value;
 var address = document.getElementById("address").value;
 var phone = document.getElementById("phone").value;
 if (fullName === "" || address === "" || phone === "") {
 alert("Please fill out all fields.");
 return false;
 }
 // Regular expression to validate phone number format (10 digits)
 var phonePattern = /^\d{10}$/;
 if (!phonePattern.test(phone)) {
 alert("Please enter a valid 10-digit phone number.");
 return false;
 }
 // Profile update successful
 alert("Profile update successful!");
 return true;
 }
 function validatePayment() {
 var cardNumber = document.getElementById("cardNumber").value;
 var expiryDate = document.getElementById("expiryDate").value;
 var cvv = document.getElementById("cvv").value;
 if (cardNumber === "" || expiryDate === "" || cvv === "") {
 alert("Please fill out all fields.");
 return false;
 }
 // Regular expression to validate credit card number format (16 digits)
 var cardNumberPattern = /^\d{16}$/;
 if (!cardNumberPattern.test(cardNumber)) {
 alert("Please enter a valid 16-digit credit card number.");
 return false;
 }
 // Payment successful
 alert("Payment successful!");
 return true;
 }
 </script>
</head>
<body>
<h2>Registration</h2>
<form onsubmit="return validateRegistration()">
 <label for="regUsername">Username:</label>
 <input type="text" id="regUsername" name="regUsername" required><br>
 <label for="regPassword">Password:</label>
 <input type="password" id="regPassword" name="regPassword" required 
minlength="8"><br>
 <label for="regConfirmPassword">Confirm Password:</label>
 <input type="password" id="regConfirmPassword" name="regConfirmPassword" 
required><br>
 <label for="regEmail">Email:</label>
 <input type="email" id="regEmail" name="regEmail" required><br>
 <input type="submit" value="Register">
</form>
<h2>Login</h2>
<form onsubmit="return validateLogin()">
 <label for="loginUsername">Username:</label>
 <input type="text" id="loginUsername" name="loginUsername" required><br>
 <label for="loginPassword">Password:</label>
 <input type="password" id="loginPassword" name="loginPassword" required><br>
 <input type="submit" value="Login">
</form>
<h2>User Profile</h2>
<form onsubmit="return validateProfile()">
 <label for="fullName">Full Name:</label>
 <input type="text" id="fullName" name="fullName" required><br>
 <label for="address">Address:</label>
 <input type="text" id="address" name="address" required><br>
 <label for="phone">Phone:</label>
 <input type="text" id="phone" name="phone" required><br>
 <input type="submit" value="Update Profile">
</form>
<h2>Payment</h2>
<form onsubmit="return validatePayment()">
 <label for="cardNumber">Credit Card Number:</label>
 <input type="text" id="cardNumber" name="cardNumber" required><br>
 <label for="expiryDate">Expiry Date:</label>
 <input type="text" id="expiryDate" name="expiryDate" required><br>
 <label for="cvv">CVV:</label>
 <input type="text" id="cvv" name="cvv" required><br>
 <input type="submit" value="Make Payment">
</form>
</body>
</html







4....

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Star Pattern</title>
</head>
<body>
    <script>
        const numRows = 5;

        for (let i = 1; i <= numRows; i++) {
            let pattern = '';

            for (let j = 1; j <= i; j++) {
                pattern += '* ';
            }

            document.write(pattern + "<br>");
        }
    </script>
</body>
</html>



5...

Index.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CRUD Operations</title>
<script>
function showAlert(message) {
alert(message);
}
</script>
</head>
<body>
<h2>CRUD Operations</h2>
<!-- Insert Form -->
<form action="insert.php" method="post"> 
<h3>Insert Record</h3>
<!-- <label for="name">id:</label>
<input type="text" id="id_insert" name="id" required><br> --> 
<label for="name">Name:</label>
<input type="text" id="name" name="name" required><br> 
<label for="email">Email:</label>
<input type="email" id="email" name="email" required><br>
<button type="submit" onclick="showAlert('Record inserted 
successfully')">Insert</button>
</form>
<!-- Update Form -->
<form action="update.php" method="post"> 
<h3>Update Record</h3>
<label for="id_update">ID:</label>
<input type="number" id="id_update" name="id" required><br> 
<label for="name_update">Name:</label>
<input type="text" id="name_update" name="name" required><br> 
<label for="email_update">Email:</label>
<input type="email" id="email_update" name="email" required><br>
<button type="submit" onclick="showAlert('Record updated 
successfully')">Update</button>
</form>
<!-- Delete Form -->
<form action="delete.php" method="post"> 
<h3>Delete Record</h3>
<label for="id_delete">ID:</label>
<input type="number" id="id_delete" name="id" required><br>
<button type="submit" onclick="showAlert('Record deleted 
successfully')">Delete</button>
</form>
<!-- Display Records -->
<h3>Display Records</h3>
<a href="display.php">Display Records</a>
</body>
</html>
<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "sonoo";
// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);
// Check connection
if ($conn->connect_error) {
die("Connection failed: " . $conn->connect_error);
}
?>
<?php
include 'db_config.php';
$name = $_POST['name'];
$email = $_POST['email'];
$sql = "INSERT INTO emp (name, email) VALUES ('$name', '$email')";
if ($conn->query($sql) === TRUE) {
echo "Record inserted successfully";
} else {
echo "Error: " . $sql . "<br>" . $conn->error;
}
$conn->close();
?>
<?php
include 'db_config.php';
$id = $_POST['id'];
$name = $_POST['name'];
$email = $_POST['email'];
$sql = "UPDATE emp SET name='$name', email='$email' WHERE id=$id";
if ($conn->query($sql) === TRUE) {
echo "Record updated successfully";
} else {
echo "Error: " . $sql . "<br>" . $conn->error;
}
$conn->close();
?>
<?php
include 'db_config.php';
$id = $_POST['id'];
$sql = "DELETE FROM emp WHERE id=$id";
if ($conn->query($sql) === TRUE) {
echo "Record deleted successfully";
} else {
echo "Error: " . $sql . "<br>" . $conn->error;
}
$conn->close();
?>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Employee Information</title>
<style>
body {
font-family: Arial, sans-serif;
background-color: #f0f0f0;
}
.container {
max-width: 800px;
margin: 20px auto;
padding: 20px;
background-color: #fff;
border-radius: 8px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
table {
width: 100%;
border-collapse: collapse;
border: 1px solid #ddd;
border-radius: 8px;
overflow: hidden;
}
th, td {
padding: 12px;
text-align: left;
border-bottom: 1px solid #ddd;
}
th {
background-color: #f2f2f2;
}
tr:hover {
background-color: #f5f5f5;
}
.btn {
background-color: #4CAF50;
color: white;
padding: 10px 20px;
border: none;
border-radius: 4px;
cursor: pointer;
text-decoration: none;
display: inline-block;
transition: background-color 0.3s;
}
.btn:hover {
background-color: #45a049;
}
</style>
</head>
<body>
<div class="container">
<?php
include 'db_config.php';
$sql = "SELECT * FROM emp";
$result = $conn->query($sql);
if ($result->num_rows > 0) {
echo "<table><tr><th>ID</th><th>Name</th><th>Email</th></tr>"; 
while($row = $result->fetch_assoc()) {
echo
"<tr><td>".$row["id"]."</td><td>".$row["name"]."</td><td>".$row["email"]."</td>
</tr>";
}
echo "</table>";
} else {
echo "0 results";
}
$conn->close();
?>
</div>
</body>
</html>




6....
