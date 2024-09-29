<?php
echo " one";
$servername = "database-1.cx0iyacc8tzg.ap-south-1.rds.amazonaws.com";
// Add a rds end point 
$username = "root";
$password = "pass1234";
$dbname = "facebook";
 
// Create connection
$conn = mysqli_connect($servername, $username, $password, $dbname);
// Check connection
if (!$conn) {
  die("Connection failed: " . mysqli_connect_error());
}
$sql = "INSERT INTO users (name)VALUES('ravi')";
if (mysqli_query($conn, $sql)) {
  echo "New record created successfully";
} else {
  echo "Error: " . $sql . "<br>" . mysqli_error($conn);
}
mysqli_close($conn);
?>
