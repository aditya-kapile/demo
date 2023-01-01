# demo
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Protfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Serif:ital,opsz,wght@1,8..144,500&display=swap"
        rel="stylesheet">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Ubuntu:wght@300&display=swap" rel="stylesheet">
    <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <link rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.1/jquery.min.js"></script>
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
    <script>
        $(document).ready(function () {
            $(".hero .navbar #cls").click(function () {
                $(".hero .navbar").toggle();
            });

            $('.hero .hnav i').click(function () {
                $('.hero .navbar').toggle();
            });

            $('.second .right .tab .about-btn').click(function () {
                $(this).css("color", "red");
                $('.second .right .tab .skill-btn').css("color", "black");
                $('.second .right .aboutme').css("display", "block");
                $('.second .right .skill').css("display", "none");
            });

            $('.second .right .tab .skill-btn').click(function () {
                $(this).css("color", "red");
                $('.second .right .tab .about-btn').css("color", "black");
                $('.second .right .aboutme').css("display", "none");
                $('.second .right .skill').css("display", "block");
            });
        });
    </script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            text-decoration: none;
        }

        html {
            font-family: 'Ubuntu', sans-serif;
            scroll-behavior: smooth;
        }

        .hero {
            position: relative;
            width: 100%;
            min-height: 100vh;
            font-size: 1.3rem;
        }

        .hero::before {

            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url(https://images.unsplash.com/21/mac-glasses.JPG?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80);
            background-size: cover;
            z-index: -999;
            filter: brightness(0.5);
            box-shadow: inset 8px 8px 60px 50px rgba(0, 0, 0, 0.3),
                inset -8px -8px 10px rgba(0, 0, 0, 0.3);
            display: grid;
            place-items: center;
            font-size: 5rem;
        }

        .hero-text {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);

            padding: 10px;
            font-size: 3rem;
            font-family: 'Roboto Serif', serif;
            color: white;
            text-align: center;
            text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.4);
            z-index: -33;
        }

        .hero-text h1 span {
            font-size: 5rem;
            color: yellow;
        }

        .hero nav {
            padding: 10px;
            position: sticky;
            top: 0;
            left: 0;
            background-color: rgba(0, 0, 0, 0.1);

            display: flex;
            justify-content: space-between;
        }

        .hero nav a {
            display: none;
            text-decoration: none;
            padding: 10px;
            color: white;
            font-size: 1.2rem;
        }

        .hero nav a:hover {
            color: yellow;
            border-bottom: 1px solid yellow;
        }

        .hero .navbar {

            height: 90vh;
            text-align: center;
            padding: 20px;
            background-color: #252525;
            color: #fcf6f6;
            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
            z-index: 999;
        }

        .hero .navbar a {
            display: block;
            padding: 10px;
            color: #fcf6f6;
            margin-top: 20px;
        }

        .hero .navbar a:hover {

            background-color: white;
            color: #252525;
        }

        /* .hero button {
       border: none;
       padding: 10px 60px;
       background-image: linear-gradient(to right, #fc5c7d, #6a82fb);       
       color: white;
       box-shadow: 5px 5px 10px rgba(0,0,0,0.3);
       cursor: pointer;
    } */

        @media only screen and (min-width:800px) {

            .hero nav a {
                display: inline-block;
            }

            .hero nav i {
                display: none;
            }
        }

        .second {

            position: relative;
            width: 100%;
            min-height: 100vh;

            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10%;

            align-items: center;
            padding: 40px;
            word-spacing: 3px;
            letter-spacing: 1px;
        }

        .second img {
            box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
        }

        .second .skill meter {
            width: 100%;
            font-size: 2rem;
            border: none;
        }

        meter::-webkit-meter-optimum-value {
            background: linear-gradient(to right, rgb(255, 81, 0), rgb(46, 50, 245));
        }


        @media only screen and (max-width:900px) {
            .second {
                grid-template-columns: auto;
            }

            .second .skill meter {
                font-size: 3rem;
            }
        }

        .my-service {

            position: relative;
            top: 10vh;
            min-height: 100vh;
            display: grid;
            grid-template-columns: auto auto auto;
            gap: 20px;
            padding: 20px;
            text-align: center;
            background-color: rgb(247, 241, 241);
        }

        .my-service #service {
            grid-column: 1/4;
        }

        .my-service span {
            font-size: 3rem;
            filter: drop-shadow(5px 5px 5px rgba(0, 0, 0, 0.4));
        }

        .my-service .container * {
            padding: 5px;
        }

        @media only screen and (max-width: 900px) {
            .my-service {
                grid-template-columns: auto auto;
            }

            .my-service #service {
                grid-column: 1/3;
            }

        }

        @media only screen and (max-width: 600px) {
            .my-service {
                grid-template-columns: auto;
            }

            .my-service #service {
                grid-column: 1/2;

            }

        }

        /* .recent-work {
margin-top: 40px;
min-height: 100vh;
display: grid;
grid-template-columns: 1fr 1fr 1fr;
gap: 10px;
text-align: center;
}
.recent-work .container img{
    height: 300px;
    width: 350px;
}
.recent-work #work {
    grid-column: 1/4;
}  */

        .greeting {

            position: relative;
            top: 20vh;
            width: 100%;
            min-height: 30vh;
            text-align: center;
            padding: 10px;
            color: white;
        }

        .greeting::before {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            content: '';
            background-image: url(https://images.unsplash.com/photo-1670992367974-d11122d8e8c8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80);
            background-size: cover;
            filter: brightness(.4);
            z-index: -666;
        }

        .greeting button {
            border: none;
            padding: 10px 40px;
            border-radius: 20px;
            background-color: rgb(240, 78, 4);
            color: white;
            cursor: pointer;
        }

        .footer {
            position: relative;
            top: 30vh;
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            text-align: center;
            background-color: rgb(202, 188, 188);
        }

        .footer > h1 {
            grid-column: 1/4;
            padding: 10px;
           
        }

        .footer .wrapper i {

            background-color: red;
            color: white;
            padding: 20px;
            border-radius: 50%;
        }

        .footer .bottom {
            padding: 10px;
            grid-column: 1/4 ;
            background-color: #252525;
            color: white;
            box-shadow: -3px -3px 10px rgba(0,0,0,0.4);
        }

        .footer .bottom ul li {
            padding: 10px;
        }

        .footer .bottom ul li a i{

            padding: 10px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            
        }

        @media only screen and (max-width:600px){
            .footer{
                grid-template-columns: auto;
            }

            .footer >h1 {
                grid-column: 1/2;
            }

            .footer .bottom {
            grid-column: 1/2 ;
            
        }
            
        }

        #top-btn {

            position: fixed;
            top: 50vh;
            right: 0;
            padding: 10px;
            background-color: rgba(0,0,0,0.3);
            border: none;
            color: white;
            z-index: 9999;

        }
 
        
    </style>

    


</head>

<body>

    <section class="hero">
        <nav>
            <div style="font-family: 'Rubik Bubbles', cursive; color:white">
                <h2 style="font-family: 'Roboto Serif', serif">PORICHOY</h2>
            </div>
            <div class="hnav">
                <a href="#">HOME</a>
                <a href="#about">ABOUT</a>
                <a href="#service">SERVICE</a>
                <a href="#work">WORK</a>
                <a href="#start">START</a>
                <a href="#contact">CONTACT</a>
                <i class="fa fa-bars" style="color: white;"></i>

            </div>
        </nav>

        <div class="hero-text">
            <h1 style="font-family: 'Roboto Serif', serif;
            ">I'm <span>S</span>elena</h1>
            <p style="font-size: 1.5rem;">Freelance web designer and developer</p>
            <!-- <a href="#about"><button>More <br> <i class="fa fa-angle-double-down" aria-hidden="true"></i></button></a> -->

        </div>

        <div class="navbar" style="display: none;">
            <a href="#">HOME</a>
            <a href="#about">ABOUT</a>
            <a href="#service">SERVICE</a>
            <a href="#work">WORK</a>
            <a href="#">RESUME</a>
            <a href="#contact">CONTACT</a>
            <a id="cls"><i class="fa fa-times" aria-hidden="true"></i></a>
        </div>


    </section>

    <section class="second" id="about">

        <div class="left">
            <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTV8fHBvcnRyYWl0fGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
                height="400px" style="display:block;margin: 10px auto;">
        </div>

        <div class="right" style="padding: 20px;">

            <div class="tab" style="display: flex; justify-content: space-around;">
                <a class="about-btn"
                    style="color: red; border-bottom: 1px solid ; padding: 10px; cursor: pointer;">About</a>
                <a class="skill-btn" style=" border-bottom: 1px solid ; padding: 10px; cursor: pointer;">Skill</a>
            </div>

            <div class="aboutme" style="display: block;">
                <h3 style="padding: 20px 0; word-spacing: 3px;">Hi There I'm <span
                        style="color: rgb(255, 8, 0);">Selena</span></h3>
                <p>I'm a web developer with 10+ years of professional experience—I've
                    seen it all! I've worked on numerous websites, from small-scale
                    personal sites to large corporate projects. I'm well-versed in
                    a variety of development tools and technologies, such as HTML, CSS,
                    JavaScript, databases (MySQL/SQL Server), content management systems
                    (Drupal/WordPress), and more. <br><br>
                    I also have expertise creating custom
                    back-end solutions using Python/PHP, building secure APIs for mobile
                    apps, developing stunning front-end UIs using React/Vue.js as well as
                    bundling software packages into Docker containers. No matter the project
                    requirements, I'm confident my skills will get the job done efficiently and accurately.</p>
            </div>

            <div class="skill" style="display: none; padding-top: 40px;">
                <label>CSS</label>
                <meter max="100" value="95"></meter>
                <br>

                <label>Javascript</label>
                <meter max="100" value="80"></meter>
                <br>

                <label>Angular</label>
                <meter max="100" value="70"></meter>
                <br>

                <label>React</label>
                <meter max="100" value="85"></meter>
                <br>

                <label>Bootstrap</label>
                <meter max="100" value="100"></meter>


            </div>
        </div>

    </section>

    <section class="my-service">

        <div id="service">
            <h1 style="font-size: 2rem; padding: 10px;">MY SERVICES</h1>
            <p>Awesome features</p>
        </div>

        <div class="container">

            <span class="material-symbols-outlined">
                developer_mode
            </span>
            <h4>Development</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>

        <div class="container">

            <span class="material-symbols-outlined">
                computer
            </span>
            <h4>Easy Installation</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>
        <div class="container">

            <span class="material-symbols-outlined">
                devices
            </span>
            <h4>Fully Rsponsive</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>
        <div class="container">

            <span class="material-symbols-outlined">
                monitoring
            </span>
            <h4>Easy Monitoring</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>
        <div class="container">

            <span class="material-symbols-outlined">
                web
            </span>
            <h4>Fully Responsive</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>
        <div class="container">

            <span class="material-symbols-outlined">
                support_agent
            </span>
            <h4>Trusted Support</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing
                elit. Possimus perferendis velit officia ipsum eaque sit
                iusto, provident, nihil consequatur dolores atque maxime
                ad reprehenderit iste accusamus voluptas ab dolorem facilis.</p>
        </div>
    </section>

    <section class="recent-work" id="work" style="text-align: center;position: relative; top: 10vh;">

        <h1>Recent Work</h1>
        <p>Latest Projects</p>

        <!-- <div class="container">
            <img src="https://images.unsplash.com/photo-1605647540924-852290f6b0d5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=837&q=80">
        </div>
        <div class="container">
            <img src="https://images.unsplash.com/photo-1624355511224-14da0f11e256?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80">
        </div>
        <div class="container">
            <img src="">
        </div>
        <div class="container">
            <img src="">
        </div>
        <div class="container">
            <img src="">
        </div>
        <div class="container">
            <img src="https://images.unsplash.com/photo-1588358230769-9eca5b212954?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80">
        </div>
        </div> -->

        <div class="w3-content w3-display-container" style="width: fit-content;">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1605647540924-852290f6b0d5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=837&q=80"
                style="width:400px; height:300px">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1624355511224-14da0f11e256?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80"
                style="width:400px; height:300px">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1661206514777-2463d0d0599a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80"
                style="width:400px; height:300px">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1657539810416-ee7a3063ff45?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=725&q=80"
                style="width:400px; height:300px">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1657405826726-ac52271d3bb1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=967&q=80"
                style="width:400px; height:300px">
            <img class="mySlides"
                src="https://images.unsplash.com/photo-1588358230769-9eca5b212954?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80"
                style="width:400px; height:300px">

            <button class="w3-button w3-black w3-display-left" onclick="plusDivs(-1)">&#10094;</button>
            <button class="w3-button w3-black w3-display-right" onclick="plusDivs(1)">&#10095;</button>
        </div>
    </section>

    <div class="greeting" id="start">
        <p>Do you have any project ?</p>
        <h1>Let's Work Together Indeed!</h1>
        <button>Get Started</button>
    </div>

    <div class="footer" id="contact">

        <h1>CONTACT ME</h1>

        <div class="wrapper">
            <i class="fa fa-map-marker" aria-hidden="true"></i>
            <h4>My Location</h4>
            <p>3481 Melrose Place Berely Hills 90 210 USA</p>
        </div>
    
    <div class="wrapper">
        <i class="fa fa-phone-square" aria-hidden="true"></i>
        <h4> Phone Number</h4>
        <p>(+33) 123 456 789 <br>
            (+33) 221 453 975</p>
    </div>
    
    <div class="wrapper">
        <i class="fa fa-envelope" aria-hidden="true"></i>
        <h4>Email Address</h4>
        <p>demo@porichoy.com <br>demo2@porichoy.com</p>
    </div>

    
    <div class="bottom">
        <h1>PORICHOY</h1>
        <ul style="list-style-type: none; display: flex;justify-content: center">
            <li><a href="#"><i class="fa fa-facebook" aria-hidden="true" style="background: #3b5998;"></i></a></li>
            <li><a href="#"><i class="fa fa-instagram" aria-hidden="true" style="background: #fa7e1e;"></i></a></li>
            <li><a href="#"><i class="fa fa-pinterest-p" aria-hidden="true" style="background: #c8232c;"></i></a></li>
            <li><a href="#"><i class="fa fa-linkedin" aria-hidden="true" style="background:#0072b1 ;"></i></a></li>
        </ul>
        <p>Copyright &#169 2022. All Rights Reserved By @<a href="#" style="color: cyan;">Aditya Kapile</a></p>
    </div>
    </div>

    <button id="top-btn"><a href="#"><i class="fa fa-arrow-up" aria-hidden="true"></i></a></button>

<div class="last"></div>
    <script>
        var slideIndex = 1;
        showDivs(slideIndex);

        function plusDivs(n) {
            showDivs(slideIndex += n);
        }

        function showDivs(n) {
            var i;
            var x = document.getElementsByClassName("mySlides");
            if (n > x.length) { slideIndex = 1 }
            if (n < 1) { slideIndex = x.length }
            for (i = 0; i < x.length; i++) {
                x[i].style.display = "none";
            }
            x[slideIndex - 1].style.display = "block";
        }
    </script>

</body>

</html>
