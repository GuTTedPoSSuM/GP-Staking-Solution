<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $email = $_POST['email'];
    $message = $_POST['message'];
    $to = "guttedpossum@gmail.com";
    $subject = "New Message from GPSS Contact Form";
    $headers = "From: " . $email;

    mail($to, $subject, $message, $headers);

    echo "Message sent successfully!";
}
?>
