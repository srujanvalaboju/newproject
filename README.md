<?php
include "script.php";
?>
<!DOCTYPE html>
<html>
    <head>
        <title>ApiCrud</title>
        <link rel = "stylesheet" type = "text/css" href = "<?php echo base_url(); ?>css/style.css"> 
    </head>
    <br>
    <br>
    <div class="container">
        <form method="post" id="formRegister" class="form-horizontal" enctype="multipart/form-data" role="form">
            <h3><span class="label label-default" style="margin-left: 180px;">Change Password</span></h3><br>
            <div class="form-group">
                <label for="Password" class="col-sm-4 control-label">Old Password*</label>
                <div class="col-sm-6">
                    <input type="Password" name="OldPassword" id="OldPassword" placeholder="Enter Old Password" class="form-control">
                    <span style="color:red; display:none" id="inline_OldPassword">Enter Old Password.</span>
                    <span style="color:red; display:none" id="inline_OldPasswordFormat"> Password Does not match with your old password. </span>
                    <span style="color:red; display:none" id="inline_OldPasswordMatch"> matched. </span>
                </div>
            </div>

            <div class="form-group">
                <label for="Password" class="col-sm-4 control-label">New Password*</label>
                <div class="col-sm-6">
                    <input type="Password" name="NewPassword" id="NewPassword" placeholder="Enter New Password" class="form-control">
                    <span style="color:red; display:none" id="inline_NewPassword"> Please enter Password. </span>
                    <span style="color:red; display:none" id="inline_NewPasswordMatch"> Password Must contain number and uppercase and lowercase letter and special char, Max 8 len. </span>
                    <span style="color:red; display:none" id="inline_NewPasswordDone"> Password Changed. </span>
                </div>
            </div>

            <div class="form-group">
                <label for="Password" class="col-sm-4 control-label">Confirm Password*</label>
                <div class="col-sm-6">
                    <input type="Password" name="ConfirmPassword" id="ConfirmPassword" placeholder="Confirm Password" class="form-control">
                    <span style="color:red; display:none" id="inline_ConfirmPassword"> Please enter conform password </span><br>
                    <span style="color:red; display:none" id="inline_ConfirmPasswordMatch"> Password doesn't match..! </span><br>
                </div>
            </div>
            <div class="form-group">
                <button type="button" id="register" onclick="ValidateForm()" class="btn btn-danger" style="margin-left: 200px;">Reset</button>
                <a href="<?php echo base_url().'Apis/home/userdetailes';?>" class="btn btn-info">Back</a>
            </div>
        </form>
    </div>
    <div id="wait" style="display:none" class='pointer'></div>
    <div id="img" style="display:none;width:45px;height:45px;position:absolute;top:50%;left:50%;">
    <img src="<?php echo base_url().'imguploads/demo_wait.gif';?>" width="32" height="32" />
    </div>
</html>


