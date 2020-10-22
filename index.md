

<html>

    <head>

        <title>Website UI Demo</title>

        <meta name="viewport" content="width=device-width, initial-scale=1">

        <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">

        <link href="https://fonts.googleapis.com/css?family=Oswald|Raleway&display=swap" rel="stylesheet">

        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

        <script src="https://cdnjs.cloudflare.com/ajax/libs/sweetalert/2.1.0/sweetalert.min.js"></script>

        <script src="https://www.gstatic.com/firebasejs/7.24.0/firebase-app.js"></script>

<script src="https://www.gstatic.com/firebasejs/7.24.0/firebase-auth.js"></script>

 <script src="https://www.gstatic.com/firebasejs/7.24.0/firebase-database.js"></script>

        <style>

            body, h1, h2, h3, h4, h5, h5, p {

                font-family:Raleway;

                transition:0.5s;

            }

            button, input,textarea {

                outline:none;

                border:none;

            }

            a {

                text-decoration:none;

            }

            .loader {

             position:fixed;

             top:40%;

             left:38%;

             display:none;

  border: 16px solid #f3f3f3;

  border-radius: 50%;

  border-top: 16px solid teal;

  width: 100px;

  height: 100px;

  -webkit-animation: spin 2s linear infinite; /* Safari */

  animation: spin 2s linear infinite;

}

/* Safari */

@-webkit-keyframes spin {

  0% { -webkit-transform: rotate(0deg); }

  100% { -webkit-transform: rotate(360deg); }

}

@keyframes spin {

  0% { transform: rotate(0deg); }

  100% { transform: rotate(360deg); }

}

#loader2{

    display:block;

}

#date {

        font-size:12px;

    }

        </style>

        

    </head>

    <body>

        

        

        <div class="w3-sidebar w3-bar-block w3-border-right w3-animate-left" style="display:none;z-index:6; background-image: linear-gradient(to right, teal 0%, #00f2fe 100%); font-size:17px;" id="mySidebar">

            

          

          <button onclick="w3_close()" class="w3-bar-item w3-teal w3-text-black w3-large" style="margin-top:-25px;">Close</button>

          <a href="#os" onclick="w3_close()" class="w3-bar-item w3-ripple">Our Services</a>

          <a href="#ot" onclick="w3_close()" class="w3-bar-item w3-ripple">Our Team</a>

          <a href="#cu" onclick="w3_close()" class="w3-bar-item w3-ripple">Contact Us</a>

        </div>

        

       <div id="loader" class="loader" style="z-index:7;"></div> 

        

        <div class="w3-overlay w3-animate-opacity" onclick="w3_close()" style="cursor:pointer; z-index:7;" id="myOverlay2"></div>

        

<div class="w3-overlay w3-animate-opacity" onclick="w3_close()" style="cursor:pointer; z-index:5;" id="myOverlay"></div>

        

        <div style="width:100%; position:fixed; top:0px;left:0px; z-index:4; background-image: linear-gradient(to right, teal 0%, #00f2fe 100%);" class="w3-container w3-text-black">

            

            <h2><span class="w3-button w3-xlarge" onclick="w3_open()" ><i class="fa fa-bars"></i></span> Saviee Demo Web</h2>

        </div>

        <br /><br /><br /><br /><br />

        

        

        <div class="w3-card-4 w3-margin w3-hover-shadow w3-round">

            <div class="w3-display-container">

                <img  class="w3-hover-opacity w3-opacity-min" src="https://www.w3schools.com/w3css/img_snowtops.jpg" style="width:100%;" alt="A landscape image">

                <div class="w3-display-middle w3-medium">

                    <button class="w3-center w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Explore</button>

                </div>

            </div>

            <div class="w3-container w3-center">

                <p>Welcome to Demo Website</p>

            </div>

        </div>

        <br><br>

        <div id="os" class="w3-panel w3-container w3-center">

            <h3>Our Services</h3>

        </div>

        

        

        <div class="w3-row w3-container w3-center">

        

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

                <h4 class="w3-text-teal">HTML</h4>

                <p>We provide you with great HTML lessons. <br /> <br />

                 Learn the complete HTML course with examples and tests.</p>

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Start Lesson</button>

            </div>

            

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

                <h4 class="w3-text-teal">CSS</h4>

                <p>We provide you with very good CSS lessons. <br /> <br />

                 Learn the complete CSS course with examples and tests.</p>

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Start Lesson</button>

            </div>

            

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

                <h4 class="w3-text-teal">Javascript</h4>

                <p>We provide you with great Javascript lessons. <br /> <br />

                 Learn the complete Javascript course with examples and tests.</p>

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Start Lesson</button>

            </div>

            

        </div>

        <br><br>

        

        <div id="ot" class="w3-panel w3-container w3-center">

            <h3>Our Team</h3>

        </div>

        

        

        <div class="w3-row w3-container w3-center">

        

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

                <img class="w3-center w3-padding" src="https://images.vexels.com/media/users/3/145908/preview2/52eabf633ca6414e60a7677b0b917d92-male-avatar-maker.jpg" alt="Avatar" style="width:140px; height:120px; border-radius:50%; border-style:none;">

                <h5 class="w3-teal">Name: John Doe</h5>

                <h5 class="w3-teal">Skills: HTML CSS and Javascript</h5>

                

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Contact</button>

            </div>

            

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

               <img class="w3-center w3-padding" src="https://nofiredrills.com/wp-content/uploads/2016/10/myavatar.png" alt="Avatar" style="width:140px; height:120px; border-radius:50%; border-style:none;">

                <h5 class="w3-teal">Name: Jane Doe</h5>

                <h5 class="w3-teal">Skills: HTML CSS and Javascript</h5>

                

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Contact</button>            </div>

            

            <div class="w3-card w3-margin-right w3-margin-bottom w3-container w3-third w3-round-large w3-center w3-leftbar w3-hover-shadow">

                <img class="w3-center w3-padding" src="https://i0.wp.com/www.yugatech.com/wp-content/uploads/2020/09/Facebook-Avatar.jpg?w=500&ssl=1" alt="Avatar" style="width:140px; height:120px; border-radius:50%; border-style:none;">

                <h5 class="w3-teal">Name: James Doe</h5>

                <h5 class="w3-teal">Skills: HTML CSS and Javascript</h5>

                

                 <button class="w3-right w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin w3-ripple">Contact</button>

            </div>

            

        </div>

        <br><br>

        

        <div class="w3-panel w3-round-medium w3-margin w3-container w3-text-teal w3-center" style="border-style:solid; border-color:teal;">

            <h4>Our Aim</h4>

            <p>To Raise Highly Qualified Web developers.</p>

        </div>

        <br><br>

        <div class="w3-container w3-card w3-light-grey w3-margin">

            <h4 class="w3-text-teal w3-center">Receive Notifications</h4>

            

            <label class="w3-text-teal"><b>Email</b></label>

            <input class="w3-input w3-margin-bottom w3-border-teal" type="email" id="namesign" required>

            

            <label class="w3-text-teal"><b>Username</b></label>

            <input class="w3-input w3-border-teal w3-margin-bottom" type="text" id="passwordsign" required>

            <button class="w3-btn w3-teal w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin-top w3-margin-bottom w3-ripple w3-block" onclick="writeData()">Register</button>

            

            

        </div><br><br>

        

        

        <div id="messages" class="w3-panel w3-round-medium w3-margin w3-container w3-teal" style="border-style:solid; border-color:teal;">

            <h3>Comments</h3>

            <div id="loader2" style="position:relative;" class="loader"></div><br>

        </div>

        <br><br>

        

        <div id="sign" class="w3-container w3-card w3-light-grey w3-margin">

            <h4 class="w3-text-teal w3-center">Add Comment</h4>

            

            <label class="w3-text-teal"><b>Username</b></label>

            <input class="w3-input w3-border-teal w3-margin-bottom" type="text" id="commentuser" required>

            <label class="w3-text-teal"><b>Comment</b></label>

            <textarea class="w3-input w3-border-teal w3-margin-bottom" type="text" id="commentadd" required></textarea>

            <button class="w3-btn w3-teal w3-round-large w3-teal w3-hover-shadow w3-text-black w3-padding w3-margin-top w3-margin-bottom w3-ripple w3-block" onclick="comment()">Add Comment </button>   </div> <br><br>

        

        <div id="cu" class="w3-panel-padding w3-container w3-center" style="border-style:solid; border-color:teal; background-image: linear-gradient(to right, teal 0%, #00f2fe 100%);">

            <h4>Contact Us</h4>

            <p><span class="w3-padding" style="font-size:30px; color:blue;"><i class="fa fa-facebook"></i></span><span style="font-size:30px; color:orange;" class="w3-padding"><i class="fa fa-google"></i></span><span style="font-size:30px; color:blue;" class="w3-padding"><i class="fa fa-twitter"></i></span></p>

            

            <h4>Credits</h4>

            <p><a href="https://www.w3schools.com/" target="_blank">W3schools</a></p>

            <p><a href="https://www.google.com/url?sa=t&source=web&rct=j&url=https://sweetalert.js.org/guides/&ved=2ahUKEwjW_r7Kn8TsAhWPDxQKHexPBHAQFjABegQIBBAI&usg=AOvVaw2lOfbPSTqeJLsQia58kgLe" target="_blank">Sweet alert</a></p>

            <p><a href="https://fontawesome.com/" target="_blank">Font awesome</a></p>

            <p>Images from Google</p>

            

            

            

            

        </div>

        

        

        

        <script>

            window.onload = function() {

                swal({

                    title: "Hello",

                    text: "It's just a web UI demo.",

                    icon: "info",

                });

                document.getElementById("loader").style.display = "none";

            }

            function w3_open() {

  document.getElementById("mySidebar").style.display = "block";

                document.getElementById("mySidebar").style.width = "60%";

                document.getElementById("myOverlay").style.display = "block";

                document.getElementById("mySidebar").style.transition = "0.5s";

                

}

            function w3_close() {

  document.getElementById("mySidebar").style.display = "none";

                document.getElementById("myOverlay").style.display = "none";

                document.getElementById("mySidebar").style.transition = "0.5s";

                

}

            

            

            

            

            // Your web app's Firebase configuration

            var firebaseConfig = {

                apiKey: "AIzaSyAWSSDW4V0qRhZ4vAHA_XOy-jQpLFqhgck",

                authDomain: "sign-up-bf8aa.firebaseapp.com",

                databaseURL: "https://sign-up-bf8aa.firebaseio.com",

                projectId: "sign-up-bf8aa",

                storageBucket: "sign-up-bf8aa.appspot.com",

                messagingSenderId: "1055698873019",

                appId: "1:1055698873019:web:33a008b59550d0c8fc979e"

  };

  // Initialize Firebase

  firebase.initializeApp(firebaseConfig);

  

  

  

  

            function writeData() {

                      

              document.getElementById("loader").style.display = "block";

                      document.getElementById("myOverlay").style.display = "block";

              name = document.getElementById("namesign").value,

              password = document.getElementById("passwordsign").value

              

          if (name != "" && password != "") {

                  

             firebase.auth().createUserWithEmailAndPassword(name, password).then(function(){

                      var user = firebase.auth().currentUser;

user.sendEmailVerification().then(function() {

  // Email sent.

  swal({

      title: "Hello user",

      text: "Verification email sent",

      icon: "success",

  });

  document.getElementById("myOverlay").style.display = "none";

  document.getElementById("loader").style.display = "none";

  document.getElementById("namesign").value = ""

                  document.getElementById("passwordsign").value = ""

}).catch(function(error) {

  swal({

      title: "Hello user",

      text: "Couldn't verify email",

      icon: "warning",

  });

  document.getElementById("myOverlay").style.display = "none";

  document.getElementById("loader").style.display = "none";

  document.getElementById("namesign").value = ""

                  document.getElementById("passwordsign").value = ""

});

             })

             .catch(function(error) {

             // Handle Errors here.

                 var errorCode = error.code;

                 var errorMessage = error.message;

                 swal({

              title: "Hello user",

              text: errorMessage,

              icon: "error",

              });

              document.getElementById("myOverlay").style.display = "none";

  document.getElementById("loader").style.display = "none";

              document.getElementById("namesign").value = ""

                  document.getElementById("passwordsign").value = ""

              });

              

              

                  

               }

               

              

          

                

          

          

          else {swal({

              text:"Please input all fields",

              title: "Hello user",

              icon:"info",

          })

          document.getElementById("myOverlay").style.display = "none";

  document.getElementById("loader").style.display = "none";

           document.getElementById("namesign").value = ""

                  document.getElementById("passwordsign").value = ""}

       

      }

              function comment() {

                      document.getElementById("loader").style.display = "Block";

                      document.getElementById("loader2").style.display = "block";

                

                      document.getElementById("myOverlay2").style.display = "block";

              commentuser = document.getElementById("commentuser").value,

              commentadd = document.getElementById("commentadd").value

              

          if (commentuser != "" && commentadd != "") {

              if (commentuser.length <= 3) {

                  swal({

                      title: "Hello",

                      text: "Username is too short",

                      icon: "warning",

                  })

              }

              else if (commentadd.length <= 3) {

                  swal({

                      title: "Hello",

                      text: "Comment is too short",

                      icon: "warning",

                  })

              }

              else if(commentuser == "Saviour(Owner)" || commentuser == "saviour(Owner)" || commentuser == "Saviour(owner)" || commentuser == "saviour(owner)" || commentuser == "Saviour(Own)" || commentuser == "saviour(Own)" || commentuser == "Saviour(own)" || commentuser == "saviour(own)") {

              swal({

                      title: "Hello",

                      text: "Sorry, you can't use that username",

                      icon: "warning",

                  })

                  

              }

              else {

                       var a = new Date

                var aa = a.getFullYear()

                var ab = a.getMonth()

                var ac = a.getDate()

                var ad = a.getHours()

                var ae = a.getMinutes()

              firebase.database().ref("User").push().set({

                  user: document.getElementById("commentuser").value,

                  comment: document.getElementById("commentadd").value,

                  year: aa,

                  month: ab+1,

                  date: ac,

                  hour: ad,

                  min: ae

                  });

                  swal("Hello " + commentuser ,"Comment Posted", "success")

              }

              document.getElementById("commentuser").value = ""

              document.getElementById("commentadd").value = ""

               document.getElementById("loader").style.display = "None";

               document.getElementById("myOverlay2").style.display = "none";

                document.getElementById("loader2").style.display = "None";

                  

               }

               

              

           

                

          

          

          else {swal("Hello User","Please fill all fields", "info");

          document.getElementById("loader").style.display = "none"

          document.getElementById("loader2").style.display = "None";}

      document.getElementById("myOverlay2").style.display = "none";

      }

      

      

firebase.database().ref("User").on("child_added", function(snapshot){

          cc = snapshot.val().comment

          uu = snapshot.val().user

          if (uu == "Saviour(Owner)"){

          uu = "<b>" + snapshot.val().user + "</b>"

          cc = "<b>" + snapshot.val().comment + "</b>"

          var html = "";

          html += "<p id='message-" + snapshot.key + "'>";

          

              html += uu + ": " + cc + "  ";

              html += "<br>"

              html += "<span id='date'>"

              html += snapshot.val().date + "/" + snapshot.val().month + "/" + snapshot.val().year + "  " + snapshot.val().hour + ":" + snapshot.val().min

              html += "</span>"

          

          html += "</p>"

          html += "<hr>"

          document.getElementById("loader2").style.display = "None";

          document.getElementById("messages").innerHTML += html;

  }

  else{

      

  var html = "";

          html += "<p id='message-" + snapshot.key + "'>";

          

              html += "<b>" + uu + ": " +"</b>"+ cc + "  ";

              html += "<br>"

              html += "<span id='date'>"

              html += snapshot.val().date + "/" + snapshot.val().month + "/" + snapshot.val().year + "  " + snapshot.val().hour + ":" + snapshot.val().min

              html += "</span>"

          

          html += "</p>"

          html += "<hr>"

          document.getElementById("loader2").style.display = "None";

          document.getElementById("messages").innerHTML += html;

          }

  });

  

            

        </script>

        

    </body>

</html>
