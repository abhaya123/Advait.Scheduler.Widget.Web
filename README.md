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
   <div id='btnAppointment'> </div>
   ```
3. Then add the below code after ending of the </body> tag.
```
<div id='modernScheduler'>
</div>
<script>
    var asButton = "<button class=\"btn btn-primary\" data-toggle=\"modal\" data-target=\"#asModernScheduler\">Schedule an Appointment<\/button>";
    
    var asModal = "<div class=\"modal fade\" id=\"asModernScheduler\" tabindex=\"-1\" role=\"dialog\" aria-labelledby=\"myModalLabel\" aria-hidden=\"true\">";
    asModal += "<div class=\"modal-dialog\" style=\"width:650px !important;\">";
    asModal += "<div class=\"modal-content\">";
    asModal += "<div class=\"modal-header\">";
    asModal += "<button type=\"button\" class=\"close\" data-dismiss=\"modal\" aria-hidden=\"true\">&times;<\/button>";
    asModal += "<h4 class=\"modal-title\" id=\"myModalLabel\">Schedule an Appointment<\/h4>";
    asModal += "<\/div>";
    asModal += "<div class=\"modal-body\">";
    asModal += "<iframe src=\"http:\/\/doctorscheduler.abhayatech.co.in\/Home\/Index\/def37861\" width=\"600\" height=\"600\" frameborder=\"0\" allowtransparency=\"true\"><\/iframe>";
    asModal += "<\/div>";
    asModal += "<\/div>";

    var buttonLink = document.getElementById('btnAppointment');
    buttonLink.innerHTML = asButton;

    var modalLink = document.getElementById('modernScheduler');
    modalLink.innerHTML = asModal;
</script>

```
That's All your widget is ready to use.
