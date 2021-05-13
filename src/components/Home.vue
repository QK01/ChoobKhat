<template>

<div id="mainPage" style="display: block;">
    <!-- Nav Bar in Home Page -->
    <nav class="w3-bar w3-black" id="mainNavbar">
        <a href="#home" class="btn btn-secondary mx-1 my-1"  @click="goHomePage()">خانه</a>
        <a href="#products" class="btn btn-secondary mx-1 my-1" @click="goProductPage()">محصولات</a>
        <a href="#contact" class="btn btn-secondary mx-1 my-1" @click="goContactPage()">تماس با ما</a>
        <a href="#about" class="btn btn-secondary mx-1 my-1" @click="goAboutPage()">درباره ما</a>
        <a href="#LoginRegister" class="btn btn-secondary mx-1 my-1" @click="openFormLogin()">ورود/ثبت نام</a>
    </nav>

    <!-- Home Page -->
    <div  id="homePage" style="display: none;">
        <h1 class="text-muted">سلام چوب خط :)</h1> 
    </div>

    <!-- Product Page -->
    <div id="productPage" style="display: none;">
        <h1 class="text-muted">محصولات :)</h1> 
    </div>

    <!-- Contact Page -->
    <div id="contactPage" style="display: none;">
        <h1 class="text-muted">تماس با ما :)</h1> 
    </div>

    <!-- َAbout Page -->
    <div id="aboutPage" style="display: none;">
        <h1 class="text-muted">درباره ما :)</h1> 
    </div>


    <!-- Login Form in Home Page -->
    <form action="action_page.php" method="post" dir="ltr" id="formLogin" style="display: none;">
        <div class="imgcontainer">
            <img src="../assets/logo.png">
        </div>

        <div class="container">
            <label for="uname"><b>Username</b></label>
            <input type="text" placeholder="Enter Username" name="uname" required>

            <label for="psw"><b>Password</b></label>
            <input type="password" placeholder="Enter Password" name="psw" required>

            <button type="submit">Login</button>
            <label>
            <input type="checkbox" checked="checked" name="remember"> Remember me
            </label>
        </div>

        <div class="container" style="background-color:#f1f1f1">
            <button type="button" class="cancelbtn" >Cancel</button>
            <span class="psw" > <a href="#"> Forgot password?</a></span>
        </div>
    </form>
</div>  
    
</template>

<script>

export default ({
  methods:{
    goHomePage(){
        document.getElementById("homePage").style.display = "block";
        document.getElementById("productPage").style.display = "none";
        document.getElementById("contactPage").style.display = "none";
        document.getElementById("aboutPage").style.display = "none";
        document.getElementById("formLogin").style.display = "none";
    },

    goProductPage(){
        document.getElementById("homePage").style.display = "none";
        document.getElementById("productPage").style.display = "block";
        document.getElementById("contactPage").style.display = "none";
        document.getElementById("aboutPage").style.display = "none";
        document.getElementById("formLogin").style.display = "none";
    },

    goContactPage(){
        document.getElementById("homePage").style.display = "none";
        document.getElementById("productPage").style.display = "none";
        document.getElementById("contactPage").style.display = "block";
        document.getElementById("aboutPage").style.display = "none";
        document.getElementById("formLogin").style.display = "none";       
    },
    goAboutPage(){
        document.getElementById("homePage").style.display = "none";
        document.getElementById("productPage").style.display = "none";
        document.getElementById("contactPage").style.display = "none";
        document.getElementById("aboutPage").style.display = "block";
        document.getElementById("formLogin").style.display = "none";       
    },
    openFormLogin(){
        document.getElementById("homePage").style.display = "none";
        document.getElementById("productPage").style.display = "none";
        document.getElementById("contactPage").style.display = "none";
        document.getElementById("aboutPage").style.display = "none";
        document.getElementById("formLogin").style.display = "block";       
    },

  },
})

</script>



<style scoped>
    header * {
        display: inline;
    }

    header li {
        margin: 20px;
    }
    /* Bordered form */
    form {
    border: 3px solid #f1f1f1;
    
    }

    /* Full-width inputs */
    input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
    }

    /* Set a style for all buttons */
    button {
    background-color: #04AA6D;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    cursor: pointer;
    width: 100%;
    }

    /* Add a hover effect for buttons */
    button:hover {
    opacity: 0.8;
    }

    /* Extra style for the cancel button (red) */
    .cancelbtn {
    width: auto;
    padding: 10px 18px;
    background-color: #f44336;
    }

    /* Center the avatar image inside this container */
    .imgcontainer {
    text-align: center;
    margin: 24px 0 12px 0;
    }

    /* Avatar image */
    img.avatar {
    width: 40%;
    border-radius: 50%;
    }

    /* Add padding to containers */
    .container {
    padding: 16px;
    }

    /* The "Forgot password" text */
    span.psw {
    float: right;
    padding-top: 16px;
    }

    /* Change styles for span and cancel button on extra small screens */
    @media screen and (max-width: 300px) {
    span.psw {
        display: block;
        float: none;
    }
    .cancelbtn {
        width: 100%;
    }
    }
</style>