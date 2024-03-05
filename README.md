<!DOCTYPE html>
<html lang="en">
<head>
     <link href="css.css" rel="stylesheet">
    
    <title>colour changer</title>
</head>
<body>
    <h1>colour changer</h1>
    <div class="container">
        <div class="row">
            <div class="col-12 col-lg-6">
               
                <button class="button button1" id="gray">gray</button>
                <button class="button button2" id="yellow">yellow</button>
                <button class="button button1" id="red">red</button>
                <button class="button button2" id="multi">multi</button>
                <button class="button button1" id="green">Green</button>
                <button class="button button2" id="blue">Blue</button>
            </div>
            <div class="col-12 col-lg-6">
                <h2>click the buttons to change the colour</h2>
                <p>the colour of yhe background will change based on your option</p>
            </div>
        </div>

    </div>
    <script src="js/bootstrap.bundel.js"></script> 

</body>
<script>
    const buttn = document.querySelectorAll('.button');
    const bdy = document.querySelector('body');

 buttn.forEach(function(buttn){
        console.log(buttn);
        buttn.addEventListener('click',function(e){
            console.log(e);
            console.log(e.target);

            if(e.target.id=='gray'){
                bdy.style.backgroundColor = e.target.id;
            }
            if(e.target.id=='yellow'){
                bdy.style.backgroundColor = e.target.id;
            }
            if(e.target.id=='red'){
                bdy.style.backgroundColor = e.target.id;
            }
            if(e.target.id=='blue'){
                bdy.style.backgroundColor = e.target.id;
            }
            if(e.target.id=='green'){
                bdy.style.backgroundColor = e.target.id;
            }
            if(e.target.id=='multi'){

                var x=Math.round(0xffffff * Math.random()).toString(16);
                 var y=(6-x.length);
                   var z = "000000";
                 var z1 = z.substring(0,y);
                  var color= "#" + z1 + x;
                
                
                bdy.style.backgroundColor = color;
            }
            
        })

    });

</script>
<script src="colourchanger/js.js"></script> 

</html>
