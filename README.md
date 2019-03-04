# Validate.js
its short and simple 

dependency 
  * bootstrap ^4.3
  * jquery ^3.3.1
  
please reads the short manual 

this only if you want help text
--------------------------------
    $("input[type='tel']").keyup(function(){
      $(this).phoneValidate();
    });
    
if you want a validation of form onsubmit 

in html page
----------------------------------
    <form onsubmit="return validateForm()">
      ... your input fields 
    </form>

onyour script file
----------------------------
    function validateForm(){
      let flag = null;
      // #id - it can be your inupt field id or selector of that input email field which is inside the form 
      // #pass - it can be your inupt field id or selector of that input password field which is inside the form 
      if(($("#id").emailValidate())&&($("#pass").passValidate())){
        flag = true;
      }else{
        flag = false;
      }
      return flag;
    }

there are number of methods like
-----------------------------------------
call this methods on input elements not or any other elements if you call these on other you might can get errors

1. nameValidate - return true or false and adds the help text message by default
2. urlValidate - return true or false and adds the help text message by default
3. emailValidate - return true or false and adds the help text message by default
4. isbnValidate - return true or false and adds the help text message by default
5. gstinValidate - return true or false and adds the help text message by default
6. pancardValidate - return true or false and adds the help text message by default
7. toolfreeValidate - return true or false and adds the help text message by default
8. phoneValidate - return true or false and adds the help text message by default
9. passValidate - return true or false and adds the help text message by default


10. allInputValidate
    -- all text message get applied on  input types when you input data 
      - email
      - url
      - password
      - tel
-------------------------------
    <script>
      allInputValidate();
    </script>
-------------------------------
