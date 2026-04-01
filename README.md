<?php
$conn = pg_connect("host=localhost dbname=test user=postgres password=yourpassword");

$query = "SELECT * FROM employee WHERE salary > 50000";

$res = pg_query($conn, $query);

while($row = pg_fetch_assoc($res))
{
  echo $row['emp_no']." ".$row['emp_name']." ".$row['salary']."<br>";
}
?>
