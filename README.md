# glassmorphism
responsive Glassmorphism login UI with pure html and css
# how it appearces on iphone 13 and above
![glass iphone 14](https://github.com/Gelgeloberiso/glassmorphism/assets/81536915/c67a7c00-53bd-4c1c-b894-46c8d95b0e10)

# how it appears on samsung s20s
![glassmorphosm s20s](https://github.com/Gelgeloberiso/glassmorphism/assets/81536915/1595c860-9385-41c6-9a2f-e0242747fa86)

# how it appearch on desktop 
![responsive glassmorphism login ux desktop](https://github.com/Gelgeloberiso/glassmorphism/assets/81536915/1dd8570c-3b09-47cd-96a7-e6ef6a7a0e25)


# html code
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glassmorphism</title>
    <link rel="stylesheet" href="style.css">
</head>

<section>
    <div class="login-box">
        <form action="">
            <h2>Login</h2>
            <div class="input-box">
                <span class="icon"><ion-icon name="mail"></ion-icon></span>
                <input type="email" required>
                <label for="">Email</label>
            </div>
            <div class="input-box">
                <span class="icon"><ion-icon name="lock-closed"></ion-icon></span>
                <input type="password" required>
                <label for="">Password</label>
            </div>
            <div class="remember-forget">
                <label for=""><input type="checkbox">Remember Me</label>
                <a href="#">Forget Password?</a>
            </div>
            <button type="submit">Login</button>
            <div class="register-link">
                <p>Don't Have an Account? <a href="">Create Account!</a></p>
            </div>
        </form>
    </div>
</section>
<script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
<script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
</body>

</html>

# css
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
body{

}
section{
   display: flex;
   justify-content: center;
   align-items: center;
   width: 100%;
   height: 100vh;
   background: url('image2.jpg') no-repeat;
   background-size: cover;
   background-position: center;
   animation: animateBg 5s linear infinite;
}
@keyframes animateBg{
    100%{
        filter: hue-rotate(360deg);
    }
}
.login-box{
    position: relative;
    width: 400px;
    height: 450px;
    background: transparent;
    border: 2px solid rgba(255, 255, 255, 0.5);
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    backdrop-filter: blur(10px);
}
h2{
    font-size: 2rem;
    color: #fff;
    text-align: center;
}
.input-box{
    position: relative;
    width: 310px;
    margin: 30px 0;
    border-bottom: 2px solid #fff;
}
.input-box label{
    position: absolute;
    top: 50%;
    left: 5px;
    transform: translateY(-50%);
    font-size: 1em;
    color: #fff;
    pointer-events: none;
    transition: 0.3s;
}
.input-box input:focus~label,
.input-box input:valid~label{
    top: -5px;
}
.input-box input{
    width: 100%;
    height: 50px;
    background: transparent;
    border: none;
    outline: none;
    font-size: 1em;
    color: #fff;
    padding: 0 35px 0 5px;
}
.input-box .icon{
    position: absolute;
    right: 8px;
    color: #fff;
    font-size: 1.2em;
    line-height: 57px;
}
.remember-forget{
    margin: -15px 0 15px;
    font-size: 0.9em;
    color: #fff;
    display: flex;
    justify-content: space-between;
}
.remember-forget label input{
    margin-right: 5px;
}
.remember-forget a{
    color: #fff;
    text-decoration: none;
}
.remember-forget a:hover{
    text-decoration: underline;
}
button{
    width: 100%;
    height: 40px;
    background: #fff;
    border: none;
    outline: none;
    border-radius: 10px;
    cursor: pointer;
    font-size: 1em;
    color: #000;
    font-weight: 600;
}
.register-link{
    font-size: 1em;
    color: #fff;
    text-align: center;
    margin: 25px 0 10px;
}
.register-link p a{
    color: #fff;
    font-weight: 600;
    text-decoration: none;
}
.register-link p a:hover{
    text-decoration: underline;
}
@media (max-width: 360px) {
    .login-box{
        width: 100%;
        height: 100vh;
        border: none;
        border-radius: 0;
    }
    .input-box{
        width: 290px;
    }
}
