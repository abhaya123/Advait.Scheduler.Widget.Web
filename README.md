# Scheduler-Widget
**Steps to add Scheduler Widget**

1. Add the below bootstrap scripts and styles to the page where you want to display the widget (if Required).
```
 <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"> 
 
 <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script> 
 
 <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
 ```
2. Add the below ```<div>``` DOM element where you want to place the button on the page.
   ```
   <div id='advait_appointment'> </div>
   ```
3. Then add the below code after ending of the </body> tag.
```
<div id='appointment_modal'>
</div>
<script>
    var appointmentButton = "<button class=\"btn btn-primary\" onclick=\"openScheduler()\">Schedule an Appointment<\/button>";
    
    var advaitScheduler = "    <div class=\"modal fade\" id=\"myModalScheduler\" tabindex=\"-1\" role=\"dialog\" aria-labelledby=\"myModalLabel\" aria-hidden=\"true\">";
    advaitScheduler += "        <div class=\"modal-dialog\" style=\"width:650px !important;\">";
    advaitScheduler += "            <div class=\"modal-content\">";
    advaitScheduler += "                <div class=\"modal-header\">";
    advaitScheduler += "                    <button type=\"button\" class=\"close\" data-dismiss=\"modal\" aria-hidden=\"true\">&times;<\/button>";
    advaitScheduler += "                    <h4 class=\"modal-title\" id=\"myModalLabel\">Schedule an Appointment<\/h4>";
    advaitScheduler += "                <\/div>";
    advaitScheduler += "                <div class=\"modal-body\">";
    advaitScheduler += "                    <iframe src=\"http:\/\/doctorscheduler.abhayatech.co.in\/Home\/Index\/def37861\" width=\"600\" height=\"600\" frameborder=\"0\" allowtransparency=\"true\"><\/iframe>";
    advaitScheduler += "                <\/div>";
    advaitScheduler += "            <\/div>";

    var link = document.getElementById('advait_appointment');
    link.innerHTML = appointmentButton;

    var link2 = document.getElementById('appointment_modal');
    link2.innerHTML = advaitScheduler;

    function openScheduler() {
        $('#myModalScheduler').modal("show");
    }
</script>

```
That's All your widget is ready to use.
