<!doctype html>
<html lang="en">
  <head>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">


    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">

    <style type="text/css">
        *{
            margin: 0px;
            padding: 0px;
        }
        .bx{
            background-color: blue;
            padding: 4rem;
            border: 1px solid white;
        }
    </style>
  </head>
  <body>
    <section>
        <div class="row">
            <div id="b1" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b2" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b3" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b4" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
        </div>
        <div class="row">
            <div id="b5" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b6" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b7" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b8" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
        </div>
        <div class="row">
            <div id="b9" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b10" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b11" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b12" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
        </div>

        <div class="row">
            <div id="b13" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b14" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b15" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
            <div id="b16" onclick="myfun(this.id)" class="bx col-sm-12 col-md-3 col-lg-3"></div>
        </div>
        <span style="display: none" id="rb">none</span>
        <span style="display: none" id="bb">none</span>
    </section>


    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ho+j7jyWK8fNQe+A12Hb8AhRq26LrZ/JpcUGGOn+Y7RsweNrtN/tE3MoK7ZeZDyx" crossorigin="anonymous"></script>

    <script>
        function myfun(id){
            var rb = document.getElementById('rb');
            var bb = document.getElementById('bb');
            if(id === rb.innerHTML || id === bb.innerHTML){
                return;
              }

            if(rb.innerHTML === "none"){
                rb.innerHTML = id;
                document.getElementById(id).style.backgroundColor ='red';
            }
            else if(rb.innerHTML != "none" && bb.innerHTML === "none"){
                bb.innerHTML = id;
                document.getElementById(id).style.backgroundColor ='red';
            }
            else if( rb.innerHTML != "none" && bb.innerHTML != "none" ){
                document.getElementById(rb.innerHTML).style.backgroundColor ='blue';
                rb.innerHTML = bb.innerHTML;
                bb.innerHTML = id;
                document.getElementById(id).style.backgroundColor ='red';
            }
        }
    </script>
  </body>
</html>
